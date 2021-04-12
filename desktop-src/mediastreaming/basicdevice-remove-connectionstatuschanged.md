---
title: Méthode BasicDevice.remove_ConnectionStatusChanged
description: Annule l’inscription d’un gestionnaire d’événements pour l’événement ConnectionStatusChanged. | Méthode BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- API de diffusion multimédia en continu de méthode remove_ConnectionStatusChanged
- API de diffusion multimédia en continu de méthode remove_ConnectionStatusChanged, interface BasicDevice
- API de diffusion multimédia en continu de l’interface BasicDevice, méthode remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211548"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="8cfc5-107">Méthode BasicDevice. Remove \_ ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="8cfc5-107">BasicDevice.remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="8cfc5-108">Annule l’inscription d’un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="8cfc5-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfc5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cfc5-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="8cfc5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cfc5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cfc5-111">*jeton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8cfc5-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfc5-112">Référence à un jeton obtenu à partir de la méthode [**Add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) lors de l’inscription du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="8cfc5-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cfc5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8cfc5-113">Return value</span></span>

<span data-ttu-id="8cfc5-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8cfc5-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8cfc5-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8cfc5-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8cfc5-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8cfc5-116">Return code</span></span>                                                                          | <span data-ttu-id="8cfc5-117">Description</span><span class="sxs-lookup"><span data-stu-id="8cfc5-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8cfc5-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8cfc5-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8cfc5-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cfc5-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8cfc5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cfc5-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="8cfc5-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8cfc5-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

