## Minecraft load time benchmark

### Interactions

---

<p align="center" style="font-size:160%;">
MC total load time:<br>
937.09 sec
<br>
<sup><sub>(
15:37 min
)</sub></sup>
</p>

<br>


<p align="center">
<img src="https://quickchart.io/chart?w=400&h=30&c={%20type:%20'horizontalBar',%20data:%20{%20datasets:%20[%20{label:%20'MODS:',%20data:%20[484.17]},%20{label:%20'FML%20stuff:',%20data:%20[452.91]}%20]%20},%20options:%20{%20scales:%20{%20xAxes:%20[{display:%20false,stacked:%20true}],%20yAxes:%20[{display:%20false,stacked:%20true}],%20},%20elements:%20{rectangle:%20{borderWidth:%202}},%20legend:%20{display:%20false,},%20plugins:%20{datalabels:%20{color:%20'white',formatter:%20(value,%20context)%20=>%20[context.dataset.label,%20value].join('%20')%20}}%20}%20}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={%20type:%20'outlabeledPie',%20options:%20{%20cutoutPercentage:%2025,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v,i)=>[%20v.labels[v.dataIndex],'%20',%20(v.percent*1000|0)/10,%20String.fromCharCode(37)].join('')%20}%20}%20},%20data:%20{...%20`%20436e17%2053.01s%20Had%20Enough%20Items;%203C6315%2032.92s%20Had%20Enough%20Items%20(Plugins);%208f3087%2019.43s%20Forge%20Mod%20Loader;%208f3041%2016.82s%20Tech%20Reborn;%20516fa8%2014.34s%20Ender%20IO;%205161a8%2013.73s%20CraftTweaker2;%20813e81%2012.38s%20OpenComputers;%209d2ccd%209.80s%20Immersive%20Intelligence;%208f304e%209.51s%20Astral%20Sorcery;%20cd922c%208.74s%20NuclearCraft;%20813e4d%208.57s%20GroovyScript;%208c2ccd%207.65s%20Immersive%20Engineering;%20213664%207.31s%20Forestry;%208451a8%205.85s%20LibrarianLib%20Stage%202;%202caacd%205.80s%20PneumaticCraft:%20Repressurized;%20436e17%205.12s%20Integrated%20Dynamics;%20219e4b%204.86s%20Multiblock'd;%20216364%204.70s%20Xaero's%20Minimap;%20814a3e%204.68s%20RFTools;%203e8160%204.53s%20The%20Twilight%20Forest;%20216427%204.49s%20Resource%20Pack%20Organizer;%20515ba8%204.33s%20WrapUp;%20a86e51%204.29s%20Extra%20Utilities%202;%203eb2ba%203.84s%20Botania;%203e68ba%203.79s%20AE2%20Unofficial%20Extended%20Life;%203e6c81%203.68s%20Solar%20Flux%20Reborn;%20444444%20123.06s%2068%20Other%20mods;%20333333%2077.62s%20212%20'Fast'%20mods%20(load%201.0s%20-%200.1s);%20222222%209.33s%20239%20'Instant'%20mods%20(load%20%3C%200.1s)%20`%20.split(';').reduce((a,%20l)%20=>%20{%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/)%20.slice(1).map((a,%20i)%20=>%20[[String.fromCharCode(35),a].join(''),%20parseFloat(a),%20a][i])%20.forEach((s,%20i)%20=>%20[a.datasets[0].backgroundColor,%20a.datasets[0].data,%20a.labels][i].push(s)%20);%20return%20a%20},%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%201%20}]%20})%20}%20}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={%20options:%20{%20scales:%20{%20xAxes:%20[{stacked:%20true}],%20yAxes:%20[{stacked:%20true}],%20},%20plugins:%20{%20datalabels:%20{%20anchor:%20'end',%20align:%20'top',%20color:%20'white',%20backgroundColor:%20'rgba(46,%20140,%20171,%200.6)',%20borderColor:%20'rgba(41,%20168,%20194,%201.0)',%20borderWidth:%200.5,%20borderRadius:%203,%20padding:%200,%20font:%20{size:10},%20formatter:%20(v,ctx)%20=>%20ctx.datasetIndex!=ctx.chart.data.datasets.length-1%20?%20null%20:%20[((ctx.chart.data.datasets.reduce((a,b)=>a-%20-b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')%20},%20colorschemes:%20{%20scheme:%20'office.Damask6'%20}%20}%20},%20type:%20'bar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[]%20};%20`%201:%20Construction;%202:%20Loading%20Resources;%203:%20PreInitialization;%204:%20Initialization;%205:%20InterModComms$IMC;%206:%20PostInitialization;%207:%20LoadComplete;%208:%20ModIdMapping%20`%20.split(';')%20.map(l%20=>%20l.match(/\d:%20(.*)/).slice(1))%20.forEach(([name])%20=>%20a.datasets.push({%20label:%20name,%20data:%20[]%20}));%20`%201%202%203%204%205%206%207%208%20;%20Tech%20Reborn%20|%200.16|%200.01|%2013.72|%200.62|%200.00|%202.32|%200.00|%200.00;%20Ender%20IO%20|%202.48|%200.01|%205.20|%200.89|%204.33|%200.23|%200.00|%201.21;%20CraftTweaker2%20|%201.15|%200.00|%209.98|%200.01|%200.00|%202.58|%200.00|%200.00;%20OpenComputers%20|%200.21|%200.02|%207.42|%204.42|%200.30|%200.00|%200.00|%200.00;%20Immersive%20Intelligence%20|%201.90|%200.01|%203.61|%201.26|%200.00|%203.02|%200.00|%200.00;%20Astral%20Sorcery%20|%200.47|%200.01|%205.79|%202.35|%200.00|%200.90|%200.00|%200.00;%20NuclearCraft%20|%201.23|%200.01|%206.17|%200.87|%200.00|%200.34|%200.00|%200.12;%20GroovyScript%20|%202.89|%200.01|%200.00|%200.02|%200.00|%205.65|%200.00|%200.00;%20Immersive%20Engineering%20|%201.22|%200.01|%201.65|%201.55|%200.00|%203.22|%200.00|%200.00;%20Forestry%20|%200.67|%200.02|%204.77|%201.38|%200.01|%200.48|%200.00|%200.00;%20LibrarianLib%20Stage%202%20|%200.01|%200.05|%205.63|%200.13|%200.00|%200.03|%200.00|%200.00;%20PneumaticCraft:%20Repressurized%20|%200.84|%200.01|%201.95|%201.40|%200.00|%201.60|%200.00|%200.00%20`%20.split(';').slice(1)%20.map(l%20=>%20l.split('|').map(s%20=>%20s.trim()))%20.forEach(([name,%20...arr],%20i)%20=>%20{%20a.labels.push(name);%20arr.forEach((v,%20j)%20=>%20a.datasets[j].data[i]%20=%20v)%20});%20return%20a%20})()}%20}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={%20options:%20{%20elements:%20{%20rectangle:%20{%20borderWidth:%201%20}%20},%20legend:%20false%20},%20type:%20'horizontalBar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20'rgba(0,%2099,%20132,%200.5)',%20borderColor:%20'rgb(0,%2099,%20132)',%20data:%20[]%20}]%20};%20`%205.10:%20li.cil.oc.integration.jei.ModPluginOpenComputers;%203.39:%20cofh.thermalexpansion.plugins.jei.JEIPluginTE;%202.92:%20crazypants.enderio.machines.integration.jei.MachinesPlugin;%202.58:%20com.cleanroommc.multiblocked.jei.JeiPlugin;%202.07:%20forestry.factory.recipes.jei.FactoryJeiPlugin;%201.60:%20jeresources.jei.JEIConfig;%201.53:%20com.rwtema.extrautils2.crafting.jei.XUJEIPlugin;%201.32:%20com.github.sokyranthedragon.mia.integrations.jer.JeiJerIntegration$1;%201.02:%20mezz.jei.plugins.vanilla.VanillaPlugin;%200.99:%20com.buuz135.thaumicjei.ThaumcraftJEIPlugin;%200.86:%20nc.integration.jei.NCJEI;%200.77:%20sblectric.lightningcraft.integration.jei.JEIPlugin;%200.76:%20com.buuz135.industrial.jei.JEICustomPlugin;%200.60:%20crazypants.enderio.base.integration.jei.JeiPlugin;%200.40:%20net.bdew.jeibees.BeesJEIPlugin;%200.37:%20mctmods.smelteryio.library.util.jei.JEI;%200.36:%20techreborn.compat.jei.TechRebornJeiPlugin;%200.31:%20lach_01298.qmd.jei.QMDJEI;%200.28:%20zmaster587.advancedRocketry.integration.jei.ARPlugin;%200.27:%20wanion.biggercraftingtables.compat.jei.BiggerCraftingTablesJEIPlugin;%205.42:%20Other%20134%20Plugins%20`%20.split(';')%20.map(l%20=>%20l.split(':'))%20.forEach(([time,%20name])%20=>%20{%20a.labels.push(name);%20a.datasets[0].data.push(time)%20})%20;%20return%20a%20})()%20}%20}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={%20options:%20{%20rotation:%20Math.PI,%20cutoutPercentage:%2055,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v)=>v.labels%20},%20doughnutlabel:%20{%20labels:%20[%20{%20text:%20'FML%20stuff:',%20color:%20'rgba(128,%20128,%20128,%200.5)',%20font:%20{size:%2018}%20},%20{%20text:%20[452.91,'s'].join(''),%20color:%20'rgba(128,%20128,%20128,%201)',%20font:%20{size:%2022}%20}%20]%20},%20}%20},%20type:%20'outlabeledPie',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%202%20}]%20};%20`%20993A00%2010.07s%20Loading%20sounds;%20994400%2010.15s%20Loading%20Resource%20-%20SoundHandler;%20994F00%2095.60s%20ModelLoader:%20blocks;%20995900%2023.69s%20ModelLoader:%20items;%20996300%2023.24s%20ModelLoader:%20baking;%20996D00%201.83s%20Applying%20remove%20recipe%20actions;%20997700%200.06s%20Applying%20remove%20furnace%20recipe%20actions;%20998200%201.04s%20Indexing%20ingredients;%20998C00%2013.25s%20Indexing%20ingredients;%20444444%20273.99s%20Other%20`%20.split(';')%20.map(l%20=>%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/))%20.forEach(([,%20col,%20time,%20name])%20=>%20{%20a.labels.push([name,%20'%20',%20time,%20's'].join(''));%20a.datasets[0].data.push(parseFloat(time));%20a.datasets[0].backgroundColor.push([String.fromCharCode(35),%20col].join(''))%20})%20;%20return%20a%20})()}%20}"/>
</p>

<br>
