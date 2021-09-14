---
description: 'En savoir plus sur : JET_COLUMNCREATE. Méthode ContentEquals'
title: JET_COLUMNCREATE. Méthode ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103471
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db39608007705284b4690893cb6e3196dca8dc35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854386"
---
# <a name="jet_columncreatecontentequals-method"></a>JET_COLUMNCREATE. Méthode ContentEquals

Retourne une valeur indiquant si cette instance est égale à une autre instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNCREATE _
) As Boolean
'Usage
Dim instance As JET_COLUMNCREATE
Dim other As JET_COLUMNCREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNCREATE other
)
```

#### <a name="parameters"></a>Paramètres

  - other  
    Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNCREATE](./jet-columncreate-class.md)  
    
    Instance de à comparer à cette instance.

#### <a name="return-value"></a>Valeur de retour

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si les deux instances sont égales.  

#### <a name="implements"></a>Implémente

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_COLUMNCREATE](./jet-columncreate-class.md)

[Membres JET_COLUMNCREATE](./jet-columncreate-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
