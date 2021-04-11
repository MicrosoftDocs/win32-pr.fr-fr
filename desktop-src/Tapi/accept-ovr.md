---
description: Dans certains environnements, un utilisateur n’est pas automatiquement averti d’un appel d’offre, par exemple par sonnerie ou par message sur l’écran de l’ordinateur.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Accepter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201346"
---
# <a name="accept"></a>Accepter

Dans certains environnements, un utilisateur n’est pas automatiquement averti d’un appel d’offre, par exemple par sonnerie ou par message sur l’écran de l’ordinateur. L’opération d’acceptation commence le processus d’alerte (généralement de sonnerie) et l’opération de [réponse](answer-ovr.md) a lieu après. L’application peut [supprimer](drop-ovr.md) la session, la [Rediriger](redirect-ovr.md) ou l’accepter.

Si le fournisseur de services actuel le prend en charge, l’application a la possibilité d’envoyer des informations utilisateur-utilisateur au moment de l’acceptation. Il n’y a aucune garantie que le réseau remet ces informations au tiers appelant.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).

 

 
