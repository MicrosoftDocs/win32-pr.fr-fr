---
title: Gestion de l’état des pipelines graphiques dans Direct3D 12
description: Cette rubrique décrit comment l’état du pipeline graphique est défini dans Direct3D 12.
ms.assetid: AAF97BD2-D532-469D-9242-CC94C06727C3
keywords:
- État du pipeline
- objet d’État du pipeline
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7564b5863d3efebdf8a335e2c46945aeebea93e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548617"
---
# <a name="managing-graphics-pipeline-state-in-direct3d-12"></a>Gestion de l’état des pipelines graphiques dans Direct3D 12

Cette rubrique décrit comment l’état du pipeline graphique est défini dans Direct3D 12.

## <a name="pipeline-state-overview"></a>Vue d’ensemble de l’état du pipeline

Lorsque la géométrie est soumise à l’unité de traitement graphique (GPU) à dessiner, il existe un large éventail de paramètres matériels qui déterminent la façon dont les données d’entrée sont interprétées et rendues. Collectivement, ces paramètres sont appelés l’état du pipeline graphique et incluent des paramètres communs tels que l’état du rastériseur, l’état de fusion et l’état du stencil de profondeur, ainsi que le type de topologie primitif de la géométrie soumise et les nuanceurs qui seront utilisés pour le rendu. Dans Microsoft Direct3D 12, la plupart des États de pipeline graphique sont définis à l’aide d’objets d’état de pipeline (PSO). Une application peut créer un nombre illimité de ces objets, représentés par l’interface [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) , généralement au moment de l’initialisation. Ensuite, au moment du rendu, les listes de commandes peuvent rapidement basculer entre plusieurs paramètres de l’état du pipeline en appelant [**ID3D12GraphicsCommandList :: SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate) dans une liste de commandes directe ou un bundle pour définir le PSO actif.

Dans Direct3D 11, l’état des pipelines graphiques a été regroupé en grands objets d’État à granularité grossière tels que [**ID3D11BlendState**](/windows/win32/api/d3d11/nn-d3d11-id3d11blendstate) qui pouvaient être créés et définis au moment du rendu dans le contexte immédiat avec des méthodes telles que [**ID3D11DeviceContext :: OMSetBlendState**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-omsetblendstate). L’idée derrière cela était que le GPU pouvait gagner en efficacité en définissant les paramètres associés, comme les paramètres d’état de fusion, en même temps. Toutefois, avec le matériel graphique d’aujourd’hui, il existe des dépendances entre les différentes unités matérielles. Par exemple, l’état de fusion matérielle peut avoir des dépendances avec l’état de pixellisation, ainsi que pour l’état de fusion. Dans Direct3D 12, objets PSO a été conçu pour permettre au GPU de prétraiter tous les paramètres dépendants dans chaque État de pipeline, généralement pendant l’initialisation, afin de rendre le basculement entre les États au moment du rendu le plus efficace possible.

Notez que, bien que la plupart des paramètres d’état de pipeline soient définis à l’aide de objets PSO, certains paramètres d’État sont définis séparément à l’aide des API fournies par [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist). Ces paramètres et les API associées sont présentés en détail ci-dessous. En outre, il existe des différences dans la façon dont l’état du pipeline graphique est hérité et conservé à partir des listes de commandes directes et des offres groupées. Cette rubrique fournit des détails sur les deux éléments ci-dessous.

## <a name="graphics-pipeline-states-set-with-pipeline-state-objects"></a>États de pipeline Graphics définis avec des objets d’état de pipeline

Le moyen le plus simple d’afficher tous les différents États de pipeline qui peuvent être définis à l’aide d’un objet d’état de pipeline consiste à consulter la rubrique de référence pour la description de l' [**\_ \_ \_ état \_ du pipeline Graphics D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) que vous transmettez à [**ID3D12Device :: CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) lorsque vous initialisez l’objet. Un résumé rapide des États qui peuvent être définis comprend les éléments suivants :

-   P-code pour tous les nuanceurs, y compris les nuanceurs, les vertex, les pixels, les domaines, les coques et les géométries.
-   Format du vertex d’entrée.
-   Type de topologie primitif. Notez que le type de topologie primitif d’assembleur d’entrée (point, ligne, triangle, correctif) est défini dans l’PSO à l’aide de l’énumération de [**\_ \_ \_ type de topologie primitive D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) . L’adjacence et le classement primitifs (liste de lignes, bande, ligne avec les données d’adjacence, etc.) sont définis à partir d’une liste de commandes à l’aide de la méthode [**ID3D12GraphicsCommandList :: IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology) .
-   État de fusion, état du rastériseur, état du stencil de profondeur.
-   Le stencil de profondeur et les formats de cible de rendu, ainsi que le nombre de cibles de rendu.
-   Paramètres d’échantillonnage multiple.
-   Mémoire tampon de sortie de diffusion en continu.
-   Signature racine. Pour plus d’informations, consultez [signatures racines](root-signatures.md).

## <a name="graphics-pipeline-states-set-outside-of-the-pipeline-state-object"></a>États du pipeline Graphics définis en dehors de l’objet d’État du pipeline

La plupart des États de pipeline Graphics sont définis à l’aide de objets PSO. Toutefois, il existe un ensemble de paramètres d’état de pipeline qui sont définis en appelant des méthodes de l’interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) à partir d’une liste de commandes. Le tableau suivant présente les États définis de cette façon et les méthodes correspondantes.

|État|Méthode|
|-|-|
|Liaisons de ressources|[**IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)<br/>[**IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)<br/>[**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)<br/>[**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)<br/>[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)<br/>Toutes les méthodes **SetGraphicsRoot...**<br/>Toutes les méthodes **SetComputeRoot...**<br/>
|Fenêtres d’affichage|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">**RSSetViewports**</a>|
|Rectangles ciseaux|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects">**RSSetScissorRects**</a>|
|Facteur de fusion|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">**OMSetBlendFactor**</a>|
|Valeur de référence du stencil de profondeur|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">**OMSetStencilRef**</a>|
|Ordre de topologie primitif de l’assembleur d’entrée et type d’adjacence|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology">**IASetPrimitiveTopology**</a>|

## <a name="graphics-pipeline-state-inheritance"></a>Héritage de l’état du pipeline Graphics

Étant donné que les listes de commandes directes sont généralement destinées à une utilisation à la fois et que les offres groupées sont destinées à être utilisées plusieurs fois simultanément, il existe des règles différentes sur la façon dont elles héritent de l’état du pipeline graphique défini par les listes de commandes ou les offres groupées précédentes.

Pour les États de pipeline Graphics définis à l’aide de objets PSO, aucun de ces États n’est hérité par les listes de commandes directes ou les offres groupées. L’état initial du pipeline Graphics pour les listes de commandes directes et les offres groupées est défini au moment de la création avec le paramètre [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) sur [**ID3D12Device :: CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist). Si aucun PSO n’est spécifié dans l’appel, un état initial par défaut est utilisé. Vous pouvez modifier le PSO actuel dans une liste de commandes en appelant [**ID3D12GraphicsCommandList :: SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Les listes de commandes directes n’héritent pas non plus de l’état défini avec des méthodes de liste de commandes telles que [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports). Pour plus d’informations sur les valeurs initiales par défaut des États non-PSO, consultez [**ID3D12GraphicsCommandList :: ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate).

Les offres groupées héritent de tous les États de pipeline Graphics qui ne sont pas définis avec objets PSO, à l’exception du type de topologie primitif. La topologie primitive est toujours définie sur le [**\_ type de \_ topologie primitive \_ D3D12 \_ non défini**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) lorsqu’un bundle commence à s’exécuter. Tout état défini dans un bundle (l’PSO lui-même, l’état non-PSO et les liaisons de ressources) affecte l’état de sa liste de commandes directe parente. Par exemple, si un [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports) est appelé à partir d’un bundle, les Viewports spécifiés continuent d’être définis dans la liste de commandes directe parente pour les appels postérieurs à l’appel [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) qui définissent les fenêtres d’affichage.

Les liaisons de ressources définies dans une liste de commandes ou un bundle sont conservées. Ainsi, les liaisons de ressources modifiées dans une liste de commandes directe seront toujours définies au cours de l’exécution suivante du lot enfant. Les liaisons de ressources modifiées à partir d’un bundle seront toujours définies pour les appels suivants dans la liste de commandes directe parente.

Pour plus d’informations sur les liaisons, reportez-vous à la section **sémantique de regroupement** de [à l’aide d’une signature racine](using-a-root-signature.md).

## <a name="related-topics"></a>Rubriques connexes

* [Envoi de travail dans Direct3D 12](command-queues-and-command-lists.md)