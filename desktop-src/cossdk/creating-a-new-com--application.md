---
description: Création d’une application COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Création d’une application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516797"
---
# <a name="creating-a-new-com-application"></a>Création d’une application COM+

La création d’une nouvelle application COM+ requiert deux étapes de base, comme suit :

-   Création d’une application COM+ vide (décrite ci-dessous).
-   Ajout de composants à l’application. (Voir [installation de nouveaux composants](installing-new-components.md) et [importation de composants](importing-components.md).)

**Pour créer une application COM+ vide**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sélectionnez l’ordinateur sur lequel vous souhaitez créer une application.

2.  Sélectionnez le dossier **applications com+** pour cet ordinateur.

3.  Dans le menu **action** , pointez sur **nouveau**, puis cliquez sur **application**. Vous pouvez également cliquer avec le bouton droit sur le dossier **applications com+** , pointer sur **nouveau**, puis cliquer sur **application**.

4.  Sur la page d' **Accueil** de l’Assistant Installation de l’application com+, cliquez sur **suivant**, puis dans la boîte de dialogue **installer ou créer une nouvelle application** , cliquez sur **créer une application vide**.

5.  Dans la zone prévue à cet effet, tapez un nom pour la nouvelle application. (Notez que les caractères spéciaux suivants ne peuvent pas être utilisés dans un nom d’application : \\ ,/, ~, !, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ', ", >, <,., ?, : et ;.) Sous **type d’activation**, cliquez sur application de **bibliothèque** ou **application serveur**. Cliquez sur **Suivant**.

    > [!Note]  
    > Une application serveur s’exécute dans son propre processus. Les applications serveur peuvent prendre en charge tous les services COM+. Une application de bibliothèque s’exécute dans le processus du client qui la crée. Les applications de bibliothèque peuvent utiliser la sécurité basée sur les rôles, mais ne prennent pas en charge l’accès à distance ou les composants en file d’attente.

     

6.  Dans la boîte de dialogue **définir l’identité** de l’application, choisissez l’identité sous laquelle l’application s’exécutera. Si vous sélectionnez **cet utilisateur**, tapez le nom d’utilisateur et le mot de passe. Vous devez également retaper le mot de passe dans la zone **confirmer le mot de passe** . Cliquez sur **Suivant**. (La sélection par défaut pour l’identité de l’application est **utilisateur interactif**. L’utilisateur interactif est l’utilisateur connecté à l’ordinateur serveur à un moment donné. Vous pouvez sélectionner un autre utilisateur en sélectionnant **cet utilisateur** et en entrant un utilisateur ou un groupe spécifique.)

    > [!Note]  
    > La boîte de dialogue **définir l’identité** de l’application s’affiche uniquement si vous avez sélectionné **application serveur** comme type d’activation de la nouvelle application dans la boîte de dialogue précédente de l’Assistant Installation de l’application com. La propriété Identity n’est pas utilisée pour les applications de bibliothèque.

     

7.  Dans la boîte de dialogue **Ajouter des rôles d’application** , ajoutez tous les rôles que vous souhaitez associer à l’application. Par défaut, seul le rôle **CreatorOwner** est défini. Pour plus d’informations sur les rôles, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).

8.  Dans la boîte de dialogue **Ajouter des utilisateurs aux rôles** , remplissez chaque rôle que vous avez créé lors de la dernière étape avec les utilisateurs, les groupes ou les principaux de sécurité intégrés auxquels vous souhaitez accorder les privilèges associés à ce rôle. Par défaut, l’utilisateur interactif est placé dans le rôle **CreatorOwner** .

9.  Cliquez sur **Terminer**.

La nouvelle application s’affiche désormais sous le dossier **applications com+** dans l’arborescence de la console de l’outil d’administration Services de composants.

> [!Note]  
> À compter de Windows Server 2003, les vérifications d’accès sont activées par défaut lors de la création d’une application COM+. Dans les versions précédentes, les contrôles d’accès étaient désactivés par défaut au niveau de l’application. Le résultat est que, par défaut, l’accès à une application COM+ est autorisé uniquement pour les utilisateurs qui se trouvent dans les rôles associés à l’application. (Voir [administration de la sécurité basée sur les rôles](role-based-security-administration.md).) Vous pouvez également autoriser l’accès à tous les utilisateurs en désactivant les vérifications d’accès sur une application COM+. (Voir [activation des vérifications d’accès pour une application](enabling-access-checks-for-an-application.md).)

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Copier des composants](copying-components.md)
</dt> <dt>

[Suppression d’une application COM+](deleting-a-com--application.md)
</dt> <dt>

[Importation de composants](importing-components.md)
</dt> <dt>

[Installation de nouveaux composants](installing-new-components.md)
</dt> <dt>

[Déplacement des composants](moving-components.md)
</dt> <dt>

[Suppression d’un composant d’une application COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



