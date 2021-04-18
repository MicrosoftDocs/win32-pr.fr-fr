---
description: 'En savoir plus sur : méthode API. JetDeleteColumn2'
title: API. JetDeleteColumn2, méthode
TOCTitle: 'JetDeleteColumn2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.DeleteColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn2(v=EXCHG.10)
ms:contentKeyID: 55100680
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0426ca2557dac11c565211162438db6d5c77a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516227"
---
# <a name="apijetdeletecolumn2-method"></a>API. JetDeleteColumn2, méthode

Supprime une colonne d’une table de base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetDeleteColumn2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    grbit As DeleteColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim grbit As DeleteColumnGrbitApi.JetDeleteColumn2(sesid, tableid, _
    column, grbit)
```

``` csharp
public static void JetDeleteColumn2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    DeleteColumnGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur sur la table à partir duquel supprimer la colonne.

<!-- end list -->

  - colonne  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom de la colonne à supprimer.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)  
    
    Options de suppression de colonne.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
