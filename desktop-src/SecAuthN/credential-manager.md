---
description: Un gestionnaire d’informations d’identification est semblable à un fournisseur de réseau en ce qu’il fournit des points d’entrée qui sont appelés par le routeur multifournisseur (MPR). En fait, certains fournisseurs de réseau sont également des gestionnaires d’informations d’identification.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Gestionnaire d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20165a5e6145de0a2c042c38923c41d793bd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034740"
---
# <a name="credential-manager"></a>Gestionnaire d’informations d’identification

Un gestionnaire d’informations d’identification est semblable à un fournisseur de réseau en ce qu’il fournit des points d’entrée qui sont appelés par le [*routeur multifournisseur*](/windows/desktop/SecGloss/m-gly) (MPR). En fait, certains fournisseurs de réseau sont également des gestionnaires d’informations d’identification.

L’implémentation des fonctions de gestion des informations d’identification dans la même DLL que celle des fonctions du fournisseur réseau dépend des besoins de votre application. Les gestionnaires d’informations d’identification reçoivent des notifications lorsque les informations d’authentification changent. Par exemple, les gestionnaires d’informations d’identification sont avertis lorsqu’un utilisateur ouvre une session ou qu’un mot de passe de compte change. Lorsqu’un processus d’ouverture de session, tel que [*Winlogon*](/windows/desktop/SecGloss/w-gly), est en train de se connecter ou de modifier le mot de passe d’un compte, il appelle la fonction de mise en réseau Windows MPR appropriée (WNET). Le MPR appelle ensuite le point d’entrée approprié pour chaque gestionnaire d’informations d’identification. Ces fonctions de gestion des informations d’identification seront toujours appelées dans le contexte système, LocalSystem, plutôt que dans le contexte de l’utilisateur. Pour plus d’informations sur les fonctions WNet, consultez [mise en réseau Windows](/windows/desktop/WNet/windows-networking-wnet-). Pour plus d’informations sur l’interface que les gestionnaires d’informations d’identification doivent implémenter, consultez [**API de gestion des informations d’identification**](credential-management-api.md).

 

 
