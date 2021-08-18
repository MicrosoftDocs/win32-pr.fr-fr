---
description: 'En savoir plus sur : méthode UInt16ColumnValue. GetValueFromBytes'
title: Méthode UInt16ColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint16columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104191
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51a07c2674d2053f67887ccaa3881ec25ac308dfefa079a9cdec5ab12f8768c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117701755"
---
# <a name="uint16columnvaluegetvaluefrombytes-method"></a>Méthode UInt16ColumnValue. GetValueFromBytes

Données récupérées à partir d’ESENT, décoder les données et définir la valeur dans l’objet ColumnValue.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Paramètres

  - valeur  
    Entrer \[\]  
    
    Tableau d'octets.

<!-- end list -->

  - index_début  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Position de départ dans les octets.

<!-- end list -->

  - count  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre d'octets à décoder.

<!-- end list -->

  - Raise  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    L’erreur retournée par ESENT.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[UInt16ColumnValue, classe](./uint16columnvalue-class.md)

[Membres UInt16ColumnValue](./uint16columnvalue-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
