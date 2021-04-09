---
description: 'En savoir plus sur : propriété JET_INDEXLIST. columnidLCMapFlags'
title: JET_INDEXLIST. columnidLCMapFlags, propriété
TOCTitle: 'columnidLCMapFlags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55103667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidLCMapFlags
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidLCMapFlags
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5479bda4a0b4f4b802ae42221f5bbd9879c94c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866845"
---
# <a name="jet_indexlistcolumnidlcmapflags-property"></a>JET_INDEXLIST. columnidLCMapFlags, propriété

Obtient le ColumnID de la colonne dans la table temporaire qui stocke les indicateurs de normalisation Unicode pour l’index. La colonne est de type [long](./jet-coltyp-enumeration.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property columnidLCMapFlags As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidLCMapFlags
```

``` csharp
public JET_COLUMNID columnidLCMapFlags { get; internal set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_INDEXLIST](./jet-indexlist-class.md)

[Membres JET_INDEXLIST](./jet-indexlist-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
