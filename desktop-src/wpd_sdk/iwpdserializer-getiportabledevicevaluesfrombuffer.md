---
description: La méthode GetIPortableDeviceValuesFromBuffer désérialise un tableau d’octets en une interface IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'IWpdSerializer :: GetIPortableDeviceValuesFromBuffer, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523026"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a><span data-ttu-id="deefa-103">IWpdSerializer :: GetIPortableDeviceValuesFromBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="deefa-103">IWpdSerializer::GetIPortableDeviceValuesFromBuffer method</span></span>

<span data-ttu-id="deefa-104">La méthode **GetIPortableDeviceValuesFromBuffer** désérialise un tableau d’octets en une interface **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="deefa-104">The **GetIPortableDeviceValuesFromBuffer** method deserializes a byte array to an **IPortableDeviceValues** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="deefa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="deefa-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a><span data-ttu-id="deefa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="deefa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deefa-107">*pbuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="deefa-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefa-108">Pointeur vers la mémoire tampon à désérialiser.</span><span class="sxs-lookup"><span data-stu-id="deefa-108">Pointer to the buffer to deserialize.</span></span>

</dd> <dt>

<span data-ttu-id="deefa-109">*dwInputBufferLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="deefa-109">*dwInputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefa-110">**Valeur DWORD** qui spécifie la taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="deefa-110">**DWORD** that specifies the size of the buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="deefa-111">*ppParams* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="deefa-111">*ppParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deefa-112">Adresse d’une variable qui reçoit un pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) créée à partir de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="deefa-112">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface created from the buffer.</span></span> <span data-ttu-id="deefa-113">L’application est chargée d’appeler la **version Release** sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="deefa-113">The application is responsible for calling **Release** on the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deefa-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="deefa-114">Return value</span></span>

<span data-ttu-id="deefa-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="deefa-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="deefa-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="deefa-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="deefa-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="deefa-117">Return code</span></span>                                                                                  | <span data-ttu-id="deefa-118">Description</span><span class="sxs-lookup"><span data-stu-id="deefa-118">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="deefa-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="deefa-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="deefa-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="deefa-120">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="deefa-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="deefa-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="deefa-122">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="deefa-122">A required pointer argument was **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="deefa-123"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="deefa-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="deefa-124">Une erreur de conversion non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="deefa-124">An unspecified conversion error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="deefa-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="deefa-125">Requirements</span></span>



| <span data-ttu-id="deefa-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="deefa-126">Requirement</span></span> | <span data-ttu-id="deefa-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="deefa-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deefa-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="deefa-128">Header</span></span><br/>  | <dl> <span data-ttu-id="deefa-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="deefa-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="deefa-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="deefa-130">Library</span></span><br/> | <dl> <span data-ttu-id="deefa-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deefa-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deefa-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="deefa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deefa-133">**Interface IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="deefa-133">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




