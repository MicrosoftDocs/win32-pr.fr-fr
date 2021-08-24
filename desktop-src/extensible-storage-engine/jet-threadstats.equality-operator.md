---
description: 'En savoir plus sur : JET_THREADSTATS. Opérateur d’égalité'
title: JET_THREADSTATS. Opérateur d’égalité (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 939bf3f7c9d9741dd8a54613130ea363b64a8b3fbe2f84ea22ec0efe9dbf647b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719499"
---
# <a name="jet_threadstatsequality-operator"></a>JET_THREADSTATS. Opérateur d’égalité

Détermine si deux instances spécifiées de JET_THREADSTATS sont égales.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a>Paramètres

  - LHS  
    Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Première instance à comparer.

<!-- end list -->

  - rhs  
    Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Deuxième instance à comparer.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membres JET_THREADSTATS](./jet-threadstats-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
