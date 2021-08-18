---
description: 'En savoir plus sur : méthode API. GetTableNames'
title: API. GetTableNames, méthode
TOCTitle: 'GetTableNames method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableNames(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablenames(v=EXCHG.10)
ms:contentKeyID: 55100650
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a15fed60734125552a85d6a64dd5e207e445cc8d0fe1ab32bb650a3dce62763d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983719"
---
# <a name="apigettablenames-method"></a>API. GetTableNames, méthode

Retourne les noms des tables dans la base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function GetTableNames ( _
    sesid As JET_SESID, _
    dbid As JET_DBID _
) As IEnumerable(Of String)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim returnValue As IEnumerable(Of String)

returnValue = Api.GetTableNames(sesid, _
    dbid)
```

``` csharp
public static IEnumerable<string> GetTableNames(
    JET_SESID sesid,
    JET_DBID dbid
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données contenant la table.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[String](/dotnet/api/system.string)\>  
Itérateur sur les noms des tables dans la base de données.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
