---
description: Ajoute un nouvel objet IInkStrokeDisp à l’objet InkDivider qui a été passé.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: AddOneStroke fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484000"
---
# <a name="addonestroke-function"></a><span data-ttu-id="df90a-103">AddOneStroke fonction)</span><span class="sxs-lookup"><span data-stu-id="df90a-103">AddOneStroke function</span></span>

<span data-ttu-id="df90a-104">Ajoute un nouvel objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) à l’objet [**InkDivider**](inkdivider-class.md) qui a été passé.</span><span class="sxs-lookup"><span data-stu-id="df90a-104">Adds a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to the [**InkDivider**](inkdivider-class.md) object that was passed in.</span></span>

<span data-ttu-id="df90a-105">Cette fonction n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="df90a-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="df90a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df90a-106">Syntax</span></span>


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a><span data-ttu-id="df90a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df90a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df90a-108">*hDivider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df90a-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df90a-109">Handle de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="df90a-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="df90a-110">*strokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df90a-110">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df90a-111">[**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) de l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) à ajouter à l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="df90a-111">The [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to be added to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="df90a-112">*cPoints* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df90a-112">*cPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df90a-113">Nombre de paquets qui composent le nouvel objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="df90a-113">The number of packets that make up the new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="df90a-114">*aPoints* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df90a-114">*aPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df90a-115">Tableau des paquets qui composent l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dans *strokeId*.</span><span class="sxs-lookup"><span data-stu-id="df90a-115">The array of packets that make up the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object in *strokeId*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df90a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df90a-116">Return value</span></span>

<span data-ttu-id="df90a-117">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="df90a-117">This function can return one of these values.</span></span>



| <span data-ttu-id="df90a-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="df90a-118">Return code</span></span>                                                                                  | <span data-ttu-id="df90a-119">Description</span><span class="sxs-lookup"><span data-stu-id="df90a-119">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="df90a-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df90a-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="df90a-121">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="df90a-121">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="df90a-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df90a-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="df90a-123">Le paramètre *hDivider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="df90a-123">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="df90a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df90a-124">Requirements</span></span>



| <span data-ttu-id="df90a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df90a-125">Requirement</span></span> | <span data-ttu-id="df90a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="df90a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df90a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df90a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="df90a-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df90a-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="df90a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df90a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="df90a-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="df90a-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="df90a-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df90a-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="df90a-132"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df90a-132"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




