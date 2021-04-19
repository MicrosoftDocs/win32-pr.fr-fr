---
description: 'En savoir plus sur : propriété GuidColumnValue. Size'
title: GuidColumnValue. Size, propriété
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.guidcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55107387
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b973638ac8caa4848ed5ecc65468c363ebd2f866
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524948"
---
# <a name="guidcolumnvaluesize-property"></a>GuidColumnValue. Size, propriété

Obtient la taille de la valeur dans la colonne. La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[GuidColumnValue, classe](./guidcolumnvalue-class.md)

[Membres GuidColumnValue](./guidcolumnvalue-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
