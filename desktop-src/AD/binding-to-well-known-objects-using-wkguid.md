---
title: Liaison à des objets Well-Known à l’aide de WKGUID
description: Cette rubrique montre comment effectuer une liaison à des objets à l’aide de la chaîne de liaison WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Liaison à des objets Well-Known à l’aide de WKGUID AD
- Active Directory, utilisation de, liaison, utilisation de WKGUID pour établir une liaison avec des objets connus
- objets connus AD
- objets connus AD, liaison à à l’aide de WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724645"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a>Liaison à des objets Well-Known à l’aide de WKGUID

Les conteneurs peuvent avoir un ou plusieurs sous-objets importants qui peuvent être renommés ou déplacés. Il peut être difficile de suivre ces sous-objets et de générer des chaînes de liaison correctes pour eux, en particulier s’ils sont renommés ou déplacés.

Pour prendre en charge la liaison renommée-Safe à ces objets au sein de ces conteneurs, Active Directory Domain Services avoir deux attributs : **wellKnownObjects** et **otherWellKnownObjects**. Ces attributs ont une syntaxe d’attribut de ADSTYPE \_ DN \_ avec \_ binaire. Ils autorisent plusieurs valeurs et contiennent les tuples GUID/DN des objets connus dans les conteneurs sur lesquels ils sont définis. Le serveur Active Directory conserve la partie nom unique de chaque entrée **wellKnownObjects** et **otherWellKnownObjects** afin qu’il contienne le nom unique actuel de l’objet spécifié lors de la création de l’entrée.

La propriété **otherWellKnownObjects** peut être définie et utilisée sur n’importe quel objet.

La propriété **wellKnownObjects** est utilisée sur les conteneurs de domainDNS et de configuration. La propriété **wellKnownObjects** est une propriété système uniquement et ne peut être modifiée que par le système d’exploitation.

Le conteneur **domainDNS** contient les objets connus suivants :

-   Utilisateurs
-   Ordinateurs
-   Système
-   Contrôleurs de domaine
-   Infrastructure
-   Objets supprimés
-   Perdu et trouvé

Le conteneur de configuration a l’objet connu : objets supprimés.

Ces objets se trouvent dans chaque **domainDNS** et conteneur de configuration dans un service domaine Active Directory.

Vous pouvez effectuer une liaison à un objet connu à l’aide du format de liaison WKGUID. La liaison avec WKGUID est uniquement prise en charge dans Active Directory Domain Services, autrement dit, le fournisseur LDAP.

> [!IMPORTANT]
> Utilisez toujours le format de liaison WKGUID pour effectuer une liaison aux objets connus, comme indiqué ci-dessus, dans les conteneurs domaine et configuration. Cela permet de s’assurer que ces conteneurs peuvent être liés, même s’ils sont déplacés ou renommés.

 

Le format de chaîne de liaison WKGUID est le suivant :


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



« &lt; Server name &gt; » est le nom du serveur d’annuaire. Le « &lt; nom du serveur &gt; » est facultatif.

« &lt; Xxxxx &gt; » est la représentation sous forme de chaîne de la valeur hexadécimale du GUID qui représente l’objet connu. La chaîne GUID est spécifiée dans le formulaire « XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX » et n’est pas la même forme que la chaîne GUID produite par la fonction [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , qui prend la forme « {XXXXXXXX-XXXX-XXXX-xxxx-xxxxxxxxxxxx} ». Pour plus d’informations et pour obtenir un exemple de code qui montre comment créer une chaîne pouvant être liée à partir d’un GUID, consultez l' [exemple de code permettant de créer une représentation sous forme de chaîne pouvant être liée d’un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).

Pour effectuer une liaison à un objet spécifié dans **otherWellKnownObjects** dans un objet, spécifiez « &lt; xxxxx &gt; » comme forme de chaîne de liaison du GUID d’objet connu de l’objet. Pour plus d’informations, consultez lecture de l’attribut [objectGUID d’un objet et création d’une représentation sous forme de chaîne du GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md). Pour plus d’informations sur la définition de la propriété **otherWellKnownObjects** sur les objets, consultez Activation de la [liaison de Rename-Safe avec la propriété otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).

Pour établir une liaison à un objet spécifié dans **wellKnownObjects** dans domainDNS ou dans des conteneurs de configuration, spécifiez « &lt; xxxxx &gt; » comme l’une des constantes suivantes, comme indiqué dans le tableau suivant, tel que défini dans ntdsapi. h.



| Conteneur          | Identificateur GUID                         |
|--------------------|-----------------------------------------|
| Utilisateurs              | \_conteneur d’utilisateurs GUID \_ \_ W               |
| Ordinateurs          | \_conteneur de calculs \_ GUID \_ W            |
| Système             | \_conteneur de systèmes GUID \_ \_ W             |
| Contrôleurs de domaine | \_conteneur de \_ contrôleurs de domaine GUID \_ \_ W |
| Infrastructure     | conteneur d’infrastructure de GUID \_ \_ \_ W      |
| Objets supprimés    | \_conteneur d' \_ objets supprimés GUID \_ \_ W    |
| Perdu et trouvé     | GUID \_ LOSTANDFOUND \_ conteneur \_ W        |



 

Par exemple, pour effectuer une liaison au conteneur utilisateur dans un domaine, spécifiez « xxxxx » comme **\_ conteneur des utilisateurs \_ \_ GUID** &lt; &gt; .

« &lt; container dn &gt; » est le nom unique de l’objet conteneur qui a cet objet représenté en tant que valeur dans sa propriété **wellKnownObjects** . Par exemple, pour effectuer une liaison au conteneur Users dans un domaine, spécifiez le nom unique du domaine comme « &lt; container dn &gt; ».

Par exemple, pour effectuer une liaison au conteneur Users du domaine Fabrikam.com, utilisez la chaîne de liaison suivante.

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

Pour plus d’informations et pour obtenir un exemple de code qui montre comment effectuer une liaison à un GUID connu, consultez l' [exemple de code pour la liaison à des objets bien connus](example-code-for-binding-to-well-known-objects.md).

 

 