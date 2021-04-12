---
title: Méthode IMsTscAxEvents OnRequestContainerMinimize
description: Appelé lorsque l’utilisateur appuie sur le bouton réduire de la barre de connexion en mode plein écran. Le déclenchement de cet événement est une demande que l’application conteneur réduit.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRequestContainerMinimize
- Méthode OnRequestContainerMinimize Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRequestContainerMinimize
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384879"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a><span data-ttu-id="bfc39-107">IMsTscAxEvents :: OnRequestContainerMinimize, méthode</span><span class="sxs-lookup"><span data-stu-id="bfc39-107">IMsTscAxEvents::OnRequestContainerMinimize method</span></span>

<span data-ttu-id="bfc39-108">Appelé lorsque l’utilisateur appuie sur le bouton **réduire** de la barre de connexion en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="bfc39-108">Called when the user presses the **Minimize** button on the connection bar in full-screen mode.</span></span> <span data-ttu-id="bfc39-109">Le déclenchement de cet événement est une demande que l’application conteneur réduit.</span><span class="sxs-lookup"><span data-stu-id="bfc39-109">The firing of this event is a request that the container application minimize itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc39-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfc39-110">Syntax</span></span>


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a><span data-ttu-id="bfc39-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfc39-111">Parameters</span></span>

<span data-ttu-id="bfc39-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bfc39-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bfc39-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfc39-113">Return value</span></span>

<span data-ttu-id="bfc39-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bfc39-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfc39-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bfc39-115">Remarks</span></span>

<span data-ttu-id="bfc39-116">Cette méthode sera appelée uniquement si le mode plein écran géré par le conteneur est activé. pour plus d’informations, consultez [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="bfc39-116">This method will only be called if the container-handled full-screen mode is enabled - see [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfc39-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfc39-117">Requirements</span></span>



| <span data-ttu-id="bfc39-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfc39-118">Requirement</span></span> | <span data-ttu-id="bfc39-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfc39-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc39-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfc39-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc39-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfc39-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bfc39-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfc39-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc39-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfc39-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bfc39-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bfc39-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfc39-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfc39-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfc39-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bfc39-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfc39-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfc39-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfc39-128">IID</span><span class="sxs-lookup"><span data-stu-id="bfc39-128">IID</span></span><br/>                      | <span data-ttu-id="bfc39-129">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="bfc39-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bfc39-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfc39-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc39-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="bfc39-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





