---
description: Le \_ LoopbackMode put définit le mode de bouclage de multidiffusion.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: IMulticastControl ::p ut_LoopbackMode, méthode (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540019"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a><span data-ttu-id="9e810-103">IMulticastControl ::p ut \_ LoopbackMode, méthode</span><span class="sxs-lookup"><span data-stu-id="9e810-103">IMulticastControl::put\_LoopbackMode method</span></span>

<span data-ttu-id="9e810-104">\[**mettre \_ LoopbackMode** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e810-104">\[**put\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9e810-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="9e810-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9e810-106">Le **\_ LoopbackMode put** définit le mode de bouclage de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="9e810-106">The **put\_LoopbackMode** sets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e810-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e810-107">Syntax</span></span>


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a><span data-ttu-id="9e810-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e810-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e810-109">*mode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e810-109">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e810-110">[**Multidiffusion \_ \_**](multicast-loopback-mode.md) Descripteur de mode de bouclage du nouveau mode de bouclage.</span><span class="sxs-lookup"><span data-stu-id="9e810-110">[**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the new loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e810-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e810-111">Return value</span></span>

<span data-ttu-id="9e810-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="9e810-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9e810-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9e810-113">Return code</span></span>                                                                                  | <span data-ttu-id="9e810-114">Description</span><span class="sxs-lookup"><span data-stu-id="9e810-114">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9e810-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e810-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9e810-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="9e810-116">Method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="9e810-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9e810-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9e810-118">Le paramètre de *mode* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9e810-118">The *mode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9e810-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e810-119">Requirements</span></span>



| <span data-ttu-id="9e810-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e810-120">Requirement</span></span> | <span data-ttu-id="9e810-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e810-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e810-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="9e810-122">TAPI version</span></span><br/> | <span data-ttu-id="9e810-123">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9e810-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9e810-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e810-124">Header</span></span><br/>       | <dl> <span data-ttu-id="9e810-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e810-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="9e810-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e810-126">Library</span></span><br/>      | <dl> <span data-ttu-id="9e810-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e810-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9e810-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9e810-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="9e810-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e810-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9e810-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e810-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e810-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="9e810-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




