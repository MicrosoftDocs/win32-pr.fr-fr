---
description: 'En savoir plus sur : constructeur EsentDataException (SerializationInfo, StreamingContext)'
title: Constructeur EsentDataException (SerializationInfo, StreamingContext)
TOCTitle: EsentDataException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101275
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f1453b695652675fd96b373fc08dd1a0c785fc1630182ebdb23fcd3636793fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974323"
---
# <a name="esentdataexception-constructor-serializationinfo-streamingcontext"></a>Constructeur EsentDataException (SerializationInfo, StreamingContext)

Initialise une nouvelle instance de la classe EsentDataException. Ce constructeur est utilisé pour désérialiser une exception sérialisée.

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

Dim instance As New EsentDataException(info, context)
```

``` csharp
protected EsentDataException(
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

[EsentDataException, classe](./esentdataexception-class.md)

[Membres EsentDataException](./esentdataexception-members.md)

[Surcharge EsentDataException](./esentdataexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
