---
description: La méthode CopyValuesFromPropertyStore copie le contenu d’un IPropertyStore dans la collection.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'IPortableDeviceValues :: CopyValuesFromPropertyStore, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533154"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a><span data-ttu-id="074f7-103">IPortableDeviceValues :: CopyValuesFromPropertyStore, méthode</span><span class="sxs-lookup"><span data-stu-id="074f7-103">IPortableDeviceValues::CopyValuesFromPropertyStore method</span></span>

<span data-ttu-id="074f7-104">La méthode **CopyValuesFromPropertyStore** copie le contenu d’un **IPropertyStore** dans la collection.</span><span class="sxs-lookup"><span data-stu-id="074f7-104">The **CopyValuesFromPropertyStore** method copies the contents of an **IPropertyStore** into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="074f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="074f7-105">Syntax</span></span>


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="074f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="074f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074f7-107">*pStore* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="074f7-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="074f7-108">Pointeur vers un **IPropertyStore** à copier dans la collection.</span><span class="sxs-lookup"><span data-stu-id="074f7-108">Pointer to an **IPropertyStore** to copy into the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074f7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="074f7-109">Return value</span></span>

<span data-ttu-id="074f7-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="074f7-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="074f7-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="074f7-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="074f7-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="074f7-112">Return code</span></span>                                                                          | <span data-ttu-id="074f7-113">Description</span><span class="sxs-lookup"><span data-stu-id="074f7-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="074f7-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="074f7-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="074f7-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="074f7-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="074f7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="074f7-116">Remarks</span></span>

<span data-ttu-id="074f7-117">Cette méthode convertit automatiquement toutes les valeurs **VT \_ BSTR** en valeurs **VT \_ LPWStr** .</span><span class="sxs-lookup"><span data-stu-id="074f7-117">This method automatically converts all **VT\_BSTR** values to **VT\_LPWSTR** values.</span></span>

<span data-ttu-id="074f7-118">De nombreuses applications ou composants externes qui communiquent avec votre application, tels que certaines applications de l’interpréteur de commandes, utilisent l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="074f7-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="074f7-119">Cette méthode offre un moyen simple et rapide d’échanger des données avec ces programmes.</span><span class="sxs-lookup"><span data-stu-id="074f7-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="074f7-120">Cette méthode est prise en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="074f7-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="074f7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="074f7-121">Requirements</span></span>



| <span data-ttu-id="074f7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="074f7-122">Requirement</span></span> | <span data-ttu-id="074f7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="074f7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="074f7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="074f7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="074f7-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="074f7-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="074f7-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="074f7-126">Library</span></span><br/> | <dl> <span data-ttu-id="074f7-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="074f7-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="074f7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="074f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074f7-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="074f7-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="074f7-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="074f7-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span></span>](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




