---
title: Liaison à des objets Active Directory
description: Avant de poursuivre ce scénario, vous devez comprendre comment les objets ADSI sont nommés dans Active Directory, et comment les lier. La liaison d’un objet ADSI connecte l’objet au service d’annuaire et vous permet d’accéder aux méthodes de l’objet.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b473c9e3370c3d1739fc904b8c6409d756f62b5c358db200c3de821f55349f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962258"
---
# <a name="binding-to-active-directory-objects"></a>Liaison à des objets Active Directory

Avant de poursuivre ce scénario, vous devez comprendre comment les objets ADSI sont nommés dans Active Directory, et comment les lier. La liaison d’un objet ADSI connecte l’objet au service d’annuaire et vous permet d’accéder aux méthodes de l’objet.

## <a name="adspath"></a>ADsPath

Un objet ADSI est identifié de manière unique par sa chaîne de liaison, également appelée ADsPath. Un ADsPath est une combinaison d’un identificateur programmatique (progID) du fournisseur ADSI et du nom unique (DN) de l’objet.

Voici le format d’une ADsPath :

« progID://DN »

-   pogID : identificateur programmatique du fournisseur ADSI, tel que LDAP ou Winnt.

-   :// : sépare le progID du DN.

-   DN : nom unique de l’objet ADSI, qui est le chemin d’accès complet de l’objet, où le chemin d’accès se compose de noms uniques relatifs (RDN).

Un RDN est le nom de l’objet sans le chemin d’accès et est unique à partir de ses objets frères. Un RDN se compose d’un ID d’attribut et d’une valeur, tels que « DC = fabrikam », où DC est l’attribut, et Fabrikam la valeur. DC est un ID d’attribut RDN qui représente le composant de domaine.

Voici un exemple d’ADsPath :

« LDAP://DC = fabrikam, DC = com »

## <a name="binding-the-object"></a>Liaison de l’objet

Voici comment vous pouvez lier l’objet de domaine dans ce scénario :


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Lorsque vous exécutez cet exemple de code, ADSI utilise le DN pour déterminer les objets ADSI à lier. Une fois que l’interface ADSI a lié ces objets, vous pouvez accéder à leurs méthodes. L’exemple de code précédent lie un objet de domaine à [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) et [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Vous pouvez maintenant utiliser des méthodes sur ces interfaces, telles que l' [**extraction**](/windows/desktop/api/Iads/nf-iads-iads-get), la [**mise en place**](/windows/desktop/api/Iads/nf-iads-iads-put), la [**création**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), la [**suppression**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)et l' [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).

Une fois que vous avez lié un objet de domaine, vous pouvez imprimer certains de ses attributs :


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Pour plus d’informations sur ADsPath, consultez [Binding String](binding-string.md). Pour plus d’informations sur la liaison, consultez [liaison à un objet ADSI](binding-to-an-adsi-object.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d'une unité d'organisation](creating-an-organizational-unit.md)
</dt> </dl>

 

 




