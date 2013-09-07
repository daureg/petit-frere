Chapitre 10 {.calibre1}
-----------

*Ce chapitre est dédié à Anderson’s bookshop, la librairie pour enfant
de légende à Chicago. Anderson’s est une vieille, vieille entreprise de
famille qui a commencé comme un de ces vieux drug-stores qui vendaient
aussi accessoirement quelques livres. Aujourd’hui, c’est un empire de
livres pour enfants florissant, avec plusieurs succursales et des
méthodes de vente incroyablement innovantes qui réunissent les livres et
les enfants de façon enthousiasmante. Le meilleur d’entre eux est le
marché aux livres mobile, dans lequel ils livrent de gigantesques
étagères sur roues, pré-chargées d’excellents livres pour enfants,
directement aux écoles, dans des camions — et voilà, une bourse aux
livres instantannée ! Anderson’s Bookshops: 123 West Jefferson,
Naperville, IL 60540 USA +1 630 355 2665*

Qu’est-ce que vous feriez si vous trouviez un espion dans vos rangs ?
Vous pouriez le dénoncer, le coller au mur et vous en débarasser. Mais
vous vous retrouvriez avec un autre espion, et celui-là serait plus
prudent que le précédent et ne se ferait peut-être pas attraper aussi
facilement. Voici une meilleure idée : commencez à intercepter les
communicatoins de l’espion et donnez-lui, ainsi qu’à ses maîtres, des
informations bidon. Supposons que ses maîtres lui ordonnent de récolter
des informations sur vos mouvements. Laissez-le vous suivre partout et
prendre toutes les notes qu’il veut, mais ouvrez ses enveloppes et
renvoyez-les au QG après avoir remplacé ses rapports sur vos mouvements
par d’autres, fictifs. Si vous voulez, vous pouvez lui faire avoir l’air
erratique et indigne de confiance au point que c’est eux qui se
débarasseront de lui. Vous pouvez provoquer des crises qui forcent un
camp ou l’autre à révéler l’identité d’autres espions. En bref, vous les
possédez.

Ceci s’appelle une attaque man-in-the-middle, et si vous y réfléchissez,
ça fait franchement peur. Quelqu’un qui attaque vos communications de
cette façon a des milliers de façons de vous abuser. Bien entendu, il
existe une bonne manière d’éviter les attaques man-in-the-middle :
utiliser la cryptographie. Avec la cryptographie, ça n’a pas
d’importance que l’ennemi intercepte vos messages, puisqu’il ne peut pas
les déchiffrer, les modifier et les renvoyer. C’est une des raisons
principales d’utiliser la crypto. Mais souvenez-vous : pour que la
crypto fonctionne, vous avez besoin des clefs de ceux à qui vous voulez
parler. Vous et votre partenaire devez partager un ou deux secrets, des
clefs que vous utilisez pour encrypter et décrypter vos messages pour
que ceux qui les interceptent ne puissent rien en faire. C’est de là que
vient l’idée d’une clef publique. C’est un peu complexe, mais c’est
aussi incroyablement élégant. Dans la crypto à clefs publiques, chaque
utilisateur reçoit deux clefs. Ce sont de longues suites de fourbi
mathématique, et elles ont des propriétés pratiquement magiques. Quoi
que vous chiffriez avec une clef, l’autre va le déchiffrer, et
inversement. De plus, il n’y a que ces clefs-là qui puisse le faire — si
vous déchiffrez un message avec une clef, vous savez qu’il a été chiffré
avec l’autre clef (et vice-versa). Ainsi, vous pouvez prendre l’une ou
l’autre de ces clefs (pas d’importance laquelle) et vous pouvez la
rendre publique, tout simplement. Vous en faites un non-secret complet.
Vous voulez que quiconque dans le monde sache ce que c’est. Pour des
raisons assez évidentes, ça s’appelle une “clef publique”. L’autre clef,
vous la cachez dans les plus noirs recoins de votre âme. Vous la gardez
de votre vie. Vous ne laisez personne, jamais, savoir ce que c’est. Ca
s’appelle une “clef privée” (Eh ouais !).

Maintenant, supposons que vous soyiez un espion et que vous vouliez
parler à votre chef. Sa clef publique est connue de tous. Votre clef
publique est connue de tous. Personne ne connait votre clef privée à
part vous. Personne ne connait de clef privée autre que la sienne
propre. Vous voulez envoyer un message. D’abord, vous l’encryptez avec
votre clef privée. Vous pourriez simplement envoyer ce message-là, et ça
serait déjà pas mal, puisque le destinataire saurait que le message qui
lui arrive vient réellement de vous. Comment ? parce que s’ils peuvent
le décrypter avec votre clef publique, il ne peut pas été encrypté
qu’avec votre clef privée. Cest l’équivalent de mettre votre sceau ou
votre signateur au bas d’un message. Ca dit “C’est moi qui ai écrit
cela, et personne d’autre. Personne ne peut l’avoir ouvert ou modifié.”

Malheureusement, tout ça ne va pas tenir votre message secret. C’est
parce que votre clef publique est de notoriété publique (il faut qu’elle
le soit, parce que sinon vous seriez limité à envoyer des messages aux
quelques personnes qui ont votre clef publique). Toute personne qui
intercepte votre message peut le lire. Ils ne peuvent pas le modifier et
faire croire que c’est votre version, mais si vous ne voulez pas que
tout le monde sache ce que vous dites, il vous faut une meilleure
solution. Alors, au lieu d’encrypter le message seulement avec votre
clef privée, vous l’encryptez  aussi avec la clef publique de votre
chef. Maintenant, il est verrouillé deux fois. Le premier verrouillage —
la clef publique du chef — ne s’ouvre que quand on le combine avec la
clef privée du chef. Le second verrouillage — votre clef privée — ne
s’ouvre qu’avec votre clef publique. Quand votre chef reçoit un message,
il l’ouvre avec les deux clefs et ils sont certains que a) c’est bien
vous qui l’avez écrit et b) que seul lui peut le lire. C’est très cool.
Le jour où nous l’avons découvert, Darryl et moi avons immédiatement
échangé nos clefs et avons passé des mois à nous faire des clins d’oeil
et à nous frotter les mains en échangeant des messages à encryption de
qualité militaire sur où on se retrouverait après l’école et si Van
s’intéresserait un jour à lui.

Mais si vous voulez comprendre la sécurité, vous devez réfléchir dans
les termes les plus paranoïaques possibles. Genre, qu’est-ce qui se
passerait si je vous faisais croire que ma clef publique est celle de
votre chef ? Vous crypteriez le message avec votre clef privée et ma
clef publique. Je pourrais le décrypter, le lire, le réencrypter avec la
véritable clef de votre chef, et la renvoyer. Pour autant que votre chef
pourrait en juger, personne d’autre que vous n’aurait pu écrire le
message, et personne d’autre que lui n’aurait pu le lire. Et moi, je
m’assierais au milieu, comme une araignée dodue sur une toile, et tous
vos secrets m’appartiendraint. Maintenant, la façon la plus simple de
régler ça est de faire une vraie publicité à votre clef publique. Plus
votre clef publique est notoire, plus l’attaque man-in-the-middle est
difficile. Mais vous savez quoi ? Faire connaître quelque chose vraiment
universellement est tout aussi difficile que de le tenir secret.
Réfléchissez — combien de milliards de dollars sont dépensés en
publicités pour du shampoing et d’autres conneries, juste pour faire en
sorte qu’autant de monde que possible sache quelque chose qu’un
publicitaire veut faire savoir ? Il y a une façon moins chère de régler
son compte au man-in-the-middle : le réseau de confiance.

Supposons qu’avant de quitter votre QG, vous et votre chef prenez un
café ensemble et vous échangez vos clefs. Plus de man-in-the-middle !
Vous êtes absolument certain à qui appartient la clef, parce qu’elle
vous a été remise en mains propres. Jusque-là ça va. Mais il y a une
limite naturelle à tout ceci : combien de personnes pouvez-vous
physiquement rencontrer pour échanger des clefs avec eux ? Combien
d’heures par jour voudriez-vous consacrer à ce qui équivaut à écrire
votre propre annuaire téléphonique ? Combien de gens sont prêt à vous
consacrer du temps pour ça ? Ca aide de penser à cette question en
termes d’annuaire téléphonique. Le monde était jadis plein d’annuaires
téléphoniques, et quand on avait besoin d’un numéro, on pouvait le
chercher dans l’annuaire. Mais beaucoup des numéros dont on avait besoin
pendant une journée donnée, soit on les aurait connus par coeur, soit on
aurait pu les demander à quelqu’un d’autre. Encore aujourd’hui, quand je
sors avec mon téléphone cellulaire, je demande à Jolu ou à Darryl s’ils
ont le numéro que je cherche. Ca va plus vite et c’est plus facile que
de chercher en ligne et c’est plus fiable, aussi. Si Jolu a un numéro,
je lui fais confiance, et je fais donc confiance au numéro, aussi. C’est
ce qu’on appelle la “confiance transitive” — la confiance qui se
transmet à travers le réseau de vos relations. Un réseau de confiace est
une version de ça, à grande échelle. Disons que je rencontre Jolu et que
je récupère sa clef. Je la mets sur mon trousseau de clefs — une liste
de clefs que j’ai signées avec ma clef privée. Ce qui veut dire que vous
pouvez l’ouvrir avec ma clef publique et être certain que c’est moi — ou
quelqu’un qui possède ma clef, en tout cas — qui a dit que “cette clef
appartient à ce gars”. Alors je vous donne une copie de mon trousseau et
pour peu que vous ayiez confiance que j’ai effectivement rencontré et
vérifié toutes les clefs, vous pouvez le prendre et l’ajouter à votre
trousseau. Et là, vous, vous rencontrez quelqu’un d’autre et vous lui
donnez tout le trousseau. Des trousseaux de plus en plus grands
poussent, et pour peu que vous ayiez confiance dans le suivant dans la
chaîne, et qu’il ait lui-même  confiance dans le suivant et ainsi de
suite, vous êtes pas mal en sécurité.

Ce qui m’amène aux réunions de signature de clefs. C’est exactement ce
que ça dit : une fête où tout le monde se réunit et signe les clefs de
tout le monde. Darryl et moi, quand nous échangions des clefs, ça
faisait une sorte de mini-réunion, qui ne comptait que deux pauvres
geeks comme participants. Mais avec plus de monte, vous semez les germes
d’un réseau de confiance, à partir duquel il peut s’étendre. Au fur et à
mesure que les gens de votre trousseau parcourent le monte et
rencontrent des gens, ils ajoutent de plus en plus de noms à leur
trousseau. Vous n’avez même plus besoin de rencontrer les gens, vous
avez assez confiance dans les clefs signées par les gens de votre
trousseau pour les considérer valides. C’est pourquoi les fêtes et les
réseaux de confiance vont ensemble comme les tartines et le Nutella.

“Dis-leur juste que c’est une fête super-privée, seulement sur
invitation.”, j’ai dit. “Dis-leur de n’amener personne avec eux ou on ne
les laissera pas entrer”. Jolu m’a regardé par-dessus son café.\
— “Tu plaisantes, n’est-ce pas ? Si tu dis ça, les gens vont emmener
encore plus de monde.”\
— “Arg !”\
Je passais une nuit par semaine chez Jolu, ces temps, à entretenir le
code sur Indienet. Pigspleen me payait même une somme d’argent non nulle
pour faire ça, ce qui me faisait vraiment bizarre. Je n’aurais jamais
pensé que je serais payé pour écrire du code.\
— “Alors qu’est-ce qu’on fait ? Nous voulons seulement des gens en qui
nous pouvons vraiment avoir confiance, et on ne veut pas dire pourquoi
avait d’avoir les clefs de tout le monde pour pouvoir le leur envoyer
par message secret. “\
Jolu débuggait et je regardais par-dessus sont épaule. Cette technique
s’appelait “extreme programming”, ce qui était un peu embarassant.
Maintenant nous l’appelions juste “programmation”. Deux personnes sont
bien meilleures pour repérer des erreurs qu’une seule. Comme dit le
dicton, “avec assez d’yeux, tous les bugs sont faciles”.\
Nous progressions dans le rapport de bugs et nous préparions à publier
une nouvelle version. Tout se mettait à jour automatiquement en tâche de
fond, de sorte que nos utilisateurs n’avaient besoin de rien faire, mais
ils se réveillaient toutes les semaines environ avec un meilleur
programme.

Ca faisait vraiment bizarre de savoir que le code que j’écrivais serait
utilisé le lendemain par des centaines de milliers de personnes.\
— “Qu’est-ce qu’on fait ? Pouh la, j’en sais rien. Je pense qu’il va
falloir faire avec.”\
J’ai repensé à nos jours de Harajuku Fun Madness. Le jeu comprenait
beaucoup de problèmes sociaux qui impliquaient de grands groupes de
gens.\
— “OK, tu as raison. Mais au moins tâchons de garder tout ça secret.
Dis-leur d’emmener au maximum une seule personne, et ça devra être
quelqu’un qu’ils connaissent depuis au moins cinq ans. ” Jolu a levé les
yeux de l’écran.\
— “Hé”, a-t-il dit, “Hé, ça marcherait du tonnerre ! Je m’y vois déjà.
Je veux dire, si tu me disais de n’emmener personne, je penserais ‘il se
prend pour qui, ce gars ?’ Mais si tu le présentes comme ça, ça fait un
super trip à la 007″.\
J’ai identifié un bug. Nous avons bu du café. Je suis renté et j’ai joué
un peu à Pillage Mécanique, en essayant d’oublier les remonteurs et
leurs questions indiscrètes, et j’ai dormi comme un bébé.

Les Sutro Baths sont les authentiques fausses ruines romaines de San
Francisco. Quand elles ont ouvert en 1896, c’était les plus grands bains
publics du monde, un immense solarium victorien de verre rempli de
piscines et de baignoires et même un toboggan à eau primitif. Elles se
sont déteriorées dans les années 50, et les propriétaires ont fini par y
mettre le feu pour toucher l’assurance en 1966. Tout ce qui en reste est
un labyrinthe de pierres usées posées directement au dessus de la
falaise qui domine Ocean Beach. Ca ressemble tout à fait à des ruines
romains, croulantes et mystérieuses, et juste derrière, il y a des
grottes que conduisent jusqu’à la mer. Quand la mer est grosse, les
vagues montent jusqu’aux grottes et touchent les ruines — il y a eu des
cas où des touristes se sont fait entraîner.

Ocean Beach est loin derrière le parc du Golden gate, une falaise
abrupte pointillée de maisons très chères, au destin tragique, qui
plonge vers une étroite bande de plage encombrée de méduses et de
surfers intrépides (dingues). Il y a un rocher géant qui dépasse des
récifs à quelques encablures de la plage. On l’appelle Seal Rock, et
c’était jadis un point de rassemblement pour les lions de mer jusqu’à ce
qu’on les déplace dans les environs de Fisherman’s Wharf, où ils sont
une attraction pour les touristes. La nuit venue, il n’y a guère de
monde là-bas. Il y fait très froid, avec des éclaboussures d’eau salée
qui vous trempent jusqu’aux os si vous vous laissez faire. Les rochers
sont affûtés, il y a du verre brisé, et de temps en temps, des seringues
de junkies. C’est un super endroit pour faire la fête.

C’est moi qui ai eu l’idée d’emporter des bâches et des réchauffe-main
chimiques. Jolu a trouvé comment se procurer de la bière — son frère
aîné, Javier, a un copain qui fait tourner un véritable service de
livraison d’alcool juvénile : payez-le assez et ils reviendra à votre
fête camouflée avec des glacières et autant de bières différentes que
vous voulez. J’ai claqué pas mal de mon argent de Indienet, et le gars
s’est pointé pile à l’heure : à 20 heures, une bonne heure après le
coucher du soleil. Il a déchargé six glacières de sa camionette et les a
traîneées dans les ruines des bains. Il avait même des caisses
supplémentaires pour les bouteilles vides.\
— “Amusez-vous et sayez sages, les jeunes, ” a-t-il dit en touchant son
chapeau de cow-boy. C’était un type dodu avec un sourir énorme, et un
marcel effrayant qui laissait échapper les poils de ses aisselles, de
son ventre et de ses épaules, J’ai épluché quelques billets de vingt
dollars de mon rouleau de billets et les lui ai tendus — il faisait un
profit de 150 pourcents. Un bon plan. Il a regardé mon rouleau.\
— “Tu sais, je pourrai simplement te piquer tout ça, ” a-t-il dit,
toujours en souriant. “Je suis un criminel, après tout.”\
J’ai rangé mon rouleau dans ma poche et je l’ai regardé droit dans les
yeux. J’avais été stupide de lui laisser voir ce que j’avais sur moi,
mais je savais qu’il y a des moment où il faut se faire respecter.\
— “Je blague”, il a fini par dire. “Mais fais gaffe avec tout cet
argent. Ne le fais pas voir à tout le monde.”\
— “Merci”, j’ai répondu, “mais la Sécurité Intérieure me protège.” Son
sourire s’est encore agrandi.\
— “Ah ! C’est même pas des amateurs. Ces cornichons n’ont pas la moindre
idée. “\
J’ai regardé son camion. Il y avait un FasTrak bien en évidence sur le
pare-brise. Je me demandais combien de temps ça prendrait avant qu’il se
fasse avoir.\
— “Vous avez invité des filles ce soir ? C’est pour ça que vous avez
tout cette bière ?”\
J’ai souri et je l’ai salué de la main comme s’il avait été en train de
retourner à son camion, ce qu’il aurait dû faire. A la fin il a compris
le sous-entendu, et il est reparti. Son sourire n’avait jamais faibli.

Jolu m’a aidé à dissimuler les glacières dans les éboulis, en
travaillant avec des petites lampes à LEDs montés sur des serre-tête.
Quand les glacières ont été en place, nous avons installé des petites
lampes à LED dans chacune d’elles, pour qu’il y ait de la lumière quand
on enlèverait les couvercles en styrofoam, pour que les gens voient ce
qu’ils feraient. C’était une nuit sans lune et il y avait une couverture
nuageuse, et les lampadaires des rues au loin nous illuminaient à peine.
Je savais que nous serions aussi visibles que des incendies sur des
détecteurs à infrarouge, mais nous n’avions aucune chance de rassembler
des gens sans être observés. J’ai décidé qu’on nous considèrerait comme
de simples fêtards qui s’ennivreraient sur la plage. Je ne bois pas
beaucoup. J’ai vu de la bière, de l’herbe et de l’ecstasy aux fêtes que
je fréquente depuis que j’ai 14 ans, mais je déteste la fumée (quoi que
je ne dise pas non à un space brownie de temps en temps), l’ecstasy
prend temps longtemps — qui peut consacrer tout un week-end ce que les
effets viennent et repartent — et la bière, bon, c’est pas mal, mais je
ne vois pas pourquoi on en fait tout un plat. Ce que je préfère, c’est
les grands cocktails compliqués, le genre de choses qu’on vous sret dans
un volcan en céramique, avec six couches, en flammes, avec un singe en
plastique sur le dessus, mais c’était surtout pour tout le décorum. En
fait, j’aime bien être ivre. Ce que je n’aime pas, c’est la gueule de
bois qui suit, et nom d’un chien, qu’est-ce que je me prends comme
gueules de bois. Quoi que si j’y réfléchis, ça a peut-être un rapport
avec le genre de boissons qui viennent dans ces volcans en céramique.
Mais on n’organise pas une fête sans quelques bières bien fraîches.
C’est ce que les gens attendent. Ca aide à briser la glace. Les gens
font des stupidités quand ils ont bu trop de bières, mais mes amis ne
sont pas vraiment le genre de gens à avoir des voitures. Et le gens font
des stupidités quoi qu’il arrive — la bière ou le hashish ne sont que
des épiphénomènes à ce fait central.

Jolu et moi nous sommes chacun ouvert une bière — une Anchor Steam pour
lui, une Bud Lite pour moi — et nous avons trinqué en nous asseyant sur
les rochers.\
— “Tu leur as dit 21 heures ?”\
— “Ouais”, il y a dit.\
— “Moi aussi”.\
Nous avons bu en silence. La Bud Lite était la boisson la moins
alcoolisée de la glacière. J’aurais besoin d’avoir les idées claires
plus tard.\
— “Ca t’arrive de prendre peur ?”, ai-je finalement demandé. Il s’est
tourné vers moi.\
— “Non, je prends pas peur. J’ai peur tout le temps. J’ai eu peur depuis
les explosions. Parfois j’ai tellement peur que je ne veux pas sortir de
mon lit. “\
— “Alors pourquoi est-ce que tu fais ça ?” Il a souri.\
— “Puisqu’on en parle, peut-être que je ne vais pas continuer longtemps.
Je veux dire, c’était génial de te donner un coup de main. Génial.
Vraiment excellent. Je ne vois pas quand qu’ai fais quoi que ce soit
d’aussi important. Mais Marcus, mon frère, je dois te dire…” Il s’est
interrompu.\
— “Quoi”, ai-je demandé, bien que j’aie su ce qui allait venir.\
— “Je ne peux pas continuer indéfiniment”, a-t-il finalement dit.
“Peut-être même pas un moins. Je crois que je n’en peux plus. C’est trop
dangeureux. Le DSI, tu ne peux pas leur faire la guerre. C’est dément.
C’est vraiment, réellement dément.”\
— “Tu parles comme Van”, j’ai dit. Ma voix était bien plus amère que ce
que j’aurais voulu.\
— “Je ne te critique pas. Je pense que c’est fantastique que tu sois
assez brave pour faire ce que tu fais tout le temps. Mais je ne suis pas
comme ça. Je ne peux pas vivre dans une terreur perpétuelle.”\
— “De quoi tu parles ?”\
— “Je dis que j’en ai assez. Je vais rejoindre les gens qui font comme
si tout allait bien, comme si les choses allaient revenir à la normale
un jour. Je vais utiliser Internet comme l’ai toujours fait, et
n’utiliser Xnet que pour jouer aux jeux. Je dis que je veux sortir de
tout ça. Je ne prendrai plus part à tes plans. “\
Je n’ai rien dit.\
— “Je sais que ça te laisse tout seul. Ca n’est pas ce que je veux, je
te jure. Je préfèrerais que tu laisses tomber toi aussi. Tu ne peux pas
déclarer la guerre au gouvernement des USA. Ca n’est pas une guerre que
tu peux gagner. Te regarder essayer, c’est comme regarder un oiseau qui
se cogne à une vitre, encore et encore. “\
Il aurait voulu que je dise quelque chose. Ce que je voulais dire,
c’était Bon Dieu, Jolu, merci beaucoup de m’abandonner comme ça ! Tu as
oublié comment c’était quand ils nous ont enlevés ? Tu as oublie comment
le pays était avant qu’ils en prennent le contrôle ? Mais ça n’était pas
ce qu’il voulait que je lui dise. Ce qu’il voulait que je lui dise,
c’est “Je comprends, Jolu. Je respecte ton choix.” Il a bu le reste de
sa bouteille et en a sorti une nouvelle dont il a ouvert le bouchon.\
— “Il y a autre chose”, a-t-il dit.\
— “Quoi ?”\
— “Je ne voulais pas le mentionner, mais je veux que tu comprennes
pourquoi je dois faire ça.\
— “Pour l’amour du ciel, Jolu, quoi ?”\
— “Je déteste devoir dire ça, mais tu es blanc. Moi, pas. Les blancs qui
se font chopper avec de la cocaïne font des stades de citoyenneté. Les
bruns qui se font prendre avec du crack vont en prison pour vingt ans.
Les Blancs voient un flic dans la rue et se sentent en sécurité. Les
Bruns voient un flic dans la rue et se demandent s’ils vont se faire
fouiller. La façon dont le DSI te traite ? C’est la norme dans ce pays
depuis toujours pour nous autres.”\
C’était tellement injuste. Je n’avais pas demandé à être blanc. Je ne
pensais pas que j’étais plus brave parce que j’étais blanc. Mais je
voyais ce que Jolu voulait dire. Si les flics arrêtaient quelqu’un dans
la Mission et contrôlaient son identité, il y avait de bonnes chances
pour que cette personne ne soit pas un Blanc. Quelque risque que je
coure, Jolu en courait de pires. Quelque peine que je doive payer, Jolu
payerait plus cher.\
— “Je ne sais pas quoi dire”, ai-je dit.\
— “Tu n’as pas à dire quoi que ce soit”, il a dit. “Je voulais juste que
tu saches, pour que tu puisses comprendre.

Je voyais des gens descendre le sentier dans notre direction. C’était
des amis de Jolu, deux Mexicains et une fille que je connaissait
vaguement, petite et geek, qui portait tout le temps des lunettes noires
cool à la Buddy Holly qui lui donaient un air de l’étudiante en art
rejetée qui se révèle avoir un talent caché dans les films pour
adolescents. Jolu m’a présenté et a distribué de la bière. La fille n’en
n’a pas pris, mais a sorti à la place une petite flasque de vodka en
argent de son sac, et m’en a offert. J’en ai pris une gorgée — la vodka
chaude n’est pas quelque chose qui s’apprécie sans une certaine habitude
— et lui ai fait compliment pour sa flasque, qui était rehaussée d’une
frise de personnages de Parappa the Rapper.\
— “C’est japonais”, a-t-elle dit pendant que je l’examinais avec mon
porte-clef à LED. “Ils ont plein de gadgets pour l’alcool basés sur des
jeux pour gamins. C’est totalement tordu”.\
Je me suis présenté et elle s’est présentée.\
— “Ange”, a-t-elle dit en me serrant la main — la mienne était sèche,
chaude, avec des ongles courts.\
Jolu m’a présenté à ses amis, qu’il connaissait depuis un camp
d’informatique en 4ème année. D’autres sont arrivés — cinq, puis dix, et
20. C’était un groupe sérieux, maintenant. Nous avions dit aux gens
d’être là à 21:30 précises, et nous avons accordé jusqu’à 21:45 pour
voir si tout le monde était là. Les trois quarts étaient des amis de
Jolu. J’avais invité tous les gens en qui j’avais confiance. Soit
j’étais plus sélectif que Jolu, soit j’étais moins populaire. Maintenant
qu’il m’avait annoncé sa désertion, j’avais l’impression qu’il était
seulement moins sélectif. Je lui en voulais vraiment, mais j’essayais de
n’en rien montrer en me concentrant sur les interactions avec les
invités. Mais il n’était pas stupide. Il savait ce qui se passait. Je
voyais qu’il était vraiment ennuyé. Bien.

— “OK” ai-je dit en escaladant une ruine, “OK, hé, tout le monde ?”\
Quelques personnes proches ont fait attention, mais ceux du fond
continuaient de bavarder. J’ai tendu mon bras en l’air comme un arbitre,
mais il faisait trop sombre. Finalement j’ai eu l’idée d’allumer ma
lampe LED et de la pointer vers chacun des bavards, puis vers moi.
Graduellement, la foule s’est tue. J’ai souhaité la bienvenue à tout le
monde, puis je leur ai demandé de se rapprocher pour que je puisse
expliquer pourquoi nous étions tous là. Je voyais qu’ils étaient tous
captivés par l’atmosphère secrète, intrigués et un peu lancés par la
bière.\
— “Voilà de quoi il s’agit. Vous utilisez tous Xnet. Ce n’est pas une
coïcidance si Xnet a été créé juste après que le DSI a pris le contrôle
de la ville. Les gens qui ont fait ça sont une organisation consacrée à
la liberté personnelle, qui ont créé le réseau pour nous garder des
barbouzes du DSI et de leurs gros bras.”\
Jolu et moi avions préparé ceci à l’avance. Nous n’allions pas avouer
que nous étions derrière tout, à personne. C’était trop risqué. A la
place, nous allions tout présenter comme si nous n’étions que des
lieutenants dans l’armée commandée par “M1k3y”, qui travaillaient à
organiser la résistance locale.\
— “Le Xnet n’est pas pur”, j’ai dit. “Il peut être utilisé par le camp
d’en face tout autant que par nous. Nous savons qu’il y a des espions du
DSI qui l’utilisent en ce moment même. Ils utilisent des trucs
d’ingénierie sociale pour nous inciter à nous révéler, de façon à
pouvoir nous arrêter. Si Xnet doit être un succès, nous devons trouver
comment les empêcher de nous espionner. Il nous faut un réseau à
l’intérieur du réseau.”\
J’ai fait une pause pour laisser digérer ça. Jolu avait suggéré que
c’était un peu violent — apprendre brusquement qu’on est en train de se
faire recruter dans une cellule révolutionnaire.\
— “Maintenant, je ne suis pas là pour vous demander de faire quoi que ce
soit activement. Vos n’avez pas à sortir faire du brouillage ou je ne
sais quoi. On va a fait venir ici parce qu’on sait que vous êtes cool,
et que vous êtes dignes de confiance. C’est à cette confiance que nous
voudrions vous faire contribuer ce soir. Certains d’entre vous
connaissent déjà les réseaux de confiance et les signatures de clefs,
mais pour le reste d’entre vous, je fais un petit rappel — “\
Ce que j’ai fait.\
— “Maintenant, ce que je voudrais que vous fassiez ce soir, c’est
rencontrer les gens ici et voir à quel point vous pouvez leur faire
confiance. Nous allons vous aider à générer des paires de clefs et les
partager entre vous. “\
Cette partie-là était compliquée. Demander aux gens d’apporter leurs
laptops n’aurait jamais marché, mais nous avions besoin de faire quelque
chose de bien complexe qui ne pouvait pas exactement se faire avec un
papier et un crayon. J’ai sorti un laptop que Jolu et moi avions
reconstruit la veille au soir, depuis zéro.\
— “J’ai confiance en cette machine. Nous en avons assemblé chaque
composante de nos propres mains. Elle tourne sur une version toute
récente de ParanoidLinux, bootée directement du DVD. S’il reste un
ordinateur sûr dans le monde, ça pourrait bien être celui-là. J’ai un
générateur de clefs chargé ici. Vous pouvez venir ici et lui donner des
entrées aléatoires — vous pressez les touches n’importe comment, vous
agitez la souris dans tous les sens — et il va utiliser ça comme graine
pour vous créer une paire de clefs, publique et privée, qu’il va ensuite
afficher à l’écran. Vous pouvez prendre une photo de votre clef privée
avec votre téléphone, et presser n’importe quelle touche pour la
détruire à tout jamais — elle n’est pas stockée sur le disque. Ensuite
ça va vous montrer votre clef publique. A ce moment, appelez tous ceux
ici en qui vous avez confiance et qui vous font confiance, et
faites-leur prendre une photo de vous à côté de la clef, qu’ils sachent
à qui elle appartient. Quand vous rentrez chez vous, vous devrez
convertir ces photos en clefs. ça va prendre un bon moment, j’en ai
peur, mais vous n’aurez à le faire qu’une seule fois. Soyez
super-attentifs à ce que vous tapez — une erreur et vous êtes baisé.
Heureusement, il y a une façon de savoir si vous avez tapé correctement
: sous la clef, il va y avoir un nombre beaucoup plus court, qui
s’appelle l’”empreinte”. Quand vous aurez tapé la clef, vous pourrez en
générer une empreinte et la comparer à l’empreinte de référence, et si
elles correspondent, vous êtes bon. “\
Ils m’ont tous regardé avec des yeux ronds. OK, je leur avais demandé de
faire quelque chose d’assez bizarre, soit, mais quand même.
