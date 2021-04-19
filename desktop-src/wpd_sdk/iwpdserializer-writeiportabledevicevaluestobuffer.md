---
description: La méthode WriteIPortableDeviceValuesToBuffer sérialise une interface IPortableDeviceValues dans un tableau d’octets alloué par l’appelant.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'IWpdSerializer :: WriteIPortableDeviceValuesToBuffer, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528362"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a><span data-ttu-id="ea6ad-103">IWpdSerializer :: WriteIPortableDeviceValuesToBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="ea6ad-103">IWpdSerializer::WriteIPortableDeviceValuesToBuffer method</span></span>

<span data-ttu-id="ea6ad-104">La méthode **WriteIPortableDeviceValuesToBuffer** sérialise une interface **IPortableDeviceValues** dans un tableau d’octets alloué par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-104">The **WriteIPortableDeviceValuesToBuffer** method serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea6ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea6ad-105">Syntax</span></span>


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a><span data-ttu-id="ea6ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea6ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea6ad-107">*dwOutputBufferLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea6ad-107">*dwOutputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea6ad-108">**Valeur DWORD** qui spécifie la taille de *pbuffer*, en octets.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-108">**DWORD** that specifies the size of *pBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ea6ad-109">*pResults* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea6ad-109">*pResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea6ad-110">Pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) à sérialiser.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="ea6ad-111">*pbuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ea6ad-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea6ad-112">Pointeur vers une mémoire tampon allouée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-112">Pointer to a caller-allocated buffer.</span></span> <span data-ttu-id="ea6ad-113">Pour connaître la taille de la mémoire tampon requise, appelez **GetSerializedSize**.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-113">To learn the size of the required buffer, call **GetSerializedSize**.</span></span>

</dd> <dt>

<span data-ttu-id="ea6ad-114">*pdwBytesWritten* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ea6ad-114">*pdwBytesWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea6ad-115">Pointeur vers une **valeur DWORD** qui indique le nombre d’octets réellement écrits dans la mémoire tampon allouée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-115">Pointer to a **DWORD** that indicates the number of bytes that was actually written to the caller-allocated buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea6ad-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea6ad-116">Return value</span></span>

<span data-ttu-id="ea6ad-117">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ea6ad-118">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ea6ad-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ea6ad-119">Return code</span></span>                                                                                   | <span data-ttu-id="ea6ad-120">Description</span><span class="sxs-lookup"><span data-stu-id="ea6ad-120">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="ea6ad-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea6ad-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ea6ad-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea6ad-122">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="ea6ad-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea6ad-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ea6ad-124">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-124">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="ea6ad-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea6ad-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ea6ad-126">La mémoire tampon fournie par l’appelant n’est pas assez grande.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-126">The caller-provided buffer was not big enough.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea6ad-127">Notes</span><span class="sxs-lookup"><span data-stu-id="ea6ad-127">Remarks</span></span>

<span data-ttu-id="ea6ad-128">Cette méthode copie une interface **IPortableDeviceValues** dans une mémoire tampon existante.</span><span class="sxs-lookup"><span data-stu-id="ea6ad-128">This method copies an **IPortableDeviceValues** interface into an existing buffer.</span></span> <span data-ttu-id="ea6ad-129">Si vous souhaitez allouer une nouvelle mémoire tampon, utilisez [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="ea6ad-129">If you want to allocate a new buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea6ad-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea6ad-130">Requirements</span></span>



| <span data-ttu-id="ea6ad-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea6ad-131">Requirement</span></span> | <span data-ttu-id="ea6ad-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea6ad-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6ad-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea6ad-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ea6ad-134"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea6ad-134"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea6ad-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea6ad-135">Library</span></span><br/> | <dl> <span data-ttu-id="ea6ad-136"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea6ad-136"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea6ad-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea6ad-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6ad-138">**Interface IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="ea6ad-138">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




