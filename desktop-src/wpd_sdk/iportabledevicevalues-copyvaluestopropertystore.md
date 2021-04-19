---
description: La méthode CopyValuesToPropertyStore copie toutes les valeurs d’une collection dans une interface IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'IPortableDeviceValues :: CopyValuesToPropertyStore, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537592"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a><span data-ttu-id="29377-103">IPortableDeviceValues :: CopyValuesToPropertyStore, méthode</span><span class="sxs-lookup"><span data-stu-id="29377-103">IPortableDeviceValues::CopyValuesToPropertyStore method</span></span>

<span data-ttu-id="29377-104">La méthode **CopyValuesToPropertyStore** copie toutes les valeurs d’une collection dans une interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="29377-104">The **CopyValuesToPropertyStore** method copies all the values from a collection into an **IPropertyStore** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="29377-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29377-105">Syntax</span></span>


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="29377-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29377-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29377-107">*pStore* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29377-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29377-108">Pointeur vers un objet de magasin.</span><span class="sxs-lookup"><span data-stu-id="29377-108">Pointer to a store object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29377-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29377-109">Return value</span></span>

<span data-ttu-id="29377-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="29377-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="29377-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="29377-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="29377-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="29377-112">Return code</span></span>                                                                          | <span data-ttu-id="29377-113">Description</span><span class="sxs-lookup"><span data-stu-id="29377-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="29377-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="29377-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="29377-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="29377-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29377-116">Notes</span><span class="sxs-lookup"><span data-stu-id="29377-116">Remarks</span></span>

<span data-ttu-id="29377-117">Cette méthode ne convertit pas les valeurs de VT \_ LPWStr en VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="29377-117">This method does not convert values of VT\_LPWSTR into VT\_BSTR.</span></span> <span data-ttu-id="29377-118">De nombreuses applications ou composants externes qui communiquent avec votre application, tels que certaines applications de l’interpréteur de commandes, utilisent l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="29377-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="29377-119">Cette méthode offre un moyen simple et rapide d’échanger des données avec ces programmes.</span><span class="sxs-lookup"><span data-stu-id="29377-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="29377-120">Cette méthode est prise en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="29377-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="29377-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29377-121">Requirements</span></span>



| <span data-ttu-id="29377-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29377-122">Requirement</span></span> | <span data-ttu-id="29377-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="29377-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29377-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="29377-124">Header</span></span><br/>  | <dl> <span data-ttu-id="29377-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="29377-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="29377-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="29377-126">Library</span></span><br/> | <dl> <span data-ttu-id="29377-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29377-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29377-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29377-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29377-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="29377-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="29377-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="29377-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span></span>](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




