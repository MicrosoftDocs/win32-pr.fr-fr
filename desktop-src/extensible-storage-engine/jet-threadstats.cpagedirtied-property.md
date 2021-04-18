---
description: 'En savoir plus sur : propriété JET_THREADSTATS. cPageDirtied'
title: JET_THREADSTATS. cPageDirtied, propriété (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'cPageDirtied property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagedirtied(v=EXCHG.10)
ms:contentKeyID: 39512428
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageDirtied
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d1f628ce821a6e35c231ccf4b469b5b1c1ff60c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524994"
---
# <a name="jet_threadstatscpagedirtied-property"></a>JET_THREADSTATS. cPageDirtied, propriété

Obtient le nombre total de pages de base de données, sans modifications non écrites, qui ont été modifiées par le moteur de base de données sur le thread actuel.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property cPageDirtied As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageDirtied
```

``` csharp
public int cPageDirtied { get; internal set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membres JET_THREADSTATS](./jet-threadstats-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
