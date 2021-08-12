---
description: 'En savoir plus sur : méthode API. JetDeleteTable'
title: API. JetDeleteTable, méthode
TOCTitle: 'JetDeleteTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletetable(v=EXCHG.10)
ms:contentKeyID: 55100683
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fb62823f083c77cec9f91f6ecd3e43b27bd73756cfea903849bb35b66bf4505d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272528"
---
# <a name="apijetdeletetable-method"></a>API. JetDeleteTable, méthode

Supprime une table d’une base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetDeleteTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As StringApi.JetDeleteTable(sesid, dbid, _
    table)
```

``` csharp
public static void JetDeleteTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données à partir de laquelle supprimer la table.

<!-- end list -->

  - table  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom de la table à supprimer.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
