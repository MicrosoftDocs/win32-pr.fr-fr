---
description: 'En savoir plus sur : opérateur JET_COMMIT_ID. GreaterThanOrEqual'
title: Opérateur JET_COMMIT_ID. GreaterThanOrEqual (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 55104298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e531168d2c0656c465d8eace46d00181375bc4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010244"
---
# <a name="jet_commit_idgreaterthanorequal-operator"></a>Opérateur JET_COMMIT_ID. GreaterThanOrEqual

Déterminez si un commitid est avant un autre commitid.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a>Paramètres

  - LHS  
    Type : [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Premier commitid à comparer.

<!-- end list -->

  - rhs  
    Type : [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Deuxième commitid à comparer.

#### <a name="return-value"></a>Valeur de retour

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si LHS vient après ou est égal à RHS.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe JET_COMMIT_ID](./jet-commit-id-class.md)

[Membres JET_COMMIT_ID](./jet-commit-id-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
