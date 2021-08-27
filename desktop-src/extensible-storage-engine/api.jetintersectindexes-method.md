---
description: 'En savoir plus sur : méthode API. JetIntersectIndexes'
title: API. JetIntersectIndexes, méthode
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b2e9e259d9c90a3067931fbba425ab1b21e5c2a36a73563f593d3b280a40496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978029"
---
# <a name="apijetintersectindexes-method"></a>API. JetIntersectIndexes, méthode

Calcule l’intersection entre plusieurs jeux d’entrées d’index à partir d’index secondaires différents sur la même table. Cette opération est utile pour Rechercher l’ensemble des enregistrements d’une table qui correspondent à plusieurs critères qui peuvent être exprimés à l’aide de plages d’index. Consultez également [IntersectIndexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - ranges  
    Entrer \[\]  
    
    Une plage d’index à croiser. Les TableID des plages doivent avoir des plages d’index définies. Utilisez [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) pour créer une plage d’index.

<!-- end list -->

  - numRanges  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre de plages d’index.

<!-- end list -->

  - recordlist  
    Type : [Microsoft.ISAM.esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)  
    
    Retourne des informations sur la table temporaire contenant les résultats de l’intersection.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)  
    
    Options d’intersection.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
