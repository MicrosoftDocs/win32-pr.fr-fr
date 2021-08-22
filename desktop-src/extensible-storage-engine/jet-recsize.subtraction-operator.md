---
description: 'En savoir plus sur : JET_RECSIZE. Soustraction (opérateur)'
title: JET_RECSIZE. Opérateur de soustraction (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39516016
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 40ff320ed629790bad0f2b23aebae5b5092df2b0d25665c2eb2c5d468361216c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616499"
---
# <a name="jet_recsizesubtraction-operator"></a>JET_RECSIZE. Soustraction (opérateur)

Calculez la différence de tailles entre deux structures de JET_RECSIZE.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Operator - ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left - right)
```

``` csharp
public static JET_RECSIZE operator -(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a>Paramètres

  - gauche  
    Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Premier JET_RECSIZE.

<!-- end list -->

  - droite  
    Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Deuxième JET_RECSIZE.

#### <a name="return-value"></a>Valeur retournée

Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
JET_RECSIZE contenant la différence de tailles entre gauche et droite.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_RECSIZE](./jet-recsize-structure2.md)

[Membres JET_RECSIZE](./jet-recsize-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
