---
description: Crée une copie de l’interface IEnumPortableDeviceConnectors actuelle.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'IEnumPortableDeviceConnectors :: Clone, méthode (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320402"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a><span data-ttu-id="06147-103">IEnumPortableDeviceConnectors :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="06147-103">IEnumPortableDeviceConnectors::Clone method</span></span>

<span data-ttu-id="06147-104">La méthode **clone** crée une copie de l’interface [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) actuelle.</span><span class="sxs-lookup"><span data-stu-id="06147-104">The **Clone** method creates a copy of the current [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="06147-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06147-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="06147-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06147-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06147-107">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="06147-107">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06147-108">Adresse d’un pointeur vers une interface [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) .</span><span class="sxs-lookup"><span data-stu-id="06147-108">The address of a pointer to an [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span> <span data-ttu-id="06147-109">L’application appelante doit libérer cette interface quand elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="06147-109">The calling application must release this interface when it is done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06147-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06147-110">Return value</span></span>

<span data-ttu-id="06147-111">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="06147-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="06147-112">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="06147-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="06147-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="06147-113">Return code</span></span>                                                                          | <span data-ttu-id="06147-114">Description</span><span class="sxs-lookup"><span data-stu-id="06147-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="06147-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="06147-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="06147-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="06147-116">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="06147-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06147-117">Requirements</span></span>



| <span data-ttu-id="06147-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06147-118">Requirement</span></span> | <span data-ttu-id="06147-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="06147-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06147-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06147-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06147-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06147-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="06147-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06147-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06147-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="06147-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="06147-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="06147-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="06147-125"><dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06147-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="06147-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="06147-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06147-127"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06147-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="06147-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06147-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="06147-129"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06147-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="06147-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06147-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06147-131">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="06147-131">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




