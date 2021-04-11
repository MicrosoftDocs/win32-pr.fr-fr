---
description: La suppression ou la déconnexion d’une session met fin à la communication. L’application a la possibilité d’envoyer des informations utilisateur-utilisateur au moment de la déconnexion, si le fournisseur de services la prend en charge.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Supprimer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951064"
---
# <a name="drop"></a>Supprimer

La suppression ou la déconnexion d’une session met fin à la communication. L’application a la possibilité d’envoyer des informations utilisateur-utilisateur au moment de la déconnexion, si le fournisseur de services la prend en charge.

Les raisons habituelles de la suppression d’une session sont qu’un utilisateur a demandé une déconnexion ou que l’autre extrémité de la session a été supprimée. Une opération Drop peut également être appelée lorsque l’interface TAPI offre une session à l’application. Si le fournisseur de services prend cela en charge, l’effet est que l’application rejette l’appel.

Lors de l’appel d’une opération de déplacement, les sessions associées peuvent parfois être affectées. Par exemple, la suppression d’un appel de conférence peut supprimer tous les participants individuels. Les messages de changement d’État sont envoyés à l’application pour tous les appels dont l’État est affecté.

Dans les configurations par pont ou par ligne de tiers lorsque plusieurs tiers sont sur l’appel, une opération de suppression peut ne pas réellement effacer l’appel. Par exemple, dans une situation de pont, l’appel ne peut pas être supprimé car l’état des autres stations sur l’appel peut être régi. Au lieu de cela, l’appel peut simplement être remplacé par l’état inactif tout en restant connecté sur d’autres stations.

Après une opération Drop, l’identificateur de session et la plupart des ressources associées à la session restent utilisables pour la plupart des opérations de requête. Quand une application n’a plus besoin de ces ressources, elle doit [mettre fin à la session](terminate-a-session-ovr.md) afin d’éviter les fuites de mémoire.

**TAPI 2. x :** Consultez [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).

**TAPI 3. x :** Consultez [**ITBasicCallControl ::D éconnecter**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
