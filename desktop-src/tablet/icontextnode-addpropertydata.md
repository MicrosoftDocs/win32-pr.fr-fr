---
description: Ajoute un élément de données spécifiques à l’application.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'IContextNode :: AddPropertyData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113391"
---
# <a name="icontextnodeaddpropertydata-method"></a><span data-ttu-id="72251-103">IContextNode :: AddPropertyData, méthode</span><span class="sxs-lookup"><span data-stu-id="72251-103">IContextNode::AddPropertyData method</span></span>

<span data-ttu-id="72251-104">Ajoute un élément de données spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="72251-104">Adds a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="72251-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72251-105">Syntax</span></span>


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="72251-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72251-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72251-107">*pPropertyDataId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72251-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72251-108">Identificateur global unique (GUID) utilisé pour identifier le type de données.</span><span class="sxs-lookup"><span data-stu-id="72251-108">A globally unique identifier (GUID) that is used to identify the type of data.</span></span>

</dd> <dt>

<span data-ttu-id="72251-109">*ulPropertyDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72251-109">*ulPropertyDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72251-110">Taille des données en octets.</span><span class="sxs-lookup"><span data-stu-id="72251-110">The size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="72251-111">*pbPropertiesData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72251-111">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72251-112">\[dans, la taille \_ est (ulPropertyDataSize)\]</span><span class="sxs-lookup"><span data-stu-id="72251-112">\[in, size\_is(ulPropertyDataSize)\]</span></span>

<span data-ttu-id="72251-113">Tableau d’entiers non signés 8 bits contenant les informations de propriété à ajouter.</span><span class="sxs-lookup"><span data-stu-id="72251-113">An 8-bit unsigned integer array containing the property information to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72251-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72251-114">Return value</span></span>

<span data-ttu-id="72251-115">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="72251-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="72251-116">Notes</span><span class="sxs-lookup"><span data-stu-id="72251-116">Remarks</span></span>

<span data-ttu-id="72251-117">Utilisez **IContextNode :: AddPropertyData** pour associer des données à un nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="72251-117">Use **IContextNode::AddPropertyData** to associate data with a context node.</span></span> <span data-ttu-id="72251-118">Pour récupérer les données ultérieurement, utilisez [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="72251-118">To retrieve the data later, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

<span data-ttu-id="72251-119">L’analyseur d’encre peut supprimer le nœud dans le cadre de l’analyse de l’encre, sauf si le nœud de contexte est confirmé (consultez [**IContextNode :: Confirm**](icontextnode-confirm.md)).</span><span class="sxs-lookup"><span data-stu-id="72251-119">The ink analyzer may delete the node as part of ink analysis, unless the context node is confirmed (see [**IContextNode::Confirm**](icontextnode-confirm.md)).</span></span> <span data-ttu-id="72251-120">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="72251-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72251-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72251-121">Requirements</span></span>



| <span data-ttu-id="72251-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72251-122">Requirement</span></span> | <span data-ttu-id="72251-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="72251-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72251-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72251-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72251-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72251-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="72251-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72251-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72251-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="72251-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="72251-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="72251-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="72251-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="72251-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="72251-130">DLL</span><span class="sxs-lookup"><span data-stu-id="72251-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72251-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72251-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="72251-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72251-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72251-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="72251-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="72251-134">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="72251-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="72251-135">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="72251-135">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="72251-136">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="72251-136">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="72251-137">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="72251-137">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="72251-138">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="72251-138">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="72251-139">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="72251-139">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




