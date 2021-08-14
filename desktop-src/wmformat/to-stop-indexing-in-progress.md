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
ms.openlocfilehash: 9d441e42bc3c7033e776d353cf64fc5938183a4f8d720f086b4fb5fd9828be02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432622"
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

 

 




