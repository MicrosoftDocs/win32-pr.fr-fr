---
description: 'En savoir plus sur : propriété JET_ENUMCOLUMNID. rgtagSequence'
title: JET_ENUMCOLUMNID. rgtagSequence, propriété
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 026432a6d5b2363df09640141ec9f190d6637258692ce8233b32c004a1dbde86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765965"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a>JET_ENUMCOLUMNID. rgtagSequence, propriété

Obtient ou définit le tableau d’index de base un dans le tableau de valeurs de colonne pour une colonne donnée. Un élément unique est un itagSequence qui est défini dans JET_RETRIEVECOLUMN. Un itagSequence de 0 (zéro) signifie « Skip ». Un itagSequence de 1 signifie que retourne la première valeur de colonne de la colonne, 2 le second, et ainsi de suite.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Entrer \[\]  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)

[Membres JET_ENUMCOLUMNID](./jet-enumcolumnid-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
