---
description: API de gestion des informations d’identification
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API de gestion des informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a290cf9d7e5a2d527368c2fd7350fa1bb9549af862c7da7c3845ceae9efc8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008837"
---
# <a name="credential-management-api"></a>API de gestion des informations d’identification

Les fonctions de gestion des informations d’identification constituent l’ensemble des fonctions qu’un gestionnaire d’informations d’identification doit implémenter. Celles-ci sont les suivantes :

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), une fonction de gestionnaire d’événements que le MPR appelle lorsqu’un utilisateur ouvre une session.
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), une fonction de gestionnaire d’événements que MPR appelle lorsqu’un mot de passe de compte est modifié.

Les fonctions de gestion des informations d’identification sont toujours appelées dans le contexte du système (LocalSystem) plutôt que dans le contexte de l’utilisateur.

Pour plus d’informations sur la création et l’inscription d’une application Gestionnaire d’informations d’identification, consultez [implémentation d’un gestionnaire d’informations d’identification](implementing-a-credential-manager.md) et [inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification](registering-network-providers-and-credential-managers.md).

 

 



