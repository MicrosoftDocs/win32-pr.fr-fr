---
description: 'En savoir plus sur : méthode API. JetUpdate (JET_SESID, JET_TABLEID, Byte, Int32, Int32)'
title: Méthode API. JetUpdate (JET_SESID, JET_TABLEID, Byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863218"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a>Méthode API. JetUpdate (JET_SESID, JET_TABLEID, Byte, Int32, Int32)

La fonction JetUpdate effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante. La suppression d’une ligne de table s’effectue en appelant [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
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

## <a name="remarks"></a>Notes

JetUpdate est la dernière étape de l’exécution d’une instruction INSERT ou Update. La mise à jour commence par appeler [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , puis en appelant [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) une ou plusieurs fois pour définir l’état de l’enregistrement. Enfin, JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) est appelé pour terminer l’opération de mise à jour. Les index sont mis à jour uniquement par JetUpdate ou et non pendant JetSetColumn.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge JetUpdate](./api.jetupdate-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
