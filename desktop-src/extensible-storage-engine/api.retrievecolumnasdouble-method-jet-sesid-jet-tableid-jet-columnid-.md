---
description: 'En savoir plus sur : méthode API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Méthode API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsDouble method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDouble(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdouble(v=EXCHG.10)
ms:contentKeyID: 55100847
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDouble
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9bf86595870b03447dd8a859ac66f0aa0c5f9a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530598"
---
# <a name="apiretrievecolumnasdouble-method-jet_sesid-jet_tableid-jet_columnid"></a>Méthode API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)

Récupère une valeur de colonne double de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDouble ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Double)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Double)

returnValue = Api.RetrieveColumnAsDouble(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<double> RetrieveColumnAsDouble(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
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

#### <a name="return-value"></a>Valeur retournée

Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[Double](/dotnet/api/system.double)\>  
Données extraites de la colonne sous la forme d’un double. NULL si la colonne est null.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge RetrieveColumnAsDouble](./api.retrievecolumnasdouble-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
