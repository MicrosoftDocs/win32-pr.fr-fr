---
description: 'En savoir plus sur : propriété JET_SETINFO. ibLongValue'
title: JET_SETINFO. ibLongValue, propriété
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103918
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324b3cd5c45be8f463ff9b2a9cfe11f1dcad4554
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525563"
---
# <a name="jet_setinfoiblongvalue-property"></a>JET_SETINFO. ibLongValue, propriété

Obtient ou définit offset pour le premier octet à définir dans une colonne de type [LONGBINARY](./jet-coltyp-enumeration.md) ou [LONGTEXT](./jet-coltyp-enumeration.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_SETINFO](./jet-setinfo-class.md)

[Membres JET_SETINFO](./jet-setinfo-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
