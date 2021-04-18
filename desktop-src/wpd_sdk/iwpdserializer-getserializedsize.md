---
description: La méthode GetSerializedSize calcule la taille de la mémoire tampon requise pour contenir une interface IPortableDeviceValues sérialisée.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'IWpdSerializer :: GetSerializedSize, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532723"
---
# <a name="iwpdserializergetserializedsize-method"></a><span data-ttu-id="35ae1-103">IWpdSerializer :: GetSerializedSize, méthode</span><span class="sxs-lookup"><span data-stu-id="35ae1-103">IWpdSerializer::GetSerializedSize method</span></span>

<span data-ttu-id="35ae1-104">La méthode **GetSerializedSize** calcule la taille de la mémoire tampon requise pour contenir une interface [**IPortableDeviceValues**](iportabledevicevalues.md) sérialisée.</span><span class="sxs-lookup"><span data-stu-id="35ae1-104">The **GetSerializedSize** method calculates the buffer size that is required to hold a serialized [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ae1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35ae1-105">Syntax</span></span>


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="35ae1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35ae1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ae1-107">*pSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35ae1-107">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ae1-108">Pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) dont vous souhaitez demander la taille.</span><span class="sxs-lookup"><span data-stu-id="35ae1-108">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface whose size you want to request.</span></span>

</dd> <dt>

<span data-ttu-id="35ae1-109">*pdwSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="35ae1-109">*pdwSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35ae1-110">Pointeur vers une **valeur DWORD** qui indique la taille de la mémoire tampon requise pour sérialiser *pSource*, en octets.</span><span class="sxs-lookup"><span data-stu-id="35ae1-110">Pointer to a **DWORD** that indicates the buffer size that is required to serialize *pSource*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ae1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35ae1-111">Return value</span></span>

<span data-ttu-id="35ae1-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="35ae1-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="35ae1-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="35ae1-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="35ae1-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="35ae1-114">Return code</span></span>                                                                                   | <span data-ttu-id="35ae1-115">Description</span><span class="sxs-lookup"><span data-stu-id="35ae1-115">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35ae1-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="35ae1-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="35ae1-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="35ae1-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="35ae1-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="35ae1-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="35ae1-119">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="35ae1-119">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="35ae1-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="35ae1-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="35ae1-121">La mémoire disponible est insuffisante pour créer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="35ae1-121">There was not enough available memory to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="35ae1-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35ae1-122">Requirements</span></span>



| <span data-ttu-id="35ae1-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35ae1-123">Requirement</span></span> | <span data-ttu-id="35ae1-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ae1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ae1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="35ae1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="35ae1-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ae1-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="35ae1-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35ae1-127">Library</span></span><br/> | <dl> <span data-ttu-id="35ae1-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35ae1-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ae1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35ae1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ae1-130">**Interface IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="35ae1-130">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




