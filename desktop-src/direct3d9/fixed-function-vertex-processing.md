---
description: Dans le pipeline de vertex de fonction fixe, le traitement des vertex dans une mémoire tampon de vertex applique les matrices de transformation actuelles pour l’appareil.
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: Résolution du traitement des vertex de fonction (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da30dd0fb6cf6e055d8b1bbb31fdfdb01d9e1e20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108846"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>Résolution du traitement des vertex de fonction (Direct3D 9)

Dans le pipeline de vertex de fonction fixe, le traitement des vertex dans une mémoire tampon de vertex applique les matrices de transformation actuelles pour l’appareil. Les opérations de vertex telles que l’éclairage, la génération d’indicateurs de séquence et la mise à jour des extensions peuvent également être appliquées, éventuellement. Lors de l’utilisation du traitement de vertex de fonction fixe, la modification des éléments dans la mémoire tampon de vertex de destination est contrôlée par l’indicateur [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) . Cet indicateur s’applique uniquement au traitement de vertex de fonction fixe. L’interface [**IDirect3DDevice9**](/windows/desktop/api) expose la méthode [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) pour traiter les vertex. Vous traitez les vertex d’un nuanceur vertex vers l’ensemble des flux de données d’entrée, en générant un flux unique de données de vertex entrelacées vers la mémoire tampon de vertex de destination en appelant la méthode **IDirect3DDevice9 ::P rocessvertices** . La méthode accepte cinq paramètres qui décrivent l’emplacement et la quantité des vertex ciblés par la méthode, la mémoire tampon de vertex de destination et les options de traitement. Après l’appel, la mémoire tampon de destination contient les données de vertex traitées.

Les premier, deuxième et troisième paramètres, SrcStartIndex, DestIndex et VertexCount, reflètent l’index du premier vertex à charger, l’index dans la mémoire tampon de destination à laquelle les sommets sont placés, et le nombre total de vertex à traiter et à placer dans la mémoire tampon de destination, respectivement. Le quatrième paramètre, pDestBuffer doit être défini sur l’adresse de l’interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) de l’objet de mémoire tampon de vertex qui recevra les vertex sources. Le paramètre SrcStartIndex spécifie l’index auquel la méthode doit commencer à traiter les vertex.

Le paramètre final, Flags, détermine les options de traitement spéciales pour la méthode. Vous pouvez définir ce paramètre sur 0 pour le traitement par défaut des vertex ou sur [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) pour optimiser le traitement dans certaines situations. Vous pouvez également combiner la \_ valeur D3DPV DONOTCOPYDATA avec une ou plusieurs valeurs [D3DLOCK](d3dlock.md) appropriées pour la mémoire tampon de destination. Lorsque vous affectez la valeur 0 à Flags, les composants de vertex du format de vertex de la mémoire tampon du vertex de destination qui ne sont pas affectés par l’opération de vertex sont toujours copiés à partir du nuanceur de sommets ou ont la valeur 0. Toutefois, lors de l’utilisation \_ de D3DPV DONOTCOPYDATA, [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) ne remplace pas les informations de coordonnées de couleur et de texture dans la mémoire tampon de destination, sauf si ces données sont générées par Direct3D. La couleur diffuse est générée lorsque l’éclairage est activé, c’est-à-dire que l’éclairage D3DRS a la valeur \_ **true**. La couleur spéculaire est générée lorsque l’éclairage est activé et que l’option spéculaire est activée, c’est-à-dire que D3DRS \_ SpecularEnable et D3DRS \_ Lighting ont la valeur **true**. La couleur spéculaire est également générée quand le brouillard est activé. Des coordonnées de texture sont générées lorsque la transformation de texture ou la génération de texture est activée. **IDirect3DDevice9 ::P rocessvertices** utilise les États de rendu actuels pour déterminer le traitement du vertex à effectuer.

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>Paramètres d’utilisation du prix final pour les mémoires tampons de vertex de destination

La méthode [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) requiert des paramètres spécifiques pour le [D3DFVF](d3dfvf.md) de la mémoire tampon de vertex de destination. Les paramètres d’utilisation du niveau de la Commission doivent être compatibles avec les paramètres actuels pour le traitement des vertex.

Pour le traitement des vertex de fonction fixe, [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) requiert les paramètres de la Commission de la Commission suivante :

-   Le type de position est toujours [D3DFVF \_ XYZRHW](d3dfvf.md) ; par conséquent, D3DFVF \_ XYZ et D3DFVF \_ XYZB1 à D3DFVF \_ XYZB5 ne sont pas valides.
-   Les indicateurs [D3DFVF \_ normal](d3dfvf.md), D3DFVF \_ RESERVED0 et D3DFVF \_ RESERVED2 ne doivent pas être définis.
-   L’indicateur de [ \_ diffusion D3DFVF](d3dfvf.md) doit être défini si une opération or des conditions suivantes retourne la valeur true :
    -   L’éclairage est activé ; autrement dit, D3DRS \_ Lighting a la **valeur true**.
    -   L’éclairage est désactivé, la couleur diffuse est présente dans les flux de vertex d’entrée et [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) n’est pas défini.
-   L' [indicateur \_ spéculaire D3DFVF](d3dfvf.md) doit être défini si une opération or des conditions suivantes retourne la valeur true :
    -   L’éclairage est activé et la couleur spéculaire est activée ; autrement dit, D3DRS \_ SpecularEnable a la **valeur true**.
    -   L’éclairage est désactivé, la couleur spéculaire est présente dans les flux de vertex d’entrée et [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) n’est pas défini.
    -   Le brouillard du vertex est activé ; autrement dit, D3DRS \_ FOGVERTEXMODE n’a pas la valeur D3DFOG \_ None.

En outre, le nombre de coordonnées de texture doit être défini de la manière suivante :

-   Si la transformation de texture et la génération de texture sont désactivées pour toutes les étapes de texture actives et que le [ \_ DONOTCOPYDATA D3DPV](other-direct3d-constants.md) n’est pas défini, le nombre et le type de coordonnées de texture de sortie sont requis pour correspondre à ceux des coordonnées de texture de vertex d’entrée. Si D3DPV \_ DONOTCOPYDATA est défini et que la transformation de texture et la génération de texture sont désactivées, les coordonnées de texture de sortie sont ignorées.
-   Si la transformation de texture ou la génération de texture est activée pour toute étape de texture active, le vertex de sortie peut avoir besoin de contenir plus de jeux de coordonnées de texture que le vertex d’entrée. Cela est dû à la prolifération des coordonnées de texture de celles qui sont générées par la génération de texture ou dérivées par des transformations de texture. Notez qu’une prolifération similaire des coordonnées de texture se produit pendant [**IDirect3DDevice9 ::D appels rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , mais n’est pas visible par le programmeur de l’application. Dans ce cas, Direct3D génère un nouvel ensemble de coordonnées de texture. Le nouvel ensemble de coordonnées de texture est dérivé en exécutant pas à pas les étapes de texture et en analysant les paramètres de génération de texture, de transformation de texture et d’index de coordonnées de texture pour déterminer si un ensemble unique de coordonnées de texture est requis pour cette étape. Chaque fois qu’un nouvel ensemble est requis, il est alloué par ordre de tri. Notez que la spécification maximale, et standard, est un jeu par étape, bien qu’elle puisse être moins due au partage de coordonnées de texture non transformées via D3DTSS \_ TEXCOORDINDEX.

Ainsi, pour chaque étape de texture, un nouvel ensemble de coordonnées de texture est généré si une texture est liée à cette étape et que l’une des conditions suivantes est vraie :

-   La génération de texture est activée pour cette étape.
-   La transformation de texture est activée pour cette étape.
-   Les coordonnées de texture d’entrée non transformées sont référencées par \_ le biais de D3DTSS TEXCOORDINDEX pour la première fois.

Lorsque Direct3D génère des coordonnées de texture, l’application est requise pour effectuer les actions suivantes :

1.  Utilisez une mémoire tampon de vertex de destination avec l’utilisation appropriée de la Commission.
2.  Reprogrammez le \_ TEXCOORDINDEX D3DTSS de l’étape de texture en fonction de l’emplacement des coordonnées de texture postprocessed. Notez que la reprogrammation du paramètre D3DTSS \_ TEXCOORDINDEX se produit lorsque la mémoire tampon de vertex traitée est utilisée dans les appels suivants de [**IDirect3DDevice9 ::D Rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) et [**IDirect3DDevice9 ::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) .

Enfin, la dimensionnalité de la coordonnée de texture ([D3DFVF \_ TEX0](d3dfvf.md) à D3DFVF \_ TEX8) doit être définie de la manière suivante :

-   Pour chaque jeu de coordonnées de texture, si la transformation de texture et la génération de texture sont désactivées, la dimensionnalité de la coordonnée de texture de sortie doit correspondre à l’entrée. Si la transformation de texture est activée, la dimensionnalité de sortie doit correspondre au nombre défini par les \_ paramètres D3DTTFF COUNT1, D3DTTFF \_ COUNT2, D3DTTFF COUNT3 ou D3DTTFF COUNT4 \_ \_ . Si la transformation de texture est désactivée et que la génération de texture est activée, la dimensionnalité de sortie doit correspondre aux paramètres pour le mode de génération de texture ; actuellement, tous les modes génèrent trois valeurs float.

Quand [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) échoue en raison d’un code de la Commission de la Commission de tampon de destination incompatible, le code attendu est imprimé dans la sortie de débogage (versions Debug uniquement).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de vertex](vertex-buffers.md)
</dt> </dl>

 

 
