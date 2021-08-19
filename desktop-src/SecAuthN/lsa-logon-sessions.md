---
description: Une session de connexion est une session de calcul qui commence lorsque l’authentification d’un utilisateur est réussie et se termine lorsque l’utilisateur se déconnecte du système.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sessions LSA Logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4bc6adc81b22b0e48a83b8aec4f9130b1fcb906bea5078afc6517563c98b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922324"
---
# <a name="lsa-logon-sessions"></a>Sessions LSA Logon

Une [*session de connexion*](../secgloss/l-gly.md) est une session de calcul qui commence lorsque l’authentification d’un utilisateur est réussie et se termine lorsque l’utilisateur se déconnecte du système.

Lorsqu’un utilisateur est authentifié avec succès, le package d’authentification crée une session de connexion et retourne des informations à l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) qui est utilisée pour créer un [*jeton*](../secgloss/t-gly.md) pour le nouvel utilisateur. Ce jeton comprend, entre autres choses, un [*identificateur unique local*](../secgloss/l-gly.md) (LUID) pour la session d’ouverture de session, appelé [*ID d’ouverture*](../secgloss/l-gly.md)de session.

Lorsqu’un jeton est créé, le [*nombre de références*](../secgloss/r-gly.md) pour la session d’ouverture de session est incrémenté. Le décompte de références est également incrémenté chaque fois que des copies du jeton sont créées pour la création du processus, l’emprunt d’identité ou d’autres utilisations. À mesure que les utilisations des jetons sont terminées et que des copies du jeton sont supprimées, le nombre de références pour la session d’ouverture de session est décrémenté. Lorsque le nombre de références atteint zéro, la session de connexion est supprimée.

> [!Note]  
> Si l’authentification échoue, le [*package d’authentification*](../secgloss/a-gly.md) ne doit pas créer de session de connexion. Si le package d’authentification doit créer une session de connexion avant de procéder à une détermination finale de la validité de l’utilisateur, et si l’authentification échoue, le package d’authentification doit supprimer la session.

 

 

 
