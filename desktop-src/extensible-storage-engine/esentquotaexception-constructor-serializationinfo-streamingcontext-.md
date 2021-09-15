---
description: 'En savoir plus sur : constructeur EsentQuotaException (SerializationInfo, StreamingContext)'
title: Constructeur EsentQuotaException (SerializationInfo, StreamingContext)
TOCTitle: EsentQuotaException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentQuotaException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102338
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36748053b8b9b48041c07ff51c99c0144093a9ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403923"
---
# <a name="esentquotaexception-constructor-serializationinfo-streamingcontext"></a>Constructeur EsentQuotaException (SerializationInfo, StreamingContext)

Initialise une nouvelle instance de la classe EsentQuotaException. Ce constructeur est utilisé pour désérialiser une exception sérialisée.

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

Dim instance As New EsentQuotaException(info, context)
```

``` csharp
protected EsentQuotaException(
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

#### <a name="reference"></a>Référence

[Classe EsentQuotaException](./esentquotaexception-class.md)

[Membres EsentQuotaException](./esentquotaexception-members.md)

[Surcharge EsentQuotaException](./esentquotaexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
