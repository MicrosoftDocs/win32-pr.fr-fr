---
description: Contient des méthodes qui vous permettent d’accéder aux paramètres de sécurité d’un espace de noms et de les modifier.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: Classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 141e659c0ddf15c0369323e5d18d6251c3334a47
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468526"
---
# <a name="__systemsecurity-class"></a>\_\_SystemSecurity, classe

La classe système **\_ \_ SystemSecurity** contient des méthodes qui vous permettent d’accéder aux paramètres de sécurité d’un espace de noms et de les modifier. La classe **\_ \_ SystemSecurity** est une classe singleton dans chaque espace de noms.

> [!Note]  
> Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a>Membres

La classe **\_ \_ SystemSecurity** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **\_ \_ SystemSecurity** possède ces méthodes.




| Méthode | Description | 
|--------|-------------|
| <a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a> | Obtient une liste des utilisateurs autorisés à accéder à distance.<br /><blockquote>[!Note]<br />Cette méthode ne fonctionne pas sur les versions prises en charge de Windows. Utilisez <a href="--systemsecurity-getsd.md"><strong>à</strong></a> la place.</blockquote><br /> | 
| <a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a> | Retourne un masque avec chaque bit qui correspond à un droit d’accès.<br /> | 
| <a href="--systemsecurity-getsd.md"><strong>Getsd a</strong></a> | Obtient le <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> de l’espace de noms auquel l’utilisateur est connecté.<br /> | 
| <a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a> | Obtient le descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI associé à l’instance de <strong>__SystemSecurity</strong>. Le descripteur de sécurité est retourné sous la forme d’une instance de<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.<br /> | 
| <a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a> | Définit une liste d’utilisateurs autorisés à accéder à distance.<br /><blockquote>[!Note]<br />Cette méthode ne fonctionne pas sur les versions prises en charge de Windows. Utilisez à la place <a href="--systemsecurity-setsd.md"><strong>sets</strong></a> .</blockquote><br /> | 
| <a href="--systemsecurity-setsd.md"><strong>Setsd a</strong></a> | Définit le descripteur de sécurité pour l’espace de noms auquel l’utilisateur est connecté.<br /> | 
| <a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a> | Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante. Le descripteur de sécurité est représenté par une instance de <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.<br /> | 




 

## <a name="remarks"></a>Remarques

Vous pouvez exiger que les applications et les scripts clients utilisent une connexion chiffrée pour l’authentification en ajoutant le qualificateur **RequiresEncryption** au fichier. MOF qui crée l’espace de noms. Vous pouvez également modifier un espace de noms existant en ajoutant cet attribut et recompiler le fichier. mof. Pour plus d’informations sur l’utilisation de **RequiresEncryption**, consultez la page [exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[Objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Établissement de l’héritage de la sécurité des espaces de noms](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[Listes de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[**Descripteur de sécurité \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

