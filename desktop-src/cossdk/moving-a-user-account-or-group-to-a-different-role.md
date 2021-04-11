---
description: Vous pouvez supprimer des comptes d’utilisateur ou des groupes d’un rôle lorsque les utilisateurs ou les membres des groupes ne doivent plus avoir accès aux ressources d’application auxquelles le rôle est attribué.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Déplacement d’un compte d’utilisateur ou d’un groupe vers un autre rôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111290"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a>Déplacement d’un compte d’utilisateur ou d’un groupe vers un autre rôle

Vous pouvez supprimer des comptes d’utilisateur ou des groupes d’un rôle lorsque les utilisateurs ou les membres des groupes ne doivent plus avoir accès aux ressources d’application auxquelles le rôle est attribué.

**Pour supprimer un compte d’utilisateur ou un groupe d’un rôle**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le rôle qui vous intéresse. Développez la vue dans l’arborescence de la console jusqu’à ce que les utilisateurs du rôle soient visibles.

2.  Cliquez avec le bouton droit sur le compte d’utilisateur ou le groupe que vous souhaitez supprimer, puis cliquez sur **supprimer**.

3.  Quand la boîte de dialogue **confirmer la suppression** de l’élément s’affiche, cliquez sur **Oui** pour supprimer le compte d’utilisateur ou le groupe.

Le compte d’utilisateur ou le groupe que vous avez supprimé du rôle ne s’affiche plus dans le dossier **utilisateurs** . La nouvelle appartenance au rôle prend effet lors du prochain démarrage de l’application. Si vous avez apporté des modifications à l' **application système**, vous devez redémarrer l’ordinateur pour que les modifications prennent effet.

 

 



