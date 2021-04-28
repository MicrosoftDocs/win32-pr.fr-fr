---
description: Méthode constructeur CPosPassThru. CPosPassThru.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Constructeur CPosPassThru. CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085597"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="ca894-103">Constructeur CPosPassThru. CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="ca894-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="ca894-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ca894-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca894-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca894-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="ca894-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca894-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca894-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ca894-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ca894-108">Pointeur vers le nom de l’objet, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="ca894-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="ca894-109">Allouez ce paramètre dans la mémoire statique.</span><span class="sxs-lookup"><span data-stu-id="ca894-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="ca894-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ca894-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ca894-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="ca894-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="ca894-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="ca894-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ca894-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ca894-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ca894-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="ca894-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ca894-115">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca894-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ca894-116">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="ca894-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="ca894-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="ca894-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="ca894-118">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche d’entrée du filtre.</span><span class="sxs-lookup"><span data-stu-id="ca894-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



