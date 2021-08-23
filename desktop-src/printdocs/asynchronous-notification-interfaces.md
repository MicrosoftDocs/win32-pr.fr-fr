---
description: En savoir plus sur les interfaces utilisées pour la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notification d’impression asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357610b30d01b89ed8fd7e2fe7354f727a44c8f04b41d71d846af622113aa435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720219"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfaces de notification d’impression asynchrone

Les interfaces suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.

## <a name="in-this-section"></a>Dans cette section



| Interface                                                                     | Description                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Crée et gère un canal de communication utilisé par les applications et les composants qui sont hébergés par le spouleur d’impression.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Représente un canal de communication utilisé par les composants hébergés par le spouleur d’impression pour envoyer des notifications aux applications. Si le canal est bidirectionnel, les applications peuvent utiliser le même canal pour renvoyer des réponses au composant.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Encapsule les données envoyées dans un canal de notification. <br/>                                                                                                                                                                                             |



 

 

 




