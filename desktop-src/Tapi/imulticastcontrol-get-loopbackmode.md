---
description: La \_ méthode obtenir LoopbackMode obtient le mode de bouclage de multidiffusion.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'IMulticastControl :: get_LoopbackMode, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525228"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a><span data-ttu-id="05171-103">IMulticastControl :: \_ LoopbackMode, méthode</span><span class="sxs-lookup"><span data-stu-id="05171-103">IMulticastControl::get\_LoopbackMode method</span></span>

<span data-ttu-id="05171-104">\[en **savoir \_ plus LoopbackMode** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="05171-104">\[**get\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="05171-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="05171-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="05171-106">La méthode **obtenir \_ LoopbackMode** obtient le mode de bouclage de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="05171-106">The **get\_LoopbackMode** method gets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="05171-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05171-107">Syntax</span></span>


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a><span data-ttu-id="05171-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05171-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05171-109">*PMODE* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05171-109">*pMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05171-110">Pointeur vers le descripteur de [**\_ \_ mode de bouclage multicast**](multicast-loopback-mode.md) du mode de bouclage actuel.</span><span class="sxs-lookup"><span data-stu-id="05171-110">Pointer to the [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the current loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05171-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05171-111">Return value</span></span>

<span data-ttu-id="05171-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="05171-112">This method can return one of these values.</span></span>



| <span data-ttu-id="05171-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="05171-113">Value</span></span>                                                                                        | <span data-ttu-id="05171-114">Signification</span><span class="sxs-lookup"><span data-stu-id="05171-114">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="05171-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05171-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="05171-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="05171-116">Method succeeded.</span></span><br/>                   |
| <dl> <span data-ttu-id="05171-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="05171-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="05171-118">Le paramètre *PMODE* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="05171-118">The *pMode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05171-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05171-119">Requirements</span></span>



| <span data-ttu-id="05171-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05171-120">Requirement</span></span> | <span data-ttu-id="05171-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="05171-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05171-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="05171-122">TAPI version</span></span><br/> | <span data-ttu-id="05171-123">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05171-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="05171-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="05171-124">Header</span></span><br/>       | <dl> <span data-ttu-id="05171-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="05171-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="05171-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05171-126">Library</span></span><br/>      | <dl> <span data-ttu-id="05171-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05171-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="05171-128">DLL</span><span class="sxs-lookup"><span data-stu-id="05171-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="05171-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05171-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="05171-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05171-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05171-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="05171-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




