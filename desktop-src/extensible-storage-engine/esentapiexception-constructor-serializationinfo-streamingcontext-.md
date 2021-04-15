---
description: 'En savoir plus sur : constructeur EsentApiException (SerializationInfo, StreamingContext)'
title: Constructeur EsentApiException (SerializationInfo, StreamingContext)
TOCTitle: EsentApiException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101059
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a00204c254378956521a1ae5fe02480dd879c832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485873"
---
# <a name="esentapiexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="4d2ac-103">Constructeur EsentApiException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="4d2ac-103">EsentApiException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="4d2ac-104">Initialise une nouvelle instance de la classe EsentApiException.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-104">Initializes a new instance of the EsentApiException class.</span></span> <span data-ttu-id="4d2ac-105">Ce constructeur est utilisé pour désérialiser une exception sérialisée.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="4d2ac-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d2ac-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d2ac-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d2ac-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d2ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d2ac-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentApiException(info, context)
```

``` csharp
protected EsentApiException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="4d2ac-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d2ac-109">Parameters</span></span>

  - <span data-ttu-id="4d2ac-110">info</span><span class="sxs-lookup"><span data-stu-id="4d2ac-110">info</span></span>  
    <span data-ttu-id="4d2ac-111">Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="4d2ac-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="4d2ac-112">Données nécessaires pour désérialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="4d2ac-113">contexte</span><span class="sxs-lookup"><span data-stu-id="4d2ac-113">context</span></span>  
    <span data-ttu-id="4d2ac-114">Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="4d2ac-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="4d2ac-115">Contexte de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d2ac-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d2ac-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d2ac-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4d2ac-117">Reference</span></span>

[<span data-ttu-id="4d2ac-118">EsentApiException, classe</span><span class="sxs-lookup"><span data-stu-id="4d2ac-118">EsentApiException class</span></span>](./esentapiexception-class.md)

[<span data-ttu-id="4d2ac-119">Membres EsentApiException</span><span class="sxs-lookup"><span data-stu-id="4d2ac-119">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="4d2ac-120">Surcharge EsentApiException</span><span class="sxs-lookup"><span data-stu-id="4d2ac-120">EsentApiException overload</span></span>](./esentapiexception-constructor.md)

[<span data-ttu-id="4d2ac-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4d2ac-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
