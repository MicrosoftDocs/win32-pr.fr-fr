---
description: 'En savoir plus sur : méthode API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Méthode API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasbyte(v=EXCHG.10)
ms:contentKeyID: 55100865
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbf7baaed340dbe61e7c10e4d64d17d93b23cdd1b4b01af0818c310ff0a7f363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983022"
---
# <a name="apiretrievecolumnasbyte-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a>Méthode API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)

Récupère une valeur de colonne d’octets à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function RetrieveColumnAsByte ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Byte)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Byte)

returnValue = Api.RetrieveColumnAsByte(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<byte> RetrieveColumnAsByte(
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
    
    Curseur à partir duquel récupérer la colonne.

<!-- end list -->

  - columnid  
    Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    ColumnID à récupérer.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Options de récupération.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\>  
Données extraites de la colonne sous la forme d’un octet. NULL si la colonne est null.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge RetrieveColumnAsByte](./api.retrievecolumnasbyte-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
