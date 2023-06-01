## Minecraft load time benchmark

### GTQT

---

<p align="center" style="font-size:160%;">
MC total load time:<br>
470.37 sec
<br>
<sup><sub>(
7:50 min
)</sub></sup>
</p>

<br>


<p align="center">
<img src="https://quickchart.io/chart?w=400&h=30&c={%20type:%20'horizontalBar',%20data:%20{%20datasets:%20[%20{label:%20'MODS:',%20data:%20[242.63]},%20{label:%20'FML%20stuff:',%20data:%20[227.73]}%20]%20},%20options:%20{%20scales:%20{%20xAxes:%20[{display:%20false,stacked:%20true}],%20yAxes:%20[{display:%20false,stacked:%20true}],%20},%20elements:%20{rectangle:%20{borderWidth:%202}},%20legend:%20{display:%20false,},%20plugins:%20{datalabels:%20{color:%20'white',formatter:%20(value,%20context)%20=>%20[context.dataset.label,%20value].join('%20')%20}}%20}%20}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={%20type:%20'outlabeledPie',%20options:%20{%20cutoutPercentage:%2025,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v,i)=>[%20v.labels[v.dataIndex],'%20',%20(v.percent*1000|0)/10,%20String.fromCharCode(37)].join('')%20}%20}%20},%20data:%20{...%20`%20436e17%2019.76s%20Had%20Enough%20Items;%203C6315%2019.24s%20Had%20Enough%20Items%20(Plugins);%205161a8%2026.70s%20CraftTweaker2;%207c813e%2011.39s%20Thaumcraft;%20214d9e%209.28s%20Minecraft%20Forge;%20a651a8%209.20s%20IndustrialCraft%202;%20516fa8%208.39s%20Ender%20IO;%20813e81%207.76s%20OpenComputers;%203e76ba%206.40s%20Railcraft;%20213664%203.81s%20Forestry;%206aba3e%203.60s%20Galacticraft;%20cd922c%203.16s%20NuclearCraft;%20308f53%203.02s%20Village%20Names;%206e2717%202.95s%20Extra%20Planets;%202c9e21%202.89s%20GregTech;%20306e8f%202.82s%20Custom%20Loading%20Screen;%20436e17%202.69s%20Integrated%20Dynamics;%20a86e51%202.44s%20Extra%20Utilities%202;%208f308f%202.17s%20JourneyMap;%203e8160%201.93s%20The%20Twilight%20Forest;%203eb2ba%201.92s%20Botania;%20516fa8%201.87s%20Touhou%20Little%20Maid;%208f3087%201.84s%20Forge%20Mod%20Loader;%20813e76%201.78s%20Modular%20Machinery:%20Community%20Edition;%209e2174%201.76s%20Tinkers'%20Construct;%203e68ba%201.58s%20AE2%20Unofficial%20Extended%20Life;%20444444%2011.65s%209%20Other%20mods;%20333333%2069.58s%20254%20'Fast'%20mods%20(load%201.0s%20-%200.1s);%20222222%201.05s%2022%20'Instant'%20mods%20(load%20%3C%200.1s)%20`%20.split(';').reduce((a,%20l)%20=>%20{%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/)%20.slice(1).map((a,%20i)%20=>%20[[String.fromCharCode(35),a].join(''),%20parseFloat(a),%20a][i])%20.forEach((s,%20i)%20=>%20[a.datasets[0].backgroundColor,%20a.datasets[0].data,%20a.labels][i].push(s)%20);%20return%20a%20},%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%201%20}]%20})%20}%20}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={%20options:%20{%20scales:%20{%20xAxes:%20[{stacked:%20true}],%20yAxes:%20[{stacked:%20true}],%20},%20plugins:%20{%20datalabels:%20{%20anchor:%20'end',%20align:%20'top',%20color:%20'white',%20backgroundColor:%20'rgba(46,%20140,%20171,%200.6)',%20borderColor:%20'rgba(41,%20168,%20194,%201.0)',%20borderWidth:%200.5,%20borderRadius:%203,%20padding:%200,%20font:%20{size:10},%20formatter:%20(v,ctx)%20=>%20ctx.datasetIndex!=ctx.chart.data.datasets.length-1%20?%20null%20:%20[((ctx.chart.data.datasets.reduce((a,b)=>a-%20-b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')%20},%20colorschemes:%20{%20scheme:%20'office.Damask6'%20}%20}%20},%20type:%20'bar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[]%20};%20`%201:%20Construction;%202:%20Loading%20Resources;%203:%20PreInitialization;%204:%20Initialization;%205:%20InterModComms$IMC;%206:%20PostInitialization;%207:%20LoadComplete;%208:%20ModIdMapping%20`%20.split(';')%20.map(l%20=>%20l.match(/\d:%20(.*)/).slice(1))%20.forEach(([name])%20=>%20a.datasets.push({%20label:%20name,%20data:%20[]%20}));%20`%201%202%203%204%205%206%207%208%20;%20CraftTweaker2%20|%200.38|%200.00|%202.20|%200.03|%200.00|%208.50|%2015.59|%200.00;%20Thaumcraft%20|%200.34|%200.01|%200.24|%200.34|%200.00|%2010.45|%200.02|%200.00;%20IndustrialCraft%202%20|%200.45|%200.01|%207.31|%200.68|%200.00|%200.74|%200.02|%200.00;%20Ender%20IO%20|%201.17|%200.01|%202.82|%200.38|%202.77|%200.23|%200.02|%200.99;%20OpenComputers%20|%200.12|%200.01|%205.40|%202.07|%200.11|%200.02|%200.02|%200.00;%20Railcraft%20|%200.20|%200.01|%204.81|%200.95|%200.00|%200.41|%200.02|%200.00;%20Forestry%20|%200.22|%200.01|%202.45|%200.64|%200.00|%200.47|%200.02|%200.00;%20Galacticraft%20|%200.13|%200.01|%200.83|%202.35|%200.00|%200.27|%200.02|%200.00;%20NuclearCraft%20|%200.47|%200.01|%202.06|%200.27|%200.00|%200.28|%200.02|%200.05;%20Village%20Names%20|%200.12|%200.00|%202.72|%200.14|%200.00|%200.02|%200.02|%200.00;%20Extra%20Planets%20|%200.26|%200.01|%202.08|%200.30|%200.00|%200.28|%200.02|%200.00;%20GregTech%20|%200.20|%200.02|%201.87|%200.54|%200.00|%200.24|%200.03|%200.00%20`%20.split(';').slice(1)%20.map(l%20=>%20l.split('|').map(s%20=>%20s.trim()))%20.forEach(([name,%20...arr],%20i)%20=>%20{%20a.labels.push(name);%20arr.forEach((v,%20j)%20=>%20a.datasets[j].data[i]%20=%20v)%20});%20return%20a%20})()}%20}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={%20options:%20{%20elements:%20{%20rectangle:%20{%20borderWidth:%201%20}%20},%20legend:%20false%20},%20type:%20'horizontalBar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20'rgba(0,%2099,%20132,%200.5)',%20borderColor:%20'rgb(0,%2099,%20132)',%20data:%20[]%20}]%20};%20`%203.13:%20gregtech.integration.jei.GTJeiPlugin;%202.55:%20li.cil.oc.integration.jei.ModPluginOpenComputers;%201.98:%20crazypants.enderio.machines.integration.jei.MachinesPlugin;%201.81:%20jeresources.jei.JEIConfig;%201.46:%20com.rwtema.extrautils2.crafting.jei.XUJEIPlugin;%201.34:%20forestry.factory.recipes.jei.FactoryJeiPlugin;%201.15:%20binnie.extratrees.integration.jei.ExtraTreesJeiPlugin;%200.97:%20mezz.jei.plugins.vanilla.VanillaPlugin;%200.72:%20ic2.jeiIntegration.SubModule;%200.59:%20com.buuz135.thaumicjei.ThaumcraftJEIPlugin;%200.46:%20thedarkcolour.futuremc.compat.jei.FutureMCJEIPlugin;%200.38:%20com.mjr.extraplanets.jei.ExtraPlanetsJEI;%200.31:%20nc.integration.jei.NCJEI;%200.17:%20crazypants.enderio.base.integration.jei.JeiPlugin;%200.16:%20xt9.deepmoblearning.plugins.jei.Plugin;%200.15:%20hellfirepvp.modularmachinery.common.integration.ModIntegrationJEI;%200.12:%20slimeknights.tconstruct.plugin.jei.JEIPlugin;%200.12:%20WayofTime.bloodmagic.compat.jei.BloodMagicJEIPlugin;%200.11:%20mods.railcraft.common.plugins.jei.RailcraftJEIPlugin;%200.11:%20micdoodle8.mods.galacticraft.core.client.jei.GalacticraftJEI;%201.48:%20Other%2079%20Plugins%20`%20.split(';')%20.map(l%20=>%20l.split(':'))%20.forEach(([time,%20name])%20=>%20{%20a.labels.push(name);%20a.datasets[0].data.push(time)%20})%20;%20return%20a%20})()%20}%20}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={%20options:%20{%20rotation:%20Math.PI,%20cutoutPercentage:%2055,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v)=>v.labels%20},%20doughnutlabel:%20{%20labels:%20[%20{%20text:%20'FML%20stuff:',%20color:%20'rgba(128,%20128,%20128,%200.5)',%20font:%20{size:%2018}%20},%20{%20text:%20[227.73,'s'].join(''),%20color:%20'rgba(128,%20128,%20128,%201)',%20font:%20{size:%2022}%20}%20]%20},%20}%20},%20type:%20'outlabeledPie',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%202%20}]%20};%20`%20993A00%201.49s%20Loading%20sounds;%20994400%201.59s%20Loading%20Resource%20-%20SoundHandler;%20994F00%2026.43s%20ModelLoader:%20blocks;%20995900%2032.11s%20ModelLoader:%20items;%20996300%208.70s%20ModelLoader:%20baking;%20996D00%200.11s%20Applying%20remove%20recipe%20actions;%20997700%200.05s%20Applying%20remove%20furnace%20recipe%20actions;%20998200%200.27s%20Indexing%20ingredients;%20998C00%204.67s%20Indexing%20ingredients;%20444444%20152.31s%20Other%20`%20.split(';')%20.map(l%20=>%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/))%20.forEach(([,%20col,%20time,%20name])%20=>%20{%20a.labels.push([name,%20'%20',%20time,%20's'].join(''));%20a.datasets[0].data.push(parseFloat(time));%20a.datasets[0].backgroundColor.push([String.fromCharCode(35),%20col].join(''))%20})%20;%20return%20a%20})()}%20}"/>
</p>

<br>
