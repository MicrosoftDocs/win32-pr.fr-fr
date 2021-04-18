---
description: Les interfaces suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Fonctions de notification d’impression asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520162"
---
# <a name="asynchronous-printing-notification-functions"></a>Fonctions de notification d’impression asynchrone

Les interfaces suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.

## <a name="in-this-section"></a>Dans cette section



| Fonction                                                                                        | Description                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Crée un canal de communication entre un composant d’impression hébergé par le spouleur d’impression, tel qu’un pilote d’impression ou un moniteur de port, et une application qui reçoit les notifications du composant.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Permet à une application de s’inscrire aux notifications à partir de composants d’impression hébergés par le spouleur d’impression, tels que les pilotes d’imprimante, les processeurs d’impression et les moniteurs de port.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Permet à une application qui s’est inscrite de recevoir des notifications des composants d’impression hébergés par le spouleur d’impression de se désinscrire.<br/>                                                              |



 

 

 




