---
description: Si un utilisateur modifie des privilèges ou si des rôles sont ajoutés à une application, vous pouvez déplacer un compte d’un rôle à un autre.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Suppression d’un compte d’utilisateur ou d’un groupe d’un rôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ed038867fad8ff24f274bf733de43d0b534cf74671b855c6e3d43ade05b657
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070369"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a>Suppression d’un compte d’utilisateur ou d’un groupe d’un rôle

Si les privilèges d’un utilisateur changent ou si des rôles sont ajoutés à une application, vous pouvez déplacer un compte d’un rôle à un autre. Pour déplacer un compte d’utilisateur ou un groupe d’utilisateurs d’un rôle à un autre, vous devez supprimer le compte d’utilisateur ou le groupe de son rôle actuel, puis l’affecter au nouveau rôle.

**Pour déplacer un compte d’utilisateur ou un groupe d’un rôle à un autre**

1.  Supprimez le compte d’utilisateur ou le groupe du rôle auquel il ne doit plus appartenir, comme suit :

    1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le rôle qui vous intéresse. Développez la vue dans l’arborescence de la console jusqu’à ce que les utilisateurs du rôle soient visibles.

    2.  Cliquez avec le bouton droit sur le compte d’utilisateur ou le groupe que vous souhaitez supprimer, puis cliquez sur **supprimer**.

    3.  Quand la boîte de dialogue **confirmer la suppression** de l’élément s’affiche, cliquez sur **Oui** pour supprimer le compte d’utilisateur ou le groupe.

    Le compte d’utilisateur ou le groupe que vous avez supprimé du rôle ne s’affiche plus dans le dossier **utilisateurs** .

2.  Affectez le compte d’utilisateur ou le groupe que vous avez supprimé aux rôles auxquels l’utilisateur ou le groupe doit être affecté, comme suit :

    1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le rôle auquel vous souhaitez ajouter le compte d’utilisateur ou le groupe. Développez la vue dans l’arborescence de la console jusqu’à ce que les rôles de l’application soient visibles.

    2.  Localisez le rôle auquel vous souhaitez ajouter le compte d’utilisateur ou le groupe.

        > [!Note]  
        > Si le rôle que vous recherchez ne figure pas dans le dossier **rôles** , le rôle n’a pas été ajouté à l’application. Il doit être ajouté à l’application par le développeur avant que vous puissiez attribuer des comptes d’utilisateur au rôle.

         

    3.  Cliquez avec le bouton droit sur le dossier **utilisateurs** dans le rôle, pointez sur **nouveau**, puis cliquez sur **utilisateur**.

    4.  Dans le volet inférieur de la fenêtre **Sélectionner les utilisateurs ou les groupes** , tapez le nom complet de l’utilisateur ou du groupe que vous souhaitez ajouter. Si vous ne connaissez pas le nom, cliquez sur le bouton **avancé** , puis cliquez sur **Rechercher maintenant** pour afficher la liste des utilisateurs et des groupes dans le domaine sélectionné. Sélectionnez un utilisateur ou un groupe dans la liste **nom (RDN)** , puis cliquez sur **OK**.

    5.  Lorsque vous avez terminé d’ajouter le compte d’utilisateur ou le groupe au rôle, cliquez sur **OK**.

    Pour chaque compte d’utilisateur ou groupe que vous avez affecté au rôle, une icône s’affiche dans le dossier **utilisateurs** .

L’appartenance au rôle modifié pour le compte d’utilisateur ou le groupe prend effet lors du prochain démarrage de l’application.

 

 



