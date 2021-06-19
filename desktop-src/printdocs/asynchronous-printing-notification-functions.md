---
description: Découvrez les fonctions utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Fonctions de notification d’impression asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc9a404d1675c8ee87be31c7c57dd14a370697c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394854"
---
# <a name="asynchronous-printing-notification-functions"></a>Fonctions de notification d’impression asynchrone

Les fonctions suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.

## <a name="in-this-section"></a>Contenu de cette section



| Fonction                                                                                        | Description                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Crée un canal de communication entre un composant d’impression hébergé par le spouleur d’impression, tel qu’un pilote d’impression ou un moniteur de port, et une application qui reçoit les notifications du composant.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Permet à une application de s’inscrire aux notifications à partir de composants d’impression hébergés par le spouleur d’impression, tels que les pilotes d’imprimante, les processeurs d’impression et les moniteurs de port.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Permet à une application qui s’est inscrite de recevoir des notifications des composants d’impression hébergés par le spouleur d’impression de se désinscrire.<br/>                                                              |



 

 

 




