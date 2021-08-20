---
description: 'En savoir plus sur : JET_SESID. Opérateur d’égalité'
title: JET_SESID. Opérateur d’égalité
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d6137ad066dd92afdce6dcf41e748ca34b3c17d4a52d437781fda69c5c6d851
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945349"
---
# <a name="jet_sesidequality-operator"></a>JET_SESID. Opérateur d’égalité

Détermine si deux instances spécifiées de JET_SESID sont égales.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a>Paramètres

  - LHS  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Première instance à comparer.

<!-- end list -->

  - rhs  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Deuxième instance à comparer.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_SESID](./jet-sesid-structure.md)

[Membres JET_SESID](./jet-sesid-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
