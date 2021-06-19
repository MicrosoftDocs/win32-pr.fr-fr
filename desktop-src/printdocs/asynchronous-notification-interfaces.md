---
description: En savoir plus sur les interfaces utilisées pour la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notification d’impression asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396094"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfaces de notification d’impression asynchrone

Les interfaces suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.

## <a name="in-this-section"></a>Contenu de cette section



| Interface                                                                     | Description                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Crée et gère un canal de communication utilisé par les applications et les composants qui sont hébergés par le spouleur d’impression.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Représente un canal de communication utilisé par les composants hébergés par le spouleur d’impression pour envoyer des notifications aux applications. Si le canal est bidirectionnel, les applications peuvent utiliser le même canal pour renvoyer des réponses au composant.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Encapsule les données envoyées dans un canal de notification. <br/>                                                                                                                                                                                             |



 

 

 




