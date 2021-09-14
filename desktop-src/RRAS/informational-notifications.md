---
title: Notifications d’information
description: Pour les États de connexion connus sous le nom d’état d’exécution, aucune action n’est requise du gestionnaire de notification à moins qu’une erreur ne se produise.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194279"
---
# <a name="informational-notifications"></a>Notifications d’information

Pour les [États de connexion](connection-states.md) connus sous le nom d’état d’exécution, aucune action n’est requise du gestionnaire de notification à moins qu’une erreur ne se produise. Les États en cours d’exécution se produisent pendant les parties de l’opération de connexion que RAS gère automatiquement, comme la connexion aux appareils nécessaires, l’authentification de l’utilisateur et l’attente d’un rappel du serveur distant. La notification est simplement un rapport de progression vers le client.

Le client peut choisir de transmettre ces notifications d’information à l’utilisateur. Dans certains États en cours d’exécution, le client peut souhaiter afficher des informations supplémentaires. Par exemple, un gestionnaire de notification qui reçoit une \_ notification CONNECTDEVICE RASCS peut appeler la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour obtenir le nom et le type de l’appareil auquel la connexion est établie. Un autre exemple est lorsque le client reçoit une \_ notification RASCS Projected. Cela se produit lorsque la phase de projection RAS de l’opération de connexion est terminée. Le client peut appeler la fonction [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) pour obtenir des informations supplémentaires sur la projection. Le client peut utiliser ces informations pour indiquer à l’utilisateur les protocoles réseau qui peuvent être utilisés par cette connexion.

Vous devez éviter d’écrire du code qui dépend de l’ordre ou de l’occurrence d’États d’information particuliers, car cela peut varier d’une plateforme à l’autre.

 

 




