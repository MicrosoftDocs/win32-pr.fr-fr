---
description: 'En savoir plus sur : méthode API. ResetIndexRange'
title: API. ResetIndexRange, méthode
TOCTitle: 'ResetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.ResetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.resetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100832
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 434740a549fa83d4601bf88ab09f307f4d19f189
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292394"
---
# <a name="apiresetindexrange-method"></a>API. ResetIndexRange, méthode

Supprime une plage d’index créée avec [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) ou [TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md). Si aucune plage d’index n’est présente, cette méthode n’a aucun effet.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub ResetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.ResetIndexRange(sesid, tableid)
```

``` csharp
public static void ResetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur sur lequel supprimer la plage d’index.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
