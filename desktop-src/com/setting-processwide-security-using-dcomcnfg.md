---
title: Définition de la sécurité Process-Wide à l’aide de DCOMCNFG
description: Vous pouvez activer la sécurité pour une application particulière si les besoins en matière de sécurité d’une application diffèrent de ceux requis par d’autres applications sur l’ordinateur.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03174dd66e83a88724ff5d421d7b0dcb0c17699e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363503"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Définition de la sécurité Process-Wide à l’aide de DCOMCNFG

Vous pouvez activer la sécurité pour une application particulière si les besoins en matière de sécurité d’une application diffèrent de ceux requis par d’autres applications sur l’ordinateur. Par exemple, vous pouvez décider d’utiliser des paramètres à l’échelle du système pour vos applications qui nécessitent un niveau de sécurité faible tout en définissant un niveau de sécurité plus élevé pour une application particulière.

Toutefois, les paramètres de sécurité du Registre qui s’appliquent à une application particulière ne sont parfois pas utilisés. Par exemple, les paramètres à l’ensemble du processus que vous définissez dans le registre à l’aide de Dcomcnfg.exe sont remplacés si un client appelle [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour définir la sécurité pour un proxy d’interface particulier. De même, si un client ou un serveur (ou les deux) appellent la valeur [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir la sécurité d’un processus, les paramètres du Registre sont ignorés et les paramètres spécifiés pour **CoInitializeSecurity** sont utilisés à la place.

Lorsque vous activez la sécurité pour une application, il peut être nécessaire de modifier plusieurs paramètres. Cela inclut le niveau d’authentification, l’emplacement, les autorisations de lancement, les autorisations d’accès et l’identité. Pour obtenir des procédures pas à pas, consultez les rubriques suivantes :

-   [Définition du niveau d’authentification pour une application](#setting-the-authentication-level-for-an-application)
-   [Définition de l’emplacement d’une application](#setting-the-location-for-an-application)
-   [Définition des autorisations de lancement pour une application](#setting-launch-permissions-for-an-application)
-   [Définition des autorisations d’accès pour une application](#setting-access-permissions-for-an-application)
-   [Définition de l’identité d’une application](#setting-the-identity-for-an-application)
-   [Exploration de la base de données utilisateur](#browsing-the-user-database)
-   [ ApplicationsDcomcnfg.exe et 64 bits](#dcomcnfgexe-and-64-bit-applications)
-   [Rubriques connexes](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Définition du niveau d’authentification pour une application

Pour activer la sécurité pour une application, vous devez définir un niveau d’authentification autre que aucun. Le niveau d’authentification indique à COM la quantité de protection requise pour l’authentification, et il peut aller de l’authentification du client au premier appel de méthode au chiffrement complet des États de paramètres.

**Pour définir le niveau d’authentification d’une application**

1.  Dans la page de propriétés **applications** de Dcomcnfg.exe, sélectionnez l’application et cliquez sur le bouton des **Propriétés** (ou double-cliquez sur l’application sélectionnée).

2.  Sur la page **général** , sélectionnez un niveau d’authentification autre que **(aucun)** dans la zone de liste **niveau d’authentification** .

3.  Si vous devez définir d’autres propriétés pour cette application, cliquez sur le bouton **appliquer** pour appliquer le nouveau niveau d’authentification. Cliquez sur **OK** si vous avez terminé de définir les propriétés de cette application et que vous souhaitez appliquer les modifications.

## <a name="setting-the-location-for-an-application"></a>Définition de l’emplacement d’une application

L’emplacement que vous définissez pour votre application détermine l’ordinateur sur lequel l’application s’exécutera. Vous pouvez choisir d’exécuter votre application sur l’ordinateur sur lequel se trouvent les données, sur l’ordinateur que vous utilisez pour définir l’emplacement ou sur un ordinateur spécifié.

**Pour définir l’emplacement d’une application**

1.  Avec Dcomcnfg.exe en cours d’exécution, sélectionnez l’application à partir de la page **applications** et choisissez le bouton **Propriétés** (ou double-cliquez sur l’application sélectionnée).

2.  Dans la page **emplacement** , activez une ou plusieurs cases à cocher correspondant aux emplacements où vous souhaitez que l’application s’exécute. Si vous sélectionnez plusieurs cases à cocher, COM utilise le premier qui s’applique. Si Dcomcnfg.exe est en cours d’exécution sur l’ordinateur serveur, sélectionnez toujours **exécuter l’application sur cet ordinateur**.

3.  Si vous devez définir d’autres propriétés pour cette application, cliquez sur le bouton **appliquer** pour appliquer le nouvel emplacement. Choisissez **OK** si vous avez terminé de définir les propriétés de cette application et que vous souhaitez appliquer les modifications.

## <a name="setting-launch-permissions-for-an-application"></a>Définition des autorisations de lancement pour une application

Avec Dcomcnfg.exe, vous pouvez définir des autorisations de lancement pour contrôler la liste des utilisateurs qui sont autorisés ou non à lancer un serveur particulier. Vous pouvez ajouter des utilisateurs ou des groupes à la liste, en spécifiant si l’autorisation d’accès est accordée ou refusée. Vous pouvez également supprimer des utilisateurs de la liste.

**Pour définir des autorisations de lancement pour une application**

1.  Avec Dcomcnfg.exe en cours d’exécution, sélectionnez l’application à partir de la page **applications** et choisissez le bouton **Propriétés** (ou double-cliquez sur l’application sélectionnée).

2.  Sur la page des propriétés de **sécurité** , sélectionnez la case d’option **utiliser des autorisations d’exécution personnalisées** et choisissez le bouton **modifier** dans la même zone.

3.  Pour supprimer des utilisateurs ou des groupes, sélectionnez l’utilisateur ou le groupe que vous souhaitez supprimer, puis choisissez le bouton **supprimer** . L’utilisateur ou le groupe sélectionné n’apparaît plus dans la zone de liste. Une fois la suppression de l’utilisateur et des groupes terminée, cliquez sur **OK**.

4.  Si vous souhaitez ajouter des utilisateurs ou des groupes, cliquez sur le bouton **Ajouter** .

5.  Si vous connaissez le nom d’utilisateur complet que vous souhaitez ajouter, tapez-le dans la zone de texte **Ajouter des noms** . Si vous ne connaissez pas le nom d’utilisateur, vous pouvez accéder à la base de données utilisateur pour la trouver (voir navigation dans la base de données utilisateur ci-dessous). Une fois que vous avez localisé le nom d’utilisateur, sélectionnez l’utilisateur ou le groupe dans la zone de liste **noms** , puis cliquez sur le bouton **Ajouter** .

6.  Dans la zone **de liste type d’accès** , sélectionnez le type d’accès ( **autoriser le lancement** ou refuser le **lancement**). Pour ajouter d’autres utilisateurs qui auront le type d’accès sélectionné, répétez l’étape 5. Lorsque vous avez terminé d’ajouter des utilisateurs pour le type d’accès sélectionné, cliquez sur le bouton **OK** .

7.  Pour ajouter des utilisateurs qui auront un type d’accès différent, répétez les étapes 5 et 6. Dans le cas contraire, choisissez **OK** pour appliquer les modifications.

## <a name="setting-access-permissions-for-an-application"></a>Définition des autorisations d’accès pour une application

Avec Dcomcnfg.exe, vous pouvez gérer la liste des utilisateurs qui se voient accorder ou refuser l’accès aux méthodes d’un serveur spécifique en définissant des autorisations d’accès. Vous pouvez ajouter des utilisateurs ou des groupes à la liste, en spécifiant si l’autorisation d’accès est accordée ou refusée. Vous pouvez également supprimer des utilisateurs de la liste.

Lors de la définition des autorisations d’accès, vous devez vous assurer que le système est inclus dans la liste des utilisateurs auxquels l’accès est accordé. Si vous avez accordé des autorisations d’accès à tout le monde, SYSTEM est inclus implicitement.

Le processus de définition des autorisations d’accès pour une application est similaire à la définition des autorisations de lancement. Les étapes sont les suivantes.

**Pour définir des autorisations d’accès pour une application**

1.  Avec Dcomcnfg.exe en cours d’exécution, sélectionnez l’application à partir de la page **applications** et choisissez le bouton **Propriétés** (ou double-cliquez sur l’application sélectionnée).

2.  Sur la page propriété de **sécurité** , sélectionnez la case d’option **utiliser des autorisations d’accès personnalisées** et choisissez le bouton **modifier** dans la même zone.

3.  Pour supprimer des utilisateurs ou des groupes, sélectionnez l’utilisateur ou le groupe que vous souhaitez supprimer, puis choisissez le bouton **supprimer** . L’utilisateur ou le groupe sélectionné n’apparaît plus dans la zone de liste. Une fois la suppression de l’utilisateur et des groupes terminée, cliquez sur **OK**.

4.  Si vous souhaitez ajouter un utilisateur ou un groupe, cliquez sur le bouton **Ajouter** .

5.  Si vous connaissez le nom d’utilisateur complet que vous souhaitez ajouter, tapez-le dans la zone de texte **Ajouter des noms** . Si vous ne connaissez pas le nom d’utilisateur, vous pouvez parcourir la base de données utilisateur pour la trouver. Une fois que vous avez localisé le nom d’utilisateur, sélectionnez l’utilisateur ou le groupe dans la zone de liste **noms** , puis cliquez sur le bouton **Ajouter** .

6.  Dans la zone **de liste type d’accès** , sélectionnez le type d’accès ( **autoriser l’accès** ou refuser l' **accès**). Pour ajouter d’autres utilisateurs qui auront le type d’accès sélectionné, répétez l’étape 5. Lorsque vous avez terminé d’ajouter des utilisateurs pour le type d’accès sélectionné, cliquez sur le bouton **OK** .

7.  Pour ajouter des utilisateurs qui auront un type d’accès différent, répétez les étapes 5 et 6. Dans le cas contraire, choisissez **OK** pour appliquer les modifications.

## <a name="setting-the-identity-for-an-application"></a>Définition de l’identité d’une application

L’identité d’une application est le compte utilisé pour exécuter l’application. L’identité peut être celle de l’utilisateur actuellement connecté (l’utilisateur interactif), le compte d’utilisateur du processus client qui a lancé le serveur, un utilisateur spécifié ou un service. Vous pouvez utiliser Dcomcnfg.exe pour choisir l’une de ces identités pour l’application. Pour obtenir de l’aide sur le choix de l’identité à définir pour votre application, consultez identité de l' [application](application-identity.md).

**Pour définir l’identité d’une application**

1.  Avec Dcomcnfg.exe en cours d’exécution, sélectionnez l’application à partir de la page **applications** et choisissez le bouton **Propriétés** (ou double-cliquez sur l’application sélectionnée).

2.  Dans la page de propriétés **identité** , sélectionnez la case d’option correspondant à l’identité de votre choix. Si vous choisissez **cet utilisateur**, vous devez taper le nom d’utilisateur, le mot de passe et le mot de passe confirmé.

3.  Si vous devez définir d’autres propriétés pour cette application, cliquez sur le bouton **appliquer** pour appliquer la nouvelle identité. Choisissez **OK** si vous avez terminé de définir les propriétés de cette application et que vous souhaitez appliquer les modifications.

## <a name="browsing-the-user-database"></a>Exploration de la base de données utilisateur

Vous parcourez la base de données utilisateur dans Dcomcnfg.exe lorsque vous avez besoin de rechercher le nom d’utilisateur complet d’un utilisateur particulier. Par exemple, vous pouvez parcourir la base de données utilisateur pour localiser un utilisateur que vous souhaitez ajouter pour des autorisations d’accès ou de lancement.

**Pour parcourir la base de données utilisateur**

1.  Dans la zone liste **des noms à partir de** , sélectionnez le domaine contenant l’utilisateur ou le groupe que vous souhaitez ajouter.

2.  Pour afficher les utilisateurs qui appartiennent au domaine sélectionné, cliquez sur le bouton **afficher les utilisateurs** .

3.  Pour afficher les membres d’un groupe particulier, sélectionnez le groupe dans la zone de liste **noms** , puis cliquez sur le bouton **afficher les membres** .

4.  Si vous ne trouvez pas l’utilisateur ou le groupe que vous souhaitez ajouter, cliquez sur le bouton **Rechercher** , qui affiche la boîte de dialogue **Rechercher un compte** . Sélectionnez le domaine dans lequel vous souhaitez effectuer la recherche (ou sélectionnez **Rechercher tout**), tapez le nom d’utilisateur que vous souhaitez rechercher, puis choisissez le bouton **Rechercher** .

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Applications Dcomcnfg.exe et 64 bits

sur les systèmes d’exploitation x64 de Windows XP à Windows Server 2008, la version 64 bits de DCOMCNFG.EXE ne configure pas correctement les applications DCOM 32 bits pour l’activation à distance. Ce comportement provoque l’activation locale des composants qui sont censés être activés à distance. ce comportement ne se produit pas dans Windows 7 et Windows Server 2008 R2 et versions ultérieures.

La solution de contournement consiste à utiliser la version 32 bits de DCOMCNFG. Exécutez la version 32 bits de mmc.exe et chargez la version 32 bits du composant logiciel enfichable Services de composants à l’aide de la ligne de commande suivante.

C : \\ Windows \\ SysWOW64>**mmc comexp. msc/32**

La version 32 bits des services de composants inscrit correctement les applications DCOM 32 bits pour l’activation à distance.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 




