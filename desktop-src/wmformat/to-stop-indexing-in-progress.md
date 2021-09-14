---
title: Pour arrêter l’indexation en cours
description: Pour arrêter l’indexation en cours
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Media Format SDK, arrêt de l’indexation en cours
- ASF (Advanced Systems Format), arrêt de l’indexation en cours
- ASF (format avancé des systèmes), arrêt de l’indexation en cours
- index, arrêt de l’indexation en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195920"
---
# <a name="to-stop-indexing-in-progress"></a>Pour arrêter l’indexation en cours

Une fois que vous avez commencé l’indexation à l’aide d’un appel à [**IWMIndexer :: StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), l’indexeur continue normalement jusqu’à ce que le fichier soit indexé. Vous pouvez arrêter les opérations d’indexation en appelant la méthode [**IWMIndexer :: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) . Après avoir annulé l’indexation, vous pouvez appeler de nouveau **StartIndexing** , mais l’indexeur démarrera à partir du début du fichier au lieu de reprendre à partir du point d’annulation.

Étant donné que **StartIndexing** est un appel asynchrone, vous devrez normalement appeler **Cancel** à partir d’un autre thread ou gestionnaire d’événements dans votre application. en général, **Cancel** est appelé à partir d’une procédure d’événement associée à un contrôle button d’une application Windows.

Lorsque l’indexation est annulée, l’indexeur transmet un message d’état de WMT \_ Closed, comme si le fichier avait été indexé correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




