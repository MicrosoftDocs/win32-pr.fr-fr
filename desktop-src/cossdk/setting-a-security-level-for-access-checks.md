---
description: Une fois que vous avez activé les vérifications d’accès, pour votre application COM+, vous devez sélectionner le niveau auquel vous souhaitez que les vérifications d’accès soient effectuées.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Définition d’un niveau de sécurité pour les vérifications d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111279"
---
# <a name="setting-a-security-level-for-access-checks"></a>Définition d’un niveau de sécurité pour les vérifications d’accès

Une fois que vous avez activé les [vérifications d’accès](enabling-access-checks-for-an-application.md), pour votre application com+, vous devez sélectionner le niveau auquel vous souhaitez que les vérifications d’accès soient effectuées.

**Pour sélectionner un niveau de sécurité**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application COM+ pour laquelle vous souhaitez activer les vérifications d’accès, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .

3.  Sous **niveau de sécurité**, sélectionnez l’une des options suivantes :

    -   **Effectuer des vérifications d’accès uniquement au niveau du processus**: ce paramètre indique que les utilisateurs dans les rôles affectés à l’application seront ajoutés au descripteur de sécurité du processus. Cela a les effets et les implications suivants :

        La vérification des rôles affinée est désactivée au niveau du composant, de la méthode et de l’interface. Les vérifications de sécurité sont effectuées uniquement au niveau de l’application.

        La propriété de sécurité n’est pas incluse dans le contexte pour les objets qui s’exécutent dans l’application. Cela peut affecter la manière dont les objets sont activés. Consultez la [propriété contexte de sécurité](security-context-property.md).

        Le contexte de l’appel de sécurité ne sera pas mis à disposition. La sécurité par programme qui s’appuie sur les informations de contexte d’appel de sécurité ne fonctionnera pas. Consultez les informations de contexte de l' [appel de sécurité](security-call-context-information.md).

    -   **Effectuer des vérifications d’accès au niveau du processus et du composant**: ce paramètre indique que les contrôles du descripteur de sécurité au niveau du processus et les vérifications de sécurité basées sur les rôles sont effectués intégralement. Cela a les effets et les implications suivants :

        Pour activer la vérification de rôle pour des composants particuliers, vous devez [activer les vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md).

        La propriété de sécurité est incluse dans le contexte des objets qui s’exécutent dans l’application. Cela peut affecter la manière dont les objets sont activés. Consultez la [propriété contexte de sécurité](security-context-property.md).

        Le contexte de l’appel de sécurité est disponible. La sécurité basée sur les rôles par programmation est activée. Consultez les informations de contexte de l' [appel de sécurité](security-call-context-information.md).

        > [!Note]  
        > Pour les applications de bibliothèque COM+, vous devez choisir de vérifier les niveaux au niveau du processus et au niveau du composant pour que les contrôles d’accès pertinents fonctionnent. Les applications de bibliothèque s’appuient sur le processus hôte pour la sécurité au niveau du processus. Vous pouvez déterminer la manière dont l’application de bibliothèque interagit avec l’authentification effectuée par le processus hôte en [définissant l’authentification](enabling-authentication-for-a-library-application.md). Pour plus d’informations, consultez [bibliothèque de sécurité des applications](library-application-security.md).

         

4.  Cliquez sur **OK**.

Lors du prochain démarrage de l’application, la sécurité est automatiquement vérifiée au niveau spécifié. Seuls les utilisateurs affectés aux rôles affectés à l’application auront accès à l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assignation de rôles à des composants, des interfaces ou des méthodes](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuration de la sécurité de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Définition des rôles pour une application](defining-roles-for-an-application.md)
</dt> <dt>

[Activation des vérifications d’accès pour une application](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Activation des vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



