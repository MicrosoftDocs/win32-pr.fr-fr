---
description: L’objet CallHub représente une vue tierce d’un appel en une partie.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Objet CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952354"
---
# <a name="callhub-object"></a>Objet CallHub

L’objet CallHub représente une vue tierce d’un appel en une partie. Les interfaces et les méthodes associées obtiennent et définissent des informations relatives au concentrateur, par exemple s’il est actif ou non. À l’aide de l’objet CallHub, un utilisateur ayant la sécurité requise peut découvrir et contrôler potentiellement les autres participants dans un appel.

Un objet CallHub ne peut pas être créé directement par une application. Un objet CallHub est créé indirectement lors de la réception d’un appel entrant via TAPI 3.

TAPI 3 s’appuie sur les fournisseurs de services TAPI pour fournir les informations nécessaires sur les appels à implémenter à l’aide de l’objet CallHub. Étant donné que tous les fournisseurs de services ne fournissent pas ces informations, et que tous les matériels ne prennent pas en charge le suivi des concentrateurs d’appels, les informations disponibles sur les autres utilisateurs de la connexion peuvent être limitées ou inexistantes.

L’exemple de code de [création d’une conférence simple](create-a-simple-conference.md) illustre l’utilisation d’un objet CallHub.

Consultez la page interfaces de l' [objet CallHub](callhub-object-interfaces.md) pour obtenir la liste de toutes les interfaces associées à l’objet CallHub.

 

 



