---
description: 'En savoir plus sur : conversion implicite d’instance (instance to JET_INSTANCE)'
title: Conversion implicite d’instance (instance à JET_INSTANCE)
TOCTitle: Implicit conversion (Instance to JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.op_Implicit(Microsoft.Isam.Esent.Interop.Instance)~Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55103290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
- Microsoft.Isam.Esent.Interop.Instance.op_Implicit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44e0cd05ae4d97c5e0e5f343bc34de5a2bedc55e836cd23642dce6c0ed36c630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117895827"
---
# <a name="instance-implicit-conversion-instance-to-jet_instance"></a>Conversion implicite d’instance (instance à JET_INSTANCE)

Fournir la conversion implicite d’un objet d’instance en une structure JET_INSTANCE. Cette opération est effectuée afin qu’une instance puisse être utilisée partout où une JET_INSTANCE est requise.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    instance As Instance _
) As JET_INSTANCE
'Usage
Dim input As Instance
Dim output As JET_INSTANCE

output = CType(input, JET_INSTANCE)
```

``` csharp
public static implicit operator JET_INSTANCE (
    Instance instance
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft. ISAM. esent. Interop. instance](./instance-class.md)  
    
    Instance à convertir.

#### <a name="return-value"></a>Valeur retournée

Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
JET_INSTANCE encapsulé par l’instance de.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’instance](./instance-class.md)

[Membres d’instance](./instance-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
