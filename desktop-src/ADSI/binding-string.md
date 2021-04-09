---
title: Chaîne de liaison
description: En raison du nombre d’objets accessibles à partir d’un service d’annuaire, des collisions de noms peuvent se produire.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Chaîne de liaison ADSI
- ADsPath ADSI, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941356"
---
# <a name="binding-string"></a>Chaîne de liaison

En raison du nombre d’objets accessibles à partir d’un service d’annuaire, des collisions de noms peuvent se produire. La chaîne de liaison, qui est communément appelée ADsPath, vous permet de spécifier un objet particulier sans provoquer de collision de noms. Cela peut s’appliquer à un fournisseur de services d’annuaire unique ou à plusieurs fournisseurs de services d’annuaire.

Un ADsPath est une chaîne qui identifie de façon unique un objet ADSI sur un service d’annuaire. Étant donné que les objets ADSI existent dans le contexte de l’espace de noms du service d’annuaire sous-jacent, une partie de la syntaxe d’un nom ADsPath est spécifique au fournisseur.

Le tableau suivant répertorie les fournisseurs ADSI fournis par défaut.



| Fournisseur         | Description                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WinNT<br/> | Utilisé pour communiquer avec les contrôleurs de domaine Windows. Pour plus d’informations sur le ADsPath de WinNT, consultez [winnt ADsPath](winnt-adspath.md).<br/>           |
| LDAP<br/>  | Utilisé pour communiquer avec les serveurs LDAP, par exemple Active Directory. Pour plus d’informations sur l’ADsPath LDAP, consultez [LDAP ADsPath](ldap-adspath.md).<br/>  |
| Fenêtres<br/>   | Fournit une implémentation de [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) qui peut être utilisée pour énumérer tous les fournisseurs ADSI installés sur le client.<br/> |



 

Utilisez ces noms de fournisseurs pour accéder à l’espace de noms du fournisseur par défaut. Par exemple, si vous établissez une liaison à LDAP, ADSI est lié à un conteneur qui contient l’objet de domaine actuellement connecté. Si vous effectuez une liaison à WinNT, ADSI est lié à un conteneur qui contient des objets qui correspondent à tous les domaines du réseau.

Les éléments initiaux de la chaîne ADsPath sont l’identificateur programmatique (progID) du fournisseur ADSI, suivi de « :// », suivi de la syntaxe dictée par l’espace de noms du fournisseur. La chaîne progID peut ou non respecter la casse, en fonction du fournisseur. Les chaînes progID pour les fournisseurs répertoriés ci-dessus respectent la casse.

La chaîne de chemin d’accès peut ou non respecter la casse, en fonction du fournisseur. Les chaînes de chemin d’accès pour les fournisseurs répertoriés ci-dessus ne respectent pas la casse.

Voici quelques exemples de ADsPaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Pour rechercher tous les fournisseurs installés sur votre ordinateur, établissez une liaison avec le fournisseur ADs comme indiqué dans l’exemple de code suivant.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



À l’aide du fournisseur LDAP, vous pouvez spécifier l’ADsPath dans un format de nom unique X. 500 (DN), en commençant par la balise CN, ou vous pouvez spécifier son inverse hiérarchique, en commençant par la balise O. Le formulaire que vous utilisez dans l’ADsPath initial détermine l’ordre des balises.

Le tableau suivant répertorie les caractères spéciaux ADsPath.



| Nom                      | Caractère           | Description                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Guillemet double<br/>   | "<br/>        | Utilisé pour citer une partie quelconque de l’ADsPath qui peut contenir un caractère spécial afin que la chaîne soit interprétée littéralement. Par exemple, « CN = nom/préfixe ».<br/>                                     |
| Barre oblique inverse<br/>      | \\<br/>       | Utilisé pour précéder les caractères spéciaux pour indiquer qu’ils doivent être utilisés en tant que littéraux. Pour plus d’informations et pour obtenir la liste des caractères spéciaux, consultez [noms uniques](/previous-versions/windows/desktop/ldap/distinguished-names).<br/> |
| Barr<br/>          | /<br/>        | Séparateur de composants.<br/>                                                                                                                                                                       |
| Crochets pointus<br/> | <><br/> | Délimiter une ADsPath dans une autre convention d’affectation de noms.<br/>                                                                                                                                       |



 

Pour délimiter une ADsPath dans une spécification de recherche ou dans le cadre d’une URL, utilisez le Chevron gauche et le Chevron droit (< >). Par exemple, « &lt; winnt://MyDomain/UserAccount &gt; ».

Certains fournisseurs ADSI peuvent avoir ajouté des restrictions de syntaxe en raison des exigences de l’espace de noms.

## <a name="active-directory-binding-options"></a>Options de liaison Active Directory

Active Directory permet de lier un objet à l’aide de plusieurs autres types de chaînes de liaison, par exemple un identificateur global unique (GUID) COM ou un identificateur de sécurité (SID). Pour plus d’informations, consultez [liaison à Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).

 

