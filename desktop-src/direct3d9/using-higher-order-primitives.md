---
description: Cette section vous montre comment utiliser des primitives d’ordre supérieur dans votre application.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Utilisation de primitives Higher-Order (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7d7a7b7f619c033665f8cb9894db5d60d5d6ecf9116de4ada230accc476c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797290"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Utilisation de primitives Higher-Order (Direct3D 9)

Cette section vous montre comment utiliser des primitives d’ordre supérieur dans votre application.

-   [Détermination de la prise en charge de la primitive Higher-Order](#determining-higher-order-primitive-support)
-   [Dessin des correctifs](#drawing-patches)
-   [Génération de normales et de coordonnées de texture](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Détermination de la prise en charge de la primitive Higher-Order

Le membre DevCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) peut être interrogé pour déterminer le niveau de prise en charge pour les opérations impliquant des primitives d’ordre supérieur. Le tableau suivant répertorie les fonctionnalités de l’appareil liées aux primitives d’ordre supérieur dans Direct3D 9.



| Fonctionnalité d’appareil             | Description                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ NPATCHES          | L’appareil prend en charge N-patchs et est basé sur des [triangles PN incurvés](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (un type spécial de triangles de Bézier cubiques). |
| D3DDEVCAPS \_ QUINTICRTPATCHES  | L’appareil prend en charge les courbes de Bézier quintaux et les splines B-splines.                                                                                                         |
| D3DDEVCAPS \_ RTPATCHES         | L’appareil prend en charge les correctifs rectangulaires et triangulaires (RT-patches).                                                                                             |
| D3DDEVCAPS \_ RTPATCHHANDLEZERO | RT-les correctifs peuvent être tracés efficacement à l’aide du handle zéro.                                                                                                     |



 

Notez que D3DDEVCAPS \_ RTPATCHHANDLEZERO ne signifie pas qu’un correctif avec le descripteur zéro peut être dessiné. Un handle Zero patch peut toujours être dessiné, que cette fonctionnalité de périphérique soit définie ou non. Lorsque cette fonctionnalité est définie, l’architecture matérielle ne nécessite pas la mise en cache de toutes les informations et les correctifs non mis en cache (handle zéro) sont dessinés aussi efficacement que les correctifs mis en cache.

## <a name="drawing-patches"></a>Dessin des correctifs

Direct3D 9 prend en charge deux types de primitives d’ordre supérieur ou les correctifs. Ils sont appelés correctifs N-patchs et Rect/tri. N-les correctifs peuvent être rendus à l’aide de n’importe quel appel de rendu de triangle en activant N-patchs via l’appel à [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)(nSegments) avec une valeur nSegments supérieure à 1,0. Les correctifs Rect/tri doivent être rendus à l’aide des points d’entrée explicites suivants.

Vous pouvez utiliser les méthodes suivantes pour dessiner des correctifs.

-   [**IDirect3DDevice9 ::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch). Pour mieux comprendre comment les données des correctifs sont référencées dans la mémoire tampon de vertex, consultez [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).
-   [**IDirect3DDevice9 ::D rawtripatch**](/windows/desktop/api). Pour mieux comprendre comment les données des correctifs sont référencées dans la mémoire tampon de vertex, consultez [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

[**IDirect3DDevice9 ::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) dessine un correctif de poids fort rectangulaire spécifié par le paramètre pRectPatchInfo à l’aide des flux actuellement définis. Le paramètre descripteur est utilisé pour associer le correctif à un handle, de sorte que la prochaine fois que le correctif est dessiné, il n’est pas nécessaire de respécifier pRectPatchInfo. Cela permet de précalculer et de mettre en cache les coefficients de différence ou d’autres informations qui, à leur tour, permettent les appels suivants à **IDirect3DDevice9 ::D rawrectpatch** utilisant le même handle pour s’exécuter efficacement.

Il est conçu pour les correctifs statiques, une application qui définit le nuanceur de sommets et les flux appropriés, fournit des informations sur les correctifs dans le paramètre pRectPatchInfo et spécifie un descripteur afin que Direct3D puisse capturer et mettre en cache les informations. L’application peut ensuite appeler [**IDirect3DDevice9 ::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) par la suite avec pRectPatchInfo défini sur la **valeur null** pour dessiner efficacement le correctif. Lors du dessin d’un correctif mis en cache, les flux actuellement définis sont ignorés. Toutefois, il est possible de substituer les pNumSegs mis en cache en spécifiant de nouvelles valeurs pour pNumSegs. En outre, il est nécessaire de définir le même nuanceur vertex lors du rendu d’un correctif mis en cache tel qu’il a été défini lors de sa capture.

Pour les correctifs dynamiques, les données des correctifs sont modifiées pour chaque rendu du correctif. il n’est donc pas efficace de mettre en cache les informations. L’application peut transmettre cela à Direct3D en affectant à handle la valeur 0. Dans ce cas, Direct3D dessine le correctif à l’aide des flux actuellement définis et des valeurs pNumSegs et ne met pas en cache les informations. Il n’est pas possible de définir simultanément un handle sur 0 et pPatch sur **null**.

En respécifiant pRectPatchInfo pour le même handle, l’application peut remplacer les informations précédemment mises en cache.

[**IDirect3DDevice9 ::D rawtripatch**](/windows/desktop/api) est semblable à [**IDirect3DDevice9 ::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) , à ceci près qu’il dessine un correctif de poids fort triangulaire.

## <a name="generating-normals-and-texture-coordinates"></a>Génération de normales et de coordonnées de texture

Si vous utilisez un nuanceur de format de vertex flexible, la génération automatique de normales et de coordonnées de texture n’est pas possible.

Pour les normales, vous pouvez soit les fournir directement, soit faire en sorte que Direct3D les calcule pour vous.

Les coordonnées générées pour les correctifs rectangulaires sont des coordonnées splines, comme indiqué dans les illustrations suivantes.

![illustration d’une texture d’origine et de la texture avec des coordonnées reposant sur une spline](images/texturespline.png)

Les coordonnées générées pour les correctifs triangulaires sont des coordonnées basées sur une spline Barycentric, comme illustré dans les illustrations suivantes.

![illustration d’une texture d’origine et de la texture avec des coordonnées basées sur spline Barycentric](images/texturebarycentricspline.png)

Si une application doit modifier la plage des coordonnées de texture générées, cette opération peut être effectuée à l’aide de transformations de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives d’ordre supérieur](higher-order-primitives.md)
</dt> </dl>

 

 
