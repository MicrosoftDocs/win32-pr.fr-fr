---
description: 'En savoir plus sur : JET_BKLOGTIME. Opérateur d’inégalité'
title: JET_BKLOGTIME. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512908
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91a209d0bb3251b536a2facbedc0bb95517eabc689646eb07c512e8ab6560587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781129"
---
# <a name="jet_bklogtimeinequality-operator"></a>JET_BKLOGTIME. Opérateur d’inégalité

Détermine si deux instances spécifiées de JET_BKLOGTIME ne sont pas égales.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a>Paramètres

  - LHS  
    Type : [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    Première instance à comparer.

<!-- end list -->

  - rhs  
    Type : [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    Deuxième instance à comparer.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances ne sont pas égales.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_BKLOGTIME](./jet-bklogtime-structure2.md)

[Membres JET_BKLOGTIME](./jet-bklogtime-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
