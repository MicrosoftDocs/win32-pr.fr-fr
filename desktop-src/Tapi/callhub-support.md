---
description: Le suivi CallHub est une nouvelle fonctionnalité de TAPI version 3,0.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Support CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530609"
---
# <a name="callhub-support"></a>Support CallHub

Le suivi CallHub est une nouvelle fonctionnalité de TAPI version 3,0. La fonctionnalité CallHub a été ajoutée aux éléments de programmation TAPI 2,1 avec la remise de Windows 2000. Un *CallHub* représente une vue tierce d’un appel, et les handles d’appel de l’interface TAPI représentent la vue du premier tiers d’un appel. Avec le suivi CallHub, le fournisseur de services est invité à suivre CallHubs et à fournir des informations sur l’appel pendant la durée de vie d’un CallHub. À mesure que les nouveaux tiers joignent et laissent le CallHub, le fournisseur de services doit informer l’interface TAPI.

Un fournisseur de services n’a pas besoin d’implémenter de nouvelles fonctions pour prendre en charge CallHub. Elle doit simplement remplir le membre **dwCallID** de la structure [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) . Dans TAPI 3, l’interface TAPI collecte tous les appels avec le même **dwCallID** et crée un handle CallHub que l’application peut utiliser pour suivre l’appel.

 

 
