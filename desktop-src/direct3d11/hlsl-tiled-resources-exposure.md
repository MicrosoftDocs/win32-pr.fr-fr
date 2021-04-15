---
title: Exposition des ressources en mosaïque HLSL
description: La nouvelle syntaxe HLSL (High Level Shader Language) de Microsoft est requise pour prendre en charge les ressources en mosaïque dans le nuancier Model 5.
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b266b98045b38645e1e8d24ed0014a5f448a38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463387"
---
# <a name="hlsl-tiled-resources-exposure"></a>Exposition des ressources en mosaïque HLSL

La nouvelle syntaxe HLSL (High Level Shader Language) de Microsoft est requise pour prendre en charge les ressources en mosaïque dans le [nuancier Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).

La nouvelle syntaxe HLSL est autorisée uniquement sur les appareils avec prise en charge des ressources en mosaïque. Chaque méthode HLSL appropriée pour les ressources en mosaïque dans le tableau suivant accepte soit un (commentaire) soit deux (verrouillage et commentaires dans cet ordre) des paramètres facultatifs supplémentaires. Par exemple, voici un **exemple** de méthode :

**Exemple (échantillonneur, emplacement \[ , décalage \[ , bride \[ , commentaires \] \] \] )**

[**Texture2D. Sample (S, float, int, float, uint)**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-)est un exemple de méthode d' **exemple** .

Les paramètres décalage, Clamp et Feedback sont facultatifs. Vous devez spécifier tous les paramètres facultatifs jusqu’à celui dont vous avez besoin, ce qui est cohérent avec les règles C++ pour les arguments de fonction par défaut. Par exemple, si l’état des commentaires est requis, les paramètres de décalage et de fixation doivent être fournis explicitement à **Sample**, même s’ils ne sont pas nécessaires logiquement.

Le paramètre clamp est une valeur flottante scalaire. La valeur littérale de Clamp = 0.0 f indique que l’opération de verrouillage n’est pas effectuée.

Le paramètre feedback est une variable **uint** que vous pouvez fournir à la fonction [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) intrinsèque d’interrogation de l’accès mémoire. Vous ne devez pas modifier ni interpréter la valeur du paramètre Feedback ; Toutefois, le compilateur ne fournit aucune analyse et aucun diagnostic avancés pour déterminer si vous avez modifié la valeur.

Voici la syntaxe de [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped):

**bool CheckAccessFullyMapped (dans uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interprète la valeur de *FeedbackVar* et retourne true si toutes les données en cours d’accès ont été mappées dans la ressource ; Sinon, **CheckAccessFullyMapped** retourne false.

Si le paramètre clamp ou feedback est présent, le compilateur émet une variante de l’instruction de base. Par exemple, l’exemple d’une ressource en mosaïque génère l' `sample_cl_s` instruction. Si ni clamp ni Feedback n’est spécifié, le compilateur émet l’instruction de base, afin qu’il n’y ait aucune modification par rapport au comportement actuel. La valeur Clamp de 0.0 f indique qu’aucune bride n’est exécutée ; ainsi, le compilateur de pilotes peut affiner l’instruction sur le matériel cible. Si les commentaires sont un registre NULL dans une instruction, les commentaires ne sont pas utilisés ; par conséquent, le compilateur de pilotes peut adapter l’instruction à l’architecture cible.

Si le compilateur HLSL déduit que la bride est 0.0 f et que les commentaires sont inutilisés, le compilateur émet l’instruction de base correspondante (par exemple, `sample` plutôt que `sample_cl_s` ).

Si un accès aux ressources en mosaïque est constitué de plusieurs instructions de code d’octet constitutives, par exemple, pour les ressources structurées, le compilateur agrège les valeurs de commentaires individuelles via l’opération ou pour produire la valeur de retour finale. Par conséquent, vous voyez une valeur de commentaire unique pour un accès complexe.

Il s’agit de la table de résumé des méthodes HLSL qui sont modifiées pour prendre en charge les commentaires et/ou la fixation. Tout fonctionne sur les ressources en mosaïque et non en mosaïque de toutes les dimensions. Les ressources non juxtaposées semblent toujours être entièrement mappées.



| [Objets HLSL](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Méthodes intrinsèques avec l’option Feedback ( \* )-possède également l’option clamp                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[\]TEXTURE2D RW<br/> \[\]TEXTURE2DARRAY RW<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | Gather<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[\]TEXTURE1D RW<br/> \[\]TEXTURE1DARRAY RW<br/> \[\]TEXTURE2D RW<br/> \[\]TEXTURE2DARRAY RW<br/> \[\]TEXTURE3D RW<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | Exemple\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[\]TEXTURE1D RW<br/> \[\]TEXTURE1DARRAY RW<br/> \[\]TEXTURE2D RW<br/> Texture2DMS<br/> \[\]TEXTURE2DARRAY RW<br/> Texture2DArrayMS<br/> \[\]TEXTURE3D RW<br/> \[\]Mémoire tampon RW<br/> \[\]BYTEADDRESSBUFFER RW<br/> \[\]STRUCTUREDBUFFER RW<br/> | Load                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès du pipeline aux ressources en mosaïque](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

