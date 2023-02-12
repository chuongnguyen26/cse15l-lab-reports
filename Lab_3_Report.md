# Lab Report 3

- Name: Chuong Nguyen
- Email: chn021@ucsd.edu
---

## I use command **grep** for this research:


### Command-line option 1:  -i

#### Example 1:
``` ruby
[cs15lwi23afp@ieng6-201]:berlitz2:547$ grep -i lUCAYANS Bahamas-History.txt

Centuries before the arrival of Columbus, a peaceful 
Amerindian people who called themselves the Luccucairi 
had settled in the Bahamas. Originally from South 
America, they had traveled up through the Caribbean 
islands, surviving by cultivating modest crops and from 
what they caught from sea and shore. Nothing in the 
experience of these gentle people could have prepared 
them for the arrival of the Pinta, the Niña, and the 
Santa Maria at San Salvador on 12 October 1492. 
Columbus believed that he had reached the East Indies 
and mistakenly called these people Indians. We know 
them today as the Lucayans. Columbus claimed the island 
and others in the Bahamas for his royal Spanish 
patrons, but not finding the gold and other riches he 
was seeking, he stayed for only two weeks before 
sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, 
but the number of shipwrecks attest that their galleons 
frequently passed through the archipelago en route to 
and from the Caribbean, Florida, Bermuda, and their 
home ports. On Eleuthera the explorers dug a fresh-
water well — at a spot now known as “Spanish Wells” — 
which was used to replenish the supplies of water on 
their ships before they began the long journey back to 
Europe with their cargoes of South American gold. As 
for the Lucayans, within 25 years all of them, perhaps 
some 30,000 people, were removed from the Bahamas to 
work — and die — in Spanish gold mines and on farms and 
pearl fisheries on Hispaniola (Haiti), Cuba, and 
elsewhere in the Caribbean.
```

- This command "grep -i lUCAYANS Bahamas-History.txt" is searching for and returning lines/paragraph within the Bahamas-History.txt file containing the string Lucayans. The command-line option -i will ignore all cases like uppercase or lowercase characters. This command-line option is useful when the user wants to search for a particular line containing the specified word inside a file but don't remember the cases of the word. In the worst case, using grep itself might return no lines. So using grep -i will avoid such return.
- [Citations: ChatGPT](https://chat.openai.com/chat)

#### Example 2:

``` ruby
[cs15lwi23afp@ieng6-201]:travel_guides:551$ grep -ir "lUcAyAnS" berlitz2

berlitz2/Bahamas-History.txt:Centuries before the 
arrival of Columbus, a peaceful Amerindian people who 
called themselves the Luccucairi had settled in the 
Bahamas. Originally from South America, they had 
traveled up through the Caribbean islands, surviving by 
cultivating modest crops and from what they caught from 
sea and shore. Nothing in the experience of these 
gentle people could have prepared them for the arrival 
of the Pinta, the Niña, and the Santa Maria at San 
Salvador on 12 October 1492. Columbus believed that he 
had reached the East Indies and mistakenly called these 
people Indians. We know them today as the Lucayans. 
Columbus claimed the island and others in the Bahamas 
for his royal Spanish patrons, but not finding the gold 
and other riches he was seeking, he stayed for only two 
weeks before sailing towards Cuba.

berlitz2/Bahamas-History.txt:The Spaniards never 
bothered to settle in the Bahamas, but the number of 
shipwrecks attest that their galleons frequently passed 
through the archipelago en route to and from the 
Caribbean, Florida, Bermuda, and their home ports. On 
Eleuthera the explorers dug a fresh-water well — at a 
spot now known as “Spanish Wells” — which was used to 
replenish the supplies of water on their ships before 
they began the long journey back to Europe with their 
cargoes of South American gold. As for the Lucayans, 
within 25 years all of them, perhaps some 30,000 
people, were removed from the Bahamas to work — and die 
— in Spanish gold mines and on farms and pearl 
fisheries on Hispaniola (Haiti), Cuba, and elsewhere in 
the Caribbean.
```

- This command "grep -ir lUcAyAnS berlitz2 " is searching for and returning text files and the lines/paragraphs inside the files within the berlitz2 directory containing the string Lucayans. The command-line option -i will ignore all cases like uppercase or lowercase characters. While r helps trace throuh all files recursively in the berlitz2 directory. This command-line option is useful when the user wants to search for a particular file containing the specified word in a directory/subdirectories but don't remember the cases of the word. In the worst case, using grep itself might return no files. So using grep -i will avoid such return.
- [Citations: ChatGPT](https://chat.openai.com/chat)


### Command-line option 2:  -v

#### Example 1:

``` ruby
[cs15lwi23afp@ieng6-201]:berlitz2:555$ grep -v "Bahama" Bahamas-History.txt 

A Brief History
Colonization and Piracy
New Providence knew some spells of prosperity in the mid-18th century as privateering resumed with England at war with Spain. The town of Nassau expanded, and improvements were made between 1760 and 1768 by another revered governor, William Shirley from Massachusetts.
The American Revolutionary War
Emancipation and Decline
Nassau became a free port in 1787, sparking a surge in trading activity. Loyalists built a number of the attractive colonial-style homes and public buildings still standing today, and during the War of 1812, privateers enjoyed another profitable spell against American vessels.
Civil War Blockade Running
For a time a new fiber called sisal seemed promising. But Bahamian soil was too poor and Mexico grew a better plant. Neville Chamberlain, future British Prime Minister, took over his family’s sisal operation on Andros in the 1890s. It failed, the natives said, because of that island’s evil elves called chickcharnies, who cast a spell on the family for disturbing the land. Hopes were raised, and also fizzled, over Bahamian citrus and pineapple. Sponging, another vitally important industry at the end of the 19th century, also had setbacks. A hurricane in 1839 drowned some 300 sponge fishermen in the ‘mud’ off Andros, and a devastating fungus some 40 years later killed almost all the sponges.
The 20th Century
Desperate for work, perhaps 20 percent of the Bahamian population left to take construction jobs in Florida between the turn of the century and World War I. During that war hundreds of Bahamians saw active service with British forces. The islands suffered food shortages and a serious bank failure, but nothing more threatening militarily than rumors of German submarines offshore.
Liquor money bought Nassau better houses, churches, lighting, water, roads, sewers, docks, and hotels. The city’s first gambling casino opened in 1920; the first daily air service from Miami began in 1929; the yacht set decided Nassau was fashionable, and many wealthy Americans as well as Prohibition millionaires built homes on the islands.
Then, to the astonishment of the local populace, the Duke of Windsor, having given up his throne for an American divorcée, was named governor of the little colony in 1940. He and the Duchess remained until 1945.
```

- This command "grep -v Bahama Bahamas-History.txt" is searching for and returning lines/paragraph within the Bahamas-History.txt file not containing the string Bahama. The command-line option -v will ignore all lines/paragraphs containing the specified string. This command is case sensitive meaning that "Bahama" and "bAHAMA" are not the same.This command-line option is useful when the user wants to filter out lines/paragraphs containing the specified string.
- [Citations: ChatGPT](https://chat.openai.com/chat)


#### Example 2:

```ruby
[cs15lwi23afp@ieng6-201]:travel_guides:520$ grep -vr "history" berlitz2

berlitz2/Vallarta-WhereToGo.txt:The developed areas are easily divided into three sections: the original resort development at Bahía Santa Cruz, Tangolunda Bay, and the town of Crucecita, home to the area’s residents and workers. The original settlement in this area is Santa María de Huatulco, a more traditional town found 17 miles inland approaching the Sierra foothills, but generally not explored by visitors to Huatulco.
berlitz2/Vallarta-WhereToGo.txt:Along with several older hotels, banks, and various tourist services, the Bahía Santa Cruz is home to a marina, from which numerous bay cruises and private panga fishing and sightseeing charters depart. Several seafood restaurants are located on a stretch of sheltered beach here, next to the marina. They double as daytime beach clubs, and have water-sports equipment for rent, along with food and beverage service. Adjacent to the marina is the “town’s” central plaza, where the traditional central kiosk has been converted into a small stand selling espresso drinks, whole-bean coffee from the region, and tours to the neighboring coffee plantations — all sponsored by the coffee-growers’ co-op. A small artisan’s market separates the plaza from the main road, calle Juárez.
berlitz2/Vallarta-WhereToGo.txt:Crucecita is the true soul of this area, where all the shops, services, and facilities that make a town run are located. Recently, a few stylish, yet inexpensive, hotels have cropped up. The central plaza here is lovely and tree-lined, with a bandstand at its center. It fronts the Iglesia Guadalupana, the main church in town, which is decorated with an enormous ceiling mural of the Virgin of Guadalupe, set in a background of indigo-blue night sky; additional, brilliantly colored murals adorn the walls.
berlitz2/Vallarta-WhereToGo.txt:Tangolunda Bay is where the larger hotel developments are located, along with the 18-hole Tangolunda Golf Course.
berlitz2/Vallarta-WhereToGo.txt:Chahúe Bay lies between Tangolunda and Santa Cruz bays, and is the next to be slated for development. For now, it is home to a few beach clubs used by non-oceanfront hotels, and a small marina that is under construction. Bahía Conejos lies to the east of Tangolunda, and has residential developments already in progress.
berlitz2/Vallarta-WhereToGo.txt:Outlying Bays
berlitz2/Vallarta-WhereToGo.txt:Most people choose to visit the various outlying bays on an excursion boat. You can also charter a panga to drop you off, and arrange a return pick-up. The twin bays of Maguey and El Órgano are the closest and most popular, with a string of palapa restaurants and vendors who rent snorkeling gear and kayaks at Maguey.
berlitz2/Vallarta-WhereToGo.txt:Beyond these two bays, the landscape has more of a desert-like appearance, with large cacti interspersed among the palms. The bays of Cacaluta, Chachacual, and Riscalillo are still pristine and peaceful, with overnight camping allowed at Cacaluta. An exquisite beach is nestled into the cove of Bahía San Agustín, a small fisherman’s village located about an hour by boat west of Santa Cruz, also accessible by road. Known for its outstanding offshore coral reefs, it’s the favorite with divers and snorkelers.
berlitz2/Vallarta-WhereToGo.txt:Day Trips from Huatulco
berlitz2/Vallarta-WhereToGo.txt:The mountainous region north of Huatulco is considered a prime area for the production of pluma coffee, a Mexican coffee noted for its powerful aroma and rich, earthy flavor. Visits to the various coffee fincas (plantations), located just under two hours north of Crucecita by car, make for an interesting day or overnight trip. The production zone for Huatulco’s coffee is comprised of over 50,000 hectares (100,000 acres), in the small towns surrounding the Copalita River. Notable are the continued use of traditional cultivation methods with minimal use of agricultural chemicals, and the open-air drying of the beans in sun beds.
berlitz2/Vallarta-WhereToGo.txt:The mountain areas surrounding the Capalita River are also the site of many natural treasures, including the Capalitilla Cascades. About 30 km (18.5 miles) north of Tangolunda a grouping of waterfalls, with heights averaging 25 m (80 feet) form natural Jacuzzis and clear pools for swimming. The area is also popular for horseback riding and rappelling.
berlitz2/Vallarta-WhereToGo.txt:
berlitz2/Vallarta-WhereToGo.txt:
berlitz2/Vallarta-WhereToGo.txt:
```

- This command "grep -vr sistory berlitz2 " is searching for and returning text files and the lines/paragraphs inside the files within the berlitz2 directory not containing the string history. Due to a large volume of files and lines not containing the string history being returned, I took the last few files and lines displayed in the terminal to show in this report. The command-line option -v will skip over any lines and files containing the specified string. While r helps trace throuh all files recursively in the berlitz2 directory. This command-line option is useful when the user wants to filter out any files containing lines with the string history. This command-line option helps speed up and efficiently filter out non important data inside files without having the ucser to manually go to one and each file but rather just stay in the directory.
- [Citations: ChatGPT](https://chat.openai.com/chat)


### Command-line option 3:  -c

#### Example 1:
