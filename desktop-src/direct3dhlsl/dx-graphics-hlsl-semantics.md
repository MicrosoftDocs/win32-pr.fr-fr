---
title: Sémantique
description: Une sémantique est une chaîne attachée à une entrée ou une sortie de nuanceur qui transmet des informations sur l’utilisation prévue d’un paramètre.
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- Binormal, sémantique (DirectX HLSL)
- BLENDINDICES, sémantique (DirectX HLSL)
- BLENDWEIGHT, sémantique (DirectX HLSL)
- COULEUR, sémantique (DirectX HLSL)
- BROUILLARD, sémantique (DirectX HLSL)
- POSITIONt, sémantique (DirectX HLSL)
- PSIZE, sémantique (DirectX HLSL)
- TANGENTe, sémantique (DirectX HLSL)
- TESSFACTOR, sémantique (DirectX HLSL)
- TEXCOORD, sémantique (DirectX HLSL)
- VFACE, sémantique (DirectX HLSL)
- VPOS, sémantique (DirectX HLSL)
- Sémantique de System-Value
- Sémantique des valeurs système
- ClipDistance, sémantique (DirectX HLSL)
- Couverture, sémantique (DirectX HLSL)
- CullDistance, sémantique (DirectX HLSL)
- Profondeur, sémantique (DirectX HLSL)
- InstanceID, sémantique (DirectX HLSL)
- IsFrontFace, sémantique (DirectX HLSL)
- Position, sémantique (DirectX HLSL)
- PrimitiveID, sémantique (DirectX HLSL)
- RenderTargetArrayIndex, sémantique (DirectX HLSL)
- Cible, sémantique (DirectX HLSL)
- SampleIndex, sémantique (DirectX HLSL)
- VertexID, sémantique (DirectX HLSL)
- ViewportArrayIndex, sémantique (DirectX HLSL)
- SV_ClipDistance, sémantique (DirectX HLSL)
- SV_CullDistance, sémantique (DirectX HLSL)
- SV_Depth, sémantique (DirectX HLSL)
- SV_DepthGreaterEqual, sémantique (DirectX HLSL)
- SV_DepthLessEqual, sémantique (DirectX HLSL)
- SV_IsFrontFace, sémantique (DirectX HLSL)
- SV_Position, sémantique (DirectX HLSL)
- SV_RenderTargetArrayIndex, sémantique (DirectX HLSL)
- SV_Target, sémantique (DirectX HLSL)
- SV_ViewportArrayIndex, sémantique (DirectX HLSL)
- SV_InstanceID, sémantique (DirectX HLSL)
- SV_PrimitiveID, sémantique (DirectX HLSL)
- SV_VertexID, sémantique (DirectX HLSL)
- SV_Coverage, sémantique (DirectX HLSL)
- SV_SampleIndex, sémantique (DirectX HLSL)
- SV_InnerCoverage, semanitcs (DirectX HLSL)
- SV_StencilRef, sémantique (DirectX HLSL)
- SV_GroupID, sémantique (DirectX HLSL)
- SV_GroupThreadID, sémantique (DirectX HLSL)
- Sémantique de SV_DispatchThreadID (DirectX HLSL)
- SV_GroupIndex, sémantique (DirectX HLSL)
- SV_OutputControlPointID, sémantique (DirectX HLSL)
- SV_TessFactor, sémantique (DirectX HLSL)
- SV_InsideTessFactor, sémantique (DirectX HLSL)
- SV_DomainLocation, sémantique (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8979b4e4842a4c84317b456802ed8f1beefea35
ms.sourcegitcommit: 1d3c59a7066a75facc0565027251cad1ca1dd9c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2021
ms.locfileid: "107594164"
---
# <a name="semantics"></a>Sémantique

Une sémantique est une chaîne attachée à une entrée ou une sortie de nuanceur qui transmet des informations sur l’utilisation prévue d’un paramètre. La sémantique est obligatoire sur toutes les variables transmises entre les étapes du nuanceur. La syntaxe permettant d’ajouter une sémantique à une variable de nuanceur est présentée ici ([syntaxe de variable (DirectX HLSL)](dx-graphics-hlsl-variable-syntax.md)).

En général, les données transmises entre les étapes de canalisation sont entièrement génériques et ne sont pas interprétées de façon unique par le système ; les sémantiques arbitraires sont autorisées, ce qui n’a aucune signification particulière. Les paramètres (dans Direct3D 10 et versions ultérieures) qui contiennent ces sémantiques spéciales sont appelés [sémantiques de valeur système](#system-value-semantics).

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>Sémantique prise en charge dans Direct3D 9 et Direct3D 10 et versions ultérieures

Les types de sémantiques suivants sont pris en charge dans Direct3D 9 et Direct3D 10 et versions ultérieures.

- [Sémantique du nuanceur de sommets](#vertex-shader-semantics)
- [Sémantique de nuanceur de pixels](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>Sémantique du nuanceur de sommets

Cette sémantique a un sens lorsqu’elle est attachée à un paramètre de nuanceur de sommets. Ces sémantiques sont prises en charge dans Direct3D 9 et Direct3D 10 et versions ultérieures.

| Entrée | Description | Type |
|-|-|-|
| N-NORMAL \[ n\] | Binormal | float4 |
| BLENDINDICES \[ n\] | Index de fusion | uint |
| BLENDWEIGHT \[ n\] | Masses de fusion | float |
| COULEUR \[ n\] | Couleur diffuse et spéculaire | float4 |
| \[N normal\] | Vecteur normal | float4 |
| POSITION \[ n\] | Position du vertex dans l’espace de l’objet. | float4 |
| POSITION | Position du vertex transformée. | float4 |
| PSIZE \[ n\] | Taille du point | float |
| TANGENT \[ n\] | Tangente | float4 |
| TEXCOORD \[ n\] | Coordonnées de texture | float4 |

| Output | Description | Type |
|-|-|-|
| COULEUR \[ n\] | Couleur diffuse ou spéculaire | float4 |
| VONT | Brouillard du vertex | float |
| POSITION \[ n\] | Position d’un vertex dans un espace homogène. Placez la position dans l’espace à l’écran en divisant (x, y, z) par w. Chaque nuanceur vertex doit écrire un paramètre avec cette sémantique. | float4 |
| PSIZE | Taille du point | float |
| TESSFACTOR \[ n\] | Facteur de pavage | float |

`n` est un entier facultatif compris entre 0 et le nombre de ressources prises en charge. Par exemple, POSITION0, TEXCOORD1, etc.

### <a name="pixel-shader-semantics"></a>Sémantique de nuanceur de pixels

Ces sémantiques ont une signification lorsqu’elles sont attachées à un paramètre d’entrée de nuanceur de pixels. Ces sémantiques sont prises en charge dans Direct3D 9 et Direct3D 10 et versions ultérieures.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Entrée</th>
<th>Description</th>
<th>Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COULEUR [n]</td>
<td>Couleur diffuse ou spéculaire.</td>
<td>float4</td>
</tr>
<tr class="even">
<td>TEXCOORD [n]</td>
<td>Coordonnées de texture</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>VFACE</td>
<td>Scalaire à virgule flottante qui indique une primitive orientée vers l’arrière. Une valeur négative est retournée vers l’arrière, tandis qu’une valeur positive est face à l’appareil photo.
<blockquote>
[!Note]<br />
Cette sémantique est disponible dans le <a href="dx-graphics-hlsl-sm3.md">modèle de nuanceur Direct3D 9 3,0</a>. Pour Direct3D 10 et versions ultérieures, utilisez <a href="#semantics-supported-only-for-direct3d-10-and-newer">SV_IsFrontFace</a> à la place.
</blockquote>
<br/></td>
<td>float</td>
</tr>
<tr class="even">
<td>VPOS</td>
<td>Emplacement de pixel (x, y) dans l’espace à l’écran. Pour convertir un nuanceur Direct3D 9 (qui utilise cette sémantique) en un nuanceur Direct3D 10 et versions ultérieures, consultez <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">Direct3D 9 VPOS et Direct3D 10 SV_Position</a>)</td>
<td>float2</td>
</tr>
</tbody>
</table>

<table>
<th>Output</th>
<th>Description</th>
<th>Type</th>
</tr>
<td>COULEUR [n]</td>
<td>Couleur de sortie</td>
<td>float4</td>
</tr>
<td>PROFONDEUR [n]</td>
<td>Profondeur de sortie</td>
<td>float</td>
</tr>
</table>

`n` est un entier facultatif compris entre 0 et le nombre de ressources prises en charge. Par exemple, PSIZE0, COLOR1, etc.

La sémantique de couleur est valide uniquement dans le mode de compatibilité du nuanceur (autrement dit, lorsque le nuanceur est créé à l’aide du \_ nuanceur D3D10 \_ , activer la \_ compatibilité descendante \_ ).

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>Sémantique prise en charge uniquement pour Direct3D 10 et versions ultérieures.

Les types de sémantiques suivants ont été récemment introduits pour Direct3D 10 et ne sont pas disponibles pour Direct3D 9.

- [Sémantique de valeur système](#system-value-semantics)

### <a name="system-value-semantics"></a>Sémantique de System-Value

La sémantique de valeur système est une nouveauté de Direct3D 10. Toutes les valeurs système commencent par un \_ préfixe VP, un exemple courant est \_ la position SV, qui est interprétée par l’étape rastériseur. Les valeurs système sont valides dans d’autres parties du pipeline. Par exemple, \_ la fonction position SV peut être spécifiée comme entrée d’un nuanceur de sommets et d’une sortie. Les nuanceurs de pixels peuvent uniquement écrire dans des paramètres avec la \_ \_ sémantique de valeur système cible SV Depth et SV.

Les autres valeurs système (SV \_ VertexID, SV \_ InstanceId, SV \_ IsFrontFace) peuvent uniquement être entrées dans le premier nuanceur actif dans le pipeline qui peut interpréter la valeur particulière. après cela, la fonction du nuanceur doit passer les valeurs aux étapes suivantes.

SV \_ PrimitiveID est une exception à cette règle qui consiste uniquement à entrer dans le premier nuanceur actif dans le pipeline qui peut interpréter la valeur particulière ; le matériel peut fournir la même valeur d’ID qu’une entrée à l’étape de nuanceur de coque, à l’étape de nuanceur de domaine, et après cette étape, la première étape étant activée : Geometry-Shader stage ou Pixel-Shader

Si le pavage est activé, l’étape de nuanceur de coque et l’étape de nuanceur de domaine sont présentes. Pour un correctif donné, le même PrimitiveID s’applique à l’appel du nuanceur de la coque du correctif et à tous les appels de nuanceur de domaine fractionnés. Le même PrimitiveID se propage également à l’étape active suivante ; Geometry : étape de nuanceur ou étape de nuanceur de pixels si elle est activée.

Si le nuanceur Geometry entre SV \_ PrimitiveID et qu’il peut sortir zéro ou une ou plusieurs primitives par appel, le nuanceur doit programmer son propre choix de \_ valeur de PrimitiveID SV pour chaque primitive de sortie si un nuanceur de pixels suivant entre SV \_ PrimtiveID.

En guise d’autre exemple, SV \_ PrimitiveID ne peut pas être interprété par l’étape vertex-shader, car un vertex peut être membre de plusieurs Primitives.

Ces sémantiques ont été ajoutées à Direct3D 10. ils ne sont pas disponibles dans Direct3D 9.

Sémantique de valeur système pour l’étape de rastérisation.

| System-Value sémantique | Description | Type |
|-|-|-|
| SV \_ ClipDistance \[ n\] | Données de distance de la découpage. \_Les valeurs de SV ClipDistance sont chacune supposée être une distance signée float32 à un plan. Le programme d’installation primitif appelle uniquement la pixellisation sur les pixels pour lesquels la ou les distances du plan interpolées sont >= 0. Plusieurs plans de clip peuvent être implémentés simultanément, en déclarant plusieurs composants d’un ou plusieurs éléments vertex comme \_ CLIPDISTANCE SV. Les valeurs combinées de clip et de distance de réforme sont au plus des \# \_ \_ composants D3D ou \_ \_ \_ de nombre de distances de Culling dans les registres de nombre d’éléments de l' \# \_ \_ élément ou de \_ \_ \_ la distance d’élimination au maximum \_ . Disponible pour tous les nuanceurs à lire ou à écrire, à l’exception du nuanceur de sommets qui peut écrire la valeur, mais pas l’accepter comme entrée.<br/> L’attribut **clipplanes** fonctionne comme SV \_ ClipDistance, mais fonctionne sur toutes les [fonctionnalités](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) matérielles 9 \_ x et supérieures. Pour plus d’informations, consultez l' [image des plans d’utilisateur sur le matériel de niveau de fonctionnalité 9](./user-clip-planes-on-10level9.md).<br/> | float |
| SV \_ CullDistance \[ n\] | Données de distance de la réforme. Lorsque le ou les composants d’un ou plusieurs éléments de vertex reçoivent cette étiquette, ces valeurs sont supposées être une distance signée float32 vers un plan. Les primitives seront complètement ignorées si la ou les distances de plan pour tous les vertex de la primitive sont < 0. Plusieurs plans de réforme peuvent être utilisés simultanément, en déclarant plusieurs composants d’un ou plusieurs éléments vertex comme \_ CULLDISTANCE SV. Les valeurs combinées de clip et de distance de réforme sont au plus des \# \_ \_ composants D3D ou \_ \_ \_ de nombre de distances de Culling dans les registres de nombre d’éléments de l' \# \_ \_ élément ou de \_ \_ \_ la distance d’élimination au maximum \_ . Disponible pour tous les nuanceurs à lire ou à écrire, à l’exception du nuanceur de sommets qui peut écrire la valeur, mais pas l’accepter comme entrée.<br/> | float |
| \_Couverture SV | Masque qui peut être spécifié lors de l’entrée, de la sortie ou les deux d’un nuanceur de pixels. <br/> Pour \_ la couverture SV sur un nuanceur de pixels, la sortie est prise en charge sur PS \_ 4 \_ 1 ou une version ultérieure. <br/> Pour \_ la couverture SV sur un nuanceur de pixels, l’entrée requiert PS \_ 5 \_ 0 ou une version ultérieure. <br/> | uint |
| Profondeur de SV \_ | Données de mémoire tampon de profondeur. Peut être écrit par le nuanceur de pixels. | float |
| SV \_ DepthGreaterEqual | Dans un nuanceur de pixels, permet une profondeur de génération, à condition qu’elle soit supérieure ou égale à la valeur déterminée par le rastériseur. Permet d’ajuster la profondeur sans désactiver le Z au début. | float |
| SV \_ DepthLessEqual | Dans un nuanceur de pixels, permet une profondeur de génération, à condition qu’elle soit inférieure ou égale à la valeur déterminée par le rastériseur. Permet d’ajuster la profondeur sans désactiver le Z au début. | float |
| [SV \_ DispatchThreadID](sv-dispatchthreadid.md) | Définit l’offset de thread global dans l’appel de dispatch, par dimension du groupe. Disponible en tant qu’entrée pour le nuanceur de calcul. (lecture seule) | uint3 |
| [SV \_ DomainLocation](sv-domainlocation.md) | Définit l’emplacement sur la coque du point de domaine actuel en cours d’évaluation. Disponible en tant qu’entrée pour le nuanceur de domaine. (lecture seule) | float2 \| 3 |
| [\_GROUPID vs](sv-groupid.md) | Définit l’offset de groupe dans un appel de distribution, par dimension de l’appel de répartition. Disponible en tant qu’entrée pour le nuanceur de calcul. (lecture seule) | uint3 |
| [SV \_ GroupIndex](sv-groupindex.md) | Fournit un index aplati pour un thread donné au sein d’un groupe donné. Disponible en tant qu’entrée pour le nuanceur de calcul. (lecture seule) | uint |
| [SV \_ GroupThreadID](sv-groupthreadid.md) | Définit l’offset du thread dans le groupe, par dimension du groupe. Disponible en tant qu’entrée pour le nuanceur de calcul. (lecture seule) | uint3 |
| [SV \_ GSInstanceID](sv-gsinstanceid.md) | Définit l’instance du nuanceur Geometry. Disponible en tant qu’entrée pour le nuanceur Geometry. L’instance est nécessaire, car un nuanceur Geometry peut être appelé jusqu’à 32 fois sur la même primitive géométrique. | uint |
| SV \_ InnerCoverage | Représente des informations de pixellisation conservatrice sous-estimées (par exemple, si un pixel est garanti comme étant entièrement couvert). Peut être lu ou écrit par le nuanceur de pixels. | |
| [SV \_ InsideTessFactor](sv-insidetessfactor.md) | Définit la quantité de pavage dans une surface corrective. Disponible dans le nuanceur de coque pour l’écriture et est disponible dans le nuanceur de domaine pour la lecture. | float \| float \[ 2\] |
| InstanceId de SV \_ | Identificateur par instance généré automatiquement par le runtime (consultez Utilisation des [valeurs de System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponible pour tous les nuanceurs. | |
| SV \_ IsFrontFace | Spécifie si un triangle est orienté vers l’avant. Pour les lignes et les points, IsFrontFace a la valeur true. L’exception est une ligne dessinée à l’extérieur (mode filaire), qui définit IsFrontFace de la même façon que la pixellisation du triangle en mode solide. Peut être écrit par le nuanceur Geometry et lu par le nuanceur de pixels. | bool |
| [SV \_ OutputControlPointID](sv-outputcontrolpointid.md) | Définit l’index de l’ID du point de contrôle qui est traité par un appel du point d’entrée principal du nuanceur de coque. Peut être lu par le nuanceur de coque uniquement. | uint |
| Position du SV \_ | Quand \_ la position SV est déclarée pour l’entrée d’un nuanceur, elle peut avoir l’un des deux modes d’interpolation spécifiés : linearNoPerspective ou linearNoPerspectiveCentroid, où les deux valeurs XYZW alignées sur le centre de gravité de l’information sont fournies lors de l’anticrénelage à plusieurs échantillons. En cas d’utilisation dans un nuanceur, \_ la position SV décrit l’emplacement des pixels. Disponible dans tous les nuanceurs pour obtenir le centre de pixels avec un décalage de 0,5. | float4 |
| SV \_ PrimitiveID | Identificateur par primitive généré automatiquement par le runtime (consultez Utilisation des [valeurs de System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Peuvent être écrits par les nuanceurs de géométrie ou de pixels, et lus par les nuanceurs Geometry, pixel, coque ou domaine. | uint |
| SV \_ RenderTargetArrayIndex | Render-index du tableau cible. Appliqué à la sortie du nuanceur Geometry et indique la tranche du tableau cible de rendu sur laquelle la primitive sera dessinée par le nuanceur de pixels. SV \_ RenderTargetArrayIndex est valide uniquement si la cible de rendu est une ressource de tableau. Cette sémantique s’applique uniquement aux primitives. Si une primitive a plusieurs sommets, la valeur du sommet principal est utilisée. Cette valeur indique également quelle tranche de tableau d’une vue de profondeur/de gabarit est utilisée à des fins de lecture/écriture.<br/> Peut être écrit à partir du nuanceur Geometry et lu par le nuanceur de pixels.<br/> Si [D3D11_FEATURE_DATA_D3D11_OPTIONS3 :: VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) est `true` , SV \_ RenderTargetArrayIndex est appliqué à tous les nuanceurs qui alimentent le rastériseur. | uint |
| SV \_ SampleIndex | Exemple de données d’index de fréquence. Disponible pour la lecture ou l’écriture par le nuanceur de pixels uniquement. | uint |
| SV \_ StencilRef | Représente la valeur de référence du stencil de nuanceur de pixels actuel. Peut uniquement être écrit par le nuanceur de pixels. | uint |
| \_Cible SV \[ n \] , où 0 <= n <= 7 | Valeur de sortie qui sera stockée dans une cible de rendu. L’index indique laquelle des 8 cibles de rendu éventuellement liées à écrire. La valeur est disponible pour tous les nuanceurs. | float \[ 2 \| 3 \| 4\] |
| [SV \_ TessFactor](sv-tessfactor.md) | Définit la quantité de pavage sur chaque bord d’un correctif. Disponible pour l’écriture dans le nuanceur de coque et la lecture dans le nuanceur de domaine. | float \[ 2 \| 3 \| 4\] |
| SV \_ VertexID | Identificateur par vertex généré automatiquement par le runtime (consultez Utilisation des [valeurs de System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponible en tant qu’entrée pour le nuanceur vertex uniquement. | uint |
| SV \_ ViewportArrayIndex | Index du tableau de la fenêtre d’affichage. Appliqué à la sortie du nuanceur Geometry et indique la fenêtre d’affichage à utiliser pour la primitive en cours d’écriture. Peut être lu par le nuanceur de pixels. La primitive est transformée et découpée par rapport à la fenêtre d’affichage spécifiée par l’index avant d’être transmise au rastériseur. Cette sémantique s’applique uniquement aux primitives. Si une primitive a plusieurs sommets, la valeur du sommet principal est utilisée. <br/> Si [D3D11_FEATURE_DATA_D3D11_OPTIONS3 :: VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) est `true` , SV \_ ViewportArrayIndex est appliqué à tous les nuanceurs qui alimentent le rastériseur. | uint |
| SV \_ ShadingRate | Définit, à l’aide des [valeurs](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)de taux d’ombrage, le nombre de pixels écrits par un appel de nuanceur de pixels pour les appareils de niveau 2 ou supérieur de l' [ombrage variable](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) . Peut être lu à partir du nuanceur de pixels. Peut être écrit à partir d’un nuanceur de sommets ou de géométrie. | uint |

### <a name="limitations-when-writing-sv_depth"></a>Limitations lors de l’écriture de la profondeur de SV \_ :

- Lorsque l’échantillonnage multiple (MultisampleEnable a la valeur **true** dans [**D3D10 \_ rastériseur \_ desc**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc)) et l’écriture d’une valeur de profondeur (à l’aide d’un nuanceur de pixels), la valeur unique écrite est également utilisée dans le [test de profondeur](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md). par conséquent, la possibilité de restituer les bords de la primitive à une résolution supérieure est perdue lors de l’échantillonnage multiple.
- Lors de l’utilisation du contrôle de workflow dynamique, il est impossible de déterminer au moment de la compilation si un nuanceur qui écrit la \_ profondeur de SV dans certains chemins d’accès est sûr d’écrire la \_ profondeur de SV à chaque exécution. L’impossibilité d’écrire une profondeur de SV \_ quand elle est déclarée entraîne un comportement non défini (qui peut inclure ou non le rejet du pixel).
- Toute valeur float32, y compris +/-INF et NaN, peut être écrite dans la profondeur de SV \_ .
- L’écriture d’une profondeur de SV \_ est toujours valide lors de la fusion de couleurs à double source.

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>Migration de Direct3D 9 vers Direct3D 10 et versions ultérieures

Les problèmes suivants doivent être pris en compte lors de la migration du code de Direct3D 9 vers Direct3D 10 et versions ultérieures :

### <a name="mapping-to-direct3d-9-semantics"></a>Mapper à la sémantique Direct3D 9

Quelques sémantiques Direct3D 10 et versions ultérieures sont mappées directement à la sémantique Direct3D 9.

| Sémantique Direct3D 10 | Sémantique équivalente Direct3D 9 |
|-|-|
| Profondeur de SV \_ | DEPTH |
| Position du SV \_ | POSITION |
| \_Cible SV | COULEUR |

> [!] Remarque pour les développeurs Direct3D 9 : pour les cibles Direct3D 9, la sémantique du nuanceur doit être mappée à la sémantique Direct3D 9 valide. Pour la compatibilité descendante POSITION0 (et ses noms de variantes) est traitée comme une \_ position SV, la couleur est traitée comme une \_ cible VP.

- [Mapper à la sémantique Direct3D 9](#mapping-to-direct3d-9-semantics)
- [Position de la VP Direct3D 9 VPOS et Direct3D 10 \_](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [Plans d’utilisateur en HLSL](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Position de la VP Direct3D 9 VPOS et Direct3D 10 \_

La position de la VP sémantique D3D10 \_ fournit des fonctionnalités similaires à la sémantique du modèle de nuanceur 3 VPOS Direct3D 9. Par exemple, dans Direct3D 9, la syntaxe suivante est utilisée pour un nuanceur de pixels à l’aide des coordonnées de l’espace à l’écran :

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

VPOS a été ajouté pour la prise en charge de Shader Model 3, pour spécifier les coordonnées de l’espace à l’écran, puisque la sémantique de POSITION était destinée aux coordonnées de l’espace d’objet.

Dans Direct3D 10 et versions ultérieures, la \_ sémantique de position SV (lorsqu’elle est utilisée dans le contexte d’un nuanceur de pixels) spécifie les coordonnées de l’espace à l’écran (décalage par 0,5). Par conséquent, le nuanceur Direct3D 9 sera à peu près équivalent (sans tenir compte du décalage 0,5) à ce qui suit :

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

Lors de la migration de Direct3D 9 vers Direct3D 10 et versions ultérieures, vous devez être conscient de cela lors de la traduction de vos nuanceurs.

### <a name="user-clip-planes-in-hlsl"></a>Plans d’utilisateur en HLSL

À compter de Windows 8, vous pouvez utiliser l’attribut de fonction **clipplanes** dans une [déclaration de fonction](dx-graphics-hlsl-function-syntax.md) HLSL plutôt que SV \_ ClipDistance pour que votre nuanceur fonctionne sur le niveau de [fonctionnalité](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 x, ainsi que sur le niveau de \_ fonctionnalité 10 et ultérieur. Pour plus d’informations, consultez l' [image des plans d’utilisateur sur le matériel de niveau de fonctionnalité 9](./user-clip-planes-on-10level9.md).

## <a name="related-topics"></a>Rubriques connexes

* [Syntaxe du langage](dx-graphics-hlsl-language-syntax.md)
* [Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
