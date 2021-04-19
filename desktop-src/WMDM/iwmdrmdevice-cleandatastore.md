---
title: Méthode IWMDRMDevice CleanDataStore
description: La méthode CleanDataStore démarre le processus de nettoyage de la Banque de données DRM sur l’appareil.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Méthode CleanDataStore Gestionnaire de périphériques Windows Media
- Méthode CleanDataStore Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode CleanDataStore
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5aed9608a7428245edd84602ea5e7252861d938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540969"
---
# <a name="iwmdrmdevicecleandatastore-method"></a><span data-ttu-id="20bc8-106">IWMDRMDevice :: CleanDataStore, méthode</span><span class="sxs-lookup"><span data-stu-id="20bc8-106">IWMDRMDevice::CleanDataStore method</span></span>

<span data-ttu-id="20bc8-107">La méthode **CleanDataStore** démarre le processus de nettoyage de la Banque de données DRM sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20bc8-107">The **CleanDataStore** method starts the process of cleaning the DRM data store on the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="20bc8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20bc8-108">Syntax</span></span>


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="20bc8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20bc8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20bc8-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20bc8-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bc8-111">Indicateurs pour les critères de nettoyage des magasins.</span><span class="sxs-lookup"><span data-stu-id="20bc8-111">Flags for store cleaning criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20bc8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20bc8-112">Return value</span></span>

<span data-ttu-id="20bc8-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="20bc8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="20bc8-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="20bc8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="20bc8-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="20bc8-115">Return code</span></span>                                                                          | <span data-ttu-id="20bc8-116">Description</span><span class="sxs-lookup"><span data-stu-id="20bc8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="20bc8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20bc8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="20bc8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="20bc8-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="20bc8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20bc8-119">Requirements</span></span>



| <span data-ttu-id="20bc8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20bc8-120">Requirement</span></span> | <span data-ttu-id="20bc8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="20bc8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20bc8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="20bc8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="20bc8-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20bc8-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="20bc8-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20bc8-124">Library</span></span><br/> | <dl> <span data-ttu-id="20bc8-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20bc8-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bc8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20bc8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bc8-127">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="20bc8-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





