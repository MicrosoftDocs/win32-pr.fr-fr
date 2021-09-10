---
title: Définition de la sécurité System-Wide à l’aide de DCOMCNFG
description: Si vous souhaitez que toutes les applications sur un ordinateur qui ne fournissent pas leur propre sécurité partagent les mêmes paramètres de sécurité par défaut, vous devez définir la sécurité à l’échelle du système.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7feaaf356263a48c2c93eb9b3b3764b7352cd39
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363516"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Définition de la sécurité System-Wide à l’aide de DCOMCNFG

La modification des paramètres de sécurité à l’ensemble du système affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus. Cela peut empêcher de telles applications de fonctionner correctement. Si vous modifiez les paramètres de sécurité à l’ensemble du système pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière. Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau](setting-processwide-security.md)du processus.

Si vous souhaitez que toutes les applications sur un ordinateur qui ne fournissent pas leur propre sécurité partagent les mêmes paramètres de sécurité par défaut, vous devez définir la sécurité à l’échelle du système. L’utilisation de Dcomcnfg.exe permet de définir facilement des valeurs par défaut dans le Registre qui s’appliquent à toutes les applications sur un ordinateur.

Il est important de comprendre que si le client ou le serveur appelle de manière explicite la méthode [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir la sécurité au niveau du processus, les paramètres par défaut dans le Registre sont ignorés et les paramètres à la valeur **CoInitializeSecurity** sont utilisés à la place pour les paramètres de sécurité du processus. En outre, si vous utilisez Dcomcnfg.exe pour spécifier les paramètres de sécurité d’un processus particulier, les paramètres de l’ordinateur par défaut sont remplacés par les paramètres du processus.

Lorsque vous activez la sécurité à l’échelle du système, vous devez définir le niveau d’authentification sur une valeur autre que aucun et vous devez définir les autorisations d’exécution et d’accès. Vous avez la possibilité de définir le niveau d’emprunt d’identité par défaut, et vous pouvez également activer le suivi des références. Les rubriques suivantes fournissent des procédures pas à pas :

-   [Définition de System-Wide niveau d’authentification par défaut](#setting-system-wide-default-authentication-level)
-   [Définition des autorisations de lancement System-Wide](#setting-system-wide-launch-permissions)
-   [Définition des autorisations d’accès System-Wide](#setting-system-wide-access-permissions)
-   [Définition du niveau d’emprunt d’identité System-Wide](#setting-system-wide-impersonation-level)
-   [Définir System-Wide le suivi des références](#setting-system-wide-reference-tracking)
-   [Activation et désactivation de DCOM](#enabling-and-disabling-dcom)
-   [Rubriques connexes](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Définition de System-Wide niveau d’authentification par défaut

Le niveau d’authentification est utilisé pour indiquer à COM le niveau auquel vous souhaitez que le client soit authentifié. Ces niveaux offrent différents niveaux de protection, de la non-protection au chiffrement complet. Pour activer la sécurité pour un ordinateur, vous devez choisir un niveau d’authentification autre que aucun. Vous pouvez choisir un paramètre de ce type, à l’aide de Dcomcnfg.exe, en procédant comme suit.

**Pour définir le niveau d’authentification à l’échelle du système**

1.  Exécutez Dcomcnfg.exe.

2.  Choisissez l’onglet **propriétés par défaut** .

3.  Dans la zone de liste **DefaultÂ AuthenticationÂ Level** , choisissez une valeur autre que **(aucune)**.

4.  Si vous configurez plus de propriétés pour l’ordinateur, cliquez sur le bouton **appliquer** pour appliquer le nouveau niveau d’authentification. Sinon, cliquez sur **OK** pour appliquer les modifications et quitter Dcomcnfg.exe.

## <a name="setting-system-wide-launch-permissions"></a>Définition des autorisations de lancement System-Wide

Les autorisations de lancement que vous définissez avec Dcomcnfg.exe déterminer une liste d’utilisateurs, chacun d’entre eux disposant d’une autorisation ou d’un refus explicite pour lancer un serveur qui ne fournit pas ses propres paramètres d’autorisation de lancement. Lors de la définition des autorisations de lancement, vous pouvez ajouter ou supprimer un ou plusieurs utilisateurs ou groupes dans cette liste. Pour chaque utilisateur que vous ajoutez, vous devez spécifier si l’utilisateur est autorisé ou non à accéder à l’autorisation Launch.

**Pour définir des autorisations de lancement pour un ordinateur**

1.  Sur la page de propriétés **sécurité par défaut** dans Dcomcnfg.exe, choisissez le bouton **modifier par défaut** dans la zone **autorisations d’exécution par défaut** .

2.  Pour supprimer des utilisateurs ou des groupes, sélectionnez l’utilisateur ou le groupe que vous souhaitez supprimer, puis choisissez le bouton **supprimer** . L’utilisateur ou le groupe sélectionné n’apparaît plus dans la zone de liste. Lorsque vous avez terminé de supprimer des utilisateurs et des groupes, cliquez sur **OK**.

3.  Si vous souhaitez ajouter un utilisateur ou un groupe, cliquez sur le bouton **Ajouter** .

4.  Si vous connaissez le nom d’utilisateur complet que vous souhaitez ajouter, tapez-le dans la zone de texte **Ajouter des noms** . Si vous ne connaissez pas le nom d’utilisateur, consultez Définition de la **sécurité échelle à l’aide de DCOMCNFG** pour le trouver. Une fois que vous avez localisé le nom d’utilisateur, sélectionnez l’utilisateur ou le groupe dans la zone de liste **noms** , puis cliquez sur le bouton **Ajouter** .

5.  Dans la zone **de liste type d’accès** , sélectionnez le type d’accès ( **autoriser le lancement** ou refuser le **lancement**). Pour ajouter d’autres utilisateurs qui auront également le type d’accès sélectionné, répétez l’étape 4. Lorsque vous avez terminé d’ajouter des utilisateurs pour le type d’accès sélectionné, cliquez sur le bouton **OK** .

6.  Pour ajouter des utilisateurs qui auront un type d’accès différent, répétez les étapes 4 et 5. Dans le cas contraire, choisissez **OK** pour appliquer les modifications.

## <a name="setting-system-wide-access-permissions"></a>Définition des autorisations d’accès System-Wide

Dcomcnfg.exe vous permet de définir des autorisations d’accès pour contrôler la liste des utilisateurs qui se voient accorder ou refuser l’accès aux méthodes des serveurs qui ne fournissent pas leurs propres autorisations d’accès. Vous pouvez ajouter des utilisateurs ou des groupes à la liste, en spécifiant si l’autorisation d’accès est accordée ou refusée. Vous pouvez également supprimer des utilisateurs de la liste.

Lors de la définition des autorisations d’accès, vous devez vous assurer que le système est inclus dans la liste des utilisateurs auxquels l’accès est accordé. Si vous avez accordé des autorisations d’accès à tout le monde, SYSTEM est inclus implicitement.

Le processus de définition des autorisations d’accès d’un ordinateur est similaire à celui de la définition des autorisations d’exécution. Les étapes suivantes doivent être effectuées.

**Pour définir des autorisations d’accès pour un ordinateur**

1.  Dans la page de propriétés **sécurité par défaut** de Dcomcnfg.exe, choisissez le bouton **modifier par défaut** dans la zone **autorisations d’accès par défaut** .

2.  Pour supprimer des utilisateurs ou des groupes, sélectionnez l’utilisateur ou le groupe que vous souhaitez supprimer, puis choisissez le bouton **supprimer** . L’utilisateur ou le groupe sélectionné n’apparaît plus dans la zone de liste. Une fois la suppression de l’utilisateur et des groupes terminée, cliquez sur **OK**.

3.  Si vous souhaitez ajouter un utilisateur ou un groupe, cliquez sur le bouton **Ajouter** .

4.  Si vous connaissez le nom d’utilisateur complet que vous souhaitez ajouter, tapez-le dans la zone de texte **Ajouter des noms** . Si vous ne connaissez pas le nom d’utilisateur, consultez Définition de la [sécurité au niveau du processus à l’aide de DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) pour le trouver. Une fois que vous avez localisé le nom d’utilisateur, sélectionnez l’utilisateur ou le groupe dans la zone de liste **noms** , puis cliquez sur le bouton **Ajouter** .

5.  Dans la zone **de liste type d’accès** , sélectionnez le type d’accès ( **autoriser l’accès** ou refuser l' **accès**). Pour ajouter d’autres utilisateurs qui auront le type d’accès sélectionné, répétez l’étape 4. Lorsque vous avez terminé d’ajouter des utilisateurs pour le type d’accès sélectionné, cliquez sur le bouton **OK** .

6.  Pour ajouter des utilisateurs qui auront un type d’accès différent, répétez les étapes 4 et 5. Dans le cas contraire, choisissez **OK** pour appliquer les modifications.

## <a name="setting-system-wide-impersonation-level"></a>Définition du niveau d’emprunt d’identité System-Wide

Le niveau d’emprunt d’identité, défini par le client, détermine la quantité d’autorité donnée au serveur pour agir au nom du client. Par exemple, lorsque le client a défini son niveau d’emprunt d’identité à déléguer, le serveur peut accéder aux ressources locales et distantes en tant que client, et le serveur peut masquer les limites de plusieurs ordinateurs si la fonction de masquage est définie. Pour déterminer le niveau d’emprunt d’identité que vous devez choisir, consultez [niveaux d’emprunt d’identité](impersonation-levels.md) et [masquage](cloaking.md).

La définition du niveau d’emprunt d’identité par défaut pour l’ensemble de l’ordinateur indique à COM le niveau d’emprunt d’identité à utiliser lorsqu’un client particulier sur l’ordinateur ne spécifie pas un niveau d’emprunt d’identité par programmation en utilisant [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

**Pour définir le niveau d’emprunt d’identité d’un ordinateur**

1.  Avec Dcomcnfg.exe en cours d’exécution, choisissez l’onglet **propriétés par défaut** .

2.  Dans la zone de liste **niveau d’emprunt d’identité par défaut** , choisissez le niveau d’emprunt d’identité souhaité.

3.  Si vous configurez plus de propriétés pour l’ordinateur, cliquez sur le bouton **appliquer** pour appliquer le nouveau niveau d’emprunt d’identité. Dans le cas contraire, choisissez **OK** pour appliquer les modifications et quitter Dcomcnfg.exe.

## <a name="setting-system-wide-reference-tracking"></a>Définir System-Wide le suivi des références

Lorsque vous activez le suivi des références, vous demandez à COM d’effectuer des vérifications de sécurité supplémentaires et d’effectuer le suivi des informations qui empêchent les objets d’être libérés trop tôt. Gardez à l’esprit que ces vérifications supplémentaires sont coûteuses. Pour plus d’informations sur le suivi de référence, consultez [suivi des références](reference-tracking.md). Pour activer ou désactiver le suivi des références, procédez comme suit.

**Pour définir le suivi des références pour un ordinateur**

1.  Avec Dcomcnfg.exe en cours d’exécution, choisissez l’onglet **propriétés par défaut** .

2.  Pour activer (ou désactiver) le suivi des références, activez (ou désactivez) la case à cocher **fournir une sécurité supplémentaire pour le suivi des références** au bas de la page.

3.  Si vous configurez plus de propriétés pour l’ordinateur, cliquez sur le bouton **appliquer** pour appliquer le nouveau paramètre. Dans le cas contraire, choisissez **OK** pour appliquer les modifications et quitter Dcomcnfg.exe.

## <a name="enabling-and-disabling-dcom"></a>Activation et désactivation de DCOM

Lorsqu’un ordinateur fait partie d’un réseau, le protocole DCOM permet aux objets COM de cet ordinateur de communiquer avec des objets COM sur d’autres ordinateurs. Vous pouvez désactiver DCOM pour un ordinateur particulier, mais cela entraînera la désactivation de toutes les communications entre les objets sur cet ordinateur et les objets sur d’autres ordinateurs.

La désactivation de DCOM sur un ordinateur n’a aucun effet sur les objets COM locaux. COM continue de rechercher les autorisations de lancement que vous avez spécifiées. Si aucune autorisation de lancement n’a été spécifiée, les autorisations de lancement par défaut sont utilisées. Même si vous désactivez DCOM, si un utilisateur a un accès physique à l’ordinateur, il peut lancer un serveur sur l’ordinateur, sauf si vous définissez des autorisations de lancement pour ne pas l’autoriser.

> [!Note]  
> Si vous désactivez DCOM sur un ordinateur distant, vous ne pourrez pas accéder à distance à cet ordinateur par la suite pour réactiver DCOM. Pour réactiver DCOM, vous aurez besoin d’un accès physique à cet ordinateur.

 

**Pour activer (ou désactiver) manuellement DCOM pour un ordinateur**

1.  Exécutez Dcomcnfg.exe.

2.  Choisissez l’onglet **Propriétés de DefaultÂ** .

3.  Activez (ou désactivez) la case à cocher **activer les COMÂ distribués sur cet ordinateur** .

4.  Si vous configurez plus de propriétés pour l’ordinateur, cliquez sur le bouton **appliquer** pour activer (ou désactiver) DCOM. Sinon, cliquez sur **OK** pour appliquer les modifications et quitter Dcomcnfg.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité au niveau du processus](setting-processwide-security.md)
</dt> </dl>

 

 




