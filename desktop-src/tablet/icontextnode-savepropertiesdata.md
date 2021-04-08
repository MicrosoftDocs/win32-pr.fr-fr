---
description: Récupère un tableau d’octets qui contient les données de propriété internes et spécifiques à l’application pour ce IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'IContextNode :: SavePropertiesData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951222"
---
# <a name="icontextnodesavepropertiesdata-method"></a><span data-ttu-id="affda-103">IContextNode :: SavePropertiesData, méthode</span><span class="sxs-lookup"><span data-stu-id="affda-103">IContextNode::SavePropertiesData method</span></span>

<span data-ttu-id="affda-104">Récupère un tableau d’octets qui contient les données de propriété internes et spécifiques à l’application pour ce [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="affda-104">Retrieves an array of bytes that contains the application-specific and internal property data for this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="affda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="affda-105">Syntax</span></span>


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="affda-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="affda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="affda-107">*pulPropertiesDataSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="affda-107">*pulPropertiesDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="affda-108">Taille du tableau de données contenant les informations de propriété.</span><span class="sxs-lookup"><span data-stu-id="affda-108">The size of the data array containing the property information.</span></span> <span data-ttu-id="affda-109">La valeur passée n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="affda-109">The value passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="affda-110">*ppbPropertiesData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="affda-110">*ppbPropertiesData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="affda-111">Pointeur vers un tableau d’entiers non signés 8 bits qui contient les données de propriété internes et spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="affda-111">A pointer to an 8-bit unsigned integer array that contains the application-specific and internal property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="affda-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="affda-112">Return value</span></span>

<span data-ttu-id="affda-113">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="affda-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="affda-114">Notes</span><span class="sxs-lookup"><span data-stu-id="affda-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="affda-115">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppbPropertiesData* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="affda-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertiesData* when you no longer need the information.</span></span>

 

<span data-ttu-id="affda-116">Utilisez cette méthode lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="affda-116">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="affda-117">Cette méthode enregistre les données de propriétés définies par **IInkAnalyzer** sur [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="affda-117">This method saves the property data that the **IInkAnalyzer** has set on the [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="affda-118">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="affda-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="affda-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="affda-119">Requirements</span></span>



| <span data-ttu-id="affda-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="affda-120">Requirement</span></span> | <span data-ttu-id="affda-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="affda-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="affda-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="affda-122">Minimum supported client</span></span><br/> | <span data-ttu-id="affda-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="affda-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="affda-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="affda-124">Minimum supported server</span></span><br/> | <span data-ttu-id="affda-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="affda-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="affda-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="affda-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="affda-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="affda-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="affda-128">DLL</span><span class="sxs-lookup"><span data-stu-id="affda-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="affda-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="affda-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="affda-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="affda-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="affda-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="affda-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="affda-132">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="affda-132">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="affda-133">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="affda-133">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="affda-134">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="affda-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="affda-135">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="affda-135">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="affda-136">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="affda-136">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="affda-137">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="affda-137">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="affda-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="affda-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

