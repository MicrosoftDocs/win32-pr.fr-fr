---
title: Attributs de nom d’utilisateur
description: Les attributs de nom d’utilisateur identifient les objets utilisateur, tels que les noms d’ouverture de session et les ID utilisés à des fins de sécurité.
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- Attributs de nom d’utilisateur Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8548178bba8012231a803d476699e8ebb386b6fa9a29015f3721e7b32d94158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185929"
---
# <a name="user-naming-attributes"></a>Attributs de nom d’utilisateur

Les attributs de nom d’utilisateur identifient les objets utilisateur, tels que les noms d’ouverture de session et les ID utilisés à des fins de sécurité. Les attributs **CN**, **Name** et **distinguishedName** sont des exemples d’attributs de nom d’utilisateur. Un objet utilisateur étant un objet principal de sécurité, il comprend également les attributs de nom d’utilisateur suivants :

-   [userPrincipalName](#userprincipalname) : nom d’ouverture de session de l’utilisateur
-   [objectGUID](#objectguid) : identificateur unique d’un utilisateur.
-   [sAMAccountName](#samaccountname) : nom de connexion qui prend en charge la version précédente de Windows
-   [objectSID](#objectsid) : identificateur de sécurité (SID) de l’utilisateur
-   [SIDHistory](#sidhistory) : les SID précédents pour l’objet utilisateur

> [!Note]  
> Vous pouvez afficher et gérer ces attributs à l’aide du composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory, qui est disponible dans le [Outils d’administration de serveur distant (RSAT)](https://www.microsoft.com/download/details.aspx?id=45520).

 

## <a name="userprincipalname"></a>userPrincipalName

L’attribut **userPrincipalName** est le nom d’ouverture de session de l’utilisateur. l’attribut se compose d’un nom d’utilisateur principal (UPN), qui est le nom d’ouverture de session le plus courant pour les utilisateurs de Windows. Les utilisateurs utilisent généralement leur UPN pour se connecter à un domaine. Cet attribut est une chaîne indexée à valeur unique.

Un UPN est un nom de connexion de style Internet pour un utilisateur basé sur la norme Internet RFC 822. L’UPN est plus petit qu’un nom unique et il est plus facile à mémoriser. Par convention, il doit correspondre au nom de l’adresse électronique de l’utilisateur. Le point de l’UPN consiste à consolider les espaces de noms de messagerie et d’ouverture de session afin que l’utilisateur ne doive mémoriser qu’un seul nom.

### <a name="upn-format"></a>Format UPN

Un UPN se compose d’un préfixe UPN (nom de compte d’utilisateur) et d’un suffixe UPN (nom de domaine DNS). Le préfixe et le suffixe sont liés par le symbole « @ », Par exemple, « someone@ example.com ». Un UPN doit être unique parmi tous les objets principaux de sécurité d’une forêt de répertoires. Cela signifie que le préfixe d’un UPN peut être réutilisé, mais pas avec le même suffixe.

Un suffixe UPN présente les restrictions suivantes :

-   Il doit s’agir du nom DNS d’un domaine, mais il n’est pas nécessaire qu’il s’agit du nom du domaine qui contient l’utilisateur.
-   Il doit s’agir du nom d’un domaine dans la forêt de domaines en cours ou d’un autre nom figurant dans l’attribut **upnSuffixes** du conteneur partitions dans le conteneur Configuration.

### <a name="upn-management"></a>Gestion UPN

Un UPN peut être attribué, mais n’est pas obligatoire, lors de la création d’un compte d’utilisateur. Lorsqu’un UPN est créé, il n’est pas affecté par les modifications apportées à d’autres attributs de l’objet utilisateur, tels que l’utilisateur qui a été renommé ou déplacé. Cela permet à l’utilisateur de conserver le même nom de connexion si un répertoire est restructuré. Toutefois, un administrateur peut modifier un UPN. Lorsque vous créez un nouvel objet utilisateur, vous devez vérifier le domaine local et le catalogue global pour le nom proposé pour vous assurer qu’il n’existe pas déjà.

Lorsqu’un utilisateur utilise un UPN pour se connecter à un domaine, l’UPN est validé en recherchant le domaine local, puis le catalogue global. Si l’UPN est introuvable dans le catalogue global, la tentative d’ouverture de session échoue.

## <a name="objectguid"></a>objectGUID

L’attribut **objectGUID** est l’identificateur unique d’un utilisateur. L’attribut est un identificateur global unique (GUID) à valeur unique de 128 bits, et il est stocké sous la forme d’une structure de [**\_ \_ chaîne d’octets ADS**](/windows/win32/api/iads/ns-iads-ads_octet_string) . Le GUID est créé par le serveur de Active Directory lors de la création d’un objet utilisateur.

Étant donné que le nom unique d’un objet change si l’objet est renommé ou déplacé, le nom unique n’est pas un identificateur fiable d’un objet. Dans Active Directory Domain Services, l’attribut **objectGUID** d’un objet ne change jamais, même si l’objet est renommé ou déplacé. Vous pouvez récupérer la forme de chaîne de l' **objectGUID** à l’aide de la méthode de propriété **GUID** dans les [méthodes de propriété IADs](/windows/desktop/ADSI/iads-property-methods).

## <a name="samaccountname"></a>sAMAccountName

l’attribut **sAMAccountName** est un nom d’ouverture de session utilisé pour prendre en charge les clients et les serveurs de la version précédente de Windows, tels que Windows NT 4,0, Windows 95, Windows 98 et LAN Manager. Le nom d’ouverture de session doit comporter au maximum 20 caractères et être unique parmi tous les objets principaux de sécurité au sein du domaine.

## <a name="objectsid"></a>objectSid

L’attribut **objectSID** est l’identificateur de sécurité (SID) de l’utilisateur. le SID est utilisé par le système pour identifier un utilisateur et leurs appartenances aux groupes lors des interactions avec la sécurité Windows. L’attribut est à valeur unique. Le SID est une valeur binaire unique utilisée pour identifier l’utilisateur en tant que principal de sécurité.

Le SID est défini par le système lors de la création de l’utilisateur. chaque utilisateur a un SID unique émis par un domaine Windows et stocké dans l’attribut **objectSid** de l’objet utilisateur dans l’annuaire. Chaque fois qu’un utilisateur ouvre une session, le système récupère le SID de l’utilisateur à partir du répertoire et le place dans le jeton d’accès de l’utilisateur. Le SID de l’utilisateur est également utilisé pour récupérer les SID pour les groupes dont l’utilisateur est membre et les place dans le jeton d’accès de l’utilisateur. Lorsqu’un SID a été utilisé en tant qu’identificateur unique pour un utilisateur ou un groupe, il ne peut pas être réutilisé pour identifier un autre utilisateur ou groupe.

## <a name="sidhistory"></a>sIDHistory

L’attribut **SIDHistory** contient les SID précédents pour l’objet User. Il s’agit d’un attribut à valeurs multiples. Un objet utilisateur possède un SID précédent si l’utilisateur a été déplacé vers un autre domaine. Chaque fois qu’un objet utilisateur est déplacé vers un nouveau domaine, un nouveau SID est créé et l’attribut **objectSID** lui est attribué, et le SID précédent est ajouté à l’attribut **SIDHistory** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs d’objet utilisateur](user-object-attributes.md)
</dt> </dl>

 

 