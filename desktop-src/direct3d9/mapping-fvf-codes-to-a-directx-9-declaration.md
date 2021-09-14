---
description: Ce tableau met en correspondance les codes de la Commission des prix à une structure D3DVERTEXELEMENT9.
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: Mappage de codes de la Commission des prix à une déclaration Direct3D 9 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85442cf1c92c78aa1a37f4d4a4ec3de154f5b8d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918259"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>Mappage de codes de la Commission des prix à une déclaration Direct3D 9 (Direct3D 9)

Ce tableau met en correspondance les codes de la Commission des prix à une structure [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .



| CLOS                                                   | Type de données                                                           | Usage                                                                         | Index d’utilisation |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ xyz                                           | D3DDECLTYPE \_ FLOAT3                                                 | \_Position D3DDECLUSAGE                                                        | 0           |
| D3DFVF \_ XYZRHW                                        | D3DDECLTYPE \_ float4                                                 | \_Position D3DDECLUSAGE                                                       | 0           |
| D3DFVF \_ XYZW                                          | D3DDECLTYPE \_ float4                                                 | \_Position D3DDECLUSAGE                                                        | 0           |
| D3DFVF \_ XYZB5 et D3DFVF \_ LASTBETA \_ UBYTE4            | D3DVSDT \_ FLOAT3, D3DVSDT \_ float4, D3DVSDT \_ UBYTE4                   | D3DDECLUSAGE \_ position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5 et D3DFVF \_ LASTBETA \_ D3DCOLOR          | D3DVSDT \_ FLOAT3, D3DVSDT \_ float4, D3DVSDT \_ D3DCOLOR                 | D3DDECLUSAGE \_ position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5                                         | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float4, D3DDECLTYPE \_ FLOAT1       | D3DDECLUSAGE \_ position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4)                                | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ floatn                            | D3DDECLUSAGE \_ position, D3DDECLUSAGE \_ BLENDWEIGHT                             | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4) et D3DFVF \_ LASTBETA \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float (n-1), D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4) et D3DFVF \_ LASTBETA \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float (n-1), D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ normal                                        | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ normal                                                          | 0           |
| D3DFVF \_ psize                                         | D3DDECLTYPE \_ FLOAT1                                                 | D3DDECLUSAGE \_ psize                                                           | 0           |
| \_Diffusion D3DFVF                                       | D3DDECLTYPE \_ D3DCOLOR                                               | \_Couleur D3DDECLUSAGE                                                           | 0           |
| D3DFVF \_ spéculaire                                      | D3DDECLTYPE \_ D3DCOLOR                                               | \_Couleur D3DDECLUSAGE                                                           | 1           |
| D3DFVF \_ TEXCOORDSIZEm (n)                              | D3DDECLTYPE \_ Floater                                                 | D3DDECLUSAGE \_ texcoord                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>Déclarations de vertex avec D3DDECLUSAGE \_ positiont

La présence d’un élément vertex avec (D3DUSAGE \_ positiont, 0) est utilisée pour indiquer au périphérique que les données de vertex entrantes ont déjà été effectuées par le biais du traitement des vertex (par exemple, une valeur de type «Commission final avec D3DFVF \_ XYZRHW bit Set). Au moment du tracé, si la déclaration actuellement définie possède un élément avec la sémantique (D3DUSAGE \_ positiont, 0), l’intégralité du traitement du vertex est ignorée (tout comme si une Commission de la Commission avec D3DFVF \_ XYZRHW bit a été définie).

Il existe des restrictions sur les déclarations de vertex avec (D3DDECLUSAGE \_ positiont, 0) :

-   Seul le flux zéro peut être utilisé dans ces déclarations.
-   Les éléments vertex doivent être triés en incrémentant le décalage du flux.
-   Le décalage du flux doit être aligné sur un DWORD.
-   La même paire (utilisation, index d’utilisation) ne doit être listée qu’une seule fois.
-   Seule la \_ méthode par défaut D3DDECLMETHOD peut être utilisée.
-   Les autres éléments vertex ne peuvent pas avoir la \_ sémantique (position D3DDECLUSAGE, 0).

En outre, il existe des restrictions sur cette déclaration concernant la version du pilote de périphérique. Ces restrictions sont appliquées car Direct3D envoie directement ces déclarations au pilote sans effectuer de conversion.

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>Déclarations de vertex sans D3DDECLUSAGE \_ positiont

Le runtime valide la création des déclarations. Voici les règles générales pour les déclarations autorisées.

-   Tous les éléments vertex d’un flux doivent être consécutifs et triés par décalage.
-   Le décalage du flux doit être aligné sur un DWORD.
-   La même paire (utilisation, index d’utilisation) ne doit être listée qu’une seule fois.
-   Si le \_ VERTEXELEMENTSCANSHARESTREAMOFFSET D3DDEVCAPS2 est défini,
    -   Plusieurs éléments vertex peuvent partager le même offset dans un flux.
    -   Les éléments vertex peuvent tous avoir des types différents qui peuvent être de différentes tailles.
    -   Les éléments vertex peuvent se chevaucher arbitrairement. Par exemple, un élément peut démarrer à un emplacement d’un flux qui est, en même temps, au milieu d’un autre élément.
    -   Les éléments vertex peuvent avoir un décalage de flux dans n’importe quel ordre.
-   Le nombre d’éléments de vertex ne peut pas être supérieur à 64.
-   UsageIndex doit être compris dans la plage \[ 0-15 \] .
-   La déclaration, utilisée avec l’API DrawPrimitive, ne doit pas avoir d’éléments vertex autres que D3DDECLMETHOD \_ default, D3DDECLMETHOD \_ LOOKUPPRESAMPLED ou D3DDECLMETHOD \_ Lookup.
-   La déclaration, qui contient D3DDECLMETHOD \_ Lookup ou LOOKUPPRESAMPLED, doit être utilisée uniquement avec le pipeline de vertex programmable.
-   La déclaration, utilisée avec l’API DrawRectPatch/DrawTriPatch, ne peut pas avoir d’éléments vertex avec D3DDECLMETHOD \_ LOOKUPPRESAMPLED ou la \_ recherche D3DDECLMETHOD.
-   La déclaration ne doit avoir qu’un seul élément avec la \_ méthode D3DDECLMETHOD Lookup ou D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   La déclaration avec D3DDECLMETHOD \_ Lookup ou D3DDECLMETHOD \_ LOOKUPPRESAMPLED ne doit pas avoir d’éléments autres que D3DDECLMETHOD \_ default, car le mappage de déplacement est effectué uniquement pour les N-patchs.
-   Les éléments vertex avec D3DDECLMETHOD \_ Lookup ou D3DDECLMETHOD \_ LOOKUPPRESAMPLED peuvent uniquement être utilisés avec la sémantique (D3DDECLUSAGE \_ Sample, n), et vice versa.
-   Si un élément vertex avec \_ la méthode de recherche D3DDECLMETHOD a un index de flux et un décalage d’un élément vertex déjà existant, cet élément vertex doit avoir le même type de données.
-   Un élément vertex avec la \_ méthode de recherche D3DDECLMETHOD doit avoir le \_ type de données D3DDECLTYPE FLOAT2/3/4
-   Les éléments vertex avec des types D3DDECLMETHOD \_ CROSSUV, D3DDECLMETHOD \_ partial, et D3DDECLMETHOD \_ PARTIALV doivent avoir un décalage d’un élément vertex avec un type de données compatible.
-   Un élément vertex avec la méthode D3DDECLMETHOD \_ UV ou D3DDECLMETHOD \_ LOOKUPPRESAMPLED doit avoir le type D3DDECLTYPE \_ inutilisé, l’index de flux zéro et le décalage de flux zéro.
-   Les déclarations avec des méthodes D3DDECLMETHOD \_ UV, D3DDECLMETHOD \_ partial, et D3DDECLMETHOD \_ PARTIALV peuvent être utilisées uniquement avec DrawRectPatch.
-   L’utilisation \_ de D3DDECLUSAGE TESSFACTOR doit être utilisée uniquement avec le type de données D3DDECLTYPE \_ FLOAT1 et l’index d’utilisation 0.
-   Lorsqu’une déclaration est utilisée pour le pavage (DrawRectPatch, DrawTriPatch, N-patchs), le type de données doit être inférieur ou égal à D3DDECLTYPE \_ SHORT4.
-   Les déclarations qui contiennent des méthodes nécessitant certaines fonctionnalités de l’appareil (par exemple, le mappage de déplacement, les correctifs RT) peuvent être créées uniquement si l’appareil les prend en charge.
-   Une déclaration de vertex utilisée pour dessiner des points et des lignes ne peut pas avoir de méthodes autres que D3DDECLMETHOD \_ par défaut.
-   Les déclarations qui peuvent être créées dépendent également des capacités du pilote.

## <a name="driver-considerations"></a>Considérations relatives aux pilotes

### <a name="pre-direct3d-9-drivers"></a>Pilotes pré-Direct3D 9

-   La déclaration d’entrée doit pouvoir être traduite en une Commission de la Commission valide (avec le même ordre d’éléments de vertex et leurs types de données).
-   Les écarts dans les coordonnées de texture ne sont pas autorisés. Cela signifie que s’il existe un élément vertex avec (D3DDECLUSAGE \_ texcoord, n), il doit également exister un élément vertex avec (D3DDECLUSAGE \_ texcoord, n-1).

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>Pilotes Direct3D 9 sans prise en charge de nuanceur de pixels version 3

-   La déclaration d’entrée doit pouvoir être traduite en une Commission de la Commission valide (avec le même ordre d’éléments de vertex et leurs types de données).
-   Les intervalles de coordonnées de texture sont autorisés.

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>Pilotes Direct3D 9 avec prise en charge de Pixel Shader version 3

D’autres déclarations générales sont autorisées.

-   Les éléments vertex peuvent être dans l’ordre arbitraire et peuvent avoir n’importe quel type de données.
-   Plusieurs éléments vertex peuvent partager le même décalage de flux et être d’un type différent en même temps si D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET est défini par l’appareil.

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>Utilisation de la déclaration de vertex avec le pipeline de vertex programmable

-   Au moment du tracé, Direct3D recherche la même combinaison d’index d’utilisation dans la déclaration de vertex actuelle et la fonction de nuanceur de sommets actuelle. Lorsque la combinaison est trouvée, le registre à partir de la fonction de nuanceur DCL est utilisé comme destination pour l’élément vertex.
-   Lorsqu’un élément vertex dans la déclaration de vertex actuelle a une utilisation qui est introuvable dans le nuanceur de sommets actuel, cet élément vertex est ignoré.
-   Lors de l’utilisation d’une version de nuanceurs vertex inférieure à 2,0, toute la sémantique mentionnée dans le code du nuanceur doit être présente dans la déclaration liée au moment du tracé. Lorsque vous utilisez des nuanceurs vertex 2,0 et versions ultérieures, cette restriction qui permet aux applications d’utiliser différentes déclarations de vertex avec le même nuanceur de vertex n’existe pas. Cela est utile lorsqu’un nuanceur vertex lit les données d’entrée en fonction des conditions statiques. Les registres du nuanceur de sommets ne sont pas initialisés pour cette raison.

Il existe des restrictions supplémentaires lors de l’utilisation de avec le traitement du vertex matériel sur un pilote DirectX 8 :

-   Les éléments vertex ne peuvent pas se chevaucher ou partager le même offset.
-   Les types de données sont limités à ce que le pilote DirectX 8 peut comprendre.

Le CreateVertexDeclaration peut échouer si la déclaration fournie ne peut pas être convertie en une déclaration de type DirectX 8. Pour un appareil en mode mixte, cet échec se produit au \* moment du tracé, car c’est le seul moment où il est possible de savoir si ce nuanceur est utilisé avec le traitement du vertex matériel ou logiciel.

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>Utilisation d’une déclaration de vertex avec le pipeline de fonction fixe

Seules les déclarations qui adhèrent aux règles suivantes peuvent être utilisées :

-   Il ne doit y avoir aucun écart entre les éléments de vertex (SKIP n’est pas autorisé dans une déclaration DirectX 8, qui est utilisée pour le pipeline de fonction fixe).
-   La sémantique ( \_ position D3DDECLUSAGE, 0) doit être spécifiée et doit avoir le \_ type de données D3DDECLTYPE FLOAT3.
-   Un élément vertex avec la méthode D3DDECLMETHOD \_ UV doit spécifier l’utilisation D3DDECLUSAGE \_ texcoord ou D3DDECLUSAGE \_ BLENDWEIGHT.
-   Un élément vertex avec la méthode D3DDECLMETHOD \_ partial, \_ PARTIALV ou \_ CROSSUV peut être utilisé uniquement avec la \_ position D3DDECLUSAGE, \_ normal, \_ BLENDWEIGHT ou \_ texcoord, et doit utiliser le type d’entrée D3DDECLTYPE \_ FLOAT3.

Quand une déclaration est utilisée avec le traitement de vertex matériel sur un pilote DirectX 8, le runtime Direct3D le convertit en une déclaration de type DirectX 8 avec les règles suivantes :

-   Les éléments vertex ne peuvent pas partager le même offset dans un flux et ils ne peuvent pas se chevaucher.
-   Le type de données doit être inférieur ou égal à D3DDECLTYPE \_ SHORT4.
-   Seules les méthodes suivantes sont autorisées : D3DDECLMETHOD \_ par défaut, D3DDECLMETHOD \_ CROSSUV et D3DDECLMETHOD \_ UV
-   Le [mappage entre une déclaration Direct3D 9 et une déclaration Direct3D 8 (Direct3D 9)](mapping-between-a-directx-9-declaration-and-directx-8.md) illustre la sémantique Direct3D 9 pouvant être convertie en déclaration de style DirectX 8. L’utilisation et les UsageIndex sont convertis en valeur de registre.
-   S’il y a n éléments vertex dans une déclaration et que 0-m (m < n) est mappé à une Commission de la Commission (éléments décrits dans le [mappage entre une déclaration Direct3D et les codes de la Commission de la Commission (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md)), mais m + 1 ne le fait pas :
    -   Si l’un des m + 2 jusqu’à ce que les éléments de vertex n-1 soient mappés à la valeur « Commission »/dx8decl, la déclaration n’est pas valide.
    -   Les éléments de 0 à m sont convertis (par le runtime pour DirectX 8 et les pilotes plus anciens, et par les pilotes Direct3D 9) à l’aide du [mappage entre une déclaration Direct3D et les codes de la Commission (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md), m + 1, m + 2 jusqu’à n-1 sont mappés à des texcoord contigus (k), texcoord (k + 1), à
    -   Le type de données d’un texcoord mappé est supposé être float \[ 1234 en \] remplaçant le type de données que contient l’élément actuel (mais la même taille). Par conséquent, il peut s’agir d’un type de données qui n’est pas en cours de [mappage entre une déclaration Direct3D et les codes de la Commission de la Commission (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md).
    -   Si k atteint 8, la déclaration n’est pas valide pour le prix de la Commission/dx8decl.
    -   Si des mappages à TexCoords se sont produits, la déclaration entière est requise pour ne pas avoir d’éléments avec une méthode de génération autre que DEFAULT ou la déclaration n’est pas valide pour la fonction de la Commission/dx8decl.

## <a name="using-vertex-declarations-with-processvertices"></a>Utilisation de déclarations de vertex avec ProcessVertices

Une déclaration de vertex peut être utilisée pour décrire la sortie de ProcessVertices. Cette déclaration doit respecter les règles suivantes :

-   Seul Stream 0 doit être utilisé.
-   Seules \_ les méthodes par défaut D3DDECLMETHOD sont autorisées.
-   Seuls les \_ types de données D3DDECLTYPE floatn ou D3DDECLTYPE \_ D3DCOLOR peuvent être utilisés.
-   Les éléments vertex ne peuvent pas partager le même offset ou se chevauchent les uns avec les autres.
-   Les éléments vertex avec ( \_ position D3DDECLUSAGE, 0) ou (D3DDECLUSAGE \_ positiont, 0) ne sont pas requis.
-   Les éléments vertex avec ( \_ position D3DDECLUSAGE, 0) et (D3DDECLUSAGE \_ positiont, 0) ne peuvent pas être présents dans la même déclaration.
-   Le nuanceur de sommets actuel doit avoir la version 3,0 ou une version ultérieure quand une telle déclaration est utilisée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclaration de vertex](vertex-declaration.md)
</dt> </dl>

 

 



