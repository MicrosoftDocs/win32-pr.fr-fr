---
description: 'En savoir plus sur : JET_LS. Equals, méthode (JET_LS)'
title: JET_LS. Equals, méthode (JET_LS)
TOCTitle: Equals method (JET_LS)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.Equals(Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.equals(v=EXCHG.10)
ms:contentKeyID: 39510488
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c8a571f97fcf5abc5ff9a69ff476d48adfd8015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527670"
---
# <a name="jet_lsequals-method-jet_ls"></a>JET_LS. Equals, méthode (JET_LS)

Retourne une valeur indiquant si cette instance est égale à une autre instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function Equals ( _
    other As JET_LS _
) As Boolean
'Usage
Dim instance As JET_LS
Dim other As JET_LS
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_LS other
)
```

#### <a name="parameters"></a>Paramètres

  - autre  
    Type : [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)  
    
    Instance de à comparer à cette instance.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

#### <a name="implements"></a>Implémente

[IEquatable \<T\> . Égal à (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_LS](./jet-ls-structure.md)

[Membres JET_LS](./jet-ls-members.md)

[Est égal à la surcharge](./jet-ls.equals-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
