---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3931c277fbe4a5943ef5881da12cf3669b2e8894c95052f61bc8411e21c7ae3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751423"
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
| [**Annuler**](iagent--register.md)         | Inscrit un récepteur de notification pour le client.                 |
| [**Unegister**](iagent--unregister.md)      | Annule l’inscription du récepteur de notification d’un client.                     |
| [**GetCharacter**](iagent--getcharacter.md) | Retourne l’interface IAgentCharacter pour un caractère chargé. |



 

 

 




