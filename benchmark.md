## Minecraft load time benchmark

### Interactions

---

<p align="center" style="font-size:160%;">
MC total load time:<br>
953.42 sec
<br>
<sup><sub>(
15:53 min
)</sub></sup>
</p>

<br>


<p align="center">
<img src="https://quickchart.io/chart?w=400&h=30&c={%20type:%20'horizontalBar',%20data:%20{%20datasets:%20[%20{label:%20'MODS:',%20data:%20[513.05]},%20{label:%20'FML%20stuff:',%20data:%20[440.37]}%20]%20},%20options:%20{%20scales:%20{%20xAxes:%20[{display:%20false,stacked:%20true}],%20yAxes:%20[{display:%20false,stacked:%20true}],%20},%20elements:%20{rectangle:%20{borderWidth:%202}},%20legend:%20{display:%20false,},%20plugins:%20{datalabels:%20{color:%20'white',formatter:%20(value,%20context)%20=>%20[context.dataset.label,%20value].join('%20')%20}}%20}%20}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={%20type:%20'outlabeledPie',%20options:%20{%20cutoutPercentage:%2025,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v,i)=>[%20v.labels[v.dataIndex],'%20',%20(v.percent*1000|0)/10,%20String.fromCharCode(37)].join('')%20}%20}%20},%20data:%20{...%20`%20436e17%2054.15s%20Had%20Enough%20Items;%203C6315%2030.83s%20Had%20Enough%20Items%20(Plugins);%208f3087%2029.26s%20Forge%20Mod%20Loader;%20516fa8%2015.95s%20Ender%20IO;%205161a8%2014.67s%20CraftTweaker2;%208f3041%2012.93s%20Tech%20Reborn;%20813e81%2012.85s%20OpenComputers;%208f304e%208.95s%20Astral%20Sorcery;%20813e4d%208.67s%20GroovyScript;%20bab23e%208.48s%20End%20Expansion;%20cd922c%208.25s%20NuclearCraft;%20216427%208.03s%20Resource%20Pack%20Organizer;%208c2ccd%207.98s%20Immersive%20Engineering;%20213664%206.89s%20Forestry;%202caacd%206.84s%20PneumaticCraft:%20Repressurized;%206e176a%206.76s%20Unlimited%20Chisel%20Works;%208451a8%206.63s%20LibrarianLib%20Stage%202;%20436e17%205.95s%20Integrated%20Dynamics;%20216364%205.77s%20Xaero's%20Minimap;%203e8160%205.38s%20The%20Twilight%20Forest;%20219e4b%205.17s%20Multiblock'd;%20515ba8%204.85s%20WrapUp;%203eb2ba%204.65s%20Botania;%20814a3e%204.63s%20RFTools;%20216364%203.91s%20Thermal%20Expansion;%20a86e51%203.85s%20Extra%20Utilities%202;%20444444%20136.28s%2073%20Other%20mods;%20333333%2075.39s%20213%20'Fast'%20mods%20(load%201.0s%20-%200.1s);%20222222%209.12s%20232%20'Instant'%20mods%20(load%20%3C%200.1s)%20`%20.split(';').reduce((a,%20l)%20=>%20{%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/)%20.slice(1).map((a,%20i)%20=>%20[[String.fromCharCode(35),a].join(''),%20parseFloat(a),%20a][i])%20.forEach((s,%20i)%20=>%20[a.datasets[0].backgroundColor,%20a.datasets[0].data,%20a.labels][i].push(s)%20);%20return%20a%20},%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%201%20}]%20})%20}%20}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={%20options:%20{%20scales:%20{%20xAxes:%20[{stacked:%20true}],%20yAxes:%20[{stacked:%20true}],%20},%20plugins:%20{%20datalabels:%20{%20anchor:%20'end',%20align:%20'top',%20color:%20'white',%20backgroundColor:%20'rgba(46,%20140,%20171,%200.6)',%20borderColor:%20'rgba(41,%20168,%20194,%201.0)',%20borderWidth:%200.5,%20borderRadius:%203,%20padding:%200,%20font:%20{size:10},%20formatter:%20(v,ctx)%20=>%20ctx.datasetIndex!=ctx.chart.data.datasets.length-1%20?%20null%20:%20[((ctx.chart.data.datasets.reduce((a,b)=>a-%20-b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')%20},%20colorschemes:%20{%20scheme:%20'office.Damask6'%20}%20}%20},%20type:%20'bar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[]%20};%20`%201:%20Construction;%202:%20Loading%20Resources;%203:%20PreInitialization;%204:%20Initialization;%205:%20InterModComms$IMC;%206:%20PostInitialization;%207:%20LoadComplete;%208:%20ModIdMapping%20`%20.split(';')%20.map(l%20=>%20l.match(/\d:%20(.*)/).slice(1))%20.forEach(([name])%20=>%20a.datasets.push({%20label:%20name,%20data:%20[]%20}));%20`%201%202%203%204%205%206%207%208%20;%20Ender%20IO%20|%202.76|%200.01|%206.83|%200.81|%204.03|%200.22|%200.00|%201.29;%20CraftTweaker2%20|%201.10|%200.00|%2010.94|%200.01|%200.00|%202.61|%200.00|%200.00;%20Tech%20Reborn%20|%200.18|%200.00|%209.82|%200.67|%200.00|%202.25|%200.00|%200.00;%20OpenComputers%20|%200.32|%200.02|%207.58|%204.57|%200.36|%200.00|%200.00|%200.00;%20Astral%20Sorcery%20|%200.43|%200.01|%205.42|%202.22|%200.00|%200.87|%200.00|%200.00;%20GroovyScript%20|%202.85|%200.01|%200.00|%200.04|%200.00|%205.77|%200.00|%200.00;%20End%20Expansion%20|%200.07|%200.00|%208.40|%200.01|%200.00|%200.00|%200.00|%200.00;%20NuclearCraft%20|%201.43|%200.01|%205.68|%200.71|%200.00|%200.31|%200.00|%200.13;%20Resource%20Pack%20Organizer%20|%200.04|%200.00|%207.99|%200.00|%200.00|%200.00|%200.00|%200.00;%20Immersive%20Engineering%20|%201.24|%200.01|%202.01|%201.62|%200.00|%203.10|%200.00|%200.00;%20Forestry%20|%200.59|%200.01|%204.47|%201.47|%200.01|%200.34|%200.00|%200.00;%20PneumaticCraft:%20Repressurized%20|%200.85|%200.01|%203.16|%201.36|%200.00|%201.47|%200.00|%200.00%20`%20.split(';').slice(1)%20.map(l%20=>%20l.split('|').map(s%20=>%20s.trim()))%20.forEach(([name,%20...arr],%20i)%20=>%20{%20a.labels.push(name);%20arr.forEach((v,%20j)%20=>%20a.datasets[j].data[i]%20=%20v)%20});%20return%20a%20})()}%20}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={%20options:%20{%20elements:%20{%20rectangle:%20{%20borderWidth:%201%20}%20},%20legend:%20false%20},%20type:%20'horizontalBar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20'rgba(0,%2099,%20132,%200.5)',%20borderColor:%20'rgb(0,%2099,%20132)',%20data:%20[]%20}]%20};%20`%203.92:%20li.cil.oc.integration.jei.ModPluginOpenComputers;%203.19:%20cofh.thermalexpansion.plugins.jei.JEIPluginTE;%203.07:%20crazypants.enderio.machines.integration.jei.MachinesPlugin;%202.27:%20com.cleanroommc.multiblocked.jei.JeiPlugin;%202.20:%20forestry.factory.recipes.jei.FactoryJeiPlugin;%201.66:%20jeresources.jei.JEIConfig;%201.46:%20com.rwtema.extrautils2.crafting.jei.XUJEIPlugin;%201.22:%20com.github.sokyranthedragon.mia.integrations.jer.JeiJerIntegration$1;%200.95:%20mezz.jei.plugins.vanilla.VanillaPlugin;%200.80:%20nc.integration.jei.NCJEI;%200.79:%20com.buuz135.thaumicjei.ThaumcraftJEIPlugin;%200.67:%20com.buuz135.industrial.jei.JEICustomPlugin;%200.65:%20crazypants.enderio.base.integration.jei.JeiPlugin;%200.63:%20sblectric.lightningcraft.integration.jei.JEIPlugin;%200.47:%20mctmods.smelteryio.library.util.jei.JEI;%200.35:%20lach_01298.qmd.jei.QMDJEI;%200.34:%20net.bdew.jeibees.BeesJEIPlugin;%200.31:%20zmaster587.advancedRocketry.integration.jei.ARPlugin;%200.30:%20techreborn.compat.jei.TechRebornJeiPlugin;%200.27:%20wanion.biggercraftingtables.compat.jei.BiggerCraftingTablesJEIPlugin;%205.32:%20Other%20133%20Plugins%20`%20.split(';')%20.map(l%20=>%20l.split(':'))%20.forEach(([time,%20name])%20=>%20{%20a.labels.push(name);%20a.datasets[0].data.push(time)%20})%20;%20return%20a%20})()%20}%20}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={%20options:%20{%20rotation:%20Math.PI,%20cutoutPercentage:%2055,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v)=>v.labels%20},%20doughnutlabel:%20{%20labels:%20[%20{%20text:%20'FML%20stuff:',%20color:%20'rgba(128,%20128,%20128,%200.5)',%20font:%20{size:%2018}%20},%20{%20text:%20[440.37,'s'].join(''),%20color:%20'rgba(128,%20128,%20128,%201)',%20font:%20{size:%2022}%20}%20]%20},%20}%20},%20type:%20'outlabeledPie',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%202%20}]%20};%20`%20993A00%2011.40s%20Loading%20sounds;%20994400%2011.46s%20Loading%20Resource%20-%20SoundHandler;%20994F00%2093.50s%20ModelLoader:%20blocks;%20995900%2021.57s%20ModelLoader:%20items;%20996300%2015.37s%20ModelLoader:%20baking;%20996D00%201.88s%20Applying%20remove%20recipe%20actions;%20997700%200.06s%20Applying%20remove%20furnace%20recipe%20actions;%20998200%200.92s%20Indexing%20ingredients;%20998C00%2012.61s%20Indexing%20ingredients;%20444444%20271.62s%20Other%20`%20.split(';')%20.map(l%20=>%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/))%20.forEach(([,%20col,%20time,%20name])%20=>%20{%20a.labels.push([name,%20'%20',%20time,%20's'].join(''));%20a.datasets[0].data.push(parseFloat(time));%20a.datasets[0].backgroundColor.push([String.fromCharCode(35),%20col].join(''))%20})%20;%20return%20a%20})()}%20}"/>
</p>

<br>
