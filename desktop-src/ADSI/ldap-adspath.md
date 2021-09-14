---
title: Chemin d’authentification LDAP
description: Cette rubrique montre la syntaxe que vous devez utiliser pour l’ADsPath LDAP.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- Chemin d’authentification LDAP
- ADsPath, LDAP, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922052"
---
# <a name="ldap-adspath"></a>Chemin d’authentification LDAP

Le chemin ADsPath du fournisseur LDAP Microsoft requiert le format suivant.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> Les crochets gauche et droit ( \[ \] ) indiquent des paramètres facultatifs ; il ne s’agit pas d’une partie littérale de la chaîne de liaison.

 

Le « nom d’hôte » peut être un nom d’ordinateur, une adresse IP ou un nom de domaine. Un nom de serveur peut également être spécifié dans la chaîne de liaison. La plupart des fournisseurs LDAP suivent un modèle qui requiert la spécification d’un nom de serveur.

Le « numéro_port » spécifie le port à utiliser pour la connexion. Si aucun numéro de port n’est spécifié, le fournisseur LDAP utilise le numéro de port par défaut. Le numéro de port par défaut est 389 si vous n’utilisez pas de connexion SSL ou 636 si vous utilisez une connexion SSL.

Le « DistinguishedName » spécifie le nom unique d’un objet spécifique. Un nom unique pour un objet donné est garanti être unique.

Le tableau suivant répertorie des exemples de chaînes de liaison.



| Exemple d’ADsPath LDAP                                      | Description                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| LDAP                                                     | Liez à la racine de l’espace de noms LDAP.                    |
| LDAP://server01                                           | Effectuer une liaison à un serveur spécifique.                                 |
| LDAP://server01:390                                       | Établit une liaison à un serveur spécifique en utilisant le numéro de port spécifié. |
| LDAP : 0408 = Jeff Smith, CN = Users, DC = fabrikam, DC = com          | Lier à un objet spécifique.                                 |
| LDAP://server01/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com | Effectuer une liaison à un objet spécifique par le biais d’un serveur spécifique.       |



 

Si l’authentification Kerberos est requise pour la réussite d’une demande de répertoire spécifique, la chaîne de liaison doit utiliser soit un ADsPath sans serveur, tel que LDAP : menée = Jeff Smith, CN = Users, DC = fabrikam, DC = com, soit un ADsPath avec un nom de serveur DNS complet, par exemple LDAP://server01.fabrikam.com/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com. La liaison au serveur à l’aide d’un nom NETBIOS plat ou d’un nom DNS courts, par exemple, en utilisant le nom SERVEUR01 au lieu de server01.fabrikam.com, n’est pas garantie d’obtenir l’authentification Kerberos.

Pour plus d’informations et pour obtenir des exemples de chaînes de liaison LDAP, ainsi qu’une description des caractères spéciaux qui peuvent être utilisés dans les chaînes de liaison LDAP, consultez l’ADsPath LDAP.

**Windows 2000 avec SP1 et versions ultérieures :** Avec le fournisseur LDAP, si une chaîne de liaison comprend un nom de serveur, vous pouvez augmenter les performances en utilisant l’indicateur de **\_ \_ liaison de serveur ADS** avec la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . L’indicateur de **\_ \_ liaison de serveur ADS** indique qu’un nom de serveur a été spécifié, ce qui permet à ADSI d’éviter un trafic réseau supplémentaire et inutile.

## <a name="ldap-special-characters"></a>Caractères spéciaux LDAP

LDAP a plusieurs caractères spéciaux qui sont réservés à une utilisation par l’API LDAP. La liste des caractères spéciaux se trouve dans [noms uniques](/previous-versions/windows/desktop/ldap/distinguished-names). Pour utiliser l’un de ces caractères dans un ADsPath sans générer d’erreur, le caractère doit être précédé d’une barre oblique inverse ( \\ ). C’est ce que l’on appelle le caractère d' *échappement* . Par exemple, si un nom d’utilisateur est fourni sous la forme " <last name> , <first name> ", la virgule de la valeur de nom doit être placée dans une séquence d’échappement. La chaîne obtenue ressemble à ceci :


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



Le caractère d’échappement peut également être spécifié par son code hexadécimal à deux chiffres. Cela est illustré par l'exemple suivant.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



Les caractères non imprimables, tels que le saut de ligne et le retour chariot, doivent être placés dans une séquence d’échappement et spécifiés par leur code hexadécimal à deux chiffres. Cela est illustré par l'exemple suivant.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Pour plus d'informations

Pour plus d’informations sur la notation de nom unique utilisée par les services d’annuaire compatibles LDAP, consultez [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 