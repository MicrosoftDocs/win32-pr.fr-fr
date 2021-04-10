---
description: 'En savoir plus sur : propriété JET_ENUMCOLUMNID. ColumnId'
title: JET_ENUMCOLUMNID. ColumnId, propriété
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.columnid(v=EXCHG.10)
ms:contentKeyID: 55103623
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1c456a4eb208ba8c9f2ac39ea0b4dad410ee270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112099"
---
# <a name="jet_enumcolumnidcolumnid-property"></a>JET_ENUMCOLUMNID. ColumnId, propriété

Obtient ou définit l’ID ColumnID à énumérer.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="remarks"></a>Notes

Si l’ID de colonne est 0 (zéro), l’énumération de cette colonne est ignorée et un emplacement correspondant dans le tableau de sortie des structures de JET_ENUMCOLUMN est généré avec un état de colonne de JET_wrnColumnSkipped.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)

[Membres JET_ENUMCOLUMNID](./jet-enumcolumnid-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
