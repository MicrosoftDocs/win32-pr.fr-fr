---
title: Méthode BasicDevice.add_ConnectionStatusChanged
description: Inscrit un gestionnaire d’événements pour l’événement ConnectionStatusChanged. | Méthode BasicDevice.add_ConnectionStatusChanged
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- API de diffusion multimédia en continu de méthode add_ConnectionStatusChanged
- API de diffusion multimédia en continu de méthode add_ConnectionStatusChanged, interface BasicDevice
- API de diffusion multimédia en continu de l’interface BasicDevice, méthode add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538282"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="757c5-107">BasicDevice. Add \_ ConnectionStatusChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="757c5-107">BasicDevice.add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="757c5-108">Inscrit un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="757c5-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="757c5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="757c5-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="757c5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="757c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="757c5-111">*Gestionnaire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="757c5-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757c5-112">Fonction de gestionnaire d’événements [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="757c5-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="757c5-113">*jeton* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="757c5-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="757c5-114">Référence à un jeton qui peut être utilisé pour annuler l’inscription du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="757c5-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="757c5-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="757c5-115">Return value</span></span>

<span data-ttu-id="757c5-116">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="757c5-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="757c5-117">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="757c5-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="757c5-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="757c5-118">Return code</span></span>                                                                          | <span data-ttu-id="757c5-119">Description</span><span class="sxs-lookup"><span data-stu-id="757c5-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="757c5-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="757c5-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="757c5-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="757c5-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="757c5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="757c5-122">Remarks</span></span>

<span data-ttu-id="757c5-123">Pour annuler l’inscription du gestionnaire d’événements qui a été enregistré par cette méthode, transmettez la valeur de *jeton* à la méthode [**Remove \_ ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="757c5-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="757c5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="757c5-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="757c5-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="757c5-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

