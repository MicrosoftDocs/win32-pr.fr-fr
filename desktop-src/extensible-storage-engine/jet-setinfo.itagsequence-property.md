---
description: 'En savoir plus sur : propriété JET_SETINFO. itagSequence'
title: JET_SETINFO. itagSequence, propriété
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a62276cd7ec9936cc82383b20b59d9a6dc9708be2563238c02b06f6879dd7d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016479"
---
# <a name="jet_setinfoitagsequence-property"></a>JET_SETINFO. itagSequence, propriété

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
Dim instance As JET_SETINFO
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

[Classe JET_SETINFO](./jet-setinfo-class.md)

[Membres JET_SETINFO](./jet-setinfo-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
