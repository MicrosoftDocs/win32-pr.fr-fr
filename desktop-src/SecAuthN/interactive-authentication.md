---
description: L’authentification est interactive quand un utilisateur est invité à fournir des informations d’ouverture de session. L’autorité de sécurité locale (LSA) effectue une authentification interactive lorsqu’un utilisateur se connecte par le biais de l’interface utilisateur GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Authentification interactive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876f3aced39afba0d08a9643e14caae91336daf38a63f3855e76fe50136a16a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482292"
---
# <a name="interactive-authentication"></a>Authentification interactive

L’authentification est interactive quand un utilisateur est invité à fournir des informations d’ouverture de session. L' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) effectue une authentification interactive lorsqu’un utilisateur se connecte par le biais de l’interface utilisateur [*Gina*](../secgloss/g-gly.md) . L’illustration suivante montre les parties d’une authentification interactive classique.

![authentification interactive](images/lsaint3.png)

Un utilisateur signale au système de commencer la séquence d’ouverture de session en tapant la [*séquence*](../secgloss/s-gly.md) de touches Ctrl + Alt + Suppr (SAS). [*Winlogon*](../secgloss/w-gly.md) reçoit la SAP et appelle Gina pour afficher une interface utilisateur et obtenir les données d’ouverture de session de l’utilisateur, telles qu’un nom d’utilisateur et un mot de passe.

Après avoir obtenu les données de connexion, GINA appelle la fonction [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) pour authentifier l’utilisateur, en spécifiant le package d’authentification qui doit être utilisé pour évaluer les données d’ouverture de session.

L’autorité LSA appelle le package d’authentification spécifié et lui transmet les données de connexion. Le package d’authentification examine les données et détermine si l’authentification réussit. Le résultat de l’authentification est retourné à l’autorité LSA et du LSA au GINA.

GINA affiche la réussite ou l’échec de l’authentification de l’utilisateur et renvoie le résultat de l’authentification à Winlogon. Si l’authentification a échoué, la session d’ouverture de session de l’utilisateur commence et un ensemble d' [*informations d’identification*](../secgloss/c-gly.md) de connexion sont enregistrées pour référence ultérieure.

> [!Note]  
> En général, un développeur qui écrit une GINA personnalisée pour accepter des données de connexion spécialisées, telles qu’une [*carte à puce*](../secgloss/s-gly.md) ou des données d’analyse rétinienne, doit également écrire un package d’authentification responsable du traitement de ces données et de la détermination de son authenticité.

 

Pour plus d’informations sur Winlogon et les GINA, consultez [Winlogon et Gina](winlogon-and-gina.md). Pour plus d’informations sur les packages d’authentification, consultez [création de packages de sécurité personnalisés](creating-custom-security-packages.md).

 

 
