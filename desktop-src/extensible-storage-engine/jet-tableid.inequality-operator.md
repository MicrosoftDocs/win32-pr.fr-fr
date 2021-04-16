---
description: 'En savoir plus sur : JET_TABLEID. Opérateur d’inégalité'
title: JET_TABLEID. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Inequality
- Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e1cfc9a43beb8478be287e1659883d49f62239
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529296"
---
# <a name="jet_tableidinequality-operator"></a>JET_TABLEID. Opérateur d’inégalité

Détermine si deux instances spécifiées de JET_TABLEID ne sont pas égales.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_TABLEID, _
    rhs As JET_TABLEID _
) As Boolean
'Usage
Dim lhs As JET_TABLEID
Dim rhs As JET_TABLEID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_TABLEID lhs,
    JET_TABLEID rhs
)
```

#### <a name="parameters"></a>Paramètres

  - LHS  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Première instance à comparer.

<!-- end list -->

  - rhs  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Deuxième instance à comparer.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances ne sont pas égales.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_TABLEID](./jet-tableid-structure.md)

[Membres JET_TABLEID](./jet-tableid-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
