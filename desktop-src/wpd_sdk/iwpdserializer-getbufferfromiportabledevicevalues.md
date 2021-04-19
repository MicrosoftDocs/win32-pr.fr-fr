---
description: La méthode GetBufferFromIPortableDeviceValues sérialise une interface IPortableDeviceValues soumise à un tableau d’octets alloué. Le tableau d’octets retourné est alloué pour l’appelant et doit être libéré par l’appelant à l’aide de CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'IWpdSerializer :: GetBufferFromIPortableDeviceValues, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530375"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a><span data-ttu-id="094b3-104">IWpdSerializer :: GetBufferFromIPortableDeviceValues, méthode</span><span class="sxs-lookup"><span data-stu-id="094b3-104">IWpdSerializer::GetBufferFromIPortableDeviceValues method</span></span>

<span data-ttu-id="094b3-105">La méthode **GetBufferFromIPortableDeviceValues** sérialise une interface **IPortableDeviceValues** soumise à un tableau d’octets alloué.</span><span class="sxs-lookup"><span data-stu-id="094b3-105">The **GetBufferFromIPortableDeviceValues** method serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span> <span data-ttu-id="094b3-106">Le tableau d’octets retourné est alloué pour l’appelant et doit être libéré par l’appelant à l’aide de **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="094b3-106">The byte array returned is allocated for the caller and should be freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="syntax"></a><span data-ttu-id="094b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="094b3-107">Syntax</span></span>


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="094b3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="094b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="094b3-109">*pSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="094b3-109">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="094b3-110">Pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) à sérialiser.</span><span class="sxs-lookup"><span data-stu-id="094b3-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="094b3-111">*ppBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="094b3-111">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="094b3-112">Pointeur vers un **octet \* *_ qui contient les données sérialisées. Les appareils mobiles Windows allouent cette mémoire ; l’appelant doit le libérer en appelant _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="094b3-112">Pointer to a \**BYTE\**_ that contains the serialized data. Windows Portable Devices allocates this memory; the caller must free it by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="094b3-113">*pdwBufferSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="094b3-113">*pdwBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="094b3-114">Pointeur vers une **valeur DWORD** qui spécifie la taille de la mémoire tampon allouée, en octets.</span><span class="sxs-lookup"><span data-stu-id="094b3-114">Pointer to a **DWORD** that specifies the size of allocated buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="094b3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="094b3-115">Return value</span></span>

<span data-ttu-id="094b3-116">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="094b3-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="094b3-117">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="094b3-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="094b3-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="094b3-118">Return code</span></span>                                                                                   | <span data-ttu-id="094b3-119">Description</span><span class="sxs-lookup"><span data-stu-id="094b3-119">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="094b3-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="094b3-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="094b3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="094b3-121">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="094b3-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="094b3-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="094b3-123">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="094b3-123">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="094b3-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="094b3-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="094b3-125">Mémoire disponible insuffisante pour créer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="094b3-125">There was not enough memory available to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="094b3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="094b3-126">Requirements</span></span>



| <span data-ttu-id="094b3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="094b3-127">Requirement</span></span> | <span data-ttu-id="094b3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="094b3-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="094b3-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="094b3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="094b3-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="094b3-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="094b3-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="094b3-131">Library</span></span><br/> | <dl> <span data-ttu-id="094b3-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="094b3-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="094b3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="094b3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094b3-134">**Interface IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="094b3-134">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




