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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320306"
---
# <a name="esentquotaexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="2deec-103">Constructeur EsentQuotaException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="2deec-103">EsentQuotaException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="2deec-104">Initialise une nouvelle instance de la classe EsentQuotaException.</span><span class="sxs-lookup"><span data-stu-id="2deec-104">Initializes a new instance of the EsentQuotaException class.</span></span> <span data-ttu-id="2deec-105">Ce constructeur est utilisé pour désérialiser une exception sérialisée.</span><span class="sxs-lookup"><span data-stu-id="2deec-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="2deec-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2deec-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2deec-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2deec-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2deec-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2deec-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="2deec-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2deec-109">Parameters</span></span>

  - <span data-ttu-id="2deec-110">info</span><span class="sxs-lookup"><span data-stu-id="2deec-110">info</span></span>  
    <span data-ttu-id="2deec-111">Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="2deec-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="2deec-112">Données nécessaires pour désérialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="2deec-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="2deec-113">contexte</span><span class="sxs-lookup"><span data-stu-id="2deec-113">context</span></span>  
    <span data-ttu-id="2deec-114">Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="2deec-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="2deec-115">Contexte de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="2deec-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="2deec-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2deec-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2deec-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2deec-117">Reference</span></span>

[<span data-ttu-id="2deec-118">Classe EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="2deec-118">EsentQuotaException class</span></span>](./esentquotaexception-class.md)

[<span data-ttu-id="2deec-119">Membres EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="2deec-119">EsentQuotaException members</span></span>](./esentquotaexception-members.md)

[<span data-ttu-id="2deec-120">Surcharge EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="2deec-120">EsentQuotaException overload</span></span>](./esentquotaexception-constructor.md)

[<span data-ttu-id="2deec-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2deec-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
