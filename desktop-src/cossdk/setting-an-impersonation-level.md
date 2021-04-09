---
description: Lorsque vous définissez un niveau d’emprunt d’identité pour une application, vous déterminez le degré d’autorité que l’application accorde à d’autres applications pour utiliser son identité lorsqu’elle les appelle.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Définition d’un niveau d’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110898"
---
# <a name="setting-an-impersonation-level"></a>Définition d’un niveau d’emprunt d’identité

Lorsque vous définissez un niveau d’emprunt d’identité pour une application, vous déterminez le degré d’autorité que l’application accorde à d’autres applications pour utiliser son identité lorsqu’elle les appelle. Vous pouvez définir cette valeur uniquement pour les applications serveur COM+ : les applications de bibliothèque s’exécutent sous l’identité du processus d’hébergement et utilisent le niveau d’emprunt d’identité qu’elles spécifient. Pour plus d’informations, consultez [niveaux d’emprunt d’identité](/windows/desktop/com/impersonation-levels).

**Pour sélectionner un niveau d’emprunt d’identité**

1.  Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous configurez l’emprunt d’identité, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .

3.  Dans la zone **niveau d’emprunt d’identité** , sélectionnez le niveau approprié. Les niveaux sont les suivants, triés d’accordant au moins la plus grande autorité :

    -   **Anonyme**. Le client est anonyme au serveur. Le serveur peut emprunter l’identité du client, mais le jeton d’emprunt d’identité (informations d’identification locales) ne contient pas d’informations sur le client.
    -   **Identifiez**. Le serveur peut obtenir l’identité du client et peut emprunter l’identité du client pour effectuer des vérifications de liste de contrôle d’accès.
    -   **Emprunter l’identité**. Le serveur peut emprunter l’identité du client tout en agissant en son nom, bien qu’avec des restrictions. Le serveur peut accéder aux ressources sur le même ordinateur que le client. Si le serveur se trouve sur le même ordinateur que le client, il peut accéder aux ressources réseau en tant que client. Si le serveur se trouve sur un ordinateur différent du client, il ne peut accéder qu’aux ressources qui se trouvent sur le même ordinateur que le serveur. Il s’agit du paramètre par défaut pour les applications serveur COM+.
    -   **Délégué**. Le serveur peut emprunter l’identité du client tout en agissant en son nom, que ce soit sur le même ordinateur que le client. Pendant l’emprunt d’identité, les informations d’identification du client (à la fois celles avec local et celles avec une validité réseau) peuvent être transmises à n’importe quel nombre d’ordinateurs.

4.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de la sécurité de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Configuration de la stratégie de restriction logicielle](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Définition d’un niveau d’authentification pour une application serveur](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
