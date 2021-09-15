---
title: Comment lire une liste de commandes
description: Cette rubrique montre comment lire une liste de commandes.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517521"
---
# <a name="how-to-play-back-a-command-list"></a>Comment : lire une liste de commandes

Une [liste](overviews-direct3d-11-render-multi-thread-command-list.md) de commandes est une liste enregistrée de commandes de rendu. Utilisez une liste de commandes pour pré-enregistrer les commandes de dessin et les relire ultérieurement. Cette rubrique montre comment lire une liste de [commandes](overviews-direct3d-11-render-multi-thread-command-list.md). Une liste de commandes peut être utilisée pour fractionner les tâches de rendu entre les threads.

Cette section décrit comment lire une liste de commandes. Pour enregistrer une liste de commandes, consultez [Comment : enregistrer une liste de commandes](overviews-direct3d-11-render-multi-thread-command-list-record.md).

**Pour lire une liste de commandes**

-   Appelez [**ID3D11DeviceContext :: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) et transmettez un objet [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) valide.
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) doit être exécuté dans le [contexte immédiat](overviews-direct3d-11-devices-intro.md) pour que les commandes enregistrées soient exécutées sur l’unité de traitement graphique (GPU). Utilisez le contexte immédiat pour alimenter les commandes vers le GPU en vue de leur exécution, utilisez un contexte différé pour enregistrer les commandes de lecture dans une autre liste de commandes. Lorsque vous appelez **ExecuteCommandList** sur un autre contexte différé, vous créez une liste de commandes différée « fusionnée ». Pour exécuter les commandes sur la liste de commandes différée fusionnée, vous devez les exécuter dans le contexte immédiat.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liste des commandes](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




