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
ms.openlocfilehash: a0e80255d86ed6f953e4010541e98b794537f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953029"
---
# <a name="esentcorruptionexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="e4a82-103">Constructeur EsentCorruptionException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="e4a82-103">EsentCorruptionException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="e4a82-104">Initialise une nouvelle instance de la classe EsentCorruptionException.</span><span class="sxs-lookup"><span data-stu-id="e4a82-104">Initializes a new instance of the EsentCorruptionException class.</span></span> <span data-ttu-id="e4a82-105">Ce constructeur est utilisé pour désérialiser une exception sérialisée.</span><span class="sxs-lookup"><span data-stu-id="e4a82-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="e4a82-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4a82-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4a82-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e4a82-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a82-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4a82-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="e4a82-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4a82-109">Parameters</span></span>

  - <span data-ttu-id="e4a82-110">info</span><span class="sxs-lookup"><span data-stu-id="e4a82-110">info</span></span>  
    <span data-ttu-id="e4a82-111">Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="e4a82-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="e4a82-112">Données nécessaires pour désérialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="e4a82-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4a82-113">contexte</span><span class="sxs-lookup"><span data-stu-id="e4a82-113">context</span></span>  
    <span data-ttu-id="e4a82-114">Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="e4a82-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="e4a82-115">Contexte de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="e4a82-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4a82-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4a82-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4a82-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e4a82-117">Reference</span></span>

[<span data-ttu-id="e4a82-118">EsentCorruptionException, classe</span><span class="sxs-lookup"><span data-stu-id="e4a82-118">EsentCorruptionException class</span></span>](./esentcorruptionexception-class.md)

[<span data-ttu-id="e4a82-119">Membres EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="e4a82-119">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="e4a82-120">Surcharge EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="e4a82-120">EsentCorruptionException overload</span></span>](./esentcorruptionexception-constructor.md)

[<span data-ttu-id="e4a82-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e4a82-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
