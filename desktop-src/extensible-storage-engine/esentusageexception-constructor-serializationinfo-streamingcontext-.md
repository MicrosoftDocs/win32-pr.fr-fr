---
description: 'En savoir plus sur : constructeur EsentUsageException (SerializationInfo, StreamingContext)'
title: Constructeur EsentUsageException (SerializationInfo, StreamingContext)
TOCTitle: EsentUsageException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103026
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93c67f5bb8b324eaab04797f3a7d6bba6a5e4cf6867bd779e16057789503fcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781259"
---
# <a name="esentusageexception-constructor-serializationinfo-streamingcontext"></a>Constructeur EsentUsageException (SerializationInfo, StreamingContext)

Initialise une nouvelle instance de la classe EsentUsageException. Ce constructeur est utilisé pour désérialiser une exception sérialisée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
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

Dim instance As New EsentUsageException(info, context)
```

``` csharp
protected EsentUsageException(
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

[EsentUsageException, classe](./esentusageexception-class.md)

[Membres EsentUsageException](./esentusageexception-members.md)

[Surcharge EsentUsageException](./esentusageexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
