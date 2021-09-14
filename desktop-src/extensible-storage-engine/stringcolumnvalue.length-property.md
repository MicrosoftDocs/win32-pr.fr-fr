---
description: 'En savoir plus sur : propriété StringColumnValue. Length'
title: StringColumnValue. Length, propriété
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55104090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Length
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7313f66bd25653a66ebd8567a21c0ad5431ec7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196907"
---
# <a name="stringcolumnvaluelength-property"></a>StringColumnValue. Length, propriété

Obtient la longueur d’octet d’une valeur de colonne, qui est égale à zéro si la colonne est NULL ; sinon, elle correspond à la longueur en octets de la valeur de chaîne. La longueur en octets est déterminée en supposant que deux octets par caractère.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As StringColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[StringColumnValue, classe](./stringcolumnvalue-class.md)

[Membres StringColumnValue](./stringcolumnvalue-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
