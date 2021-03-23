---
title: Dessin indirect
description: Le dessin indirect permet de déplacer le parcours de scène et l’élimination du processeur vers le GPU, ce qui peut améliorer les performances. La mémoire tampon de commande peut être générée par le processeur ou le GPU.
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7731a662bc6064e635d68942e6b0b222adf1eda8
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/19/2020
ms.locfileid: "104548505"
---
# <a name="indirect-drawing"></a>Dessin indirect

Le dessin indirect permet de déplacer le parcours de scène et l’élimination du processeur vers le GPU, ce qui peut améliorer les performances. La mémoire tampon de commande peut être générée par le processeur ou le GPU.

-   [Signatures des commandes](#command-signatures)
-   [Structures de mémoire tampon d’argument indirect](#indirect-argument-buffer-structures)
-   [Création d’une signature de commande](#command-signature-creation)
    -   [Aucun argument n’est modifié](#no-argument-changes)
    -   [Constantes racine et mémoires tampons de vertex](#root-constants-and-vertex-buffers)
-   [Rubriques connexes](#related-topics)

## <a name="command-signatures"></a>Signatures des commandes

L’objet de signature de commande ([**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) permet aux applications de spécifier un dessin indirect, en particulier en définissant les éléments suivants :

-   Format de la mémoire tampon des arguments indirects.
-   Type de commande qui sera utilisé (à partir des [](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) méthodes ID3D12GraphicsCommandList [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced), [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)ou [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)).
-   Ensemble des liaisons de ressources qui vont changer l’appel par commande par rapport à l’ensemble qui sera hérité.

Au démarrage, une application crée un petit ensemble de **signatures de commande**. Lors de l’exécution, l’application remplit une mémoire tampon avec des commandes (par quelque moyen que le développeur de l’application choisit). Les commandes contiennent éventuellement l’État à définir pour les vues de mémoire tampon de vertex, les vues de mémoire tampon d’index, les constantes racine et les descripteurs racine (RAW ou Structured SRV/UAV/CBVs). Ces dispositions d’arguments ne sont pas spécifiques au matériel, ce qui permet aux applications de générer les tampons directement. La signature de la commande hérite de l’État restant de la liste de commandes. L’application appelle ensuite [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) pour indiquer au GPU d’interpréter le contenu de la mémoire tampon d’argument indirect en fonction du format défini par une signature de commande particulière.

Si la signature de la commande modifie des arguments racine, elle est stockée dans la signature de la commande en tant que sous-ensemble d’une signature racine.

Notez qu’aucun État de la signature de la commande ne renvoie à la liste des commandes lorsque l’exécution est terminée.

Par exemple, supposons qu’un développeur d’applications souhaite qu’une constante racine unique soit spécifiée par appel de dessin dans la mémoire tampon d’argument indirect. L’application crée une signature de commande qui permet à la mémoire tampon d’arguments indirects de spécifier les paramètres suivants par appel de dessin :

-   Valeur d’une constante racine.
-   Les arguments de dessin (nombre de vertex, nombre d’instances, etc.).

La mémoire tampon d’argument indirecte générée par l’application contient un tableau d’enregistrements de taille fixe. Chaque structure correspond à un appel de dessin. Chaque structure contient les arguments de dessin et la valeur de la constante racine. Le nombre d’appels de dessin est spécifié dans une mémoire tampon visible par GPU distincte.

Voici un exemple de mémoire tampon de commande généré par l’application :

![format de mémoire tampon de commande](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>Structures de mémoire tampon d’argument indirect

Les structures suivantes définissent la façon dont les arguments particuliers s’affichent dans une mémoire tampon d’arguments indirects. Ces structures n’apparaissent dans aucune API D3D12. Les applications utilisent ces définitions lors de l’écriture dans un tampon d’arguments indirect (avec le processeur ou le GPU) :

-   [**\_Arguments de dessin D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ dessiner des \_ arguments indexés \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**\_Arguments de dispatch D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**\_Vue de \_ mémoire tampon de vertex D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**\_Vue de \_ mémoire tampon d’index D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   \_ \_ Adresse virtuelle du GPU D3D12 \_ (un typedef synonyme de UINT64).
-   [**\_Vue de \_ mémoire tampon constante D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>Création d’une signature de commande

Pour créer une signature de commande, utilisez les éléments d’API suivants :

-   [**ID3D12Device :: CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (génère un [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature))
-   [**\_Type d' \_ argument \_ indirect D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**Description de l' \_ argument D3D12 indirect \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**Description de la signature de la \_ commande D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

L’ordonnancement des arguments au sein d’un tampon d’arguments indirect est défini pour correspondre exactement à l’ordre des arguments spécifiés dans le paramètre *pArguments* de la description de la signature de la [**\_ commande \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Tous les arguments d’un appel Draw (Graphics)/Dispatch (Compute) dans une mémoire tampon d’arguments indirects sont étroitement compressés. Toutefois, les applications sont autorisées à spécifier un Stride d’octet arbitraire entre les commandes de dessin/Dispatch dans une mémoire tampon d’arguments indirecte.

La signature racine doit être spécifiée si et seulement si la signature de la commande modifie l’un des arguments racine.

Pour la racine SRV/UAV/CBV, la taille spécifiée de l’application est en octets. La couche de débogage valide les restrictions suivantes sur l’adresse :

-   CBV – Address doit être un multiple de 256 octets.
-   SRV brut/UAV : l’adresse doit être un multiple de 4 octets.
-   SRV/UAV structuré : l’adresse doit être un multiple de la structure de l’octet de structure (déclaré dans le nuanceur).

Une signature de commande donnée est un dessin ou une signature de commande de calcul. Si une signature de commande contient une opération de dessin, il s’agit d’une signature de commande Graphics. Dans le cas contraire, la signature de commande doit contenir une opération de répartition, et il s’agit d’une signature de commande de calcul.

Les sections suivantes présentent quelques exemples de signatures de commande.

### <a name="no-argument-changes"></a>Aucun argument n’est modifié

Dans cet exemple, la mémoire tampon d’arguments indirects générée par l’application contient un tableau de structures de 36 octets. Chaque structure contient uniquement les cinq paramètres passés à [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (plus le remplissage).

Le code permettant de créer la description de la signature de la commande est le suivant :

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

La disposition d’une structure unique dans une mémoire tampon d’arguments indirects est la suivante :



| Octets | Description           |
|-------|-----------------------|
| 0:3   | IndexCountPerInstance |
| 4:7   | InstanceCount         |
| 8:11  | StartIndexLocation    |
| 12:15 | BaseVertexLocation    |
| 16:19 | StartInstanceLocation |
| 20:35 | Remplissage               |



 

### <a name="root-constants-and-vertex-buffers"></a>Constantes racine et mémoires tampons de vertex

Dans cet exemple, chaque structure d’un tampon d’arguments indirect modifie deux constantes racine, modifie une liaison de mémoire tampon de vertex et effectue une opération de dessin non indexée. Il n’y a pas de remplissage entre les structures.

Le code permettant de créer la description de la signature de la commande est le suivant :

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.VBSlot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INSTANCED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

La disposition d’une structure unique au sein de la mémoire tampon d’argument indirect est la suivante :



| Octets | Description                     |
|-------|---------------------------------|
| 0:3   | Données pour l’index de paramètre racine 2 |
| 4:7   | Données pour l’index de paramètre racine 6 |
| 8:15  | Adresse virtuelle de VB (64 bits)  |
| 16:19 | Taille VB                         |
| 20:23 | STRIDE VB                       |
| 24:27 | VertexCountPerInstance          |
| 28:31 | InstanceCount                   |
| 32:35 | StartVertexLocation             |
| 36:39 | StartInstanceLocation           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Didacticiels vidéo sur DirectX Advanced Learning : exécuter des éliminations de GPU indirectes et Async](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Dessin indirect et élimination du GPU : parcours du code](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[Rendu](rendering.md)
</dt> </dl>

 

 