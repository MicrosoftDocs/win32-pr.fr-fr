---
description: 'En savoir plus sur : constructeur EsentStateException (SerializationInfo, StreamingContext)'
title: Constructeur EsentStateException (SerializationInfo, StreamingContext)
TOCTitle: EsentStateException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102710
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458efcde030559122085824a99660c3d5d7fc4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319854"
---
# <a name="esentstateexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="fc165-103">Constructeur EsentStateException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="fc165-103">EsentStateException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="fc165-104">Initialise une nouvelle instance de la classe EsentStateException.</span><span class="sxs-lookup"><span data-stu-id="fc165-104">Initializes a new instance of the EsentStateException class.</span></span> <span data-ttu-id="fc165-105">Ce constructeur est utilisé pour désérialiser une exception sérialisée.</span><span class="sxs-lookup"><span data-stu-id="fc165-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="fc165-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fc165-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fc165-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fc165-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fc165-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc165-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentStateException(info, context)
```

``` csharp
protected EsentStateException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="fc165-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc165-109">Parameters</span></span>

  - <span data-ttu-id="fc165-110">info</span><span class="sxs-lookup"><span data-stu-id="fc165-110">info</span></span>  
    <span data-ttu-id="fc165-111">Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="fc165-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="fc165-112">Données nécessaires pour désérialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="fc165-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc165-113">contexte</span><span class="sxs-lookup"><span data-stu-id="fc165-113">context</span></span>  
    <span data-ttu-id="fc165-114">Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="fc165-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="fc165-115">Contexte de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="fc165-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc165-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc165-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc165-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="fc165-117">Reference</span></span>

[<span data-ttu-id="fc165-118">EsentStateException, classe</span><span class="sxs-lookup"><span data-stu-id="fc165-118">EsentStateException class</span></span>](./esentstateexception-class.md)

[<span data-ttu-id="fc165-119">Membres EsentStateException</span><span class="sxs-lookup"><span data-stu-id="fc165-119">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="fc165-120">Surcharge EsentStateException</span><span class="sxs-lookup"><span data-stu-id="fc165-120">EsentStateException overload</span></span>](./esentstateexception-constructor.md)

[<span data-ttu-id="fc165-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fc165-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
