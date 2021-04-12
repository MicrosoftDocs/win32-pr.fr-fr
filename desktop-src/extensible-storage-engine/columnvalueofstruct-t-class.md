---
description: 'En savoir plus sur : <T> classe ColumnValueOfStruct'
title: ColumnValueOfStruct(T), classe
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321413"
---
# <a name="columnvalueofstructt-class"></a>ColumnValueOfStruct, \<T\> classe

Définissez une colonne d’un type struct (par exemple, Int32/GUID).

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. esent. Interop. ColumnValue](./columnvalue-class.md)  
    Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\>  
      

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a>Paramètres de type

  - T  
    Type à définir.

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[\<T\>Membres ColumnValueOfStruct](./columnvalueofstruct-t-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Types dérivés

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. esent. Interop. ColumnValue](./columnvalue-class.md)  
    Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\>  
      [Microsoft. ISAM. esent. Interop. BoolColumnValue](./boolcolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. ByteColumnValue](./bytecolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. DateTimeColumnValue](./datetimecolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. DoubleColumnValue](./doublecolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. FloatColumnValue](./floatcolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. GuidColumnValue](./guidcolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. Int16ColumnValue](./int16columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. Int32ColumnValue](./int32columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. Int64ColumnValue](./int64columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. UInt16ColumnValue](./uint16columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. UInt32ColumnValue](./uint32columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. UInt64ColumnValue](./uint64columnvalue-class.md)