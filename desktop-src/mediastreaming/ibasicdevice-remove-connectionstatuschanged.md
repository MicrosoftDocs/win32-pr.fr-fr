---
title: IBasicDevice remove_ConnectionStatusChanged méthode)
description: Annule l’inscription d’un gestionnaire d’événements pour l’événement ConnectionStatusChanged. | IBasicDevice remove_ConnectionStatusChanged méthode)
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- API de diffusion multimédia en continu de méthode remove_ConnectionStatusChanged
- API de diffusion multimédia en continu de méthode remove_ConnectionStatusChanged, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539831"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="c6be6-107">IBasicDevice :: Remove \_ ConnectionStatusChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="c6be6-107">IBasicDevice::remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="c6be6-108">Annule l’inscription d’un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="c6be6-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6be6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6be6-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="c6be6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6be6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6be6-111">*jeton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6be6-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6be6-112">Référence à un jeton obtenu à partir de la méthode [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) lors de l’inscription du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="c6be6-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6be6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6be6-113">Return value</span></span>

<span data-ttu-id="c6be6-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c6be6-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c6be6-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c6be6-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c6be6-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c6be6-116">Return code</span></span>                                                                          | <span data-ttu-id="c6be6-117">Description</span><span class="sxs-lookup"><span data-stu-id="c6be6-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c6be6-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c6be6-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c6be6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6be6-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c6be6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6be6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6be6-121">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="c6be6-121">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





