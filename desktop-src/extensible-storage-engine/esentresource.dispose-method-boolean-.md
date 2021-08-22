---
description: 'En savoir plus sur : méthode EsentResource. Dispose (Boolean)'
title: EsentResource. dispose, méthode (Boolean)
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cc2f9fab375e2ae2b9a27611192c3db9e3bba4eb272de1dfca243d13bf7766f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119477329"
---
# <a name="esentresourcedispose-method-boolean"></a>EsentResource. dispose, méthode (Boolean)

Appelée par dispose et le finaliseur.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a>Paramètres

  - isDisposing  
    Type : [System. Boolean](/dotnet/api/system.boolean)  
    
    True si la méthode est appelée à partir de dispose.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[EsentResource, classe](./esentresource-class.md)

[Membres EsentResource](./esentresource-members.md)

[Dispose de la surcharge](./esentresource.dispose-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
