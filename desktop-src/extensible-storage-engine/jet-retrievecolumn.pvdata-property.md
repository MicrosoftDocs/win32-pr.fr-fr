---
description: 'En savoir plus sur : propriété JET_RETRIEVECOLUMN. pvData'
title: JET_RETRIEVECOLUMN. pvData, propriété
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_pvData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a791bfa6fa44b4a24387c42bac66bdf453c130ec68039119620c2a782731b39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890399"
---
# <a name="jet_retrievecolumnpvdata-property"></a>JET_RETRIEVECOLUMN. pvData, propriété

Obtient ou définit la mémoire tampon qui stocke les données extraites de la colonne.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property pvData As Byte()
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Byte()

value = instance.pvData

instance.pvData = value
```

``` csharp
public byte[] pvData { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Entrer \[\]  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)

[Membres JET_RETRIEVECOLUMN](./jet-retrievecolumn-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
