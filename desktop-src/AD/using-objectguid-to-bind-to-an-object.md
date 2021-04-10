---
title: Utilisation d’objectGUID pour la liaison à un objet
description: Un nom unique d’objet change si l’objet est renommé ou déplacé, par conséquent, le nom unique n’est pas un identificateur d’objet fiable.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Utilisation d’objectGUID pour la liaison à un objet AD
- Active Directory objectGUID
- objectGUID Active Directory, utilisant pour effectuer une liaison à un objet
- Active Directory, utilisation de, liaison, utilisation d’objectGUID pour la liaison à l’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030973"
---
# <a name="using-objectguid-to-bind-to-an-object"></a>Utilisation d’objectGUID pour la liaison à un objet

Un nom unique d’objet change si l’objet est renommé ou déplacé, par conséquent, le nom unique n’est pas un identificateur d’objet fiable. Dans Active Directory Domain Services, la propriété **objectGUID** d’un objet ne change jamais, même si l’objet est renommé ou déplacé. Pour plus d’informations sur **objectGUID** et les identificateurs, consultez [noms d’objets et identités](object-names-and-identities.md).

Le fournisseur LDAP Active Directory fournit une méthode pour établir une liaison à un objet à l’aide du GUID de l’objet. Le format de la chaîne de liaison est le suivant :


```C++
LDAP://servername/<GUID=XXXXX>
```



Dans cet exemple, « ServerName » est le nom du serveur d’annuaire et « XXXXX » est la représentation sous forme de chaîne de la valeur hexadécimale du GUID. Le « servername » est facultatif. La chaîne GUID est spécifiée dans le formulaire « XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX ». La chaîne GUID peut également prendre la forme « XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX », qui est le même formulaire que la chaîne produite par la fonction [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , sans les accolades « {} ». Pour plus d’informations et pour obtenir un exemple de code qui montre comment créer une chaîne pouvant être liée à partir d’un GUID, consultez l' [exemple de code permettant de créer une représentation sous forme de chaîne pouvant être liée d’un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md). La propriété [**IADs. Guid**](/windows/desktop/ADSI/iads-property-methods) peut être utilisée pour extraire la forme de chaîne correcte du GUID.

Lors de la liaison à l’aide du GUID d’objet, certaines méthodes et propriétés [**IADs**](/windows/desktop/api/iads/nn-iads-iads) et [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) ne sont pas prises en charge. Les propriétés **IADs** suivantes ne sont pas prises en charge par les objets obtenus par la liaison à l’aide du GUID de l’objet :

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nom**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Les méthodes **IADsContainer** suivantes ne sont pas prises en charge par les objets obtenus par la liaison à l’aide du GUID de l’objet :

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Créés**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Supprimer**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Pour utiliser ces méthodes et propriétés après avoir effectué une liaison à un objet à l’aide du GUID d’objet, utilisez la méthode [**IADs. obtenir**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer le nom unique de l’objet, puis utilisez le nom unique pour effectuer une nouvelle liaison à l’objet.

Si une application stocke ou met en cache des identificateurs ou des références à des objets stockés dans Active Directory Domain Services, le GUID de l’objet est le meilleur identificateur à utiliser pour plusieurs raisons :

-   La propriété **objectGUID** de on Object ne change jamais même si l’objet est renommé ou déplacé.
-   Il est facile de lier l’objet à l’aide du GUID de l’objet.
-   Si l’objet est renommé ou déplacé, la propriété **objectGUID** fournit un identificateur unique qui peut être utilisé pour rechercher et identifier rapidement l’objet plutôt que d’avoir à composer une requête qui a des conditions pour toutes les propriétés qui identifieraient cet objet.

 

 