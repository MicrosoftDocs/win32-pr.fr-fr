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
ms.openlocfilehash: be60da4aeeab78794f087e9c7095a16dd39eb378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524351"
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
