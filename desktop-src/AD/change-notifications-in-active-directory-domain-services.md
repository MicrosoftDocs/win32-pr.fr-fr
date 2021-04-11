---
title: Notifications de modifications dans Active Directory Domain Services
description: Active Directory Domain Services fournir un mécanisme permettant à une application cliente de s’inscrire auprès d’un contrôleur de domaine pour recevoir des notifications de modification.
ms.assetid: 27f6c7c1-b32e-457a-9be5-47836d097ab1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee564727cfbcb2bfdb367f822fdc137bca7c4e37
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031050"
---
# <a name="change-notifications-in-active-directory-domain-services"></a>Notifications de modifications dans Active Directory Domain Services

Active Directory Domain Services fournir un mécanisme permettant à une application cliente de s’inscrire auprès d’un contrôleur de domaine pour recevoir des notifications de modification. Pour ce faire, le client spécifie le contrôle de notification de modification LDAP dans une opération de recherche LDAP asynchrone. Le client spécifie également les paramètres de recherche suivants.



| Paramètre             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Étendue<br/>      | Spécifiez soit la **\_ \_ base de l’étendue LDAP** pour surveiller uniquement l’objet, soit l' **\_ étendue LDAP \_** pour surveiller les enfants immédiats de l’objet, à l’exclusion de l’objet lui-même. Ne spécifiez pas la **\_ sous- \_ arborescence de l’étendue LDAP**. Bien que l’étendue de la sous-arborescence soit prise en charge si l’objet de base est la racine d’un contexte d’appellation, son utilisation peut avoir un impact considérable sur les performances du serveur, car elle génère un message de résultat de recherche LDAP chaque fois qu’un objet dans le contexte d’appellation est modifié. Vous ne pouvez pas spécifier la **\_ sous- \_ arborescence étendue LDAP** pour une sous-arborescence arbitraire.<br/> |
| Filtrer<br/>     | Spécifiez un filtre de recherche « (objectClass = \* ) », ce qui signifie que vous recevez des notifications pour les modifications apportées à un objet dans l’étendue spécifiée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| Attributs<br/> | Spécifiez une liste d’attributs à retourner lorsqu’une modification se produit. N’oubliez pas que vous recevez des notifications lorsqu’un attribut est modifié, pas seulement les attributs spécifiés.<br/>                                                                                                                                                                                                                                                                                                                                                                               |



 

Vous pouvez inscrire jusqu’à cinq demandes de notification sur une seule connexion LDAP. Vous devez disposer d’un thread dédié qui attend les notifications et les traite rapidement. Lorsque vous appelez la \_ fonction LDAP Search \_ ext pour inscrire une demande de notification, la fonction retourne un identificateur de message qui identifie cette demande. Vous utilisez ensuite la fonction [**LDAP \_ result**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result) pour attendre les notifications de modification. Lorsqu’une modification se produit, le serveur envoie un message LDAP contenant l’identificateur de message pour la demande de notification qui a généré la notification. La fonction de **\_ résultat LDAP** est alors renvoyée avec les résultats de la recherche qui identifient l’objet modifié.

L’application cliente doit déterminer l’état initial de l’objet surveillé. Pour ce faire, vous devez d’abord inscrire la demande de notification, puis lire l’état actuel.

L’application cliente doit également déterminer la cause de la modification. Pour une recherche au niveau de base, une notification se produit lorsqu’un attribut change ou lorsque l’objet est supprimé ou déplacé. Pour une recherche à un niveau, une notification se produit lorsqu’un objet enfant est créé, supprimé, déplacé ou modifié. Sachez que le déplacement ou le changement de nom d’un objet dans la hiérarchie au-dessus d’un objet cible ne génère pas de notification, même si le nom unique de la cible a été modifié en conséquence. Par exemple, si vous surveillez les modifications apportées aux objets enfants d’un conteneur, vous ne recevrez pas de notifications si le conteneur lui-même est déplacé ou renommé.

Lorsque le client traite les résultats de la recherche, il peut utiliser \_ la \_ fonction LDAP obtenir DN pour obtenir le nom unique de l’objet qui a changé. Ne vous fiez pas à des noms uniques pour identifier les objets suivis, car les noms uniques peuvent changer. Au lieu de cela, incluez l’attribut **objectGUID** dans la liste d’attributs à récupérer. L' **objectGUID** de chaque objet reste inchangé, quel que soit l’emplacement où l’objet est déplacé dans la forêt d’entreprise.

Si un objet dans l’étendue de recherche est supprimé, le client reçoit une notification de modification et l’attribut **IsDeleted** de l’objet a la valeur **true**. Dans ce cas, les résultats de la recherche signalent le nouveau nom unique de l’objet dans le conteneur objets supprimés de sa partition. Il n’est pas nécessaire de spécifier le contrôle tombstone ([le \_ serveur LDAP \_ affiche l' \_ \_ OID supprimé](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)) pour recevoir des notifications de suppressions d’objets. Pour plus d’informations, consultez [récupération des objets supprimés](retrieving-deleted-objects.md).

Lorsqu’un client a inscrit une demande de notification, le client continue à recevoir des notifications jusqu’à ce que la connexion soit interrompue ou que le client abandonne la recherche en appelant la \_ fonction LDAP abandon. Si le client ou le serveur se déconnecte, par exemple, en cas de défaillance du serveur, la demande de notification est arrêtée. Lorsque le client se reconnecte, il doit s’inscrire à nouveau aux notifications, puis lire l’état actuel des objets qui vous intéressent en cas de modifications pendant la déconnexion du client.

Le client peut utiliser la valeur de l’attribut **uSNChanged** d’un objet pour déterminer si l’état actuel de l’objet sur le serveur reflète les dernières modifications que le client a reçues. Le système augmente l’attribut **uSNChanged** d’un objet lorsque l’objet est déplacé ou modifié. Par exemple, si le serveur échoue et que la partition d’annuaire est restaurée à partir d’une sauvegarde, le réplica du serveur d’un objet peut ne pas refléter les modifications précédemment signalées au client, auquel cas la valeur **uSNChanged** sur le serveur sera inférieure à la valeur stockée par le client.

Pour plus d’informations et pour obtenir un exemple de code qui utilise le contrôle de notification de modification LDAP dans une opération de recherche LDAP asynchrone, consultez l' [exemple de code pour recevoir des notifications de modification](example-code-for-receiving-change-notifications.md).

Pour plus d’informations sur l’utilisation du contrôle de notification de modification LDAP, consultez [vue d’ensemble des techniques de change Tracking](overview-of-change-tracking-techniques.md).

 

