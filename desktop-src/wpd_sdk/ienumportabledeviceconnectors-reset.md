---
description: 'IEnumPortableDeviceConnectors :: Reset, méthode-réinitialise la séquence d’énumération au début.'
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'IEnumPortableDeviceConnectors :: Reset, méthode (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083206"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="ac679-103">IEnumPortableDeviceConnectors :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="ac679-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="ac679-104">La méthode **Reset** réinitialise la séquence d’énumération au début.</span><span class="sxs-lookup"><span data-stu-id="ac679-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac679-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac679-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="ac679-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac679-106">Parameters</span></span>

<span data-ttu-id="ac679-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ac679-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac679-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ac679-108">Return value</span></span>

<span data-ttu-id="ac679-109">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ac679-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ac679-110">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ac679-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ac679-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ac679-111">Return code</span></span>                                                                          | <span data-ttu-id="ac679-112">Description</span><span class="sxs-lookup"><span data-stu-id="ac679-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ac679-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac679-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ac679-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac679-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac679-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac679-115">Requirements</span></span>



| <span data-ttu-id="ac679-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac679-116">Requirement</span></span> | <span data-ttu-id="ac679-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac679-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac679-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac679-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac679-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac679-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="ac679-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac679-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac679-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac679-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="ac679-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac679-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac679-123"><dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac679-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="ac679-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="ac679-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac679-125"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac679-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="ac679-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ac679-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac679-127"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac679-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="ac679-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac679-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac679-129">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="ac679-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




