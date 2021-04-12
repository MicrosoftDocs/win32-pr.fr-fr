---
description: 'En savoir plus sur : constructeur EsentDiskException (SerializationInfo, StreamingContext)'
title: Constructeur EsentDiskException (SerializationInfo, StreamingContext)
TOCTitle: EsentDiskException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4abe19b16d9e6eb6d94d5b4fe1dd067b68c2c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320790"
---
# <a name="esentdiskexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="ba1e1-103">Constructeur EsentDiskException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="ba1e1-103">EsentDiskException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="ba1e1-104">Initialise une nouvelle instance de la classe EsentDiskException.</span><span class="sxs-lookup"><span data-stu-id="ba1e1-104">Initializes a new instance of the EsentDiskException class.</span></span> <span data-ttu-id="ba1e1-105">Ce constructeur est utilisé pour désérialiser une exception sérialisée.</span><span class="sxs-lookup"><span data-stu-id="ba1e1-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="ba1e1-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ba1e1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ba1e1-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ba1e1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ba1e1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba1e1-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDiskException(info, context)
```

``` csharp
protected EsentDiskException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="ba1e1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba1e1-109">Parameters</span></span>

  - <span data-ttu-id="ba1e1-110">info</span><span class="sxs-lookup"><span data-stu-id="ba1e1-110">info</span></span>  
    <span data-ttu-id="ba1e1-111">Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="ba1e1-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="ba1e1-112">Données nécessaires pour désérialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="ba1e1-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="ba1e1-113">contexte</span><span class="sxs-lookup"><span data-stu-id="ba1e1-113">context</span></span>  
    <span data-ttu-id="ba1e1-114">Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="ba1e1-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="ba1e1-115">Contexte de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="ba1e1-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba1e1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba1e1-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ba1e1-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ba1e1-117">Reference</span></span>

[<span data-ttu-id="ba1e1-118">EsentDiskException, classe</span><span class="sxs-lookup"><span data-stu-id="ba1e1-118">EsentDiskException class</span></span>](./esentdiskexception-class.md)

[<span data-ttu-id="ba1e1-119">Membres EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="ba1e1-119">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="ba1e1-120">Surcharge EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="ba1e1-120">EsentDiskException overload</span></span>](./esentdiskexception-constructor.md)

[<span data-ttu-id="ba1e1-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ba1e1-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
