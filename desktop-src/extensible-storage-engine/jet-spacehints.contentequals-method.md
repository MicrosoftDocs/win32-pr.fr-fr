---
description: 'En savoir plus sur : JET_SPACEHINTS. Méthode ContentEquals'
title: JET_SPACEHINTS. Méthode ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ContentEquals(Microsoft.Isam.Esent.Interop.JET_SPACEHINTS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103958
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f32ca814f8a72e22d485b57528b96843067d97f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526261"
---
# <a name="jet_spacehintscontentequals-method"></a>JET_SPACEHINTS. Méthode ContentEquals

Retourne une valeur indiquant si cette instance est égale à une autre instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_SPACEHINTS _
) As Boolean
'Usage
Dim instance As JET_SPACEHINTS
Dim other As JET_SPACEHINTS
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_SPACEHINTS other
)
```

#### <a name="parameters"></a>Paramètres

  - other  
    Type : [Microsoft.ISAM.esent.Interop.JET_SPACEHINTS](./jet-spacehints-class.md)  
    
    Instance de à comparer à cette instance.

#### <a name="return-value"></a>Valeur de retour

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

#### <a name="implements"></a>Implémente

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe JET_SPACEHINTS](./jet-spacehints-class.md)

[Membres JET_SPACEHINTS](./jet-spacehints-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
