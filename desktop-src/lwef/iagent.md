---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310050"
---
# <a name="iagent"></a>IAgent

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

**IAgent** définit une interface qui permet aux applications de charger des caractères, de recevoir des événements et de vérifier l’état actuel du serveur Microsoft Agent. Ces fonctions sont également disponibles à partir de [**IAgentEx**](iagentex.md).

La méthode GetSuspended incluse dans les versions précédentes est obsolète et retourne **false** pour la compatibilité descendante.

**Méthodes dans l'ordre Vtable**



| Méthodes IAgent                               | Description                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Load**](load-method.md)                  | Charge le fichier de données d’un caractère.                                |
| [**Décharger**](unload-method.md)              | Décharge le fichier de données d’un caractère.                              |
| [**S’inscrire**](iagent--register.md)         | Inscrit un récepteur de notification pour le client.                 |
| [**Unegister**](iagent--unregister.md)      | Annule l’inscription du récepteur de notification d’un client.                     |
| [**GetCharacter**](iagent--getcharacter.md) | Retourne l’interface IAgentCharacter pour un caractère chargé. |



 

 

 




