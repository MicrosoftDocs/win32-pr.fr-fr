---
description: Activation des vérifications d’accès au niveau du composant
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Activation des vérifications d’accès au niveau du composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3063873923d3d4c491312ca4efccd9bcd665b46bf1bdfc882b69dbe4942757f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047467"
---
# <a name="enabling-access-checks-at-the-component-level"></a>Activation des vérifications d’accès au niveau du composant

Si votre application comprend un composant qui n’a pas besoin de vérifications de sécurité, vous pouvez décider de désactiver les vérifications de rôle pour ce composant afin d’améliorer les performances. Ou lors du débogage, il peut être utile de désactiver la sécurité afin que vous puissiez vous concentrer sur d’autres aspects de la fonctionnalité du programme.

Par défaut, lorsque vous installez un composant, les vérifications d’accès au niveau du composant sont activées. Toutefois, cela ne prend effet que lorsque les [contrôles d’accès au niveau](enabling-access-checks-for-an-application.md) de l’application sont activés et lorsque le [niveau de sécurité](setting-a-security-level-for-access-checks.md) est défini pour effectuer des **vérifications d’accès au niveau du processus et du composant**.

**Pour activer ou désactiver les vérifications d’accès au niveau du composant**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le composant pour lequel vous souhaitez désactiver (ou activer) les vérifications de rôle. Développez la vue dans l’arborescence pour afficher les composants dans le dossier **composants** .

2.  Cliquez avec le bouton droit sur le composant pour lequel vous souhaitez activer les vérifications de rôle, puis cliquez sur **Propriétés**.

3.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **sécurité** .

4.  Sélectionnez **appliquer les vérifications d’accès au niveau du composant** pour appliquer les vérifications au niveau du composant.

5.  Cliquez sur **OK**.

Le nouveau paramètre prendra effet lors du prochain démarrage de l’application.

> [!Note]  
> à partir de Windows Server 2003, les contrôles d’accès au niveau du composant sont désactivés par défaut lors de la création d’une application COM+. Les contrôles d’accès sont activés par défaut au niveau de l’application et sont désactivés par défaut au niveau du composant. Auparavant, les contrôles d’accès étaient désactivés par défaut au niveau de l’application et activés par défaut au niveau du composant.

 

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

[Définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



