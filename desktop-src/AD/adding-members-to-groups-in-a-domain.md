---
title: Ajout de membres à des groupes dans un domaine
description: Cette rubrique montre comment ajouter des membres à des groupes dans un domaine.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Ajout de membres à des groupes dans un domaine AD
- Groupes Active Directory, ajout de membres à des groupes dans un domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9f0c85943752b42cf3d9d8b88d385aaba9e014b21aa9f538955cb49b1a750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024756"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Ajout de membres à des groupes dans un domaine

Un groupe peut contenir un nombre quelconque d’utilisateurs, de contacts ou d’autres groupes en tant que membres. La liste suivante répertorie les attributs de l’objet de groupe qui contrôle l’appartenance à un groupe.



| Attribut                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**membre**](/windows/desktop/ADSchema/a-member)<br/>     | L’attribut [**member**](/windows/desktop/ADSchema/a-member) contient les noms uniques des objets qui sont membres du groupe.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | L’attribut [**memberOf**](/windows/desktop/ADSchema/a-memberof) contient les noms uniques des groupes qui contiennent le groupe en tant que membre direct. L’attribut **memberOf** ne contient pas de données d’appartenance au groupe héritées. Par exemple, si groupa est membre de GroupB et GroupB est membre de GroupC, l’attribut **memberOf** de groupa contiendra GroupB, mais pas GroupC.<br/> Le serveur Active Directory gère cette propriété. Lorsqu’un nom unique est ajouté à la propriété de [**membre**](/windows/desktop/ADSchema/a-member) d’un autre groupe, le nom unique de ce groupe est ajouté à la propriété [**memberOf**](/windows/desktop/ADSchema/a-memberof) de ce groupe.<br/> |



 

Chacune des méthodes suivantes peut être utilisée pour ajouter un membre à un groupe. Vous pouvez ajouter un membre à l’aide du nom unique du membre ou de la liaison à l’objet de membre, puis ajouter l’objet membre à l’objet de groupe.

Pour ajouter un membre qui appartient à un domaine de niveau inférieur à un groupe dans un domaine de niveau supérieur, utilisez la forme pouvant être liée de la chaîne SID pour le nom unique. Pour plus d’informations et pour obtenir un exemple de code qui montre comment convertir un **objectSID** en chaîne pouvant être liée, consultez la fonction exemple **GetLDAPSidBindStringFromVariantSID** dans l' [exemple de code pour la conversion d’un objectSID en chaîne pouvant être liée](example-code-for-converting-an-objectsid-into-a-bindable-string-.md).

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Ajout de membres à un groupe à l’aide de IADsGroup
</dt> <dd>

L’interface [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) peut être utilisée pour ajouter des membres à un groupe à l’aide de la méthode [**IADsGroup. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Liez et obtenez l’interface **IADsGroup** pour l’objet de groupe. Ensuite, vous pouvez utiliser la méthode **IADsGroup. Add** pour ajouter des membres au groupe.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Ajout de membres à un groupe à l’aide de IDirectoryObject
</dt> <dd>

L’interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) peut être utilisée pour ajouter des membres à un groupe à l’aide de la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) pour modifier l’attribut de [**membre**](/windows/desktop/ADSchema/a-member) du groupe. Liez et obtenez l’interface **IDirectoryObject** pour l’objet de groupe. Utilisez ensuite la méthode **IDirectoryObject :: SetObjectAttributes** pour modifier l’attribut de **membre** .

> [!Note]  
> Étant donné que l’attribut de [**membre**](/windows/desktop/ADSchema/a-member) a plusieurs valeurs, assurez-vous d’utiliser le code de contrôle de l' **\_ \_ Ajout** d’attributs ADS pour ajouter un nom unique à l’attribut de **membre** . L’utilisation du code de contrôle de **\_ \_ mise à jour de publicités attr** entraîne le remplacement des valeurs des **membres** existants.

 

L’interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) peut également être utilisée pour ajouter des membres à un groupe lors de la création du groupe en spécifiant les membres dans le paramètre *pAttributeEntries* de la méthode [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Ajout de membres à un groupe à l’aide de System. DirectoryServices
</dt> <dd>

Vous pouvez utiliser l’espace de noms [System. DirectoryServices](/dotnet/api/system.directoryservices) pour ajouter des membres à un groupe à l’aide de la méthode **PropertyValueCollection. Add** sur la propriété de **membre** de l’objet Group. Pour plus d’informations, consultez [définition des propriétés sur les objets d’annuaire](/previous-versions/ms180860(v=vs.90)).

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Ajout de membres à un groupe à l’aide de l’API LDAP
</dt> <dd>

Vous pouvez utiliser l’API [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) pour ajouter des membres à un groupe à l’aide de l’une des fonctions de [**\_ modification \* LDAP**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) . Pour plus d’informations, consultez [modification d’une entrée d’annuaire](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry).

</dd> </dl>

 

