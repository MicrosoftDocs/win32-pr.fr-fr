---
description: 'En savoir plus sur : JET_COLUMNBASE. Equals, méthode (Object)'
title: JET_COLUMNBASE. Equals, méthode (Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.equals(v=EXCHG.10)
ms:contentKeyID: 55103438
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2bff106c0988fa60b5d6d2ae45b5d132e6e4e22ff9ac387c217e192b1d9f0a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255095"
---
# <a name="jet_columnbaseequals-method-object"></a>JET_COLUMNBASE. Equals, méthode (Object)

Retourne une valeur indiquant si cette instance est égale à une autre instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_COLUMNBASE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a>Paramètres

  - obj  
    Type : [System. Object](/dotnet/api/system.object)  
    
    Objet à comparer à cette instance.

#### <a name="return-value"></a>Valeur renvoyée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_COLUMNBASE](./jet-columnbase-class.md)

[Membres JET_COLUMNBASE](./jet-columnbase-members.md)

[Est égal à la surcharge](./jet-columnbase.equals-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
