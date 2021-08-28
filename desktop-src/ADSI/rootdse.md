---
title: RootDSE (ADSI)
description: Chaque serveur d’annuaire possède une entrée unique appelée RootDSE. Il fournit des données sur le serveur, telles que ses fonctionnalités, la version LDAP qu’il prend en charge et les contextes d’attribution de noms qu’il utilise.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59176315339e7458f332e2226f880b79afa10c5afc2c5089295866f6bf93939c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770629"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Chaque serveur d’annuaire possède une entrée unique appelée **rootDSE**. Il fournit des données sur le serveur, telles que ses fonctionnalités, la version LDAP qu’il prend en charge et les contextes d’attribution de noms qu’il utilise.

par exemple, pour créer un script ou une application qui peut s’exécuter sur n’importe quel environnement de domaine Windows. Vous pouvez spécifier le nom unique, le nom du serveur ou le nom de domaine lors de la connexion à Active Directory. Si vous ne disposez pas de ces informations, vous pouvez utiliser l’objet **rootDSE** pour établir une connexion. L’exemple de code suivant modifie la description de domaine dans n’importe quel domaine.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



En obtenant l’attribut **defaultNamingContext** à partir de **rootDSE**, vous pouvez effectuer une liaison au domaine actuel, par exemple, le **DefaultNamingContext** Fabrikam est DC = fabrikam, DC = com.

Pour énumérer les propriétés du **rootDSE**, utilisez l’interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) . [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ne peut pas être utilisé pour cette tâche.

Pour plus d’informations, consultez [liaison sans serveur et RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).

 

 