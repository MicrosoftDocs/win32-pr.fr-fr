---
title: Méthode IDRMStatusCallback OnStatus
description: La méthode OnStatus reçoit les messages d’état des processus DRM asynchrones.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Méthode OnStatus format Windows Media
- Méthode OnStatus format Windows Media, interface IDRMStatusCallback
- Interface IDRMStatusCallback Windows Media format, méthode OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030096"
---
# <a name="idrmstatuscallbackonstatus-method"></a><span data-ttu-id="3985d-106">IDRMStatusCallback :: OnStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="3985d-106">IDRMStatusCallback::OnStatus method</span></span>

<span data-ttu-id="3985d-107">La méthode **OnStatus** reçoit les messages d’état des processus DRM asynchrones.</span><span class="sxs-lookup"><span data-stu-id="3985d-107">The **OnStatus** method receives status messages from asynchronous DRM processes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3985d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3985d-108">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a><span data-ttu-id="3985d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3985d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3985d-110">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3985d-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3985d-111">Code d’état.</span><span class="sxs-lookup"><span data-stu-id="3985d-111">Status code.</span></span> <span data-ttu-id="3985d-112">Les codes de message sont définis dans le type d’énumération d' **\_ État msdrm** .</span><span class="sxs-lookup"><span data-stu-id="3985d-112">Message codes are defined in the **MSDRM\_STATUS** enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="3985d-113">*RH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3985d-113">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3985d-114">Code de retour qui prend en charge le message d’État.</span><span class="sxs-lookup"><span data-stu-id="3985d-114">Return code that supports the status message.</span></span>

</dd> <dt>

<span data-ttu-id="3985d-115">*dwType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3985d-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3985d-116">Type des données vers lesquelles pointe *pValue*.</span><span class="sxs-lookup"><span data-stu-id="3985d-116">Type of the data pointed to by *pValue*.</span></span> <span data-ttu-id="3985d-117">Défini sur l’une des valeurs de l’énumération de [**\_ type de \_ données de l’attr DRM**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3985d-117">Set to one of the values of the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="3985d-118">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3985d-118">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3985d-119">Pointeur vers les données relatives au message d’État.</span><span class="sxs-lookup"><span data-stu-id="3985d-119">Pointer to data related to the status message.</span></span> <span data-ttu-id="3985d-120">Le type de données est déterminé par la valeur du paramètre *dwType* .</span><span class="sxs-lookup"><span data-stu-id="3985d-120">The type of data is determined by the value of the *dwType* parameter.</span></span> <span data-ttu-id="3985d-121">Pour plus d’informations, consultez l’énumération de [**\_ type de \_ données de l’attr DRM**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3985d-121">For more information, see the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="3985d-122">*pvContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3985d-122">*pvContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3985d-123">Paramètre facultatif qui peut être utilisé pour identifier l’objet qui a envoyé le message.</span><span class="sxs-lookup"><span data-stu-id="3985d-123">Optional parameter that can be used to identify the object that sent the message.</span></span> <span data-ttu-id="3985d-124">En définissant *pvContext* quand vous inscrivez ce rappel, vous pouvez utiliser le même rappel pour gérer plusieurs processus asynchrones.</span><span class="sxs-lookup"><span data-stu-id="3985d-124">By setting *pvContext* when you register this callback, you can use the same callback to handle multiple asynchronous processes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3985d-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3985d-125">Return value</span></span>

<span data-ttu-id="3985d-126">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3985d-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3985d-127">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3985d-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3985d-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3985d-128">Return code</span></span>                                                                          | <span data-ttu-id="3985d-129">Description</span><span class="sxs-lookup"><span data-stu-id="3985d-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3985d-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3985d-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3985d-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="3985d-131">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3985d-132">Notes</span><span class="sxs-lookup"><span data-stu-id="3985d-132">Remarks</span></span>

<span data-ttu-id="3985d-133">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3985d-133">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="3985d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3985d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3985d-135">**type de données de l' \_ attr DRM \_**</span><span class="sxs-lookup"><span data-stu-id="3985d-135">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)
</dt> <dt>

[<span data-ttu-id="3985d-136">**Interface IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="3985d-136">**IDRMStatusCallback Interface**</span></span>](idrmstatuscallback.md)
</dt> </dl>

 

 





