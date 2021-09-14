---
description: API de gestion des informations d’identification
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API de gestion des informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096421"
---
# <a name="credential-management-api"></a>API de gestion des informations d’identification

Les fonctions de gestion des informations d’identification constituent l’ensemble des fonctions qu’un gestionnaire d’informations d’identification doit implémenter. Ces règles sont les suivantes :

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), une fonction de gestionnaire d’événements que le MPR appelle lorsqu’un utilisateur ouvre une session.
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), une fonction de gestionnaire d’événements que MPR appelle lorsqu’un mot de passe de compte est modifié.

Les fonctions de gestion des informations d’identification sont toujours appelées dans le contexte du système (LocalSystem) plutôt que dans le contexte de l’utilisateur.

Pour plus d’informations sur la création et l’inscription d’une application Gestionnaire d’informations d’identification, consultez [implémentation d’un gestionnaire d’informations d’identification](implementing-a-credential-manager.md) et [inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification](registering-network-providers-and-credential-managers.md).

 

 



