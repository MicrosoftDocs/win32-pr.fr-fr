---
title: Enregistrement d’une liste de commandes
description: Cette rubrique montre comment créer et enregistrer une liste de commandes.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4590d7e6a3a309b756bbac154a3240541f1b525a0dd877e13ba77badccff841
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894449"
---
# <a name="how-to-record-a-command-list"></a>Comment : enregistrer une liste de commandes

Une [liste](overviews-direct3d-11-render-multi-thread-command-list.md) de commandes est une liste enregistrée de commandes de rendu. Cette rubrique montre comment créer et enregistrer une [liste de commandes](overviews-direct3d-11-render-multi-thread-command-list.md). Utilisez une liste de commandes pour enregistrer les commandes de rendu et les lire ultérieurement. Une liste de commandes est pratique pour fractionner les tâches de rendu entre les threads.

**Pour enregistrer une liste de commandes**

1.  Une liste de commandes doit être créée à partir d’un contexte différé, qui contient l’état de l’appareil et les actions de rendu. Pour un appareil donné, créez un contexte différé en appelant [**ID3D11Device :: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  Utilisez le contexte différé pour effectuer le rendu.

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    Cet exemple simple efface une cible de rendu, mais vous pouvez ajouter des commandes de rendu supplémentaires.

3.  Créez/enregistrez une liste de commandes en appelant [**ID3D11DeviceContext :: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) et en passant un pointeur vers une interface [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) non initialisée.

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    Lorsque la méthode retourne une valeur, une liste de commandes est créée, contenant toutes les commandes de rendu et une interface est retournée à l’application.

    Le paramètre booléen indique au runtime ce qu’il faut faire avec l’état du pipeline dans le contexte différé. **True** signifie restaurer l’état du contexte de périphérique dans sa condition de liste de pré-commandes lorsque l’enregistrement est terminé, **false** signifie ne pas modifier l’état après l’enregistrement. Cela signifie que le contexte de périphérique reflète les modifications d’État contenues dans la liste de commandes.

Pour voir un exemple de lecture d’une liste de commandes, consultez [Comment : lire une liste de commandes](overviews-direct3d-11-render-multi-thread-command-list-play.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liste des commandes](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




