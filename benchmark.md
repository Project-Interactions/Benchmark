## Minecraft load time benchmark


---

<p align="center" style="font-size:160%;">
MC total load time:<br>
1184.66 sec
<br>
<sup><sub>(
19:44 min
)</sub></sup>
</p>

<br>


<p align="center">
<img src="https://quickchart.io/chart?w=400&h=30&c={
  type: 'horizontalBar',
  data: {
    datasets: [
      {label:      'MODS:', data: [627.29]},
      {label: 'FML stuff:', data: [557.36]}
    ]
  },
  options: {
    scales: {
      xAxes: [{display: false,stacked: true}],
      yAxes: [{display: false,stacked: true}],
    },
    elements: {rectangle: {borderWidth: 2}},
    legend: {display: false,},
    plugins: {datalabels: {color: 'white',formatter: (value, context) =>
      [context.dataset.label, value].join(' ')
    }}
  }
}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={
  type: 'outlabeledPie',
  options: {
    cutoutPercentage: 25,
    plugins: {
      legend: !1,
      outlabels: {
        stretch: 5,
        padding: 1,
        text: (v,i)=>[
          v.labels[v.dataIndex],' ',
          (v.percent*1000|0)/10,
          String.fromCharCode(37)].join('')
      }
    }
  },
  data: {...
`
436e17  44.24s Had Enough Items;
3C6315  42.94s Had Enough Items (Plugins);
9e2174   5.47s Tinkers' Construct;
8E1E68  58.01s Tinkers' Construct (Oredict Melting);
5161a8  23.58s CraftTweaker2;
8f3087  21.30s Forge Mod Loader;
8f3041  19.63s Tech Reborn;
813e81  16.54s OpenComputers;
516fa8  15.49s Ender IO;
8c2ccd  14.31s Immersive Engineering;
9d2ccd  12.08s Immersive Intelligence;
3e6c81  11.31s Solar Flux Reborn;
cd922c  10.72s NuclearCraft;
8f304e  10.60s Astral Sorcery;
213664   8.91s Forestry;
813e4d   8.67s GroovyScript;
7c813e   6.92s Thaumcraft;
436e17   6.57s Integrated Dynamics;
2caacd   6.43s PneumaticCraft: Repressurized;
8451a8   5.75s LibrarianLib Stage 2;
176e43   5.35s Thaumic Additions: Reconstructed;
216364   5.32s Xaero's Minimap;
444444 179.32s 83 Other mods;
333333  78.95s 218 'Fast' mods (load 1.0s - 0.1s);
222222   8.90s 224 'Instant' mods (load %3C 0.1s)
`
    .split(';').reduce((a, l) => {
      l.match(/(\w{6}) *(\d*\.\d*)s (.*)/)
      .slice(1).map((a, i) => [[String.fromCharCode(35),a].join(''), parseFloat(a), a][i])
      .forEach((s, i) => 
        [a.datasets[0].backgroundColor, a.datasets[0].data, a.labels][i].push(s)
      );
      return a
    }, {
      labels: [],
      datasets: [{
        backgroundColor: [],
        data: [],
        borderColor: 'rgba(22,22,22,0.3)',
        borderWidth: 1
      }]
    })
  }
}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={
  options: {
    scales: {
      xAxes: [{stacked: true}],
      yAxes: [{stacked: true}],
    },
    plugins: {
      datalabels: {
        anchor: 'end',
        align: 'top',
        color: 'white',
        backgroundColor: 'rgba(46, 140, 171, 0.6)',
        borderColor: 'rgba(41, 168, 194, 1.0)',
        borderWidth: 0.5,
        borderRadius: 3,
        padding: 0,
        font: {size:10},
        formatter: (v,ctx) => 
          ctx.datasetIndex!=ctx.chart.data.datasets.length-1 ? null
            : [((ctx.chart.data.datasets.reduce((a,b)=>a- -b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')
      },
      colorschemes: {
        scheme: 'office.Damask6'
      }
    }
  },
  type: 'bar',
  data: {...(() => {
    let a = { labels: [], datasets: [] };
`
1: Construction;
2: Loading Resources;
3: PreInitialization;
4: Initialization;
5: InterModComms$IMC;
6: PostInitialization;
7: LoadComplete;
8: ModIdMapping
`
    .split(';')
      .map(l => l.match(/\d: (.*)/).slice(1))
      .forEach(([name]) => a.datasets.push({ label: name, data: [] }));
`
                           1      2      3      4      5      6      7      8  ;
Tinkers' Construct     |  1.72|  0.01|  0.24|  0.13|  0.00| 61.38|  0.00|  0.00;
CraftTweaker2          |  1.28|  0.00| 17.79|  0.01|  0.00|  4.50|  0.00|  0.00;
Tech Reborn            |  0.18|  0.01| 16.59|  0.65|  0.00|  2.20|  0.00|  0.00;
OpenComputers          |  0.27|  0.03| 11.91|  4.04|  0.30|  0.00|  0.00|  0.00;
Ender IO               |  3.16|  0.01|  4.93|  0.77|  4.42|  1.20|  0.00|  1.01;
Immersive Engineering  |  1.32|  0.01|  1.45|  1.38|  0.00| 10.15|  0.00|  0.00;
Immersive Intelligence |  3.00|  0.02|  3.59|  1.06|  0.00|  4.42|  0.00|  0.00;
Solar Flux Reborn      |  0.12|  0.00|  1.06|  0.06|  0.00| 10.07|  0.00|  0.00;
NuclearCraft           |  1.58|  0.02|  7.87|  0.66|  0.00|  0.48|  0.00|  0.12;
Astral Sorcery         |  0.53|  0.01|  6.81|  2.21|  0.00|  1.05|  0.00|  0.00;
Forestry               |  0.82|  0.02|  6.23|  1.48|  0.01|  0.36|  0.00|  0.00;
GroovyScript           |  3.03|  0.02|  0.00|  0.02|  0.00|  5.60|  0.00|  0.00
`
    .split(';').slice(1)
      .map(l => l.split('|').map(s => s.trim()))
      .forEach(([name, ...arr], i) => {
        a.labels.push(name);
        arr.forEach((v, j) => a.datasets[j].data[i] = v)
      }); return a
  })()}
}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={
  options: {
    elements: { rectangle: { borderWidth: 1 } },
    legend: false
  },
  type: 'horizontalBar',
    data: {...(() => {
      let a = {
        labels: [], datasets: [{
          backgroundColor: 'rgba(0, 99, 132, 0.5)',
          borderColor: 'rgb(0, 99, 132)',
          data: []
        }]
      };
`
 11.81: cofh.thermalexpansion.plugins.jei.JEIPluginTE;
  4.78: li.cil.oc.integration.jei.ModPluginOpenComputers;
  3.15: crazypants.enderio.machines.integration.jei.MachinesPlugin;
  2.52: forestry.factory.recipes.jei.FactoryJeiPlugin;
  2.39: com.cleanroommc.multiblocked.jei.JeiPlugin;
  2.07: com.rwtema.extrautils2.crafting.jei.XUJEIPlugin;
  1.77: com.github.sokyranthedragon.mia.integrations.jer.JeiJerIntegration$1;
  1.57: mezz.jei.plugins.vanilla.VanillaPlugin;
  1.40: jeresources.jei.JEIConfig;
  0.89: com.buuz135.industrial.jei.JEICustomPlugin;
  0.89: nc.integration.jei.NCJEI;
  0.88: com.buuz135.thaumicjei.ThaumcraftJEIPlugin;
  0.69: sblectric.lightningcraft.integration.jei.JEIPlugin;
  0.58: crazypants.enderio.base.integration.jei.JeiPlugin;
  0.52: mctmods.smelteryio.library.util.jei.JEI;
  7.04: Other 139 Plugins
`
        .split(';')
        .map(l => l.split(':'))
        .forEach(([time, name]) => {
          a.labels.push(name);
          a.datasets[0].data.push(time)
        })
        ; return a
    })()
  }
}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={
  options: {
    rotation: Math.PI,
    cutoutPercentage: 55,
    plugins: {
      legend: !1,
      outlabels: {
        stretch: 5,
        padding: 1,
        text: (v)=>v.labels
      },
      doughnutlabel: {
        labels: [
          {
            text: 'FML stuff:',
            color: 'rgba(128, 128, 128, 0.5)',
            font: {size: 18}
          },
          {
            text: [557.36,'s'].join(''),
            color: 'rgba(128, 128, 128, 1)',
            font: {size: 22}
          }
        ]
      },
    }
  },
  type: 'outlabeledPie',
  data: {...(() => {
    let a = {
      labels: [],
      datasets: [{
        backgroundColor: [],
        data: [],
        borderColor: 'rgba(22,22,22,0.3)',
        borderWidth: 2
      }]
    };
`
993A00  14.85s Loading sounds;
994400  14.94s Loading Resource - SoundHandler;
994F00 128.44s ModelLoader: blocks;
995900  34.44s ModelLoader: items;
996300  18.36s ModelLoader: baking;
996D00   3.90s Applying remove recipe actions;
997700   0.03s Applying remove furnace recipe actions;
998200   0.51s Indexing ingredients;
998C00   5.09s Indexing ingredients;
444444 336.82s Other
`
    .split(';')
      .map(l => l.match(/(\w{6}) *(\d*\.\d*)s (.*)/))
      .forEach(([, col, time, name]) => {
        a.labels.push([name, ' ', time, 's'].join(''));
        a.datasets[0].data.push(parseFloat(time));
        a.datasets[0].backgroundColor.push([String.fromCharCode(35), col].join(''))
      })
      ; return a
  })()}
}"/>
</p>

<br>
