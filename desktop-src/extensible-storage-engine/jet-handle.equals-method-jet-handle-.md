---
description: 'En savoir plus sur : JET_HANDLE. Equals, méthode (JET_HANDLE)'
title: JET_HANDLE. Equals, méthode (JET_HANDLE)
TOCTitle: Equals method (JET_HANDLE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals(Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.equals(v=EXCHG.10)
ms:contentKeyID: 39515292
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab4ea5df734b626e54a70bc690301e755013ae59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537072"
---
# <a name="jet_handleequals-method-jet_handle"></a>JET_HANDLE. Equals, méthode (JET_HANDLE)

Retourne une valeur indiquant si cette instance est égale à une autre instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function Equals ( _
    other As JET_HANDLE _
) As Boolean
'Usage
Dim instance As JET_HANDLE
Dim other As JET_HANDLE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_HANDLE other
)
```

#### <a name="parameters"></a>Paramètres

  - autre  
    Type : [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Instance de à comparer à cette instance.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

#### <a name="implements"></a>Implémente

[IEquatable \<T\> . Égal à (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_HANDLE](./jet-handle-structure.md)

[Membres JET_HANDLE](./jet-handle-members.md)

[Est égal à la surcharge](./jet-handle.equals-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
