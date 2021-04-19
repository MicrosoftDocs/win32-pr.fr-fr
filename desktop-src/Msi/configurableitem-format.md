---
description: La propriété format de l’objet ConfigurableItem retourne la valeur de la colonne format de la table ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: ConfigurableItem. format, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542588"
---
# <a name="configurableitemformat-property"></a><span data-ttu-id="7abfb-103">ConfigurableItem. format, propriété</span><span class="sxs-lookup"><span data-stu-id="7abfb-103">ConfigurableItem.Format property</span></span>

<span data-ttu-id="7abfb-104">La propriété **format** de l’objet [**ConfigurableItem**](configurableitem-object.md) retourne la valeur de la colonne format de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7abfb-104">The **Format** property of the [**ConfigurableItem**](configurableitem-object.md) object returns the value from the Format column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7abfb-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7abfb-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abfb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7abfb-106">Syntax</span></span>


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a><span data-ttu-id="7abfb-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7abfb-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7abfb-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7abfb-108">Remarks</span></span>

<span data-ttu-id="7abfb-109">Cette propriété ne peut avoir que les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7abfb-109">This property can only have the following values.</span></span>



| <span data-ttu-id="7abfb-110">Constante</span><span class="sxs-lookup"><span data-stu-id="7abfb-110">Constant</span></span>                        | <span data-ttu-id="7abfb-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="7abfb-111">Value</span></span> |
|---------------------------------|-------|
| <span data-ttu-id="7abfb-112">**msmConfigurableItemText**</span><span class="sxs-lookup"><span data-stu-id="7abfb-112">**msmConfigurableItemText**</span></span>     | <span data-ttu-id="7abfb-113">0</span><span class="sxs-lookup"><span data-stu-id="7abfb-113">0</span></span>     |
| <span data-ttu-id="7abfb-114">**msmConfigurableItemKey**</span><span class="sxs-lookup"><span data-stu-id="7abfb-114">**msmConfigurableItemKey**</span></span>      | <span data-ttu-id="7abfb-115">1</span><span class="sxs-lookup"><span data-stu-id="7abfb-115">1</span></span>     |
| <span data-ttu-id="7abfb-116">**msmConfigurableItemInteger**</span><span class="sxs-lookup"><span data-stu-id="7abfb-116">**msmConfigurableItemInteger**</span></span>  | <span data-ttu-id="7abfb-117">2</span><span class="sxs-lookup"><span data-stu-id="7abfb-117">2</span></span>     |
| <span data-ttu-id="7abfb-118">**msmConfigurableItemBitfield**</span><span class="sxs-lookup"><span data-stu-id="7abfb-118">**msmConfigurableItemBitfield**</span></span> | <span data-ttu-id="7abfb-119">3</span><span class="sxs-lookup"><span data-stu-id="7abfb-119">3</span></span>     |



 

### <a name="c"></a><span data-ttu-id="7abfb-120">C++</span><span class="sxs-lookup"><span data-stu-id="7abfb-120">C++</span></span>

<span data-ttu-id="7abfb-121">Consultez [**obtenir le \_ format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) , fonction.</span><span class="sxs-lookup"><span data-stu-id="7abfb-121">See [**get\_Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7abfb-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7abfb-122">Requirements</span></span>



| <span data-ttu-id="7abfb-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7abfb-123">Requirement</span></span> | <span data-ttu-id="7abfb-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7abfb-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7abfb-125">Version</span><span class="sxs-lookup"><span data-stu-id="7abfb-125">Version</span></span><br/> | <span data-ttu-id="7abfb-126">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7abfb-126">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="7abfb-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="7abfb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7abfb-128"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="7abfb-128"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="7abfb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7abfb-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="7abfb-130"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7abfb-130"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




