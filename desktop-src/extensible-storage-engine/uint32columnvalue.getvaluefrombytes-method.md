---
description: 'En savoir plus sur : méthode UInt32ColumnValue. GetValueFromBytes'
title: Méthode UInt32ColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.UInt32ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint32columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104176
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fdc4ada75a0d3eb2254b5a5511125697869e25fd93db8a1c151005ca78935ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978319"
---
# <a name="uint32columnvaluegetvaluefrombytes-method"></a>Méthode UInt32ColumnValue. GetValueFromBytes

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

[UInt32ColumnValue, classe](./uint32columnvalue-class.md)

[Membres UInt32ColumnValue](./uint32columnvalue-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
