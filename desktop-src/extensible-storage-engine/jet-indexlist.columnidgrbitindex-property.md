---
description: 'En savoir plus sur : propriété JET_INDEXLIST. columnidgrbitIndex'
title: JET_INDEXLIST. columnidgrbitIndex, propriété
TOCTitle: 'columnidgrbitIndex property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitindex(v=EXCHG.10)
ms:contentKeyID: 55103615
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae8d31661451a2bd1c7c5f942141c27ae552c578
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007767"
---
# <a name="jet_indexlistcolumnidgrbitindex-property"></a>JET_INDEXLIST. columnidgrbitIndex, propriété

Obtient le ColumnID de la colonne dans la table temporaire qui stocke les grbits utilisés sur l’index. Consultez [CreateIndexGrbit](./createindexgrbit-enumeration.md). La colonne est de type [long](./jet-coltyp-enumeration.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidgrbitIndex As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitIndex
```

``` csharp
public JET_COLUMNID columnidgrbitIndex { get; internal set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe JET_INDEXLIST](./jet-indexlist-class.md)

[Membres JET_INDEXLIST](./jet-indexlist-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
