---
title: présentation de l’expérience de 10 pieds pour les développeurs de jeux Windows
description: Cet article présente l’expérience de 10 pieds et explore la liste des choses que vous devez prendre en compte au sujet de ce nouveau modèle d’interaction, même si vous ne vous attendez pas à ce que votre jeu soit joué de cette façon.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049cbbe839509681f8f8629144511853d2984bbabafbf989611d1ed1db32e686
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963619"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>présentation de l’expérience de 10 pieds pour les développeurs de jeux Windows

Un nombre croissant de personnes utilisent leurs ordinateurs personnels d’une manière entièrement nouvelle. si vous pensez que l’interaction est classique avec un ordinateur Windows, vous envisagez probablement d’être assis au bureau avec une analyse et à l’aide d’une souris et d’un clavier (ou peut-être d’un appareil joystick); c’est ce que l’on appelle la « expérience de 2 pieds ». il s’agit toujours du scénario le plus courant pour les jeux de Windows, mais il existe une autre tendance avec laquelle vous commencerez probablement à vous entendre : l’expérience de 10 pieds, qui décrit l’utilisation de votre ordinateur en tant que périphérique de divertissement avec sortie sur un téléviseur. Cet article présente l’expérience de 10 pieds et explore la liste des choses que vous devez prendre en compte au sujet de ce nouveau modèle d’interaction, même si vous ne vous attendez pas à ce que votre jeu soit joué de cette façon. une partie de vos clients exécutera votre jeu Windows sur un ordinateur exécutant Windows Media Center. il est préférable de savoir à quoi cette expérience sera fondée avant que vos clients ne l’essaient.

-   [qu’est-ce que Windows Media Center ?](#what-is-windows-media-center)
-   [Expérience de 10 pieds](#the-10-foot-experience)
    -   [Installation](#installation)
    -   [Entrée utilisateur](#user-input)
    -   [Affichage](#display)
-   [Proportions et grand écran](#aspect-ratio-and-widescreen)
-   [titre-région Coffre](#title-safe-region)
-   [Suggestions NTSC](#ntsc-suggestions)
    -   [Fixer les valeurs du composant de couleur RVB entre 16 et 235](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Évitez les couleurs similaires qui peuvent apparaître identiques](#avoid-similar-colors-that-might-appear-identical)
    -   [Évitez les différences nettes en comparaison](#avoid-sharp-differences-in-contrast)
-   [Conclusion](#conclusion)

## <a name="what-is-windows-media-center"></a>qu’est-ce que Windows Media Center ?

Windows Media Center peut agir en tant qu’interface avec les fonctionnalités multimédias de l’ordinateur hôte. le site Web de cette fonctionnalité, [Windows la page d’hébergement de Media Center](https://windows.microsoft.com/windows/products/windows-media-center/), offre une présentation détaillée et présente toutes les nouveautés disponibles dans la dernière version. media center est inclus dans Windows XP édition media center, Windows vista édition familial Premium, Windows vista Ultimate et la plupart des éditions de Windows 7.

dans le passé, la seule façon d’obtenir Windows media center était d’acheter un PC media center auprès d’un fabricant de système de niveau 1, mais comme Windows media center est désormais inclus avec deux éditions de Windows Vista, la place de marché potentielle est désormais bien plus importante.

## <a name="the-10-foot-experience"></a>Expérience de 10 pieds

Windows Media center a été conçu autour de l’idée que les gens pouvaient utiliser Windows pour une expérience de divertissement riche en salle de vie, et cela suit que la plupart des utilisateurs préfèrent interagir différemment avec Windows Media Center et avec les applications informatiques traditionnelles. Pour une, si le client utilise l’ordinateur dans l’espace de vie pour le divertissement, il est probable que la vidéo s’affiche sur un autre point qu’un moniteur d’ordinateur conventionnel : les téléviseurs analogiques, les téléviseurs numériques haute définition, et tout nombre d’écrans LCD sont tous des candidats probables. Ces types d’affichages sont généralement affichés d’une distance d’environ 10 mètres, par conséquent, l’étiquette *expérience de 10 pieds*.

l’expérience de 10 pieds n’est pas limitée aux utilisateurs de Windows Media Center ; Il est courant dans les dernières années que les utilisateurs connectent leur poste de travail ou leur Notebook à leur téléviseur et à leur système audio. Il est de plus en plus courant pour les périphériques d’affichage des consommateurs d’exposer des connexions RGB ou DVI, les ports de sortie vidéo standard sur les ordinateurs. En outre, les ports S-Video sont une fonctionnalité classique des cartes vidéo haut de gamme et offrent un moyen simple de sortir sur un autre périphérique d’affichage.

Certaines règles de conception importantes doivent être prises en compte pour une expérience agréable de 10 pieds de page : installation, entrée utilisateur et affichage.

### <a name="installation"></a>Installation

Pendant l’expérience moyenne de 2 mètres, l’utilisateur se trouve dans la distance qui atteint l’ordinateur ; Si, au cours du démarrage ou du jeu, l’utilisateur est invité à insérer ou à changer de support, l’utilisateur peut rester assis. L’expérience moyenne de 10 pages place l’ordinateur dans l’espace de l’utilisateur et, par conséquent, tout ce qui nécessite que l’utilisateur interagisse physiquement avec l’ordinateur force l’utilisateur à se placer et à franchir la place. Pour cette raison, les développeurs doivent éviter de forcer l’utilisateur à changer de support. Pensez à autoriser une installation complète de votre application sur le disque dur.

### <a name="user-input"></a>Entrée utilisateur

une autre fonctionnalité de Windows Media Center est la prise en charge d’un contrôle à distance standard, qui est l’appareil d’entrée généralement préféré. Bien que le genre de votre titre de jeu décide en grande partie du fait que le contrôle à distance est apte à fournir des entrées de jeu, vous souhaiterez peut-être autoriser l’utilisateur à suspendre le jeu et à accéder aux menus du jeu à l’aide du contrôle à distance. Toutefois, assurez-vous que vous autorisez également l’utilisateur à contrôler les menus à l’aide de l’appareil d’entrée de jeu principal. pour plus d’informations sur la conception et le développement de Windows media center et de ses appareils, consultez [Windows Kit de développement logiciel (sdk) media center](/previous-versions/msdn10/bb895967(v=msdn.10)) sur MSDN.

Évitez toute interaction physique entre l’utilisateur et l’ordinateur ou ses périphériques. Il n’est pas souhaitable de demander à l’utilisateur de modifier les contrôleurs d’entrée pendant le jeu de données, car il est probable qu’il est proche uniquement de l’appareil d’entrée principal.

Microsoft a créé des contrôleurs de boîtier courants pour une utilisation avec Windows et Xbox 360, le manette Xbox 360 pour Windows et le manette sans fil Xbox 360 pour Windows. Si vous vous assurez que votre titre est bien adapté sur les contrôleurs courants, vous pourrez facilement résoudre les problèmes liés au test de votre jeu sur les périphériques d’entrée potentiels.

### <a name="display"></a>Affichage

La vaste gamme de périphériques d’affichage potentiels vous donne des conseils sur l’affichage et chaque type d’appareil présente des avertissements spéciaux. Quelques-uns des problèmes relatifs aux technologies d’affichage spécifiques sont présentés plus loin dans ce document. Quel que soit le périphérique de sortie vidéo, il est important que les polices et les graphiques de l’interface utilisateur soient dimensionnés suffisamment grand pour une lisibilité à une distance de 10 mètres. Notez également que les polices avec anticrénelage offrent généralement une meilleure lisibilité.

Vous devez également éviter les lignes horizontales et les éléments d’interface statique avec une épaisseur ou un détail de pixel simple. Les télévisions plus anciennes peuvent ne pas afficher des détails précis, et même sur les derniers appareils d’affichage, votre contenu scintille lors d’une exécution en mode entrelacé, car une seule ligne de pixels n’est visible que la moitié du temps. En remplacement de petits détails, sachez qu’une ligne grise de 2 pixels apparaît plus fine qu’une ligne blanche de 2 pixels. (Cela revient essentiellement à estomper une ligne blanche de 1 pixel.)

## <a name="aspect-ratio-and-widescreen"></a>Proportions et grand écran

Les proportions décrivent la proportion de largeur et de hauteur de l’affichage. Les affichages TV standard et moniteur d’ordinateur affichent des proportions de 4:3, ce qui signifie que chaque fois que 4 pixels s’exécutent le long de la largeur de la mémoire tampon de trame, il y a 3 pixels le long de la hauteur (parfois également représentés sous la forme 1,33).

Avec l’avènement de la HDTV, les proportions de 16:9, également appelées « large screen », sont devenues la norme pour l’avenir de la télévision, ainsi qu’avec la télévision à définition améliorée (EDTV), il existe trois modes d’affichage que vous êtes susceptible de rencontrer :

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>EDTV 480p
</dt> <dd>

480 lignes de numérisation présentées progressivement. Ce mode peut générer une sortie de 4:3 (avec une résolution de mémoire tampon de trame de 640 × 480) ou de 16:9 (720 × 480).

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>HDTV 720p
</dt> <dd>

720 lignes de numérisation présentées progressivement. Ce mode est toujours 16:9 (1280 × 720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>HDTV 1080i
</dt> <dd>

1080 lignes de numérisation présentées en entrelacé. Ce mode est toujours 16:9 (1920 × 1080, ou 1920 × 540 si le rendu des champs entrelacés est séparé).

</dd> </dl>

Si votre jeu est codé en dur pour fonctionner dans un proportions de 4:3, un utilisateur qui consulte votre jeu sur un écran 16:9 a probablement trois options pour afficher l’image, aucune d’entre elles étant particulièrement satisfaisante :

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>CDP
</dt> <dd>

La mémoire tampon de trame 4:3 est étirée pour couvrir parfaitement la résolution 16:9 native de l’affichage, ce qui entraîne l’affichage de vos objets de scène plus larges que vous le souhaitez. Certains téléviseurs offrent des modes d’étirement supplémentaires qui essaient de conserver les proportions près du centre de l’affichage et d’augmenter progressivement l’étirement sur les côtés de l’image.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Gestionnaire
</dt> <dd>

La mémoire tampon de trame 4:3 est affichée sans déformation au centre de l’affichage, avec des barres de couleur unie qui remplissent les pixels restants sur les côtés.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Focale
</dt> <dd>

La mémoire tampon de trame 4:3 est rognée dans une région 16:9, qui remplit ensuite la résolution d’affichage native sans distorsion. Notez que les pixels au-dessus et en dessous du rectangle de découpage sont complètement ignorés, qui sont des régions communes pour les éléments d’interface utilisateur d’un jeu.

</dd> </dl>

Une meilleure approche consiste à ajouter la prise en charge de l’affichage à l’écran étendu à votre jeu. La modification la plus importante consiste à définir la transformation de projection de la caméra de jeu pour utiliser un proportions de 16:9, ce qui évite la distorsion d’étirement. Même si vous laissez la mémoire tampon d’arrière-plan à une résolution de 4:3, le changement de la transformation de projection pour utiliser 16:9 améliore considérablement la précision perçue de l’image rendue. bien sûr, l’image finale est filtrée pour mettre à l’échelle la résolution de mémoire tampon d’arrière-plan 4:3 pour respecter la résolution d’affichage Native 16:9, mais il s’agit d’un artefact moins perceptible que la distorsion d’étirement provoquée par une incompatibilité des proportions.

Le coût du rendu de la scène via l’appareil photo 16:9 peut être supérieur à celui d’un appareil photo 4:3 (même dans des résolutions identiques), car davantage d’objets de scène sont visibles dans la vue frustum. Vous devez également être conscient de la façon dont la zone affichable agrandie peut influencer le jeu. par exemple, une caméra de jeu avec un ratio 16:9 révèle plus de monde de jeu qu’une caméra 4:3.

Pour obtenir les meilleurs résultats sur un affichage 16:9, vous devez effectuer un rendu sur une mémoire tampon d’arrière-plan 16:9, mais cela nécessitera évidemment un remplissage d’un nombre de pixels supérieur. La différence entre 640 × 480 et 720 × 480 est d’environ 38 400 pixels, ce qui représente un gain de 12,5%. Si vous pouvez vous permettre de remplir cette zone plus volumineuse, nous vous recommandons vivement de le faire.

## <a name="title-safe-region"></a>Title-Safe la région

La mémoire tampon de trame d’image peut être partiellement masquée par l’utilisateur, car certains pixels autour de la bordure sont souvent couverts par le cadre avant de l’affichage. Pour vous assurer que les éléments d’interface utilisateur critiques sont visibles sur une grande variété de matériel d’affichage, vous devez respecter les exigences de région de titre sécurisé pour votre mode d’affichage cible. Pour les modes non HDTV, la zone de sécurité du titre est le 85 pour cent interne de la mémoire tampon de trame, et pour les modes HDTV, la zone de sécurité du titre est le 90 de pourcentage interne. Par conséquent, pour une compatibilité optimale sur le matériel d’affichage actuel et futur, vous devez conserver tous les éléments d’interface utilisateur critiques et les indicateurs d’affichage à l’intérieur du 85 pour cent internes de la mémoire tampon de trame.

## <a name="ntsc-suggestions"></a>Suggestions NTSC

Étant donné que NTSC est le standard vidéo le plus courant dans le États-Unis pour le matériel d’affichage des consommateurs, il est important de connaître certaines des instructions que vous devez suivre pour votre image de sortie.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Fixer les valeurs du composant de couleur RVB entre 16 et 235

Les couleurs en dehors de la plage de 16-235 peuvent certainement être envoyées à une TV NTSC, mais il est probable que ces valeurs hors limites seront interprétées comme des données audio. Il s’agit souvent d’un *bourdonnement sonore*, qui serait le plus évident si votre contenu était présenté sur un fond blanc Uni. Vous pouvez facilement implémenter la mise en couleur des couleurs de sortie dans un nuanceur de pixels.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Évitez les couleurs similaires qui peuvent apparaître identiques

La gamme de couleurs NTSC n’offre pas la même palette qu’un moniteur d’ordinateur standard, donc évitez d’utiliser des couleurs similaires là où le jeu exige que le joueur reconnaisse la différence.

### <a name="avoid-sharp-differences-in-contrast"></a>Évitez les différences nettes en comparaison

Bien que cette règle ne soit pas toujours pratique à suivre, vous pouvez atténuer certaines des nuisances de couleur sur les affichages NTSC (également appelées « *analyse Chroma*») en sélectionnant les couleurs appropriées pour les éléments de premier plan et d’arrière-plan de l’interface utilisateur. le texte blanc sur un arrière-plan de couleur donnera probablement de meilleurs résultats que des couleurs contrastées.

## <a name="conclusion"></a>Conclusion

cet article a présenté l’expérience de 10 pieds du point de vue d’un développeur de jeux Windows, mais ce n’est en aucune façon une enquête complète. vous devez rechercher ces rubriques plus en détail si vous développez un titre de jeu Windows (même s’il n’est pas destiné à être utilisé avec Windows Media Center). Le véritable test consiste à essayer votre jeu sur un large éventail d’affichages vidéo pour vous assurer que votre jeu offre une expérience agréable sur chacun. en fonction de la durée de vie classique d’un jeu basé sur les Windows et de la croissance prédite de l’utilisation de Windows Media Center, il est presque garanti qu’un jeu que vous publiez aujourd’hui fait partie de l’expérience de 10 pieds de l’utilisateur, que les clients peuvent jouer à votre jeu depuis le confort des canapés ou qu’ils sont imposés à des bureaux.

 

 