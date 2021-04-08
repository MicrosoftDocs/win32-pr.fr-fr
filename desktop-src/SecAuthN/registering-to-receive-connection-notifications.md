---
description: Après avoir créé une DLL pour recevoir des notifications de connexion, vous devez l’inscrire auprès du système.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Inscription pour recevoir des notifications de connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756423"
---
# <a name="registering-to-receive-connection-notifications"></a>Inscription pour recevoir des notifications de connexion

Après avoir créé une DLL pour recevoir des notifications de connexion, vous devez l’inscrire auprès du système. Pour ce faire, ajoutez une valeur de la valeur **\_ \_ SZ reg Expand** sous le

**HKEY \_ \_** \\  \\  \\  \\  \\ **Notifications** de contrôles CurrentControlSet du système d’ordinateur local NetworkProvider

application. Cette valeur spécifie le chemin d’accès à la DLL qui implémente l' [API de notification de connexion](connection-notification-api.md).

La valeur peut avoir n’importe quel nom. Toutes les valeurs sous la clé **Notify** sont traitées comme des chemins d’accès aux dll qui sont avertis des événements de connexion. Il est recommandé d’utiliser un nom qui identifie votre DLL. Cela réduit le risque d’un conflit de noms avec d’autres applications de notification de connexion.

Pour plus d’informations sur la création d’une application qui reçoit des notifications de connexion, consultez [réception de notifications de connexion](receiving-connection-notifications.md).

 

 



