---
description: 'En savoir plus sur : méthode Int32ColumnValue. GetValueFromBytes'
title: Méthode Int32ColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int32ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int32columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103331
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c17ee9bc638a0adc2250ac0b3f2e53571ff6fdd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753284"
---
# <a name="int32columnvaluegetvaluefrombytes-method"></a>Méthode Int32ColumnValue. GetValueFromBytes

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

  - value  
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

[Int32ColumnValue, classe](./int32columnvalue-class.md)

[Membres Int32ColumnValue](./int32columnvalue-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
