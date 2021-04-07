---
description: 'En savoir plus sur : JET_THREADSTATS. Créer une méthode'
title: JET_THREADSTATS. Create, méthode (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758493"
---
# <a name="jet_threadstatscreate-method"></a>JET_THREADSTATS. Créer une méthode

Crée un nouveau [JET_THREADSTATS](./jet-threadstats-structure2.md) structure avec la valeur spécifiée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a>Paramètres

  - cPageReferenced  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre de pages visitées.

<!-- end list -->

  - cPageRead  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre de pages lues.

<!-- end list -->

  - cPagePreread  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre de pages prélues.

<!-- end list -->

  - cPageDirtied  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    TNumber de pages modifiées.

<!-- end list -->

  - cPageRedirtied  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre de pages Remodifiées.

<!-- end list -->

  - cLogRecord  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre d’enregistrements de journal générés.

<!-- end list -->

  - cbLogRecord  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Octets des enregistrements de journal écrits.

#### <a name="return-value"></a>Valeur retournée

Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Nouvelle [JET_THREADSTATS](./jet-threadstats-structure2.md) structure avec les valeurs spécifiées.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membres JET_THREADSTATS](./jet-threadstats-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
