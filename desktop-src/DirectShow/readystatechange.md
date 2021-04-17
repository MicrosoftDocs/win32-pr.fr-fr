---
description: L’événement ReadyStateChange est envoyé lorsque la propriété ReadyState du contrôle MSWebDVD a été modifiée.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522047"
---
# <a name="readystatechange"></a><span data-ttu-id="14a8a-103">ReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="14a8a-103">ReadyStateChange</span></span>

> [!Note]  
> <span data-ttu-id="14a8a-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="14a8a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="14a8a-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="14a8a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="14a8a-106">L' `ReadyStateChange` événement est envoyé lorsque la propriété **ReadyState** du contrôle mswebdvd a changé.</span><span class="sxs-lookup"><span data-stu-id="14a8a-106">The `ReadyStateChange` event is sent when the **ReadyState** property of the MSWebDVD control has changed.</span></span>

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a><span data-ttu-id="14a8a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14a8a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a8a-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*DataControl*</span><span class="sxs-lookup"><span data-stu-id="14a8a-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span></span>
</dt> <dd>

<span data-ttu-id="14a8a-109">Spécifie la nouvelle valeur de la propriété [**ReadyState**](readystate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="14a8a-109">Specifies the new value of the [**ReadyState**](readystate-property.md) property.</span></span>



| <span data-ttu-id="14a8a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="14a8a-110">Value</span></span> | <span data-ttu-id="14a8a-111">Description</span><span class="sxs-lookup"><span data-stu-id="14a8a-111">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="14a8a-112">0</span><span class="sxs-lookup"><span data-stu-id="14a8a-112">0</span></span>     | <span data-ttu-id="14a8a-113">READYSTATE \_ non initialisé</span><span class="sxs-lookup"><span data-stu-id="14a8a-113">READYSTATE\_UNINITIALIZED</span></span> |
| <span data-ttu-id="14a8a-114">1</span><span class="sxs-lookup"><span data-stu-id="14a8a-114">1</span></span>     | <span data-ttu-id="14a8a-115">chargement de READYSTATE \_</span><span class="sxs-lookup"><span data-stu-id="14a8a-115">READYSTATE\_LOADING</span></span>       |
| <span data-ttu-id="14a8a-116">2</span><span class="sxs-lookup"><span data-stu-id="14a8a-116">2</span></span>     | <span data-ttu-id="14a8a-117">READYSTATE \_ chargé</span><span class="sxs-lookup"><span data-stu-id="14a8a-117">READYSTATE\_LOADED</span></span>        |
| <span data-ttu-id="14a8a-118">3</span><span class="sxs-lookup"><span data-stu-id="14a8a-118">3</span></span>     | <span data-ttu-id="14a8a-119">\_interactive ReadyState</span><span class="sxs-lookup"><span data-stu-id="14a8a-119">READYSTATE\_INTERACTIVE</span></span>   |
| <span data-ttu-id="14a8a-120">4</span><span class="sxs-lookup"><span data-stu-id="14a8a-120">4</span></span>     | <span data-ttu-id="14a8a-121">READYSTATE \_ terminé</span><span class="sxs-lookup"><span data-stu-id="14a8a-121">READYSTATE\_COMPLETE</span></span>      |



 

</dd> </dl>

 

 



