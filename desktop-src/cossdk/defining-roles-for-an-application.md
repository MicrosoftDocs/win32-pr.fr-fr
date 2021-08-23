---
description: Pour déterminer une stratégie de sécurité pour une application, vous devez définir les privilèges de sécurité requis.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Définition des rôles pour une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc4b4fb6aaee557eea69dec405254925cd669d18ac73cdea229f548145d8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637709"
---
# <a name="defining-roles-for-an-application"></a>Définition des rôles pour une application

Pour déterminer une stratégie de sécurité pour une application, vous devez définir les privilèges de sécurité requis. Pour ce faire, vous devez déclarer un niveau de privilège symbolique en tant que rôle, c’est-à-dire définir le rôle de l’application, puis [attribuer le rôle](assigning-roles-to-components--interfaces--or-methods.md) à des ressources spécifiques au sein de l’application. Cette conception est remplie lorsque l’application est déployée et que les administrateurs système remplissent le rôle avec des utilisateurs et des groupes d’utilisateurs réels. Pour plus d’informations, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).

**Pour ajouter un rôle à une application**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, localisez l’application COM+ à laquelle vous souhaitez ajouter le rôle. Développez l’arborescence pour afficher les dossiers de l’application.

2.  Cliquez avec le bouton droit sur le dossier **rôles** pour l’application, pointez sur **nouveau**, puis cliquez sur **rôle**.

3.  Dans la boîte de dialogue **rôle**, tapez le nom du nouveau rôle dans la zone prévue à cet effet.

4.  Cliquez sur **OK**.

> [!Note]  
> Après avoir ajouté des rôles à l’application, vous devez vous assurer d’affecter les rôles aux composants, interfaces et méthodes appropriés. Dans le cas contraire, si la sécurité basée sur les rôles a été choisie et activée et si des rôles ont été ajoutés mais non affectés, tous les appels à l’application échouent. Pour plus d’informations, consultez [assignation de rôles à des composants, des interfaces ou des méthodes](assigning-roles-to-components--interfaces--or-methods.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assignation de rôles à des composants, des interfaces ou des méthodes](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuration de la sécurité de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Activation des vérifications d’accès pour une application](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Activation des vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



