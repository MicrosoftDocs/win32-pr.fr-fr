---
description: Erreurs de Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Erreurs de Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013008"
---
# <a name="client-side-errors"></a>Erreurs de Client-Side

Les défaillances côté client sont gérées d’une manière similaire aux défaillances côté serveur. [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) pouvez déplacer un message vers sa file d’attente de destination si, par exemple, le message ne peut pas être déplacé du client vers le serveur. Dans ce cas, le message est déplacé vers la file d’attente de lettres mortes côté client.

Le service composants en file d’attente COM+ analyse la file d’attente de lettres mortes. Si des messages ont été déplacés, le service Queued Components crée une instance de la classe exception et appelle [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour demander [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). En cas de réussite, le moniteur de file d’attente de lettres mortes appelle [**IPlaybackControl :: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).

L’objet peut entreprendre une action pour inverser l’effet d’une transaction antérieure. Si la lecture est validée, le message est supprimé de la file d’attente de lettres mortes Xact. Si la lecture échoue ou si le CLSID et l’interface requis ne sont pas disponibles, le message reste dans la file d’attente de lettres mortes Xact.

Si vous devez intervenir dans le processus décrit ci-dessus ou si vous devez déplacer un message incohérent hors de sa file d’attente Rest finale, utilisez l’utilitaire de déplacement de messages. Pour plus d’informations sur l’utilitaire de déplacement de messages, consultez [gestion des erreurs](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Échecs de Client-Side persistant](persistent-client-side-failures.md)
</dt> <dt>

[Erreurs côté serveur](server-side-errors.md)
</dt> </dl>

 

 
