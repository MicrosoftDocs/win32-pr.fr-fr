---
description: L’exécution de cette étape permet d’effectuer des vérifications d’accès au processus ou une sécurité complète basée sur les rôles, en fonction du niveau de sécurité que vous sélectionnez et de l’activation ou non de la vérification d’accès pour des composants individuels.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Activation des vérifications d’accès pour une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532070"
---
# <a name="enabling-access-checks-for-an-application"></a>Activation des vérifications d’accès pour une application

L’exécution de cette étape permet d’effectuer des vérifications d’accès au processus ou une sécurité complète basée sur les rôles, en fonction du niveau de sécurité que vous sélectionnez et de l’activation ou non de la vérification d’accès pour des composants individuels.

**Pour activer les vérifications d’accès pour une application**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application COM+ pour laquelle vous souhaitez activer les vérifications d’accès, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .

3.  Activez la case à cocher **appliquer les vérifications d’accès pour cette application** .

4.  Cliquez sur **OK**.

> [!Note]  
> À compter de Windows Server 2003, les vérifications d’accès sont activées par défaut lors de la création d’une application COM+. Les contrôles d’accès sont activés par défaut au niveau de l’application et sont désactivés par défaut au niveau du composant. Auparavant, les contrôles d’accès étaient désactivés par défaut au niveau de l’application et activés par défaut au niveau du composant.

 

Après avoir activé les vérifications d’accès, vous devez sélectionner le niveau de sécurité approprié. Consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md). En outre, vous devez être sûr de définir des rôles et de les ajouter à l’application. Si les vérifications d’accès sont activées mais qu’aucun rôle n’a été ajouté, tous les appels à l’application échouent. Consultez [définition des rôles pour une application](defining-roles-for-an-application.md).

> [!Note]  
> Lors du débogage de votre application, il peut être utile de désactiver la sécurité afin que vous puissiez vous concentrer sur d’autres aspects du comportement et de la conception de votre programme.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assignation de rôles à des composants, des interfaces ou des méthodes](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuration de la sécurité de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Définition des rôles pour une application](defining-roles-for-an-application.md)
</dt> <dt>

[Activation des vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



