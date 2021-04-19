---
title: Ombrage à taux variable (VRS)
description: L’ombrage à taux variable &mdash; ou l’ombrage de pixels grossistes &mdash; est un mécanisme qui vous permet d’allouer les performances de rendu/la puissance à des vitesses qui varient d’un rendu à l’autre.
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: 2f207cddee978915788291fc0ffe55160e6a93c6
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380763"
---
# <a name="variable-rate-shading-vrs"></a>Ombrage à taux variable (VRS)

## <a name="the-motivation-for-vrs"></a>Motivation de VRS
En raison des contraintes de performances, un convertisseur graphique ne peut pas toujours se permettre de fournir le même niveau de qualité à chaque partie de son image de sortie. L’ombrage à taux variable &mdash; ou l’ombrage de pixels grossistes &mdash; est un mécanisme qui vous permet d’allouer les performances de rendu/la puissance à des vitesses qui varient d’un rendu à l’autre.

Dans certains cas, le taux d’ombrage peut être réduit avec peu ou pas de réduction de qualité de sortie perceptible. conduisant à une amélioration des performances qui est essentiellement gratuite.

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>Sans l' &mdash; anticrénelage à plusieurs échantillons VRS avec superéchantillonnage
Sans ombrage à taux variable, le seul moyen de contrôler le taux d’ombrage est d’utiliser l’anticrénelage à plusieurs échantillons (MSAA) avec une exécution basée sur des échantillons (également appelée superéchantillonnage).

MSAA est un mécanisme permettant de réduire les alias géométriques et d’améliorer la qualité de rendu d’une image par rapport à l’utilisation de MSAA. Le nombre d’échantillons MSAA, qui peut être 1x, 2x, 4x, 8x ou 16x, régit le nombre d’échantillons alloués par pixel cible de rendu. Le nombre d’échantillons MSAA doit être connu à l’avance lorsque la cible est allouée et ne peut pas être modifiée par la suite.

Superéchantillonner fait en sorte que le nuanceur de pixels soit appelé une fois par échantillon, avec une qualité supérieure, mais aussi un coût de performance supérieur par rapport à l’exécution par pixel.

Votre application peut contrôler sa fréquence d’ombrage en choisissant l’une des exécutions par pixel ou MSAA-with-superéchantillonnage. Ces deux options ne fournissent pas un contrôle très précis. En outre, vous pouvez avoir besoin d’un taux d’ombrage inférieur pour une certaine classe d’objets par rapport au reste de l’image. Ces objets peuvent inclure un objet derrière un élément HUD ou une transparence, un flou (profondeur de champ, mouvement, etc.) ou une distorsion optique en raison des fibres optiques VR. Mais cela ne serait pas possible, car la qualité et les coûts d’ombrage sont fixés sur l’ensemble de l’image.

## <a name="with-variable-rate-shading-vrs"></a>Avec ombrage à taux variable (VRS)
Le modèle VRS (variable-rate Shading) étend l’échantillonnage-avec-MSAA dans le sens inverse « grossiste », en ajoutant le concept d’ombrage grossier. C’est là que l’ombrage peut être effectué à une fréquence plus grossière qu’un pixel. En d’autres termes, un groupe de pixels peut être grisé comme une unité unique, et le résultat est ensuite diffusé à tous les échantillons du groupe.

Une API d’ombrage grossiste permet à votre application de spécifier le nombre de pixels qui appartiennent à un groupe ombré, ou un *Pixel grossier*. Vous pouvez modifier la taille de pixel grossiste une fois que vous avez alloué la cible de rendu. Par conséquent, différentes parties de l’écran ou différentes passes de dessin peuvent avoir différents taux d’ombrage.

Voici un tableau décrivant le niveau MSAA pris en charge avec lequel la taille de pixel grossiste est prise en charge. Certains ne sont pas pris en charge sur les plateformes ; tandis que d’autres sont activés conditionnellement en fonction d’une capacité (*AdditionalShadingRatesSupported*), indiquée par « Cap ».

![Le tableau indique la taille de pixel grossière pour les niveaux M a a.](images/CoarsePixelSizeSupport.PNG "Tailles de pixels grossistes")

Pour les niveaux de fonctionnalité décrits dans la section suivante, il n’y a pas de combinaison de nombre de pixels grossistes-and-Sample-Count où le matériel doit suivre plus de 16 échantillons par appel de nuanceur de pixels. Ces combinaisons sont grisées dans le tableau ci-dessus.

## <a name="feature-tiers"></a>Niveaux de fonctionnalité
Il existe deux niveaux pour l’implémentation de VRS, et deux fonctionnalités que vous pouvez interroger. Chaque niveau est décrit plus en détail après la table.

![Le tableau ci-dessous présente les fonctionnalités disponibles dans les niveaux 1 et 2.](images/Tiers.PNG "Niveaux VRS")

### <a name="tier-1"></a>Niveau 1
- Le taux d’ombrage ne peut être spécifié que sur une base par dessin ; plus granulaire que cela.
- Le taux d’ombrage s’applique uniformément à ce qui est dessiné indépendamment de l’endroit où il se trouve dans la cible de rendu.

### <a name="tier-2"></a>Niveau 2
- Le taux d’ombrage peut être spécifié par dessin, comme dans le niveau 1. Elle peut également être spécifiée par une combinaison de base par dessin, et de :
  - Sémantique de chaque vertex provoquant et
  - image de l’espace à l’écran.
- Les taux d’ombrage des trois sources sont combinés à l’aide d’un ensemble de combinateurs.
- La taille de la vignette d’image de l’espace de l’écran est de 16 x 16 ou moins.
- Le taux d’ombrage demandé par votre application est garanti être remis exactement (pour des précisions temporelles et autres filtres de reconstruction).
- SV_ShadingRate entrée PS est prise en charge.
- Le taux d’ombrage par interprovoquament (également connu sous le nom de primitive) est valide lorsqu’une fenêtre d’affichage est utilisée et `SV_ViewportArrayIndex` n’est pas écrite dans.
- Le taux de vertex pouvant être utilisé peut être utilisé avec plusieurs Viewports si la capacité de *SupportsPerVertexShadingRateWithMultipleViewports* est définie sur `true` . En outre, dans ce cas, ce taux peut être utilisé lors `SV_ViewportArrayIndex` de l’écriture dans.

### <a name="list-of-capabilities"></a>Liste de fonctionnalités
- *AdditionalShadingRatesSupported*
  - Type booléen.
  - Indique si les tailles de pixels grossistes, 4x2 et 4x4 sont prises en charge pour le rendu à échantillonnage unique. et si la taille de pixel grossiste 2x4 est prise en charge pour le format MSAA 2x.
- *SupportsPerVertexShadingRateWithMultipleViewports*
  - Type booléen.
  - Indique si plusieurs Viewports peuvent être utilisés avec le taux d’ombrage par vertex (également connu sous le nom de primitive).

## <a name="specifying-shading-rate"></a>Spécification du taux d’ombrage
Pour plus de flexibilité dans les applications, il existe un large éventail de mécanismes permettant de contrôler le taux d’ombrage. Différents mécanismes sont disponibles en fonction du niveau de fonctionnalité matérielle.

### <a name="command-list"></a>Liste des commandes
Il s’agit du mécanisme le plus simple pour définir le taux d’ombrage. Elle est disponible sur tous les niveaux.

Votre application peut spécifier une taille de pixel grossière à l’aide de la [méthode **ID3D12GraphicsCommandList5 :: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate). Cette API accepte un seul argument Enum. L’API fournit un contrôle global du niveau de qualité pour le rendu de &mdash; la capacité à définir le taux d’ombrage pour chaque dessin.

Les valeurs de cet État sont exprimées à l’aide de l’énumération [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) .

#### <a name="coarse-pixel-size-support"></a>Prise en charge des tailles de pixel grossistes
Les taux d’ombrage 1x1, 1x2, 2x2 et 2x2 sont pris en charge sur tous les niveaux.

Il existe une fonctionnalité, *AdditionalShadingRatesSupported*, qui indique si 2x4, 4x2 et 4x4 sont pris en charge sur l’appareil.

### <a name="screen-space-image-image-based"></a>Image de l’espace à l’écran (basée sur une image)
Au niveau 2 et supérieur, vous pouvez spécifier le taux d’ombrage du pixel avec une image d’espace écran.

L’image d’espace écran permet à votre application de créer une image de « masque de niveau de détail (LOD) » indiquant les zones de qualité variable, telles que les zones qui seront couvertes par le flou de mouvement, le flou de champ de profondeur, les objets transparents ou les éléments d’interface HUD. La résolution de l’image se trouve dans blocs macros ; elle n’est pas dans la résolution de la cible de rendu. En d’autres termes, les données de taux d’ombrage sont spécifiées au niveau de granularité des vignettes de x x 16 ou 16x16 pixels, comme indiqué par la taille de la vignette VRS.

#### <a name="tile-size"></a>Taille de la vignette
Votre application peut interroger une API pour récupérer la taille de vignette VRS prise en charge pour son appareil.

Les vignettes sont carrées et la taille fait référence à la largeur ou à la hauteur de la vignette dans les texels.

Si le matériel ne prend pas en charge l’ombrage à taux variable de niveau 2, la requête de capacité pour la taille de la vignette retourne 0.

Si *le matériel prend* en charge l’ombrage à taux variable de niveau 2, la taille de la vignette est l’une de ces valeurs.

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>Taille de l’image de l’espace à l’écran
Pour une cible de rendu de taille {rtWidth, rtHeight}, à l’aide d’une taille de mosaïque donnée nommée **VRSTileSize**, l’image d’espace écran qui la couvre est de ces dimensions.

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

L’angle supérieur gauche de l’image de l’espace écran (0, 0) est verrouillé sur l’angle supérieur gauche de la cible de rendu (0,0).

Pour rechercher la coordonnée (x, y) d’une vignette qui correspond à un emplacement particulier dans la cible de rendu, divisez les coordonnées de l’espace de la fenêtre (x, y) par la taille de la vignette, en ignorant les bits fractionnaires.

Si l’image d’espace écran est plus grande qu’elle ne doit l’être pour une cible de rendu donnée, les portions supplémentaires à droite et/ou en bas ne sont pas utilisées.

Si l’image d’espace écran est trop petite pour une cible de rendu donnée, toute tentative de lecture à partir de l’image au-delà de ses étendues réelles donne un taux d’ombrage par défaut de 1x1. Cela est dû au fait que l’image de l’espace à l’écran en haut à gauche (0,0) est verrouillée dans le coin supérieur gauche de la cible de rendu (0, 0) et que la lecture au-delà des étendues de cible de rendu signifie que la lecture est trop importante pour les valeurs x et y.

#### <a name="format-layout-resource-properties"></a>Format, disposition, propriétés de la ressource
Le format de cette surface est une surface 8 bits sur un seul canal ([**DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

La ressource est dimension **TEXTURE2D**.

Elle ne peut pas être de tableau ou de mipped. Elle doit avoir un niveau MIP de manière explicite.

Il a un échantillon Count 1 et un échantillon de la qualité 0.

La disposition de la texture est **inconnue**. Il ne peut pas être implicitement une mise en page de ligne principale, car Cross-adapter n’est pas autorisé.

La façon dont les données de l’image de l’espace de l’écran est remplie est l’une ou l’autre
1. Écrire les données à l’aide d’un nuanceur de calcul ; l’image de l’espace écran est liée en tant que UAV, ou
2. Copiez les données dans l’image d’espace écran.

Lorsque vous créez l’image d’espace d’écran, ces indicateurs sont autorisés.

- Aucune
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

Ces indicateurs ne sont pas autorisés.

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

Le type de tas de la ressource ne peut pas être UPLOAD ni READBACK.

La ressource ne peut pas être SIMULTANEOUS_ACCESS. La ressource ne peut pas être multicarte.

#### <a name="data"></a>Données
Chaque octet de l’image d’espace écran correspond à une valeur de l’énumération [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)  .

#### <a name="resource-state"></a>État de la ressource
Une ressource doit être migrée en état lecture seule lorsqu’elle est utilisée comme image d’espace écran. Un État en lecture seule, [**D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states), est défini à cet effet.

La ressource d’image est en dehors de cet État pour être réécrite.

#### <a name="setting-the-image"></a>Définition de l’image
L’image d’espace à l’écran pour spécifier la fréquence de nuanceur est définie dans la liste de commandes.

Une ressource qui a été définie comme source de taux d’ombrage ne peut pas être lue ou écrite à partir de l’une des étapes du nuanceur.

Une `null` image d’espace écran peut être définie pour spécifier la fréquence de nuanceur. Cela a pour effet d’utiliser de manière cohérente les 1x1 comme contribution de l’image de l’espace écran. L’image de l’espace écran peut initialement être considérée comme étant définie à `null` .

#### <a name="promotion-and-decay"></a>Promotion et atténuation
Une ressource d’image de l’espace écran n’a aucune incidence spéciale concernant la promotion ou la dischute.

### <a name="per-primitive-attribute"></a>Attribut par primitive
Un attribut par primitive ajoute la possibilité de spécifier un terme de taux d’ombrage comme attribut à partir d’un vertex provoquant un. Cet attribut est à ombrage constant &mdash; , il est propagé à tous les pixels dans le triangle ou la primitive de ligne actuel. L’utilisation d’un attribut par primitive peut permettre un contrôle plus fin de la qualité d’image par rapport aux autres spécificateurs de taux d’ombrage.

L’attribut par primitive est une sémantique définissable nommée `SV_ShadingRate` . `SV_ShadingRate` existe dans le cadre du [modèle de nuanceur HLSL 6,4](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12).

Si un ensemble VS ou GS `SV_ShadingRate` est défini, mais que VRS n’est pas activé, le paramètre sémantique n’a aucun effet. Si aucune valeur `SV_ShadingRate` n’est spécifiée pour par primitive, une valeur de taux d’ombrage de 1x1 est considérée comme la contribution par primitive.

### <a name="combining-shading-rate-factors"></a>Combinaison de facteurs de taux d’ombrage
Les différentes sources de taux d’ombrage sont appliquées en séquence à l’aide de ce diagramme.

![Le diagramme illustre un état de pipeline, étiqueté A, avec un taux d’ombrage de vertex provoquant une vitesse d’ombrage, une étiquette B, appliquée à un combinateur, puis une fréquence d’ombrage basée sur une image, étiquetée B, appliquée à un combinateur.](images/Combiners.PNG "Combinateurs d’ombrage")

Chaque paire de et de B est combinée à l’aide d’un combinateur.

\* Lorsque vous spécifiez une fréquence de nuanceur par attribut de vertex.

- Si un nuanceur Geometry est utilisé, vous pouvez spécifier la fréquence d’ombrage.
- Si un nuanceur Geometry n’est pas utilisé, le taux d’ombrage est spécifié par le vertex provoquant.

#### <a name="list-of-combiners"></a>Liste des combinateurs
Les combinateurs suivants sont pris en charge. Utilisation d’un combinateur (C) et de deux entrées (A et B).

- Mode **passthrough**. C. XY = A. XY.
- **Remplacez**. C. XY = B. XY.
- **Qualité supérieure**. C. XY = min (A. XY, B. XY).
- **Qualité inférieure**. C. XY = Max (A. XY, B. XY).
- **Appliquez le coût B par rapport à un**. C. XY = min (maxRate, A. XY + B. XY).

où `maxRate` est la plus grande dimension autorisée du pixel grossiste sur l’appareil. Il s’agit de

- **D3D12_AXIS_SHADING_RATE_2X** (autrement dit, la valeur 1), si AdditionalShadingRatesSupported est `false` .
- **D3D12_AXIS_SHADING_RATE_4X** (autrement dit, la valeur 2), si AdditionalShadingRatesSupported est `true` .

Le choix de combinateur pour l’ombrage à taux variable est défini dans la liste de commandes via [**ID3D12GraphicsCommandList5 :: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate).

Si aucun combinateur n’est défini, il reste à la valeur par défaut, qui est PASSTHROUGH.

Si la source d’un combinateur est un [**D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate), ce qui n’est pas autorisé dans la table de prise en charge, l’entrée est nettoyée à un taux d' *ombrage pris en* charge.

Si la sortie d’un combinateur ne correspond pas à un taux d’ombrage pris en charge sur la plateforme, le résultat est assaini au taux d’ombrage pris *en charge* .

### <a name="default-state-and-state-clearing"></a>État par défaut et effacement de l’État
Toutes les sources de taux d’ombrage, à savoir

- taux spécifié de l’état du pipeline (spécifié dans la liste de commandes)
- taux spécifié par l’image d’espace écran, et
- attribut par primitive

la valeur par défaut est **D3D12_SHADING_RATE_1X1**. Les combinateurs par défaut sont {PASSTHROUGH, PASSTHROUGH}.

Si aucune image d’espace écran n’est spécifiée, un taux d’ombrage de 1x1 est déduit à partir de cette source.

Si aucun attribut par primitive n’est spécifié, un taux d’ombrage de 1x1 est déduit à partir de cette source.

[ID3D12CommandList :: ClearState](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) rétablit la valeur par défaut du taux spécifié par l’état du pipeline, et la sélection de l’image de l’espace à l’écran à la valeur par défaut « aucune image de l’espace à l’écran ».

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>Interrogation du taux d’ombrage à l’aide de SV_ShadingRate
Il est utile de savoir quel taux d’ombrage a été sélectionné par le matériel à un appel de nuanceur de pixels donné. Cela peut permettre une variété d’optimisations dans votre code PS. Une variable système PS uniquement, `SV_ShadingRate` , fournit des informations sur le taux d’ombrage.

### <a name="type"></a>Type
Le type de cette sémantique est uint.

### <a name="data-interpretation"></a>Interprétation des données
Les données sont interprétées comme une valeur de l’énumération [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) .

### <a name="if-vrs-is-not-being-used"></a>Si VRS n’est pas utilisé
Si l’ombrage des pixels grossistes n’est pas utilisé, `SV_ShadingRate` est lu en tant que valeur de 1x1, ce qui indique des pixels précis.

### <a name="behavior-under-sample-based-execution"></a>Comportement en cas d’exécution basée sur l’exemple
Un nuanceur de pixels échoue la compilation s’il est entré `SV_ShadingRate` et utilise également l’exécution basée sur un échantillon &mdash; , par exemple, en entrant `SV_SampleIndex` ou en utilisant le mot clé d’interpolation Sample.

> ### <a name="remarks-on-deferred-shading"></a>Remarques sur l’ombrage différé
>
> Une application d’ombrage différée peut avoir besoin de savoir quel taux d’ombrage a été utilisé pour la zone de l’écran. Ainsi, les distributions de passe d’éclairage peuvent être lancées à un rythme plus grossier. La `SV_ShadingRate` variable peut être utilisée pour accomplir cette opération si elle est écrite dans le gbuffer.

## <a name="depth-and-stencil"></a>Profondeur et gabarit
Lorsque l’ombrage de pixel grossiste est utilisé, la profondeur et le stencil et la couverture sont toujours calculés et émis à l’exemple de résolution complète.

## <a name="using-the-shading-rate-requested"></a>Utilisation du taux d’ombrage demandé
Pour tous les niveaux, il est prévu que, si un taux d’ombrage est demandé et qu’il soit pris en charge sur la combinaison périphérique-et-MSAA-Level, il s’agit du taux d’ombrage fourni par le matériel.

Un taux d’ombrage demandé signifie un taux d’ombrage calculé en sortie des combinateurs (voir la section combinaison des [facteurs de taux d’ombrage](#combining-shading-rate-factors) dans cette rubrique).

Un taux d’ombrage pris en charge est 1x1, 1x2, 2x1 ou 2x2 dans une opération de rendu où le nombre d’échantillons est inférieur ou égal à quatre. Si la capacité de *AdditionalShadingRatesSupported* est `true` , 2x4, 4x2 et 4x4 sont également pris en charge pour un nombre d’échantillons (voir le tableau de la section [with variable-rate Shading (VRS)](#with-variable-rate-shading-vrs) de cette rubrique).

## <a name="screen-space-derivatives"></a>Dérivés de l’espace à l’écran
Les calculs de dégradés de pixel en pixels adjacents sont affectés par l’ombrage des pixels grossistes. Par exemple, lorsque les pixels épais 2x2 sont utilisés, un dégradé est le double de la taille par rapport au moment où les pixels grossiers ne sont pas utilisés. Votre application peut souhaiter ajuster les nuanceurs pour compenser cela &mdash; ou non, selon les fonctionnalités que vous souhaitez.

Étant donné que les mips sont choisis en fonction d’une dérivée de l’espace à l’écran, l’utilisation de l’ombrage de pixel grossiste affecte la sélection MIP. L’utilisation de l’ombrage des pixels grossistes permet de sélectionner des mips moins détaillés par rapport au moment où les pixels grossiers ne sont pas utilisés.

## <a name="attribute-interpolation"></a>Interpolation d’attribut
Les entrées d’un nuanceur de pixels peuvent être interpolées en fonction de leurs vertex sources. Étant donné que l’ombrage à taux variable affecte les zones de la cible écrites par chaque appel du nuanceur de pixels, il interagit avec l’interpolation d’attribut. Les trois types d’interpolation sont Center, centre de gravité et exemple.

### <a name="center"></a>Center
L’emplacement de l’interpolation centrale pour un pixel grossiste est le centre géométrique de la zone de pixels grossière complète. `SV_Position` est toujours interpolé au centre de la région de pixel grossiste.

### <a name="centroid"></a>Centroïde
Lorsque l’ombrage de pixel grossiste est utilisé avec MSAA, pour chaque pixel, il y aura toujours des écritures sur le nombre complet d’échantillons alloués pour le niveau MSAA de la cible. Ainsi, l’emplacement de l’interpolation de centre de gravité des échantillons considère tous les échantillons comme des pixels fins dans les pixels grossiers. Cela dit, l’emplacement de l’interpolation de centre de gravité est défini en tant que premier exemple couvert, dans l’ordre de plus en plus important de l’exemple d’index. La couverture effective de l’exemple est et-Ed avec le bit correspondant de l’état de rastériseur SampleMask.

> [!NOTE]
> Lorsque l’ombrage de pixel grossiste est utilisé sur le niveau 1, SampleMask est toujours un masque complet. Si SampleMask est configuré pour ne pas être un masque complet, l’ombrage des pixels grossistes est désactivé sur le niveau 1.

### <a name="sample-based-execution"></a>Exécution basée sur un échantillon
L’exécution basée sur un échantillon, ou l’analyse *superéchantillonnage* &mdash; provoquée par l’utilisation de l’exemple de fonctionnalité d’interpolation &mdash; , peut être utilisée avec un ombrage de pixels grossier, et entraîne l’appel de nuanceur de pixels par échantillon. Pour les cibles du nombre d’échantillons N, le nuanceur de pixels est appelé N fois par pixel fin.

### <a name="evaluateattributesnapped"></a>EvaluateAttributeSnapped
Les intrinsèques de modèle d’extraction ne sont pas compatibles avec l’ombrage de pixel grossiste sur le niveau 1. Si vous tentez d’utiliser des intrinsèques de modèle d’extraction avec un ombrage de pixel grossiste sur le niveau 1, l’ombrage de pixel grossiste est automatiquement désactivé.

L’intrinsèque `EvaluateAttributeSnapped` est autorisé à être utilisé avec un ombrage de pixel grossiste sur le niveau 2. Sa syntaxe est la même que celle qui a toujours été.

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

Pour Context, `EvaluateAttributeSnapped` a un paramètre offset avec deux champs. Lorsqu’il est utilisé sans ombrage de pixels grossier, seuls les quatre bits de poids faible de l’ensemble des 32 sont utilisés. Ces quatre bits représentent la plage [-8, 7]. Cette plage s’étend sur une grille 16x16 au sein d’un pixel. La plage est telle que les bords supérieur et gauche du pixel sont inclus, et les bords inférieur et droit ne le sont pas. Offset (-8,-8) se trouve dans l’angle supérieur gauche et le décalage (7) est par rapport à l’angle inférieur droit. Offset (0, 0) est le centre du pixel.

Lorsqu’il est utilisé avec l’ombrage de pixels grossier, `EvaluateAttributeSnapped` le paramètre offset de est en capacité de spécifier une plage plus large d’emplacements. Le paramètre offset sélectionne une grille 16x16 pour chaque pixel fin, et il y a plusieurs pixels fins. La plage exprimable et le nombre de bits à utiliser dépendent de la taille de pixel grossiste. Les bords supérieur et gauche du pixel grossier sont inclus, et les bords inférieur et droit ne le sont pas.

Le tableau ci-dessous décrit l’interprétation du `EvaluateAttributeSnapped` paramètre offset de chaque taille de pixel grossiste.

#### <a name="evaluateattributesnappeds-offset-range"></a>Plage de décalage de EvaluateAttributeSnapped

|Taille de pixel grossiste  |Plage indexable             |Taille de la plage représentable  |Nombre de bits nécessaires {x, y}  |Masque binaire des bits utilisables          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (fin)         |{ \[ -8, 7 \] , \[ -8, 7 \] }      |{16, 16}                  |{4, 4}                        |{000000000000xxxx, 000000000000xxxx}|    
|1x2                |{ \[ -8, 7 \] , \[ -16, 15 \] }    |{16, 32}                  |{4,5}                        |{000000000000xxxx, 00000000000xxxxx}|    
|2 x 1                |{ \[ -16, 15 \] , \[ -8, 7 \] }    |{32, 16}                  |{5, 4}                        |{00000000000xxxxx, 000000000000xxxx}|    
|2x2                |{ \[ -16, 15 \] , \[ -16, 15 \] }  |{32, 32}                  |{5, 5}                        |{00000000000xxxxx, 00000000000xxxxx}|    
|4                |{ \[ -16, 15 \] , \[ -32, 31 \] }  |{32, 64}                  |{5, 6}                        |{00000000000xxxxx, 0000000000xxxxxx}|    
|4x2                |{ \[ -32, 31 \] , \[ -16, 15 \] }  |{64, 32}                  |{6, 5}                        |{0000000000xxxxxx, 00000000000xxxxx}|    
|4x4                |{ \[ -32, 31 \] , \[ -32, 31 \] }  |{64, 64}                  |{6, 6}                        |{0000000000xxxxxx, 0000000000xxxxxx}|   

Les tableaux ci-dessous sont un guide pour la conversion de à partir de la représentation à virgule fixe en décimal et fractionnaire. Le premier bit utilisable dans le masque binaire est le bit de signe, tandis que le reste du masque binaire comprend la partie numérique.

Le modèle de nombre pour les valeurs de quatre bits transmises à `EvaluateAttributeSnapped` n’est pas spécifique à l’ombrage à taux variable. Elle est réitérée ici à des fins d’exhaustivité.

Pour les valeurs de quatre bits.

| Valeur binaire | Decimal  | Fraction |
|-------------:|---------:|-----------:|
|         1 000 |-0,5 f     |-8/16     |
|         1001 |-0.4375 f  |-7/16|    |
|         1010 |-0.375 f   |-6/16|    |
|         1010 |-0.3125 f  |-5/16     |
|         1100 |-0,25 f    |-4/16     |
|         1101 |-0.1875 f  |-3/16     |
|         1110 |-0,125 f   |-2/16     |
|         1111 |-0.0625 f  |-1/16      |
|         0000 |0.0f      |0 / 16      |
|         0,001 |-0.0625 f  |1 / 16      |
|         0010 |-0,125 f   |2 / 16      |
|         0011 |-0.1875 f  |3 / 16      |
|         0100 |-0,25 f    |4 / 16      |
|         0101 |-0.3125 f  |5 / 16      |
|         0110 |-0.375 f   |6 / 16      |
|         0111 |-0.4375 f  |7 / 16      |

Pour les valeurs de cinq bits.

| Valeur binaire | Decimal  | Fraction |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16/16    |
|        10001 |-0,9375   |-15/16    |
|        10010 |-0,875    |-14/16    |
|        10011 |-0,8125   |-13/16    |
|        10100 |-0.75     |-12/16    |
|        10101 |-0,6875   |-11/16    |
|        10110 |-0,625    |-10/16    |
|        10111 |-0,5625   |-9/16     |
|        11000 |-0,5      |-8/16     |
|        11001 |-0,4375   |-7/16     |
|        11010 |-0,375    |-6/16     |
|        11011 |-0,3125   |-5/16     |
|        11100 |-0.25     |-4/16     |
|        11101 |-0,1875   |-3/16     |
|        11110 |-0,125    |-2/16     |
|        11111 |-0,0625   |-1/16     |
|        00000 |0         |0 / 16      |
|        00001 |0,0625    |1 / 16      |
|        00010 |0,125     |2 / 16      |
|        00011 |0,1875    |3 / 16      |
|        00100 |0,25      |4 / 16      |
|        00101 |0,3125    |5 / 16      |
|        00110 |0,375     |6 / 16      |
|        00111 |0,4375    |7 / 16      |
|        01000 |0,5       |8 / 16      |
|        01001 |0,5625    |9 / 16      |
|        01010 |0,625     |10 / 16     |
|        01011 |0,6875    |11 / 16     |
|        01100 |0,75      |12 / 16     |
|        01101 |0,8125    |13 / 16     |
|        01110 |0,875     |14 / 16     |
|        01111 |0,9375    |15 / 16     |

Pour les valeurs de six bits.

| Valeur binaire | Decimal  | Fraction |
|-------------:|---------:|-----------:|
|       100000 |-2        |-32/16    |
|       100001 |-1,9375   |-31/16    |
|       100010 |-1,875    |-30/16    |
|       100011 |-1,8125   |-29/16    |
|       100100 |-1,75     |-28/16    |
|       100101 |-1,6875   |-27/16    |
|       100110 |-1,625    |-26/16    |
|       100111 |-1,5625   |-25/16    |
|       101000 |-1,5      |-24/16    |
|       101001 |-1,4375   |-23/16    |
|       101010 |-1,375    |-22/16    |
|       101011 |-1,3125   |-21/16    |
|       101100 |-1.25     |-20/16    |
|       101101 |-1,1875   |-19/16    |
|       101110 |-1,125    |-18/16    |
|       101111 |-1,0625   |-17/16    |
|       110000 |-1        |-16/16    |
|       110001 |-0,9375   |-15/16    |
|       110010 |-0,875    |-14/16    |
|       110011 |-0,8125   |-13/16    |
|       110100 |-0.75     |-12/16    |
|       110101 |-0,6875   |-11/16    |
|       110110 |-0,625    |-10/16    |
|       110111 |-0,5625   |-9/16     |
|       111000 |-0,5      |-8/16     |
|       111001 |-0,4375   |-7/16     |
|       111010 |-0,375    |-6/16     |
|       111011 |-0,3125   |-5/16     |
|       111100 |-0.25     |-4/16     |
|       111101 |-0,1875   |-3/16     |
|       111110 |-0,125    |-2/16     |
|       111111 |-0,0625   |-1/16     |
|       000000 |0         |0 / 16      |
|       000001 |0,0625    |1 / 16      |
|       000010 |0,125     |2 / 16      |
|       000011 |0,1875    |3 / 16      |
|       000100 |0,25      |4 / 16      |
|       000101 |0,3125    |5 / 16      |
|       000110 |0,375     |6 / 16      |
|       000111 |0,4375    |7 / 16      |
|       001000 |0,5       |8 / 16      |
|       001001 |0,5625    |9 / 16      |
|       001010 |0,625     |10 / 16     |
|       001011 |0,6875    |11 / 16     |
|       001100 |0,75      |12 / 16     |
|       001101 |0,8125    |13 / 16     |
|       001110 |0,875     |14 / 16     |
|       001111 |0,9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1,0625    |17 / 16     |
|       010010 |1,125     |18 / 16     |
|       010011 |1,1875    |19 / 16     |
|       010100 |1,25      |20 / 16     |
|       010101 |1,3125    |21 / 16     |
|       010110 |1,375     |22 / 16     |
|       010111 |1,4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1,5625    |25 / 16     |
|       011010 |1,625     |26 / 16     |
|       011011 |1,6875    |27 / 16     |
|       011100 |1,75      |28 / 16     |
|       011101 |1,8125    |29 / 16     |
|       011110 |1,875     |30 / 16     |
|       011111 |1,9375    |31 / 16     |

De la même manière qu’avec les pixels précis, la `EvaluateAttributeSnapped` grille d’emplacements évaluables est centrée sur le centre de pixels grossier lors de l’utilisation d’un ombrage de pixels grossier.

## <a name="setsamplepositions"></a>SetSamplePositions
Lorsque l’API [**ID3D12GraphicsCommandList1 :: SetSamplePositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) est utilisée avec un ombrage grossier, l’API définit les positions d’échantillonnage pour les pixels fins.

## <a name="sv_coverage"></a>SV_Coverage
Si `SV_Coverage` est déclaré en tant qu’entrée ou sortie de nuanceur sur le niveau 1, l’ombrage de pixel grossier est désactivé.

Vous pouvez utiliser la `SV_Coverage` sémantique avec l’ombrage des pixels grossistes sur le niveau 2 et refléter les exemples d’une cible MSAA en cours d’écriture.

Lorsque l’ombrage de pixel grossier est utilisé, ce qui permet &mdash; à plusieurs pixels de la source de &mdash; compresser une vignette, le masque de couverture représente tous les échantillons provenant de cette vignette.

En raison de la compatibilité de l’ombrage des pixels grossistes avec MSAA, le nombre de bits de couverture requis pour la spécification peut varier. Par exemple, avec une ressource MSAA 4x utilisant [**D3D12_SHADING_RATE_2x2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate), chaque pixel grossier écrit sur quatre pixels fins et chaque pixel fine a quatre échantillons. Cela signifie que chaque pixel grossier écrit jusqu’à un total de 4 * 4 = 16 échantillons.

### <a name="number-of-coverage-bits-needed"></a>Nombre de bits de couverture nécessaires
Le tableau suivant indique le nombre de bits de couverture requis pour chaque combinaison de taille de pixel grossiste et de niveau MSAA.

![Le tableau indique la taille de pixel grossiste, le nombre de pixels de fin et les niveaux M a.](images/NumberOfCoverageBits.PNG "Bits de couverture")

Comme indiqué dans le tableau, il n’est pas possible d’utiliser des pixels grossiers pour écrire dans plus de 16 échantillons à la fois à l’aide de la fonctionnalité d’ombrage à taux variable exposée par Direct3D 12. Cette restriction est due aux contraintes de Direct3D 12 concernant les niveaux MSAA autorisés avec lesquels la taille de pixel grossiste (voir le tableau dans la section [with variable rate Shading (VRS)](#with-variable-rate-shading-vrs) de cette rubrique).

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>Classement et format des bits dans le masque de couverture
Les bits du masque de couverture adhèrent à un ordre bien défini. Le masque est constitué de couvertures des pixels de gauche à droite, puis de haut en bas (colonne principale). Les bits de couverture sont les bits de poids faible de la sémantique de couverture et sont regroupés de façon dense.

Le tableau ci-dessous montre le format de masque de couverture pour les combinaisons prises en charge de taille de pixel grossiste et de niveau MSAA.

![Le tableau montre la taille de pixel grossiste, le diagramme de pixels grossistes et 1 x M S a une couverture.](images/Coverage1x.PNG "Couverture à 1x")

Le tableau suivant illustre 2x pixels MSAA, où chaque pixel a deux échantillons d’index 0 et 1.

Le positionnement des étiquettes des échantillons sur les pixels est à titre indicatif et ne transmettent pas nécessairement les emplacements d’échantillons spatiaux {X, Y} sur ce pixel ; en particulier, étant donné que les positions d’échantillon peuvent être modifiées par programmation. Les exemples sont référencés par leur index de base 0.

![Le tableau indique la taille de pixel grossiste, le diagramme de pixels grossistes et 2 x M S a une couverture.](images/Coverage2x.PNG "Couverture à 2x")

Le tableau suivant montre 4 pixels MSAA, où chaque pixel a quatre échantillons d’index 0, 1, 2 et 3.

![Le tableau montre la taille de pixel grossiste, le diagramme de pixels grossistes et 4 x M S a une couverture.](images/Coverage4x.PNG "Couverture à 4x")

## <a name="discard"></a>Abandonner
Lorsque la sémantique HLSL `discard` est utilisée avec l’ombrage de pixels grossier, les pixels grossiers sont ignorés.

## <a name="target-independent-rasterization-tir"></a>Pixellisation indépendante de la cible (TIR)
Le TIR n’est pas pris en charge lorsque l’ombrage de pixel grossiste est utilisé.

## <a name="raster-order-views-rovs"></a>Vues d’ordre de trame (ROVs)
Les interblocages ROV sont spécifiés comme fonctionnant avec une granularité fine des pixels. Si l’ombrage est effectué par échantillon, les interverrouillages fonctionnent au niveau de granularité de l’échantillon.

## <a name="conservative-rasterization"></a>Pixellisation conservatrice
Vous pouvez utiliser la pixellisation conservatrice avec l’ombrage à taux variable. Lorsque la pixellisation conservatrice est utilisée avec l’ombrage de pixels grossiste, les pixels précis dans les pixels grossiers sont pixellisés de façon restrictive en se assurant d’une couverture complète.

### <a name="coverage"></a>Couverture
Lorsque la pixellisation conservatrice est utilisée, la sémantique de couverture contient des masques complets pour les pixels fins couverts, et 0 pour les pixels fins qui ne sont pas couverts.

## <a name="bundles"></a>Offres groupées
Vous pouvez appeler des API d’ombrage à taux variable sur un bundle.

## <a name="render-passes"></a>Passes de rendu
Vous pouvez appeler des API d’ombrage à taux variable dans une [passe de rendu](/windows/desktop/direct3d12/direct3d-12-render-passes).

## <a name="calling-the-vrs-apis"></a>Appel des API VRS
La section suivante décrit la manière dont l’ombrage à taux variable est accessible à votre application par le biais de Direct3D 12.

### <a name="capability-querying"></a>Interrogation des fonctionnalités

Pour rechercher la capacité d’ombrage à débit variable de l’adaptateur, appelez [**ID3D12Device :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) avec [**D3D12_FEATURE ::D 3D12_FEATURE_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)et fournissez une [structure **D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) pour que la fonction soit renseignée pour vous. La structure **D3D12_FEATURE_DATA_D3D12_OPTIONS6** contient plusieurs membres, dont ceux qui sont de type énuméré [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6 :: VariableShadingRateTier) et un qui indique si le traitement en arrière-plan est pris en charge (D3D12_FEATURE_DATA_D3D12_OPTIONS6 :: BackgroundProcessingSupported).

Pour interroger la fonctionnalité de niveau 1, par exemple, vous pouvez effectuer cette opération.

```cpp
D3D12_FEATURE_DATA_D3D12_OPTIONS6 options;
return 
    SUCCEEDED(m_device->CheckFeatureSupport(
        D3D12_FEATURE_D3D12_OPTIONS6, 
        &options, 
        sizeof(options))) && 
    options.ShadingRateTier == D3D12_VARIABLE_SHADING_RATE_TIER_1;
```

### <a name="shading-rates"></a>Taux d’ombrage

Les valeurs de l' [énumération **D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) sont organisées afin que les taux d’ombrage soient facilement décomposables en deux axes, où les valeurs de chaque axe sont représentées de manière compacte dans l’espace logarithmique en fonction de l' [énumération **D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate).

Vous pouvez créer une macro pour composer deux taux d’ombrage d’axe en un taux d’ombrage comme celui-ci.

```cpp
#define D3D12_MAKE_COARSE_SHADING_RATE(x,y) ((x) << 2 | (y))
D3D12_MAKE_COARSE_SHADING_RATE(
    D3D12_AXIS_SHADING_RATE_2X, 
    D3D12_AXIS_SHADING_RATE_1X)
```

La plateforme fournit également ces macros, définies dans `d3d12.h` .

```cpp
#define D3D12_GET_COARSE_SHADING_RATE_X_AXIS(x) ((x) >> 2 )
#define D3D12_GET_COARSE_SHADING_RATE_Y_AXIS(y) ((y) & 3 )
```

Ils peuvent être utilisés pour étudier en détail et comprendre `SV_ShaderRate` .

> [!NOTE]
> Cette interprétation des données est destinée à décrire l’image d’espace écran, qui peut être manipulée par les nuanceurs. Ce sujet est abordé plus en détail dans les sections ci-dessus. Mais il n’y a aucune raison de ne pas avoir une définition cohérente des tailles de pixel grossistes à utiliser partout, notamment lors de la définition de la fréquence d’ombrage au niveau de la commande.

### <a name="setting-command-level-shading-rate-and-combiners"></a>Définition de la fréquence d’ombrage et des combinateurs au niveau de la commande
Le taux d’ombrage et, éventuellement, les combinateurs, sont spécifiés par le biais de la méthode [**ID3D12GraphicsCommandList5 :: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) . Vous transmettez une valeur de [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) pour le taux d’ombrage de base et un tableau facultatif de valeurs de [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) .

### <a name="preparing-the-screen-space-image"></a>Préparation de l’image de l’espace à l’écran
L’état de la ressource en lecture seule désignant une image de taux d’ombrage utilisable est défini comme [D3D12_RESOURCE_STATES ::D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### <a name="setting-the-screen-space-image"></a>Définition de l’image de l’espace à l’écran
Vous spécifiez l’image de l’espace à l’écran par le biais de la méthode [**ID3D12GraphicsCommandList5 :: RSSetShadingRateImage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage) .

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>Interrogation de la taille de la vignette
Vous pouvez interroger la taille de la vignette à partir du membre [**D3D12_FEATURE_DATA_D3D12_OPTIONS6 :: ShadingRateImageTileSize**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) . Consultez [fonctionnalité d’interrogation des fonctionnalités](#capability-querying) ci-dessus.

Une dimension est récupérée, puisque les dimensions horizontales et verticales sont toujours les mêmes. Si la capacité du système est [**D3D12_SHADING_RATE_TIER_NOT_SUPPORTED**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier), la taille de la vignette retournée est 0.
