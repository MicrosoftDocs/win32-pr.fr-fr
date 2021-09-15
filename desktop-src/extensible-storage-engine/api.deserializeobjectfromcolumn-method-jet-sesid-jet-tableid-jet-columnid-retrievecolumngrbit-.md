---
description: 'En savoir plus sur : méthode API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Méthode API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.deserializeobjectfromcolumn(v=EXCHG.10)
ms:contentKeyID: 55100669
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe2bb9757216dc4b0a671ae9d5da6cdf4bd5eb7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520113"
---
# <a name="apideserializeobjectfromcolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a>Méthode API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)

Désérialiser un objet à partir d’une colonne.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function DeserializeObjectFromColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Object
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Object

returnValue = Api.DeserializeObjectFromColumn(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Object DeserializeObjectFromColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Table à partir de laquelle effectuer la lecture.

<!-- end list -->

  - columnid  
    Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Colonne à partir de laquelle effectuer la lecture.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Options de récupération à utiliser.

#### <a name="return-value"></a>Valeur de retour

Type : [System. Object](/dotnet/api/system.object)  
L'objet désérialisé. NULL si la colonne est null.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge DeserializeObjectFromColumn](./api.deserializeobjectfromcolumn-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
