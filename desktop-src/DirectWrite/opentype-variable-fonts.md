---
title: Polices de variable OpenType
description: cette rubrique décrit les polices de variable OpenType, leur prise en charge dans DirectWrite et Direct2D, et comment les utiliser dans votre application. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c671bebce73cf3bdec42d1f7f570add914db7eb33b8a6bfd1b196d569b9975d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649390"
---
# <a name="opentype-variable-fonts"></a>Polices de variable OpenType

cette rubrique décrit les polices de variable OpenType, leur prise en charge dans DirectWrite et Direct2D, et comment les utiliser dans votre application. 

-   [Que sont les polices de variable OpenType ?](#what-are-opentype-variable-fonts)
-   [Prise en charge des polices de variable OpenType dans DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Utilisation des polices de variable OpenType](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>Que sont les polices de variable OpenType ?

La version 1,8 de la [spécification de format de police OpenType](https://www.microsoft.com/typography/otspec/) a introduit une nouvelle extension au format connu sous le nom de [variantes de police OpenType](/typography/opentype/spec/otvaroverview). Les polices qui utilisent ces extensions sont appelées polices de variable OpenType. Une police de variable OpenType est une police unique qui peut se comporter comme plusieurs polices en utilisant une interpolation continue entre différentes conceptions, toutes définies dans la police unique.

Une police de variable OpenType peut définir la variation continue de sa conception sur un ou plusieurs axes indépendants, tels que le poids ou la largeur : 

 

![Affiche une police de variable OpenType à l’aide de la lettre « G » et affiche différentes variantes le long d’un axe de largeur horizontal et d’un axe de pondération verticale.](images/opentype-width-weight.png)

Un développeur de polices détermine un ensemble d’axes de variation à utiliser dans une police donnée. Ces axes peuvent inclure un ensemble d’axes de variation bien connus (ou « enregistrés »), tels que le poids et la largeur, mais ils peuvent également inclure des axes de variation personnalisés et arbitraires définis par le développeur de polices.  

En sélectionnant un ensemble d’axes de variantes pour une police, le développeur de polices définit un espace n-dimensionnel abstrait de variation de conception pour la police. Les moteurs de texte peuvent spécifier éventuellement une position, ou « instance », au sein de cet espace continu pour la disposition et le rendu du texte. 

Le développeur de polices peut également sélectionner et assigner des noms à des instances particulières au sein de l’espace de variation de conception ; celles-ci sont appelées « instances nommées ». Par exemple, une police avec une variation de poids peut prendre en charge une variation continue entre des traits très clairs et très lourds, tandis que le développeur de polices a sélectionné des pondérations particulières sur ce continuum et des noms qui leur sont attribués, tels que « Light », « Regular » et « SemiBold ». 

Le format de police de variable OpenType utilise des tables de données se trouvant dans les polices OpenType traditionnelles, ainsi que certaines tables supplémentaires qui décrivent comment les valeurs de différents éléments de données sont modifiées pour différentes instances. Le format désigne une instance de variation comme « instance par défaut », qui utilise des tables traditionnelles pour obtenir les valeurs par défaut. Toutes les autres instances dépendent des données par défaut et d’autres données Delta. Par exemple, une table « glyf » peut avoir une description de courbe de Bézier d’une forme de glyphe nominale, qui est la forme utilisée pour l’instance par défaut, tandis qu’une table « GVAR » décrit la façon dont les points de contrôle Bézier du glyphe sont ajustés pour les autres instances. De même, les autres valeurs de police peuvent avoir une valeur nominale, plus les données Delta décrivant la manière dont ces valeurs changent pour des instances différentes ; par exemple, la hauteur x et d’autres métriques à l’échelle de la police, les positions d’ancrage de marque spécifiques aux glyphes et les réglages de crénage. 

Étant donné que les polices variables peuvent prendre en charge un jeu arbitraire d’axes de variation, elles nécessitent un modèle extensible de familles de polices qui reflète plus directement la manière dont les concepteurs de polices créent des familles de polices : une famille de polices est définie par un nom de famille et certaines caractéristiques de conception constantes, avec un nombre arbitraire (déterminé par le développeur de polices) des façons dont la Une famille de polices peut être créée avec des variantes pour le poids, mais une famille de polices différente peut être créée avec des variantes pour la hauteur x, Serif-Size, « funkiness », ou tout ce que le développeur de polices souhaite. Dans ce modèle, une sélection de type de police est mieux décrite à l’aide de général, ou « par défaut » ou « typographique », nom de famille plus un ensemble de paires clé-valeur, chacune représentant un type de variation et une valeur spécifique, avec les genres de variation en général en tant que jeu extensible. Cette notion générale d’une famille de polices peut s’appliquer aux polices traditionnelles, non variables et aux polices variables. Par exemple, dans ce général, le modèle de famille typographique, une famille « Selawik VF », peut avoir des variations de poids, de taille optique et de conception Serif, avec des instances telles que « Semilight bannière San ». 

toutefois, certaines implémentations logicielles existantes, y compris les api DirectWrite existantes, peuvent être conçues en supposant un modèle de familles de polices plus limité. Par exemple, certaines applications peuvent supposer qu’une famille de polices peut avoir, au plus, des variantes normal, gras, italique et gras italiques. les interfaces [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) et [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) existantes supposent un modèle de famille poids/stretch/style (« WSS »), ce qui permet de spécifier des variantes dans une famille à l’aide de l' [**\_ \_ épaisseur de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), de l' [**\_ \_ étirement de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) ou des énumérations de [**\_ \_ style de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) en tant que paramètres. dans l’exemple précédent, la taille optique et les axes serif ne sont pas traités comme des axes internes de la famille de variation dans le modèle de WSS. 

La prise en charge complète des polices variables nécessiterait des API qui permettent de spécifier un membre de la famille avec éventuellement plusieurs paramètres, comme déterminé par la police. Toutefois, les conceptions d’API existantes peuvent être en mesure de fournir une prise en charge partielle des polices variables en projetant les instances nommées définies dans une police de variable dans les modèles de famille de polices les plus limités. dans l’exemple précédent, « Selawik vf Semilight banner san » peut être projeté dans le modèle WSS en tant que famille « Selawik vf banner san » avec « Semilight » comme variante de poids. 

Pour un autre exemple, considérez une famille de polices typographiques telle que Sitka, avec des variantes de poids et de taille optique. Les variantes nommées de la famille incluent le texte Sitka normal et le gras de la bannière Sitka (plus beaucoup d’autres). Le nom de famille typographique est « Sitka », alors que les noms de police pour ces variantes dans le modèle de famille typographique seraient « texte normal » et « bannière en gras ». les modèles de famille à quatre membres et WSS n’autorisent pas les variantes de taille optique au sein d’une famille. les distinctions de taille optique doivent donc être traitées comme des distinctions au niveau de la famille. le tableau suivant illustre la façon dont une sélection des polices de la famille typographique Sitka est traitée dans le modèle de famille WSS : 



Modèle de famille typographique

modèle de famille WSS

Famille

Visage

Famille

Visage

Sitka

Texte normal

Texte Sitka

Normal

Sitka

Bannière en gras

Bannière Sitka

Gras

Sitka

Légende en italique

Légende Sitka

Italique



 

la projection de noms d’un modèle de famille typographique sur le modèle de famille WSS peut être appliquée aux polices non variables et aux instances nommées de polices de variable. Cela ne peut toutefois pas être fait pour d’autres instances non nommées à partir de l’espace de variation de conception continue d’une police de variable. Pour cette raison, la prise en charge de la fonctionnalité complète des polices variables nécessitera des API conçues pour faire référence à des visages dans une famille typographique en termes d’un ensemble d’axes de variantes et de valeurs d’axe non restreints. 

## <a name="opentype-variable-font-support-in-directwrite"></a>Prise en charge des polices de variable OpenType dans DirectWrite

depuis la publication de la Windows 10 Creators Update, le format de police de variable OpenType est toujours très nouveau, et les fournisseurs de polices, les plateformes et les applications sont toujours en cours d’implémentation du nouveau format. Cette mise à jour fournit une implémentation initiale pour ce format dans DirectWrite. 

les éléments internes de DirectWrite ont été mis à jour pour prendre en charge les polices de variable OpenType. À l’aide des API actuelles, cela prend en charge toutes les instances nommées d’une police de variable. Cette prise en charge peut être utilisée pour les flux de travail complets, de l’énumération des instances nommées, la sélection d’une instance nommée, l’utilisation de la mise en page et de la mise en forme, le rendu et l’impression. Pour l’avantage des applications qui utilisent également l’interopérabilité de texte GDI pour certaines opérations, une prise en charge similaire a également été ajoutée dans les API GDI existantes. 

dans le Windows 10 Creators Update, DirectWrite ne prend pas en charge les instances arbitraires qui utilisent la fonctionnalité de variation continue des polices variables.

dans de nombreuses opérations, le comportement de DirectWrite des instances nommées d’une police de variable ne peut pas être distingué du comportement des polices non variables. et dans la mesure où la prise en charge est assurée à l’aide des api DirectWrite existantes, les instances nommées des polices variables peuvent même fonctionner dans de nombreuses applications DirectWrite existantes sans aucune modification. Toutefois, des exceptions peuvent s’appliquer dans certains cas :  

-   Si une application traite les données de police directement pour certaines opérations. Par exemple, si une application lit les données de contour de glyphe directement à partir du fichier de police pour créer certains effets visuels.
-   Si une application utilise une bibliothèque tierce pour certaines opérations. par exemple, si une application utilise DirectWrite pour la disposition, pour obtenir les index et les positions des glyphes finaux, mais utilise ensuite une bibliothèque tierce pour le rendu.
-   Si une application incorpore des données de police dans un document ou d’une autre façon, transmet des données de police à un processus en aval.

Si des opérations sont effectuées à l’aide d’implémentations qui ne prennent pas en charge les polices variables, ces opérations peuvent ne pas produire les résultats attendus. Par exemple, les positions de glyphes peuvent être calculées pour une instance nommée de la police de la variable, mais les glyphes peuvent être rendus en supposant une instance nommée différente. En fonction de l’implémentation de l’application, les résultats peuvent fonctionner dans certains contextes, mais pas dans d’autres contextes dans lesquels d’autres bibliothèques peuvent être utilisées. Par exemple, le texte peut s’afficher correctement à l’écran, mais pas à l’impression. si les flux de travail de bout en bout sont implémentés uniquement à l’aide de DirectWrite, le comportement correct pour les instances nommées d’une police variable peut être attendu. 

étant donné que les api DirectWrite existantes prennent en charge la sélection de visage à l’aide du modèle poids/stretch/style, les instances nommées des polices qui utilisent d’autres axes de variation seront projetées à partir du modèle de famille typographique général dans le modèle de WSS, comme décrit ci-dessus. Cela repose sur une police variable incluant une table « attributs de style » (« STAT ») avec des sous-tables de valeurs d’axe, que DWrite utilise pour distinguer les jetons de nom de police qui désignent les attributs de poids, d’étirement ou de style des jetons qui se rapportent à d’autres axes de variation.  

si une police de variable n’inclut pas de table « STAT », comme requis pour les polices variables par la spécification OpenType, DirectWrite traite la police comme une police non variable contenant uniquement l’instance par défaut.  

Si une police contient une table « STAT », mais qu’elle n’inclut pas les sous-tables de valeur AXIS appropriées, cela peut entraîner des résultats inattendus, par exemple avoir plusieurs faces ayant des noms de visages identiques. Ces polices ne sont pas prises en charge pour l’instant. 

La spécification OpenType permet de représenter les données de plan de glyphe dans l’un des deux formats suivants : à l’aide d’une table « glyf », qui utilise le format de plan et d’affinage TrueType, ou à l’aide d’une table « CFF », qui utilise la représentation au format de police compact (« CFF »). Dans une police de variable avec des contours TrueType, la table « glyf » continue à être utilisée et est complétée par une table « GVAR » qui fournit les données de variation pour les contours. Cela signifie que l’instance par défaut d’une police de variable avec des contours TrueType utilise uniquement les tables OpenType traditionnelles qui seront prises en charge dans les anciens logiciels qui n’ont pas de prise en charge de police variable. Toutefois, dans une police de variable avec des contours CFF, la table « CFF » est remplacée par la table « CFF2 », qui encapsule les données de plan par défaut et les données de variation associées dans une table. Les données CFF sont traitées par un rastériseur distinct de celui utilisé pour les données TrueType, et une table « CFF2 » nécessite un rastériseur CFF mis à jour qui a la prise en charge de « CFF2 ». Une table « CFF2 » ne peut pas être traitée par des rastériseurs CFF plus anciens. Pour une police variable avec des données de plan CFF, cela signifie que même l’instance par défaut ne fonctionnera pas dans les anciens logiciels. 

dans le Windows 10 Creators Update, DirectWrite ne prend pas en charge les polices variables avec des données de plan CFF à l’aide de la table’CFF2 '. 

## <a name="using-opentype-variable-fonts"></a>Utilisation des polices de variable OpenType

Les polices de variable OpenType peuvent être faciles à utiliser, en gardant à l’esprit les limitations actuelles mentionnées ci-dessus : 

-   Seules les instances nommées d’une police de variable sont prises en charge pour l’instant.
-   Seules les polices variables qui utilisent des données de plan de glyphe TrueType (pas les contours CFF) sont prises en charge pour l’instant. 
-   pour les polices qui utilisent des axes de variations de conception autres que le poids, l’étirement ou le style, les instances nommées sont projetées dans le modèle de famille WSS, ce qui peut entraîner l’affichage de certaines instances nommées en tant que familles distinctes (comme dans le passé pour les polices non variables). Pour prendre cela en charge, les polices variables doivent avoir une table « STAT » qui comprend des sous-tables de valeurs d’axe appropriées.
-   les instances nommées de polices de variable sont prises en charge dans les api DirectWrite, mais si certaines opérations sont effectuées dans des implémentations plus anciennes qui ne prennent pas en charge les polices variables, celles-ci peuvent produire des résultats incorrects. 
-   certaines api DirectWrite utilisent l' [**\_ \_ épaisseur**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)de police DWRITE, l' [**\_ \_ étirement de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) et les énumérations de [**\_ \_ style de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) pour spécifier les attributs de poids, d’étirement et de style lors de la sélection des visages. Si une police variable utilise des axes de variation correspondants mais possède de nombreuses instances nommées qui nécessitent une granularité plus fine, toutes les instances nommées ne peuvent pas être sélectionnées dans ces API.

les polices de variable opentype conformes à ces exigences peuvent être installées à partir de l’interpréteur de commandes Windows comme d’autres polices OpenType, et peuvent également être utilisées dans des jeux de polices personnalisés créés par une application.  

Lorsqu’elles sont installées dans le système, toutes les instances nommées d’une police de variable sont incluses dans le jeu de polices retourné par l’appel de la méthode IDWriteFontFamily3 ::[**GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) . notez qu’un jeu de polices est une liste plate sans hiérarchie de regroupement de famille, mais chaque élément du jeu a une propriété de nom de famille basée sur le modèle de famille WSS. Le jeu de polices peut être filtré pour une instance nommée de police variable particulière à l’aide des méthodes [**IDWriteFontSet :: GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) . toutefois, si vous utilisez la surcharge **GetMatchingFonts** qui prend un familyName, le familyName spécifié doit utiliser le nom conforme à la WSS modèle de famille de polices. la liste complète des noms de famille compatibles WSS qui se trouvent dans un jeu de polices peut être obtenue à l’aide des méthodes [**IDWriteFontSet :: GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) utilisant le \_ nom de \_ famille ID de propriété DWRITE \_ \_ \_ .  

De même, toutes les instances nommées d’une police de variable sont représentées dans la collection de polices retournée par la méthode IDWriteFactory ::[**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . étant donné que les éléments d’une collection de polices sont des familles de polices basées sur le modèle WSS, les instances nommées d’une police variable peuvent être représentées dans une collection en tant que membres de deux familles de polices ou plus. si la méthode [**IDWriteFontCollection :: FindFamilyName**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) est utilisée, le paramètre familyName doit être un nom de famille compatible WSS. pour rechercher tous les noms de famille compatibles WSS à partir d’une collection de polices, une application peut parcourir chaque famille et appeler [**IDWriteFontFamily :: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames), bien qu’il soit plus facile d’obtenir un jeu de polices correspondant et d’utiliser la méthode [**GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) comme décrit ci-dessus. 

Lorsque vous utilisez des polices personnalisées, les différentes approches décrites dans la rubrique [jeux de polices personnalisées](custom-font-sets-win10.md) peuvent être utilisées pour créer un jeu de polices. Pour ajouter une police variable à un jeu de polices personnalisé, il est recommandé d’utiliser la méthode [**IDWriteFontSetBuilder1 :: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) , car elle prend en charge les polices variables et ajoute toutes les instances nommées d’une police variable en un seul appel. Pour le moment, il n’existe aucun moyen d’ajouter des instances nommées individuelles d’une police de variable personnalisée à un jeu de polices à l’aide des méthodes [**IDWriteFontSetBuilder :: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) , car il n’existe aucun moyen de créer une référence de type de police qui spécifie les instances nommées d’un fichier de police de variable. Cela signifie qu’il n’existe actuellement aucun moyen d’ajouter des instances nommées d’une police personnalisée à un jeu de polices personnalisé avec des propriétés personnalisées assignées. cela signifie qu’à son tour, les polices de variables personnalisées ne peuvent pas être facilement utilisées conjointement avec les api DirectWrite pour les polices distantes. Si des instances nommées d’une police de variable sont incluses dans un jeu de polices système, toutefois, les références de type de police pour chaque instance nommée existent déjà, et elles peuvent être ajoutées aux jeux de polices personnalisés, notamment avec l’utilisation de valeurs de propriétés personnalisées. Pour plus d’informations, consultez la rubrique jeux de polices personnalisés. 

lorsque vous travaillez avec des polices variables, les énumérations de l' [**\_ \_ épaisseur de police DirectWrite DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) et de la [**\_ police \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) sont étroitement connectées aux axes de variation de poids et de largeur définis dans la spécification OpenType, mais ne sont pas identiques. Tout d’abord, l’échelle numérique d’un axe de variation prend toujours en charge les valeurs fractionnaires, tandis que fontWeight et fontStretch utilisent des entiers. L’échelle de l’axe de poids OpenType utilise des valeurs comprises entre 1 et 1000, qui sont également prises en charge par fontWeight. Par conséquent, le changement d’une valeur d’axe de poids de variation en fontWeight est relativement mineur : l’fontWeight signalé pour une instance nommée peut être arrondie à partir de la valeur exacte utilisée pour définir l’instance nommée dans la police. la distinction entre DirectWrite fontStretch et l’échelle de l’axe de largeur OpenType est supérieure : DirectWrite utilise des valeurs comprises entre 1 et 9, en suivant les valeurs [usWidthClass](/typography/opentype/spec/os2#uswidthclass) de la table du système d’exploitation/2 opentype, tandis que l’échelle de l’axe de la largeur opentype utilise des valeurs positives représentant un pourcentage de la largeur normale. La documentation [usWidthClass](/typography/opentype/spec/os2#uswidthclass) dans la spécification OpenType fournit un mappage entre les valeurs de 1 à 9 et les pourcentages de valeurs normales. La valeur fontStretch signalée pour une instance nommée peut impliquer l’arrondi lors de la conversion des valeurs de l’axe de largeur. 

lorsque vous créez un [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), vous devez spécifier une collection de polices et des propriétés de police compatibles WSS (nom de famille, poids, stretch et style). Cela s’applique également lors de la définition des propriétés de mise en forme des polices sur une plage de texte [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Les propriétés peuvent être obtenues à partir d’un objet [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) ou d’objets [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) et [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) qui représentent une instance nommée particulière. comme observé ci-dessus, les valeurs retournées par les méthodes GetWeight et GetStretch peuvent être des approximations arrondies pour les valeurs d’axe réelles utilisées pour définir l’instance nommée, mais DirectWrite mappera la combinaison de propriétés à l’instance nommée souhaitée. 

de même, si une application utilise [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) pour créer des données de police de secours personnalisées, des familles sont spécifiées pour les mappages de plage de caractères à l’aide de noms de famille compatibles WSS. la substitution de police au sein de DirectWrite est basée sur les familles avec DirectWrite sélectionnant une variante au sein d’une famille de secours qui correspond à la correspondance la plus proche pour la variante de la famille de départ. pour les variantes qui impliquent des dimensions autres que le poids, l’étirement et le style, DirectWrite n’êtes pas en mesure de sélectionner ces variantes au sein d’une famille de secours, à moins que des données de secours personnalisées aient été créées spécifiquement pour fournir des mappages de secours pour les familles qui ont des attributs non WSS particuliers, tels que des variantes de taille optique de

 

 