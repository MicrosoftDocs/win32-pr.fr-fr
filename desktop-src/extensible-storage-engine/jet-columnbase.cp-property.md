---
description: 'En savoir plus sur les éléments suivants : JET_COLUMNBASE. CP, propriété'
title: JET_COLUMNBASE. CP, propriété
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cp(v=EXCHG.10)
ms:contentKeyID: 55103468
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8928ba3ae46283f856359b36d8f7c4c12f5891b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042836"
---
# <a name="jet_columnbasecp-property"></a>JET_COLUMNBASE. CP, propriété

Obtient la page de codes de la colonne. Cela est significatif uniquement pour les colonnes de type [Text](./jet-coltyp-enumeration.md) et [LONGTEXT](./jet-coltyp-enumeration.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As JET_CP

value = instance.cp
```

``` csharp
public JET_CP cp { get; internal set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [Microsoft.ISAM.esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_COLUMNBASE](./jet-columnbase-class.md)

[Membres JET_COLUMNBASE](./jet-columnbase-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
