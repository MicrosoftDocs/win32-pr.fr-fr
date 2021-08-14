---
description: 'En savoir plus sur : constructeur EsentCorruptionException (SerializationInfo, StreamingContext)'
title: Constructeur EsentCorruptionException (SerializationInfo, StreamingContext)
TOCTitle: EsentCorruptionException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101038
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45c967fbecf19149faedafc4a6188a14fb21ba825079c979e154dd366d0be66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117713361"
---
# <a name="esentcorruptionexception-constructor-serializationinfo-streamingcontext"></a>Constructeur EsentCorruptionException (SerializationInfo, StreamingContext)

Initialise une nouvelle instance de la classe EsentCorruptionException. Ce constructeur est utilisé pour désérialiser une exception sérialisée.

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

Dim instance As New EsentCorruptionException(info, context)
```

``` csharp
protected EsentCorruptionException(
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

[EsentCorruptionException, classe](./esentcorruptionexception-class.md)

[Membres EsentCorruptionException](./esentcorruptionexception-members.md)

[Surcharge EsentCorruptionException](./esentcorruptionexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
