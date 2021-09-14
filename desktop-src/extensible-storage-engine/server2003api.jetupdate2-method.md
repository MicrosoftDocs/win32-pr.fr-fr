---
description: 'En savoir plus sur : méthode Server2003Api. JetUpdate2'
title: Méthode Server2003Api. JetUpdate2 (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294215"
---
# <a name="server2003apijetupdate2-method"></a>Méthode Server2003Api. JetUpdate2

La fonction JetUpdate effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante. La suppression d’une ligne de table s’effectue en appelant [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session qui a démarré la mise à jour.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur à mettre à jour. Une mise à jour doit être préparée.

<!-- end list -->

  - signet  
    Entrer \[\]  
    
    Retourne le signet de l’enregistrement mis à jour. Peut être Null.

<!-- end list -->

  - bookmarkSize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille de la mémoire tampon du signet.

<!-- end list -->

  - actualBookmarkSize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Retourne la taille réelle du signet.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. Server2003. UpdateGrbit](./updategrbit-enumeration.md)  
    
    Options de mise à jour.

## <a name="remarks"></a>Notes

JetUpdate est la dernière étape de l’exécution d’une instruction INSERT ou Update. La mise à jour commence par appeler [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , puis en appelant [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) une ou plusieurs fois pour définir l’état de l’enregistrement. Enfin, JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit) est appelé pour terminer l’opération de mise à jour. Les index sont mis à jour uniquement par JetUpdate ou et non pendant JetSetColumn.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Server2003Api, classe](./server2003api-class.md)

[Membres Server2003Api](./server2003api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
