---
description: 'En savoir plus sur : constructeur EsentFragmentationException (SerializationInfo, StreamingContext)'
title: Constructeur EsentFragmentationException (SerializationInfo, StreamingContext)
TOCTitle: EsentFragmentationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101633
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 251e4beaacb1e895c1da1d501b38cf03f211dd99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321185"
---
# <a name="esentfragmentationexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="55576-103">Constructeur EsentFragmentationException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="55576-103">EsentFragmentationException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="55576-104">Initialise une nouvelle instance de la classe EsentFragmentationException.</span><span class="sxs-lookup"><span data-stu-id="55576-104">Initializes a new instance of the EsentFragmentationException class.</span></span> <span data-ttu-id="55576-105">Ce constructeur est utilisé pour désérialiser une exception sérialisée.</span><span class="sxs-lookup"><span data-stu-id="55576-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="55576-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55576-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55576-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55576-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55576-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55576-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentFragmentationException(info, context)
```

``` csharp
protected EsentFragmentationException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="55576-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55576-109">Parameters</span></span>

  - <span data-ttu-id="55576-110">info</span><span class="sxs-lookup"><span data-stu-id="55576-110">info</span></span>  
    <span data-ttu-id="55576-111">Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="55576-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="55576-112">Données nécessaires pour désérialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="55576-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="55576-113">contexte</span><span class="sxs-lookup"><span data-stu-id="55576-113">context</span></span>  
    <span data-ttu-id="55576-114">Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="55576-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="55576-115">Contexte de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="55576-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="55576-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55576-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55576-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="55576-117">Reference</span></span>

[<span data-ttu-id="55576-118">EsentFragmentationException, classe</span><span class="sxs-lookup"><span data-stu-id="55576-118">EsentFragmentationException class</span></span>](./esentfragmentationexception-class.md)

[<span data-ttu-id="55576-119">Membres EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="55576-119">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="55576-120">Surcharge EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="55576-120">EsentFragmentationException overload</span></span>](./esentfragmentationexception-constructor.md)

[<span data-ttu-id="55576-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="55576-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
