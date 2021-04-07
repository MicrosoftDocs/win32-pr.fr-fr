---
description: 'En savoir plus sur : constructeur DurableCommitCallback'
title: Constructeur DurableCommitCallback (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'DurableCommitCallback constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.durablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.DurableCommitCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade1952615b98d9ea41a7a1b83d0bf1a3c6fc8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759412"
---
# <a name="durablecommitcallback-constructor"></a>Constructeur DurableCommitCallback

Initialise une nouvelle instance de la classe [DurableCommitCallback](./durablecommitcallback-class.md) .

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE, _
    wrappedCallback As JET_PFNDURABLECOMMITCALLBACK _
)
'Usage
Dim instance As JET_INSTANCE
Dim wrappedCallback As JET_PFNDURABLECOMMITCALLBACK

Dim instance As New DurableCommitCallback(instance, _
    wrappedCallback)
```

``` csharp
public DurableCommitCallback(
    JET_INSTANCE instance,
    JET_PFNDURABLECOMMITCALLBACK wrappedCallback
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instance de à laquelle associer le rappel.

<!-- end list -->

  - wrappedCallback  
    Type : [Microsoft.ISAM.esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)  
    
    Rappel de code managé à appeler.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[DurableCommitCallback, classe](./durablecommitcallback-class.md)

[Membres DurableCommitCallback](./durablecommitcallback-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
