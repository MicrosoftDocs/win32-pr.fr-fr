---
description: 'En savoir plus sur : propriété JET_SETCOLUMN. itagSequence'
title: JET_SETCOLUMN. itagSequence, propriété
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103935
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7870f6e29cf8f6810c6aa41049868fbceb370dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519267"
---
# <a name="jet_setcolumnitagsequence-property"></a>JET_SETCOLUMN. itagSequence, propriété

Obtient ou définit le numéro de séquence de la valeur dans une colonne à valeurs multiples à définir. Le tableau de valeurs est de base un. La première valeur est Sequence 1, et non 0 (zéro). Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé comme itagSequence si cette valeur est remplacée. La valeur 0 (zéro) signifie que vous pouvez ajouter une nouvelle instance de valeur de colonne à la fin de la séquence de valeurs de colonne.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_SETCOLUMN](./jet-setcolumn-class.md)

[Membres JET_SETCOLUMN](./jet-setcolumn-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
