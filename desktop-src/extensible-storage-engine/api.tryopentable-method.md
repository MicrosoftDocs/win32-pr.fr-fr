---
description: 'En savoir plus sur : méthode API. TryOpenTable'
title: API. TryOpenTable, méthode
TOCTitle: 'TryOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryopentable(v=EXCHG.10)
ms:contentKeyID: 55100889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 556d3f12f24229326a6b26f357e5b19801119b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393480"
---
# <a name="apitryopentable-method"></a>API. TryOpenTable, méthode

Essayez d’ouvrir une table.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function TryOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryOpenTable(sesid, _
    dbid, tablename, grbit, tableid)
```

``` csharp
public static bool TryOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données dans laquelle rechercher la table.

<!-- end list -->

  - tablename  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom de la table.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)  
    
    Options d’ouverture de la table.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Retourne l’TableID ouvert.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si la table a été ouverte, false si elle n’existe pas.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
