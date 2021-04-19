---
description: 'En savoir plus sur : JET_UNICODEINDEX. Méthode ContentEquals'
title: JET_UNICODEINDEX. Méthode ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.ContentEquals(Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ce2ad8c91b772b3d7da98469db2946cd1c6d2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526242"
---
# <a name="jet_unicodeindexcontentequals-method"></a>JET_UNICODEINDEX. Méthode ContentEquals

Retourne une valeur indiquant si cette instance est égale à une autre instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_UNICODEINDEX _
) As Boolean
'Usage
Dim instance As JET_UNICODEINDEX
Dim other As JET_UNICODEINDEX
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_UNICODEINDEX other
)
```

#### <a name="parameters"></a>Paramètres

  - autre  
    Type : [Microsoft.ISAM.esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  
    
    Instance de à comparer à cette instance.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

#### <a name="implements"></a>Implémente

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_UNICODEINDEX](./jet-unicodeindex-class.md)

[Membres JET_UNICODEINDEX](./jet-unicodeindex-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
