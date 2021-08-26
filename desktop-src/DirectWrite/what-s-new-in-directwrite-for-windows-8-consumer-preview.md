---
title: Nouveautés de DirectWrite
description: Voici quelques-uns des nouveaux ajouts à DirectWrite.
ms.assetid: 2512D222-C6EB-4C2D-80A6-7978FED56F7A
ms.topic: article
ms.date: 09/23/2019
ms.openlocfilehash: 2184ce1df7a9912a67baf1e15aa8c19f6c44f300f991506c505b672025067ae4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963809"
---
# <a name="whats-new-in-directwrite"></a>Nouveautés de DirectWrite

cette rubrique décrit les nouveautés de [DirectWrite](direct-write-portal.md) pour différentes versions de Windows 10.

## <a name="windows-app-sdk"></a>Kit de développement logiciel (SDK) pour application Windows

le [kit de développement logiciel (SDK) d’application Windows](/windows/apps/windows-app-sdk/) introduit une nouvelle version de DirectWrite, appelée DWriteCore. Pour plus d’informations, consultez [vue d’ensemble de DWriteCore](dwritecore-overview.md).

## <a name="windows-10-may-2019-update"></a>Mise à jour de Windows 10 de mai 2019

aucune fonctionnalité ou api n’a été ajoutée ni mise à jour pour Windows 10, version 1903 (10,0 ; Build 18362) &mdash; également connu sous le nom de Mise à jour de mai 2019 de Windows 10.

## <a name="windows-10-october-2018-update"></a>Windows 10 avec la mise à jour d’octobre 2018

les fonctionnalités et les api suivantes ont été ajoutées ou mises à jour pour Windows 10, version 1809 (10,0 ; Build 17763) &mdash; également connu sous le nom de Mise à jour d’octobre 2018 de Windows 10.

### <a name="new"></a>Nouveau

- Énumération [**DWRITE_FONT_SOURCE_TYPE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type)
- Interface [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) et ses méthodes

## <a name="windows-10-april-2018-update"></a>Mise à jour d’avril 2018 de Windows 10

les fonctionnalités et les api suivantes ont été ajoutées ou mises à jour pour Windows 10, version 1803 (10,0 ; Build 17134) &mdash; également connue sous le nom de Windows 10 mise à jour d’avril 2018.

### <a name="new"></a>Nouveau

- Interface [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) et ses méthodes
- Interface [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) et ses méthodes
- Interface [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) et ses méthodes

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

les fonctionnalités et les api suivantes ont été ajoutées ou mises à jour pour Windows 10, version 1709 (10,0 ; Build 16299) &mdash; également connu sous le nom de Windows 10 Fall Creators Update.

### <a name="new"></a>Nouveau

- Énumération [**DWRITE_AUTOMATIC_FONT_AXES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes)
- Énumération [**DWRITE_FONT_AXIS_ATTRIBUTES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes)
- Énumération [**DWRITE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag)
- Énumération [**DWRITE_FONT_FAMILY_MODEL**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model)
- Interface [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) et ses méthodes
- Interface [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) et ses méthodes
- Interface [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) et ses méthodes
- Interface [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) et ses méthodes
- Interface [**IDWriteFontFallback1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfallback1) et ses méthodes
- Interface [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) et ses méthodes
- Interface [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) et ses méthodes
- Interface [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) et ses méthodes
- Interface [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) et ses méthodes
- Interface [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) et ses méthodes
- Interface [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) et ses méthodes
- Interface [**IDWriteTextLayout4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextlayout4) et ses méthodes
- Macro [**DWRITE_MAKE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/nf-dwrite_3-dwrite_make_font_axis_tag)
- Structure [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)
- Structure [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)

### <a name="moved"></a>Ramené

L’énumération [**DWRITE_GLYPH_IMAGE_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) déplacée de `dwrite_3.h` vers `dcommon.h` .

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

les fonctionnalités et les api suivantes ont été ajoutées ou mises à jour pour Windows 10, version 1703 (10,0 ; Build 15063) &mdash; également connu sous le nom de Windows 10 Creators Update.

### <a name="expanded-api-support-for-cloud-fonts-and-custom-font-sets"></a>Prise en charge étendue des API pour les polices Cloud et les jeux de polices personnalisés

Windows 10 des api incluses qui permettent aux applications d’accéder facilement aux polices d’un service de police Windows. dans le Windows 10 Creators Update, les api pour les polices distantes sont étendues pour permettre un accès facile aux polices à partir d’autres sources sur le Web accessibles via http ou https. 

Les nouvelles API de police à distance peuvent être utilisées avec des services Web publics ou privés. En outre, ils peuvent être utilisés pour accéder aux fichiers de police OpenType bruts (. ttf,. otf.,. TTC,. OTC) ou aux polices empaquetées dans des formats de conteneur [WOFF](https://www.w3.org/TR/WOFF/) ou [WOFF2](https://www.w3.org/TR/WOFF2/) . Les nouvelles API sont utilisées conjointement avec les API existantes pour la mise en file d’attente des demandes de téléchargement des données de police à distance et pour la gestion du processus de téléchargement réel.

D’autres nouvelles API permettent aux applications de travailler plus facilement avec les polices personnalisées stockées dans le système de fichiers local ou qui sont chargées dans une mémoire tampon.

Pour plus d’informations sur les nouvelles API permettant d’utiliser des polices distantes, des jeux de polices personnalisés ou des formats de conteneur WOFF/WOFF2, consultez la rubrique suivante :

[Jeux de polices personnalisés](custom-font-sets-win10.md)

Consultez également les liens vers les rubriques de référence sur les API fournies dans cette rubrique.  l’utilisation des api nouvelles et existantes pour l’utilisation des polices personnalisées est également illustrée dans la [DirectWrite exemple de jeux de polices personnalisés](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). Cet exemple illustre l’implémentation de code pour différents scénarios, notamment les polices locales sur le disque, les polices distantes sur le Web, les données de police en mémoire et les polices dans les formats WOFF ou WOFF2 compressés.

### <a name="initial-support-for-opentype-font-variations"></a>Prise en charge initiale des variantes de police OpenType

La version 1,8 de la spécification de format de police OpenType a introduit une nouvelle extension passionnante pour le format connu sous le nom de variantes de police OpenType. DirectWrite a été mis à jour dans la Windows 10 Creators Update pour prendre en charge les instances nommées de polices de variables. Pour plus d'informations, voir la rubrique suivante :

[Polices de variable OpenType](opentype-variable-fonts.md)

## <a name="windows-10-anniversary-update"></a>Mise à jour anniversaire Windows 10

les fonctionnalités et les api suivantes ont été ajoutées ou mises à jour pour Windows 10, version 1607 (10,0 ; Build 14393) &mdash; également connue sous le nom de Windows 10 mise à jour anniversaire.

### <a name="improved-support-for-color-fonts"></a>Prise en charge améliorée des polices en couleur

à partir de Windows 10 mise à jour anniversaire, DirectWrite fournit une prise en charge intégrée d’un large éventail de formats de police de couleur, ce qui permet aux développeurs d’utiliser plus de types de polices dans leurs applications DirectWrite que jamais auparavant. Cela inclut la prise en charge des éléments suivants :

-   La table OpenType « COLR », qui active le contenu vectoriel compact dans les polices. (Pris en charge depuis Windows 8.1.)
-   La table OpenType « SVG », qui active le contenu SVG dans les polices.
-   La table OpenType « CBDT », qui permet de coloriser le contenu de la bitmap dans les polices.
-   La table OpenType « sbix », qui permet de coloriser le contenu de la bitmap dans les polices.

[Direct2D](../direct2d/direct2d-portal.md), qui utilise DirectWrite pour le rendu de texte, prend en charge automatiquement ces formats de police de couleur lorsque l' [**\_ option D2D1 dessiner le \_ texte \_ \_ activer \_ \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) l’indicateur de police de couleur est activée. Pour plus d'informations, voir les rubriques suivantes :

-   [Polices de couleur](color-fonts.md)
-   [exemple de glyphe de couleur DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="support-for-adobe-typekit-and-other-font-service-clients"></a>Prise en charge d’Adobe Typekit et d’autres clients de service de polices

certains services de police, tels qu’Adobe Typekit, possèdent des utilitaires côté client qui permettent à un utilisateur de charger des polices à partir du service et de les utiliser dans différentes applications sur leur ordinateur Windows. Ces utilitaires fonctionnent généralement en effectuant des appels au moment de l’exécution à GDI pour charger des polices supplémentaires, plutôt que d’installer définitivement des polices sur le système. en raison de cette conception, sur les versions antérieures de Windows, les polices seraient utilisables dans les applications GDI, mais pas dans les applications DirectWrite. à partir de la Windows 10 mise à jour anniversaire, les polices qui sont chargées par ces utilitaires sont également disponibles dans DirectWrite et dans GDI.

Les polices chargées par un utilitaire de service de polices sont visibles dans la collection de polices système obtenue en appelant la méthode [**IDWriteFactory :: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Étant donné que les services de police suivent généralement un modèle de licence par utilisateur, les polices chargées par ces utilitaires sont gérées par utilisateur. par conséquent, les applications DirectWrite existantes peuvent utiliser des polices que les utilisateurs finaux ont obtenues à l’aide de ces services, sans aucune modification de code requise dans l’application, offrant ainsi une expérience plus transparente pour les utilisateurs.

### <a name="support-for-opentype-collections-using-cff-outlines"></a>Prise en charge des collections OpenType à l’aide des contours CFF

Les formats de police OpenType et TrueType bénéficient d’une prise en charge de plusieurs polices qui peuvent être regroupées dans un même fichier de polices, appelé « collection de polices ». La spécification OpenType a toujours permis aux polices d’utiliser des formats TrueType ou CFF pour les données de plan de glyphe. Jusqu’à récemment, toutefois, la spécification n’est autorisée que pour les collections dans lesquelles les contours de glyphe utilisent le format TrueType. La version 1,7 de OpenType permet désormais aux collections d’utiliser des formats TrueType ou CFF pour les données de plan de glyphe. à partir de la Windows 10 mise à jour anniversaire, DirectWrite prend en charge les collections OpenType à l’aide des données de plan CFF.

## <a name="windows-10"></a>Windows 10

### <a name="windows-font-service-integration"></a>intégration du service de police Windows

à partir de Windows 10, les polices incluses avec Windows sont disponibles dans un service en ligne et sont accessibles via DirectWrite sur tout appareil Windows 10. cela s’applique à toutes les éditions de Windows 10, y compris Windows 10 Mobile, Xbox et HoloLens, ainsi que le client desktop. cela permet aux applications d’afficher du contenu à l’aide de n’importe quelle police Windows même si la police n’est pas installée actuellement sur l’appareil.

la prise en charge des mécanismes de DirectWrite font-service a été implémentée dans l’infrastructure xaml, ce qui signifie que toutes les applications qui utilisent XAML ne nécessitent aucune modification de code pour tirer parti du service de police. L' [exemple de code de polices téléchargeables (XAML)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/XamlCloudFontIntegration) illustre cela. les Applications qui appellent DirectWrite des api directement devront utiliser de nouvelles api pour utiliser les mécanismes de service de police. Pour plus d'informations, voir les rubriques suivantes :

-   [**IDWriteFactory3 :: GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) , méthode
-   Interface [**IDWriteTextLayout3**](idwritetextlayout3.md)
-   Interface [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue)
-   Interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)

l' [exemple de code des polices téléchargeables (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) illustre l’utilisation de plusieurs nouvelles api.

### <a name="font-set-apis"></a>API de jeu de polices

les interfaces de collection de polices d’DirectWrite fournissent une vue d’une collection de polices organisée par familles de polices, en utilisant le poids, l’étirement et le style en tant qu’attributs de sous-famille. en interne, DirectWrite implémente l’interface de collection de polices à l’aide d’une liste plate de polices avec différents attributs. Cette approche est plus flexible dans et peut prendre en charge l’énumération des familles poids/Stretch/style, mais également prendre en charge l’interrogation et le filtrage à l’aide d’autres attributs de police.

dans Windows 10, ce mécanisme de gestion de polices plus flexible est mis à la disposition des applications via IDWriteFontSet et les api associées. Les API de jeu de polices peuvent être utilisées, par exemple, pour créer une interface utilisateur personnalisée de sélecteur de polices, en tirant parti des propriétés de police personnalisées de l’application dans un jeu de polices personnalisé.

Pour plus d'informations, voir les rubriques suivantes :

-   Interface [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   Interface [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**DWRITE \_ \_ \_**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) Énumération de l’ID de propriété de police
-   [**IDWriteFontFactory3 :: GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) , méthode

### <a name="new-text-layout-line-spacing-modes"></a>Nouveaux modes d’espacement de ligne de disposition du texte

le format de texte et les interfaces de mise en forme de texte de DirectWrite prennent en charge de nouveaux modes d’espacement de ligne. dans les versions antérieures, l’implémentation de la disposition du texte de DirectWrite était autorisée pour l’interligne dans laquelle la hauteur de chaque ligne était définie automatiquement en fonction de l’élément le plus haut dans une ligne (mode « par défaut ») ou de l’interligne avec toutes les lignes définies sur une hauteur uniforme déterminée par l’application (mode « uniforme »). dans Windows 10, un mode d’espacement de lignes « proportionnel » supplémentaire est pris en charge qui donne aux applications plus d’options pour le comportement de l’interligne. Pour plus d'informations, voir les rubriques suivantes :

-   Interface [**IDWriteTextLayout3**](idwritetextlayout3.md)
-   [**IDWriteTextLayout3 :: SetLineSpacing**](idwritetextlayout3-setlinespacing.md) , méthode
-   [**DWRITE \_ Structure \_ d’INTERligne**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)
-   [**DWRITE \_ Énumération de \_ \_ méthode d’interligne**](/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method)
-   [**DWRITE \_ Énumération \_ \_ \_ utilisation de l’intervalle de ligne de police**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage)
-   [**IDWriteTextLayout3 :: GetLineMetrics**](idwritetextlayout3-getlinemetrics.md) , méthode
-   [**DWRITE \_ Structure \_ METRICS1 de ligne**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1)

l' [exemple de code d’interligne (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteLineSpacingModes) illustre l’utilisation de plusieurs nouvelles api, et fournit également une visualisation de tous les différents modes d’interligne qui facilite grandement la compréhension des différentes options d’espacement de ligne disponibles.

### <a name="gdi-interop"></a>Interopérabilité GDI

depuis son introduction dans Windows 7, DirectWrite a fourni un chemin de migration pour les applications qui ont été implémentées à l’origine à l’aide du modèle de police GDI, de la disposition du texte et du rendu. Celui-ci a été fourni par le biais de l' \[ \[ \] \] interface IDWriteGdiInterop. dans Windows 10, des api supplémentaires fournissent des fonctionnalités d’interopérabilité GDI supplémentaires. Pour plus d’informations, consultez la rubrique suivante :

-   Interface [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1)

## <a name="windows-81"></a>Windows 8.1

### <a name="rendering-color-fonts"></a>Rendu des polices de couleur

à partir de Windows Windows 8.1, DirectWrite prend en charge les polices de couleur. [Direct2D](../direct2d/direct2d-portal.md), qui utilise DirectWrite pour le rendu de texte, a ajouté la valeur d’énumération D2D1 les \_ OPTIONS de dessin du \_ texte activer la \_ \_ \_ \_ police de couleur pour activer cette fonctionnalité lors du dessin de texte. Pour plus d'informations, voir les rubriques suivantes :

-   [**D2d1 \_ Énumération des \_ \_ options de dessin de texte**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options)
-   [**IDWriteFactory2 :: TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun) , méthode

## <a name="windows-8"></a>Windows 8

Nouvelle interface de fabrique, [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1), pour la création d’interfaces supplémentaires disponibles.

Propriétés de police supplémentaires, telles que : Super/indice, pente du signe insertion, Panose et plages Unicode.

-   [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
-   [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)

Des améliorations de l’espacement, telles que : contrôler l’espacement des caractères, les paires de crénage héritées et la justification. Pour plus d’informations, consultez la rubrique [justification, crénage et espacement](justification--kerning--and-spacing.md) .

-   [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Amélioration des cibles de rendu et des paramètres.

-   [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)
-   [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1)

Améliorations de l’analyse de complexité du texte.

-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Nouvelles propriétés de script, nouvelle prise en charge des scripts (Unicode 6), ajouts de polices de secours, parenthèses jumelées et augmentation bidi.

Améliorations des performances du cache de polices. à partir de Windows 8 le cache de police est global et démarre au démarrage de l’ordinateur.

Nouveaux modes de rendu.

à partir de Windows 8, [DirectWrite](direct-write-portal.md) prend en charge un certain nombre de fonctionnalités qui vous aident à créer des applications pour le marché mondial.

Voici plusieurs zones qui vous permettent d’implémenter des applications de texte enrichi qui peuvent être personnalisées pour les clients dans le monde entier.

### <a name="chinese-japanese-and-korean-extensions-c--d"></a>Extensions chinoises, japonaises et coréennes C & D

Au bout de quelques années, le consortium Unicode libère une liste standardisée d’ajouts au bloc idéogramme, japonais et coréen unifié. Avec la révision Unicode 6,0, elles ont publié des blocs d’extension C et D. Ces blocs de idéogrammes se trouvent sur l’extension de site Web Unicode [C](https://www.unicode.org/charts/PDF/U2A700.pdf) et l' [extension D](https://www.unicode.org/charts/PDF/U2B740.pdf).

à partir de Windows 8, [DirectWrite](direct-write-portal.md) prend en charge les points de dépassements Unicode pour ces nouveaux blocs de idéogrammes cjc standardisés, vous pouvez donc les utiliser dans DirectWrite applications.

### <a name="indian-rupee-symbol"></a>Symbole indien Roupie

En mars de 2005, le gouvernement indien a annoncé une compétition pour choisir un symbole pour la monnaie indienne Roupie. après une concurrence importante, le 15 juillet 2010, le gouvernement indien a choisi la conception créée par D. Udaya Kumar, et [DirectWrite](direct-write-portal.md) prend en charge le point de code Unicode lié au symbole. par conséquent, les applications DirectWrite prennent désormais en charge ce symbole monétaire.

### <a name="emoji"></a>Emoji

[DirectWrite](direct-write-portal.md) prend désormais en charge l’utilisation d’emoji dans les applications. les versions précédentes de DirectWrite, présentées avec une zone de glyphe manquante si vous avez essayé d’effectuer le rendu d’un idéogramme d’emoji. à partir de Windows 8, DirectWrite prend en charge les codeblock unicode associés à emoji. par conséquent, si votre application utilise les points de référence standard unicode pour l’emoji, elle affiche les glyphes appropriés.

### <a name="myanmar-tiffinagh-and-old-hangul-languages"></a>Myanmar, Tiffinagh et vieil langages Hangul

à partir de Windows 8, [DirectWrite](direct-write-portal.md) prend en charge le bloc de points de suspension Unicode qui correspondent aux glyphes dans les langues hangûl, Tiffinagh et Old, ce qui vous permet de créer des applications qui incluent du texte de ces trois langages. outre la prise en charge de ces caractères, DirectWrite prend en charge la manière dont l’ancien gère le saut de ligne.

### <a name="new-scripts"></a>Nouveaux scripts

à partir de Windows 8, la méthode [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties) retourne des informations pour un certain nombre de nouveaux scripts. voici la liste des scripts pris en charge par [DirectWrite](direct-write-portal.md) dans Windows 8 et après.

-   Avestan
-   Bamoum
-   Batik
-   Brahmi
-   Hieroglyphics égyptienne
-   Samaritain impérial
-   Pahlavi d’inscription
-   Parthian d’inscription
-   Javanais
-   Kaithi
-   Lisu (Fraser)
-   Mandéen
-   Meitei mayek
-   Vieil-arabe du Sud
-   Ancien turc (Orkhon)
-   Samaritaine
-   Taï Tham (Lanna)
-   Taï Viêt
