---
description: 'En savoir plus sur : constructeur EsentException (SerializationInfo, StreamingContext)'
title: Constructeur EsentException (SerializationInfo, StreamingContext) (Microsoft. ISAM. esent)
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bdcfe5c3b37746f50926850b45763f9d70de893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523717"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a>Constructeur EsentException (SerializationInfo, StreamingContext)

Initialise une nouvelle instance de la classe EsentException. Ce constructeur est utilisé pour désérialiser une exception sérialisée.

**Espace de noms :**  [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Paramètres

  - info  
    Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Données nécessaires pour désérialiser l’objet.

<!-- end list -->

  - contexte  
    Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Contexte de la désérialisation.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[EsentException, classe](./esentexception-class.md)

[Membres EsentException](./esentexception-members.md)

[Surcharge EsentException](./esentexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)
