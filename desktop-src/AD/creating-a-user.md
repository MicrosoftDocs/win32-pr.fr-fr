---
title: Création d’un utilisateur
description: Pour créer un utilisateur dans Active Directory Domain Services, créez un objet utilisateur dans le conteneur de domaine du domaine dans lequel vous souhaitez placer l’utilisateur.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Active Directory exemples Active Directory, création d’un utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3422d269351ae29fd15d12585ca02b91a4b9c23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469226"
---
# <a name="creating-a-user"></a>Création d’un utilisateur

Pour créer un utilisateur dans Active Directory Domain Services, créez un objet utilisateur dans le conteneur de domaine du domaine dans lequel vous souhaitez placer l’utilisateur. Les utilisateurs peuvent être créés à la racine du domaine, au sein d’une unité d’organisation ou au sein d’un conteneur.

lorsque vous créez un objet utilisateur, vous devez également définir les attributs, indiqués dans le tableau suivant, pour définir l’objet en tant qu’utilisateur légal reconnu par Active Directory Domain Services et le système Sécurité Windows.



| Attribut                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**8525**](/windows/desktop/ADSchema/a-cn)                         | Spécifie le nom de l’objet utilisateur dans le répertoire. Il s’agit du RDN (relative Distinguished Name) de l’objet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) | Spécifie une chaîne qui est le nom utilisé pour prendre en charge les clients et les serveurs d’une version précédente de Windows. Le [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) doit comporter moins de 20 caractères pour prendre en charge les clients d’une version précédente de Windows.<br/> [**SAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) doit être unique parmi tous les objets principaux de sécurité au sein du domaine. Vous devez exécuter une requête sur le domaine pour vérifier que le **sAMAccountName** est unique au sein du domaine.<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) est un attribut facultatif. Le serveur crée une valeur **sAMAccountName** aléatoire si aucune valeur n’est spécifiée.<br/> |



 

Vous pouvez également définir d’autres attributs. Les attributs utilisateur suivants sont définis avec des valeurs par défaut si vous ne les définissez pas explicitement au moment de la création.




| Attribut | Description | 
|-----------|-------------|
| <a href="/windows/desktop/ADSchema/a-accountexpires"><strong>AccountExpires dans</strong></a> | Spécifie la date d’expiration du compte. La valeur par défaut est <strong>TIMEQ_FOREVER</strong>, ce qui indique que le compte n’expirera jamais.<br /> | 
| <a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>nTSecurityDescriptor</strong></a> | Un descripteur de sécurité est créé en fonction de règles spécifiques. Pour plus d’informations, voir <a href="how-security-descriptors-are-set-on-new-directory-objects.md">Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire</a>.<br /> | 
| <a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a> | Spécifie la catégorie d’utilisateur. La valeur par défaut est « Person ».<br /> | 
| <a href="/windows/desktop/ADSchema/a-name"><strong>nomme</strong></a> | Spécifie le nom d'utilisateur. La valeur par défaut est la valeur définie pour <a href="/windows/desktop/ADSchema/a-cn"><strong>CN</strong></a>.<br /> | 
| <a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a> | Spécifie quand l’utilisateur a défini le mot de passe pour la dernière fois. La valeur par défaut est zéro, ce qui indique que l’utilisateur doit modifier le mot de passe à la prochaine ouverture de session.<br /> | 
| <a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a> | Contient des valeurs qui déterminent plusieurs fonctionnalités d’ouverture de session et de compte pour l’utilisateur.<br /> Par défaut, les indicateurs suivants sont définis :<br /><ul><li><strong>UF_ACCOUNTDISABLE</strong> -le compte est désactivé.</li><li><strong>UF_PASSWD_NOTREQD</strong> -aucun mot de passe n’est requis.</li><li><strong>UF_NORMAL_ACCOUNT</strong> : type de compte par défaut qui représente un utilisateur standard.</li></ul> | 
| <a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a> | Spécifie le ou les groupes dont l’utilisateur est membre direct. La valeur par défaut est « utilisateurs du domaine ».<br /> | 




 

Un utilisateur est créé en liant le conteneur souhaité, puis en utilisant l’une des méthodes suivantes. Les attributs [**CN**](/windows/desktop/ADSchema/a-cn) et [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) doivent être définis avant que l’utilisateur ne soit validé sur le serveur.



| Méthode                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | L’attribut [**CN**](/windows/desktop/ADSchema/a-cn) est extrait du paramètre *bstrRelativeName* . Le nouvel utilisateur doit être validé en appelant [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) ou l’objet ne sera pas créé. Pour plus d’informations, consultez [exemple de code pour la création d’un utilisateur](example-code-for-creating-a-user.md).<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | L’attribut [**CN**](/windows/desktop/ADSchema/a-cn) est extrait du paramètre *pszRDNName* . Le nouvel utilisateur est validé quand [**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) est appelé. Pour plus d’informations, consultez [exemple de code pour la création d’un utilisateur](example-code-for-creating-a-user.md).<br/>                                                                                                                |
| [DirectoryEntries. Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | L’attribut [**CN**](/windows/desktop/ADSchema/a-cn) est extrait du paramètre *Name* . Le nouvel objet utilisateur doit être validé en appelant [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) ou l’objet ne sera pas créé. Pour plus d’informations, consultez [Ajout d’objets d’annuaire](/previous-versions/ms180851(v=vs.90)).<br/> |



 

Le nouvel utilisateur doit être validé sur le serveur avant de pouvoir modifier les attributs autres que [**CN**](/windows/desktop/ADSchema/a-cn) et [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) . Cela est dû au fait que le compte d’utilisateur n’existe pas tant que l’utilisateur n’a pas été validé. Si un attribut est récupéré ou modifié pour un objet qui n’existe pas sur le serveur, une erreur se produit. Cela comprend l’appel de la méthode [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . Par exemple, la séquence suivante est suivie lors de la création d’un utilisateur avec [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create):

1.  Appelez [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) pour créer l’utilisateur dans le cache local avec le nom [**commun**](/windows/desktop/ADSchema/a-cn)spécifié.
2.  Affectez à l’attribut [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) la valeur souhaitée avec la méthode [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) .
3.  À présent, modifiez d’autres attributs, tels que [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol). Cette restriction s’applique également aux propriétés ADSI, telles que [**IADsUser. AccountDisabled**](/windows/desktop/ADSI/iadsuser-property-methods), et aux méthodes telles que [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword).
4.  Appelez [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider le nouvel utilisateur sur le serveur.

Lorsqu’un nouveau compte d’utilisateur est créé, il est désactivé par défaut. Le compte doit être activé manuellement ou par programme. Pour activer un compte d’utilisateur par programme, supprimez l’indicateur **\_ \_ ACCOUNTDISABLE de publicités UF** de l’attribut [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

Lorsqu’un nouveau compte d’utilisateur est créé, l’attribut [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) du compte est automatiquement associé à l’indicateur **\_ \_ NOTREQD passwd passwd** défini, ce qui indique qu’aucun mot de passe n’est requis pour le compte. Si les stratégies de sécurité du domaine dans lequel le compte est créé requièrent un mot de passe pour tous les comptes d’utilisateur, l’indicateur de **\_ \_ NOTREQD passwd passwd** doit être supprimé de l’attribut **UserAccountControl** pour le compte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de code pour la création d’un utilisateur](example-code-for-creating-a-user.md)
</dt> </dl>
