---
description: 'En savoir plus sur : JET_COLUMNDEF. Méthode ContentEquals'
title: JET_COLUMNDEF. Méthode ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNDEF)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103479
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3273a48212432b21482f7caa713509b7a9d58b4d3fb6e49bb42f0ed026d29c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487133"
---
# <a name="jet_columndefcontentequals-method"></a>JET_COLUMNDEF. Méthode ContentEquals

Retourne une valeur indiquant si cette instance est égale à une autre instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNDEF _
) As Boolean
'Usage
Dim instance As JET_COLUMNDEF
Dim other As JET_COLUMNDEF
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNDEF other
)
```

#### <a name="parameters"></a>Paramètres

  - Autres  
    Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)  
    
    Instance de à comparer à cette instance.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

#### <a name="implements"></a>Implémente

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_COLUMNDEF](./jet-columndef-class.md)

[Membres JET_COLUMNDEF](./jet-columndef-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
