---
description: Un gestionnaire d’informations d’identification est semblable à un fournisseur de réseau en ce qu’il fournit des points d’entrée qui sont appelés par le routeur multifournisseur (MPR). En fait, certains fournisseurs de réseau sont également des gestionnaires d’informations d’identification.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Gestionnaire d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a33b1a47ff17123a1974823d7fee1421df7755850d46d2992fec51f62f5fac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008827"
---
# <a name="credential-manager"></a>Gestionnaire d’informations d’identification

Un gestionnaire d’informations d’identification est semblable à un fournisseur de réseau en ce qu’il fournit des points d’entrée qui sont appelés par le [*routeur multifournisseur*](/windows/desktop/SecGloss/m-gly) (MPR). En fait, certains fournisseurs de réseau sont également des gestionnaires d’informations d’identification.

L’implémentation des fonctions de gestion des informations d’identification dans la même DLL que celle des fonctions du fournisseur réseau dépend des besoins de votre application. Les gestionnaires d’informations d’identification reçoivent des notifications lorsque les informations d’authentification changent. Par exemple, les gestionnaires d’informations d’identification sont avertis lorsqu’un utilisateur ouvre une session ou qu’un mot de passe de compte change. lorsqu’un processus d’ouverture de session, tel que [*Winlogon*](/windows/desktop/SecGloss/w-gly), est en train de se connecter ou de modifier le mot de passe d’un compte, il appelle la fonction WNet (mise en réseau de mise en réseau) Windows MPR appropriée. Le MPR appelle ensuite le point d’entrée approprié pour chaque gestionnaire d’informations d’identification. Ces fonctions de gestion des informations d’identification seront toujours appelées dans le contexte système, LocalSystem, plutôt que dans le contexte de l’utilisateur. pour plus d’informations sur les fonctions WNet, consultez [mise en réseau Windows](/windows/desktop/WNet/windows-networking-wnet-). Pour plus d’informations sur l’interface que les gestionnaires d’informations d’identification doivent implémenter, consultez [**API de gestion des informations d’identification**](credential-management-api.md).

 

 
