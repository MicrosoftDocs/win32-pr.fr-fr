---
description: Assignation de rôles à des composants, des interfaces ou des méthodes
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Assignation de rôles à des composants, des interfaces ou des méthodes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393143"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>Assignation de rôles à des composants, des interfaces ou des méthodes

Vous pouvez affecter explicitement un rôle à n’importe quel élément d’une application COM+ qui est visible à l’aide de l’outil d’administration Services de composants. Cela garantit que tous les utilisateurs membres du rôle seront autorisés à accéder à cet élément et à tous les autres éléments qu’il contient. Par exemple, si vous affectez le rôle « Readers » à un composant, n’importe quel membre de « Readers » est autorisé à accéder à ce composant et à toutes les interfaces et méthodes qu’il expose. « Readers » s’affichera en tant que rôle hérité pour l’une de ces interfaces et méthodes.

Une méthode est accessible aux appelants uniquement si vous lui assignez un rôle, soit en affectant explicitement le rôle directement à la méthode, soit en affectant un rôle à l’interface de la méthode ou au composant de la méthode, auquel cas le rôle est hérité par la méthode. Si aucun rôle n’est assigné et si les contrôles d’accès sont activés, tous les appels à la méthode échouent.

Avant de pouvoir assigner un rôle, vous devez le [définir](defining-roles-for-an-application.md) pour l’application. Tous les rôles définis pour l’application s’affichent dans la fenêtre **rôles explicitement définis pour les éléments sélectionnés** dans l’onglet **sécurité** pour les composants, les méthodes et les interfaces de l’application.

**Pour assigner des rôles à un composant, une méthode ou une interface**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, localisez l’application COM+ pour laquelle le rôle a été défini. Développez l’arborescence pour afficher les composants, les interfaces ou les méthodes de l’application, en fonction de ce à quoi vous affectez le rôle.

2.  Cliquez avec le bouton droit sur l’élément auquel vous souhaitez affecter le rôle, puis cliquez sur **Propriétés**.

3.  Dans la boîte de dialogue Propriétés, cliquez sur l’onglet **sécurité** .

4.  Dans la zone **rôles définis explicitement pour le ou les éléments sélectionnés** , sélectionnez les rôles que vous souhaitez affecter à l’élément.

5.  Cliquez sur **OK**.

Tous les rôles que vous avez définis explicitement pour un élément sont hérités par les éléments de niveau inférieur qu’il contient et s’affichent dans la fenêtre **rôles hérités par élément sélectionné** pour ces éléments.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de la sécurité de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Définition des rôles pour une application](defining-roles-for-an-application.md)
</dt> <dt>

[Activation des vérifications d’accès pour une application](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Activation des vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



