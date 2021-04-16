---
title: Création et suppression d’objets dans Active Directory Domain Services
description: La procédure utilisée pour créer et supprimer des objets par programmation dans Active Directory Domain Services dépend de la technologie de programmation utilisée.
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- Création et suppression d’objets Active Directory Active Directory
- Active Directory Domain Services Active Directory, utilisation de la création et de la suppression d’objets
- objets Active Directory, créer et supprimer des objets Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d3e85ef3c356978faeab059e3969bb657185bd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462895"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a>Création et suppression d’objets dans Active Directory Domain Services

La procédure utilisée pour créer et supprimer des objets par programmation dans Active Directory Domain Services dépend de la technologie de programmation utilisée. Pour plus d’informations sur la création et la suppression d’objets dans Active Directory Domain Services avec une technologie de programmation spécifique, consultez les rubriques figurant dans le tableau suivant.



| Technologie de programmation                                                                       | Informations supplémentaires                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Interfaces de service Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Création et suppression d’objets](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Modification d’une entrée d’annuaire](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [System.DirectoryServices](/dotnet/api/system.directoryservices) | [Créer, supprimer, renommer et déplacer des objets](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx) |



 

## <a name="creating-an-object"></a>Création d’un objet

En général, les seuls attributs requis pour un objet à créer sont les attributs **CN** et **objectClass** . Le simple fait de créer un objet ne le rend pas obligatoirement un objet fonctionnel. Certains types d’objets, tels que les utilisateurs et les groupes, possèdent des attributs supplémentaires requis pour les rendre fonctionnels. Pour plus d’informations sur la création de types spécifiques d’objets, consultez [création d’un utilisateur](creating-a-user.md) et [création de groupes dans un domaine](creating-groups-in-a-domain.md).

**Windows Server 2003 :** Lorsqu’un objet de la classe [**utilisateur**](/windows/desktop/ADSchema/c-user), [**groupe**](/windows/desktop/ADSchema/c-group)ou [**ordinateur**](/windows/desktop/ADSchema/c-computer) est créé sur un contrôleur de domaine qui s’exécute sur le serveur comparaison 2003 ou une version ultérieure, le contrôleur de domaine définit automatiquement l’attribut [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) de l’objet sur une chaîne unique, si aucune n’est spécifiée.

## <a name="deleting-an-object"></a>Suppression d’un objet

Le serveur Active Directory effectue les actions suivantes lorsqu’un objet est supprimé :

-   L’attribut **IsDeleted** de l’objet supprimé a la valeur **true**. Les objets avec une valeur d’attribut **IsDeleted** définie sur **true** sont appelés des objets [*Tombstone*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85)).
-   L’objet supprimé est déplacé vers le conteneur objets supprimés pour son contexte d’appellation. Si la propriété **systemFlags** de l’objet contient l’indicateur 0x02000000, l’objet n’est pas déplacé vers le conteneur objets supprimés. Pour plus d’informations sur la liaison et l’énumération du contenu du conteneur d’objets supprimés, consultez [récupération des objets supprimés](retrieving-deleted-objects.md).
-   Le conteneur objets supprimés est plat, donc tous les objets résident au même niveau dans le conteneur objets supprimés. Ainsi, le nom unique relatif de l’objet supprimé est modifié pour garantir que le nom est unique dans le conteneur objets supprimés. Si le nom d’origine est plus long que 75 caractères, il est tronqué à 75 caractères. Les éléments suivants sont ensuite ajoutés au nouveau nom :
    1.  Un caractère 0x0A
    2.  La chaîne « DEL : »
    3.  Forme de chaîne d’un GUID unique, par exemple « 947e3228-70c9-4311-8B7A-e5c9b5bd4432 »

    Voici un exemple de nom d’objet supprimé :
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   La plupart des valeurs d’attribut de l’objet supprimé sont supprimées. Les attributs suivants sont automatiquement conservés :

    -   **attributeID**
    -   **attributeSyntax**
    -   **distinguishedName**
    -   **dNReferenceUpdate**
    -   **flatName**
    -   **governsID**
    -   **groupType**
    -   **instanceType**
    -   **lDAPDisplayName**
    -   **legacyExchangeDN**
    -   **mS-DS-CreatorSID**
    -   **mSMQOwnerID**
    -   **name**
    -   **nCName**
    -   **objectClass**
    -   **Guid**
    -   **objectSid**
    -   **oMSyntax**
    -   **proxiedObjectName**
    -   **replPropertyMetaData**
    -   **sAMAccountName**
    -   **securityIdentifier**
    -   **subClassOf**
    -   **systemFlags**
    -   **trustAttributes**
    -   **trustDirection**
    -   **trustPartner**
    -   **trustType**
    -   **userAccountControl**
    -   **uSNChanged**
    -   **uSNCreated**
    -   **whenCreated**

    D’autres attributs qui ont une valeur d’attribut **searchFlags** contenant 0x00000008 sont également conservés.

    Les valeurs d’attribut suivantes sont toujours supprimées d’un objet supprimé :

    -   **objectCategory**
    -   **samAccountType**

-   Le descripteur de sécurité de l’objet supprimé est conservé et les entrées de contrôle d’accès héritables ne sont pas propagées. Le descripteur de sécurité est conservé tel quel au moment de la suppression de l’objet.
-   Les liens vers et à partir de l’objet supprimé sont effacés. Cette opération est effectuée en arrière-plan après la suppression de l’objet. Si l’objet supprimé est restauré avant que tous les liens soient effacés, une erreur est reçue.
-   Si l’objet est supprimé sur un contrôleur de domaine Windows Server 2003, l’attribut **lastKnownParent** de l’objet supprimé est défini sur le nom unique du conteneur dans lequel l’objet a été contenu au moment de sa suppression.

L’objet supprimé reste dans le conteneur objets supprimés pendant une période de temps appelée durée de *vie de désactivation*. Par défaut, la durée de vie de la désactivation est de 60 jours, mais cette valeur peut être modifiée par l’administrateur système. Une fois la durée de vie de désactivation expirée, l’objet est supprimé définitivement du service d’annuaire. Pour éviter une opération de suppression manquante, une application doit effectuer des synchronisations incrémentielles plus fréquemment que la durée de vie de désactivation.

Windows Server 2003 ajoute la possibilité de restaurer les objets supprimés. Pour plus d’informations sur la restauration d’objets supprimés, consultez [restauration d’objets supprimés](restoring-deleted-objects.md).

Lorsqu’un élément est supprimé, aucun des attributs de l’objet ne peut être modifié. Dans Windows Server 2003, il est possible de modifier le descripteur de sécurité (l’attribut **ntSecurityDescriptor** ) sur un objet supprimé. Cela permet de restaurer les objets lorsque la personne qui restaure l’objet n’a pas d’autorisations d’accès en écriture à des attributs obligatoires. Pour mettre à jour le descripteur de sécurité sur un objet supprimé, l’appelant doit disposer du droit d’accès au contrôle « réanimer l’objet tombstone » sur le contexte d’appellation, en plus de la **\_ DAC d’écriture** normale et de l’accès en **écriture au \_ propriétaire** . Même si le descripteur de sécurité est restrictif, l’administrateur peut tout d’abord prendre possession de l’objet, en supposant que l’administrateur dispose du privilège **se \_ prendre \_ possession du \_ nom** , puis de modifier le descripteur de sécurité. Pour ce faire, utilisez la fonction [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) avec le contrôle [**\_ \_ Show \_ Deleted \_ OID du serveur LDAP**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) . La liste de modifications doit contenir un seul attribut de remplacement pour l’attribut **ntSecurityDescriptor** .

 

 