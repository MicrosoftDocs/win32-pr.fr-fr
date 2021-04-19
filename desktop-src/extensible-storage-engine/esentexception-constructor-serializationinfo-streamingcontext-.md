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
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="a27c8-103">Constructeur EsentException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="a27c8-103">EsentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="a27c8-104">Initialise une nouvelle instance de la classe EsentException.</span><span class="sxs-lookup"><span data-stu-id="a27c8-104">Initializes a new instance of the EsentException class.</span></span> <span data-ttu-id="a27c8-105">Ce constructeur est utilisé pour désérialiser une exception sérialisée.</span><span class="sxs-lookup"><span data-stu-id="a27c8-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="a27c8-106">**Espace de noms :**  [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a27c8-106">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="a27c8-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a27c8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a27c8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a27c8-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="a27c8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a27c8-109">Parameters</span></span>

  - <span data-ttu-id="a27c8-110">info</span><span class="sxs-lookup"><span data-stu-id="a27c8-110">info</span></span>  
    <span data-ttu-id="a27c8-111">Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="a27c8-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="a27c8-112">Données nécessaires pour désérialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="a27c8-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="a27c8-113">contexte</span><span class="sxs-lookup"><span data-stu-id="a27c8-113">context</span></span>  
    <span data-ttu-id="a27c8-114">Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="a27c8-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="a27c8-115">Contexte de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="a27c8-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="a27c8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a27c8-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a27c8-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a27c8-117">Reference</span></span>

[<span data-ttu-id="a27c8-118">EsentException, classe</span><span class="sxs-lookup"><span data-stu-id="a27c8-118">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="a27c8-119">Membres EsentException</span><span class="sxs-lookup"><span data-stu-id="a27c8-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="a27c8-120">Surcharge EsentException</span><span class="sxs-lookup"><span data-stu-id="a27c8-120">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="a27c8-121">Espace de noms Microsoft. ISAM. esent</span><span class="sxs-lookup"><span data-stu-id="a27c8-121">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
