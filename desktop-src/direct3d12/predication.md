---
title: Prédication
description: Un prédicat est une fonctionnalité qui permet au GPU plutôt qu’au processeur de déterminer de ne pas dessiner, copier ou distribuer un objet.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548581"
---
# <a name="predication"></a>Prédication

Un prédicat est une fonctionnalité qui permet au GPU plutôt qu’au processeur de déterminer de ne pas dessiner, copier ou distribuer un objet.

-   [Vue d'ensemble](#overview)
-   [SetPredication](#setpredication)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

L’utilisation classique de la prédicat est avec l’occlusion ; Si un cadre englobant est dessiné et est bloqués, il n’y a évidemment aucun point dans le dessin de l’objet lui-même. Dans ce cas, le dessin de l’objet peut être « prédicat », ce qui permet sa suppression du rendu réel par le GPU.

Dans un premier temps, cela peut paraître redudant au-dessus du test de profondeur standard plus une passe de profondeur. Toutefois, un prédicat peut supprimer la surcharge de l’état de la commande de dessin, ainsi que la pixellisation. Tandis qu’un test de profondeur précoce supprime les pixels inutiles, il peut toujours exécuter des nuanceurs de vertex, de coques, de domaines et de géométrie, et appeler l’assembleur d’entrée de fonction fixe, Tesselator et rastériseur. En dessinant un simple cadre englobant ou un volume englobant similaire &mdash; qui est plus simple à traiter et à pixelliser que le modèle réel, &mdash; vous évitez la pixellisation et le traitement inutiles.

Contrairement à Direct3D 11, le prédicat est dissocié des requêtes et est développé dans Direct3D 12 pour permettre à une application de définir des prédicats d’objets en fonction de tout raisonnement que le développeur de l’application peut décider (pas seulement d’occlusion).

## <a name="setpredication"></a>SetPredication

Un prédicat peut être défini en fonction de la valeur de 64 bits dans une mémoire tampon (reportez-vous à [**D3D12 \_ Predicate \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).

Lorsque le GPU exécute une commande [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , il aligne la valeur dans la mémoire tampon. Les modifications ultérieures apportées aux données dans la mémoire tampon n’affectent pas rétroactivement l’état de prédicat.

Si la mémoire tampon du paramètre d’entrée a la valeur NULL, la prédicat est désactivé.

Les indicateurs de prédicat ne sont pas présents dans l’API Direct3D 12 ; les prédicats et sont autorisés sur les listes de commandes directes, de calcul et de copie. La mémoire tampon source peut être dans n’importe quel type de segment (par défaut, charger, readback, personnalisé).

Le runtime principal validera les éléments suivants :

-   *AlignedBufferOffset* est un multiple de 8 octets
-   La ressource est une mémoire tampon
-   L’opération est un membre valide de l’énumération
-   [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) ne peut pas être appelé à partir d’un bundle
-   Le type de liste de commandes prend en charge la prédicat
-   Le décalage ne dépasse pas la taille de la mémoire tampon

La couche de débogage génère une erreur si la mémoire tampon source n’est pas dans le [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (ce qui est identique à [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), et simplement à un alias).

L’ensemble d’opérations qui peut être prédicat est le suivant :

-   [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) n’est pas prédicat lui-même. Au lieu de cela, les opérations individuelles de la liste ci-dessus qui sont contenues dans le regroupement sont prédicats.

Les méthodes ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) et [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) ne sont pas prédicats.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compteurs et requêtes](counters-and-queries.md)
</dt> <dt>

[Mesure des performances](performance-measurement.md)
</dt> <dt>

[Parcours des requêtes de prédicat](predication-queries.md)
</dt> </dl>

 

 




