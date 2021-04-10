---
description: 'En savoir plus sur les éléments suivants : JET_COLUMNDEF. CP, propriété'
title: JET_COLUMNDEF. CP, propriété
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cp(v=EXCHG.10)
ms:contentKeyID: 55103411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df383b212105a4b871f0c44d341d6113abf94d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114434"
---
# <a name="jet_columndefcp-property"></a>JET_COLUMNDEF. CP, propriété

Obtient ou définit la page de codes de la colonne. Cela est significatif uniquement pour les colonnes de type [Text](./jet-coltyp-enumeration.md) et [LONGTEXT](./jet-coltyp-enumeration.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [Microsoft.ISAM.esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_COLUMNDEF](./jet-columndef-class.md)

[Membres JET_COLUMNDEF](./jet-columndef-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
