---
description: 'En savoir plus sur : constructeur EsentInconsistentException (SerializationInfo, StreamingContext)'
title: Constructeur EsentInconsistentException (SerializationInfo, StreamingContext)
TOCTitle: EsentInconsistentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInconsistentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f907288bd4f88cae0b022a74cf558a65415d214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532328"
---
# <a name="esentinconsistentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="34759-103">Constructeur EsentInconsistentException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="34759-103">EsentInconsistentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="34759-104">Initialise une nouvelle instance de la classe EsentInconsistentException.</span><span class="sxs-lookup"><span data-stu-id="34759-104">Initializes a new instance of the EsentInconsistentException class.</span></span> <span data-ttu-id="34759-105">Ce constructeur est utilisé pour désérialiser une exception sérialisée.</span><span class="sxs-lookup"><span data-stu-id="34759-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="34759-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34759-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34759-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34759-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34759-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34759-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentInconsistentException(info, context)
```

``` csharp
protected EsentInconsistentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="34759-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34759-109">Parameters</span></span>

  - <span data-ttu-id="34759-110">info</span><span class="sxs-lookup"><span data-stu-id="34759-110">info</span></span>  
    <span data-ttu-id="34759-111">Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="34759-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="34759-112">Données nécessaires pour désérialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="34759-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="34759-113">contexte</span><span class="sxs-lookup"><span data-stu-id="34759-113">context</span></span>  
    <span data-ttu-id="34759-114">Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="34759-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="34759-115">Contexte de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="34759-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="34759-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34759-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34759-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="34759-117">Reference</span></span>

[<span data-ttu-id="34759-118">EsentInconsistentException, classe</span><span class="sxs-lookup"><span data-stu-id="34759-118">EsentInconsistentException class</span></span>](./esentinconsistentexception-class.md)

[<span data-ttu-id="34759-119">Membres EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="34759-119">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="34759-120">Surcharge EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="34759-120">EsentInconsistentException overload</span></span>](./esentinconsistentexception-constructor.md)

[<span data-ttu-id="34759-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="34759-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
