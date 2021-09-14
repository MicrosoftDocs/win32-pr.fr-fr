---
description: 'En savoir plus sur : JET_LGPOS. GreaterThan (opérateur)'
title: JET_LGPOS. GreaterThan (opérateur)
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThan(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 39510131
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThan
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f3e0c060311205d1f5d47bc4678c6ff9458b589
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126850887"
---
# <a name="jet_lgposgreaterthan-operator"></a>JET_LGPOS. GreaterThan (opérateur)

Déterminez si une position de journal se trouve après une autre position de journal.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a>Paramètres

  - LHS  
    Type : [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Première position du journal à comparer.

<!-- end list -->

  - rhs  
    Type : [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Deuxième position du journal à comparer.

#### <a name="return-value"></a>Valeur de retour

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si LHS vient après RHS.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_LGPOS](./jet-lgpos-structure2.md)

[Membres JET_LGPOS](./jet-lgpos-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
