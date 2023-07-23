## Minecraft load time benchmark

### Interactions

---

<p align="center" style="font-size:160%;">
MC total load time:<br>
1076.92 sec
<br>
<sup><sub>(
17:56 min
)</sub></sup>
</p>

<br>


<p align="center">
<img src="https://quickchart.io/chart?w=400&h=30&c={%20type:%20'horizontalBar',%20data:%20{%20datasets:%20[%20{label:%20'MODS:',%20data:%20[622.99]},%20{label:%20'FML%20stuff:',%20data:%20[453.93]}%20]%20},%20options:%20{%20scales:%20{%20xAxes:%20[{display:%20false,stacked:%20true}],%20yAxes:%20[{display:%20false,stacked:%20true}],%20},%20elements:%20{rectangle:%20{borderWidth:%202}},%20legend:%20{display:%20false,},%20plugins:%20{datalabels:%20{color:%20'white',formatter:%20(value,%20context)%20=>%20[context.dataset.label,%20value].join('%20')%20}}%20}%20}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={%20type:%20'outlabeledPie',%20options:%20{%20cutoutPercentage:%2025,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v,i)=>[%20v.labels[v.dataIndex],'%20',%20(v.percent*1000|0)/10,%20String.fromCharCode(37)].join('')%20}%20}%20},%20data:%20{...%20`%20436e17%2083.51s%20Had%20Enough%20Items;%203C6315%2049.93s%20Had%20Enough%20Items%20(Plugins);%208f3087%2023.19s%20Forge%20Mod%20Loader;%20813e81%2018.15s%20OpenComputers;%20516fa8%2017.75s%20Ender%20IO;%20219e4b%2017.48s%20Multiblock'd;%208f3041%2017.43s%20Tech%20Reborn;%205161a8%2016.27s%20CraftTweaker2;%20213664%2010.57s%20Forestry;%208f304e%2010.05s%20Astral%20Sorcery;%20cd922c%209.75s%20NuclearCraft;%208c2ccd%209.36s%20Immersive%20Engineering;%202caacd%207.93s%20PneumaticCraft:%20Repressurized;%208451a8%207.56s%20LibrarianLib%20Stage%202;%20216364%207.46s%20Xaero's%20Minimap;%206e176a%206.97s%20Unlimited%20Chisel%20Works;%20436e17%206.15s%20Integrated%20Dynamics;%20515ba8%205.63s%20WrapUp;%20814a3e%205.15s%20RFTools;%203e68ba%205.13s%20AE2%20Unofficial%20Extended%20Life;%20216364%205.11s%20Thermal%20Expansion;%20444444%20187.22s%2089%20Other%20mods;%20333333%2086.93s%20240%20'Fast'%20mods%20(load%201.0s%20-%200.1s);%20222222%208.32s%20214%20'Instant'%20mods%20(load%20%3C%200.1s)%20`%20.split(';').reduce((a,%20l)%20=>%20{%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/)%20.slice(1).map((a,%20i)%20=>%20[[String.fromCharCode(35),a].join(''),%20parseFloat(a),%20a][i])%20.forEach((s,%20i)%20=>%20[a.datasets[0].backgroundColor,%20a.datasets[0].data,%20a.labels][i].push(s)%20);%20return%20a%20},%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%201%20}]%20})%20}%20}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={%20options:%20{%20scales:%20{%20xAxes:%20[{stacked:%20true}],%20yAxes:%20[{stacked:%20true}],%20},%20plugins:%20{%20datalabels:%20{%20anchor:%20'end',%20align:%20'top',%20color:%20'white',%20backgroundColor:%20'rgba(46,%20140,%20171,%200.6)',%20borderColor:%20'rgba(41,%20168,%20194,%201.0)',%20borderWidth:%200.5,%20borderRadius:%203,%20padding:%200,%20font:%20{size:10},%20formatter:%20(v,ctx)%20=>%20ctx.datasetIndex!=ctx.chart.data.datasets.length-1%20?%20null%20:%20[((ctx.chart.data.datasets.reduce((a,b)=>a-%20-b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')%20},%20colorschemes:%20{%20scheme:%20'office.Damask6'%20}%20}%20},%20type:%20'bar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[]%20};%20`%201:%20Construction;%202:%20Loading%20Resources;%203:%20PreInitialization;%204:%20Initialization;%205:%20InterModComms$IMC;%206:%20PostInitialization;%207:%20LoadComplete;%208:%20ModIdMapping%20`%20.split(';')%20.map(l%20=>%20l.match(/\d:%20(.*)/).slice(1))%20.forEach(([name])%20=>%20a.datasets.push({%20label:%20name,%20data:%20[]%20}));%20`%201%202%203%204%205%206%207%208%20;%20OpenComputers%20|%200.28|%200.02|%2010.56|%206.84|%200.45|%200.00|%200.00|%200.00;%20Ender%20IO%20|%202.56|%200.01|%205.10|%201.37|%206.75|%200.37|%200.00|%201.59;%20Multiblock'd%20|%200.17|%200.00|%2011.78|%200.53|%200.00|%204.98|%200.02|%200.00;%20Tech%20Reborn%20|%200.13|%200.01|%2010.37|%203.97|%200.00|%202.96|%200.00|%200.00;%20CraftTweaker2%20|%201.58|%200.00|%208.30|%200.01|%200.00|%206.38|%200.00|%200.00;%20Forestry%20|%201.04|%200.01|%205.97|%203.07|%200.02|%200.47|%200.00|%200.00;%20Astral%20Sorcery%20|%200.33|%200.01|%205.38|%202.96|%200.00|%201.37|%200.00|%200.00;%20NuclearCraft%20|%201.28|%200.01|%206.68|%201.15|%200.00|%200.47|%200.00|%200.17;%20Immersive%20Engineering%20|%201.47|%200.01|%202.02|%202.16|%200.00|%203.70|%200.00|%200.00;%20PneumaticCraft:%20Repressurized%20|%201.32|%200.01|%202.40|%202.11|%200.00|%202.09|%200.00|%200.00;%20LibrarianLib%20Stage%202%20|%200.01|%200.05|%207.26|%200.19|%200.00|%200.05|%200.00|%200.00;%20Xaero's%20Minimap%20|%200.34|%200.00|%200.04|%204.09|%200.00|%203.00|%200.00|%200.00%20`%20.split(';').slice(1)%20.map(l%20=>%20l.split('|').map(s%20=>%20s.trim()))%20.forEach(([name,%20...arr],%20i)%20=>%20{%20a.labels.push(name);%20arr.forEach((v,%20j)%20=>%20a.datasets[j].data[i]%20=%20v)%20});%20return%20a%20})()}%20}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={%20options:%20{%20elements:%20{%20rectangle:%20{%20borderWidth:%201%20}%20},%20legend:%20false%20},%20type:%20'horizontalBar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20'rgba(0,%2099,%20132,%200.5)',%20borderColor:%20'rgb(0,%2099,%20132)',%20data:%20[]%20}]%20};%20`%207.67:%20li.cil.oc.integration.jei.ModPluginOpenComputers;%204.56:%20jeresources.jei.JEIConfig;%204.53:%20cofh.thermalexpansion.plugins.jei.JEIPluginTE;%203.51:%20com.cleanroommc.multiblocked.jei.JeiPlugin;%203.35:%20crazypants.enderio.machines.integration.jei.MachinesPlugin;%203.26:%20forestry.factory.recipes.jei.FactoryJeiPlugin;%203.16:%20com.rwtema.extrautils2.crafting.jei.XUJEIPlugin;%201.56:%20com.buuz135.industrial.jei.JEICustomPlugin;%201.48:%20nc.integration.jei.NCJEI;%201.38:%20mezz.jei.plugins.vanilla.VanillaPlugin;%201.09:%20com.buuz135.thaumicjei.ThaumcraftJEIPlugin;%200.89:%20crazypants.enderio.base.integration.jei.JeiPlugin;%200.80:%20sblectric.lightningcraft.integration.jei.JEIPlugin;%200.76:%20techreborn.compat.jei.TechRebornJeiPlugin;%200.54:%20mctmods.smelteryio.library.util.jei.JEI;%2011.39:%20Other%20144%20Plugins%20`%20.split(';')%20.map(l%20=>%20l.split(':'))%20.forEach(([time,%20name])%20=>%20{%20a.labels.push(name);%20a.datasets[0].data.push(time)%20})%20;%20return%20a%20})()%20}%20}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={%20options:%20{%20rotation:%20Math.PI,%20cutoutPercentage:%2055,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v)=>v.labels%20},%20doughnutlabel:%20{%20labels:%20[%20{%20text:%20'FML%20stuff:',%20color:%20'rgba(128,%20128,%20128,%200.5)',%20font:%20{size:%2018}%20},%20{%20text:%20[453.93,'s'].join(''),%20color:%20'rgba(128,%20128,%20128,%201)',%20font:%20{size:%2022}%20}%20]%20},%20}%20},%20type:%20'outlabeledPie',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%202%20}]%20};%20`%20993A00%2010.11s%20Loading%20sounds;%20994400%2010.28s%20Loading%20Resource%20-%20SoundHandler;%20994F00%204.94s%20Applying%20remove%20recipe%20actions;%20995900%200.09s%20Applying%20remove%20furnace%20recipe%20actions;%20996300%201.80s%20Indexing%20ingredients;%20996D00%2020.65s%20Indexing%20ingredients;%20444444%20406.06s%20Other%20`%20.split(';')%20.map(l%20=>%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/))%20.forEach(([,%20col,%20time,%20name])%20=>%20{%20a.labels.push([name,%20'%20',%20time,%20's'].join(''));%20a.datasets[0].data.push(parseFloat(time));%20a.datasets[0].backgroundColor.push([String.fromCharCode(35),%20col].join(''))%20})%20;%20return%20a%20})()}%20}"/>
</p>

<br>
