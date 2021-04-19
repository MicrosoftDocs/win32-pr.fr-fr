---
title: Méthode IMsTscAxEvents OnFocusReleased
description: Appelé lorsque la combinaison de touches de focus de mise en sortie est enfoncée. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la touche CTRL + ALT + gauche ou sur la combinaison de touches CTRL + ALT + flèche droite.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnFocusReleased
- Méthode OnFocusReleased Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnFocusReleased
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513794"
---
# <a name="imstscaxeventsonfocusreleased-method"></a><span data-ttu-id="9e433-107">IMsTscAxEvents :: OnFocusReleased, méthode</span><span class="sxs-lookup"><span data-stu-id="9e433-107">IMsTscAxEvents::OnFocusReleased method</span></span>

<span data-ttu-id="9e433-108">Appelé lorsque la combinaison de touches de focus de mise en sortie est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="9e433-108">Called when the release focus key combination is pressed.</span></span> <span data-ttu-id="9e433-109">Par exemple, cet événement est appelé quand l’utilisateur appuie sur la touche CTRL + ALT + gauche ou sur la combinaison de touches CTRL + ALT + flèche droite.</span><span class="sxs-lookup"><span data-stu-id="9e433-109">For example, this event is called when the user presses the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="9e433-110">Cet événement permet au conteneur de contrôles ActiveX de retirer le contrôle du contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9e433-110">This event enables the ActiveX control container to take away control from the ActiveX control.</span></span> <span data-ttu-id="9e433-111">Par exemple, cela est utile dans un scénario où vous n’avez pas de souris, et les combinaisons de touches spéciales, telles que ALT + TAB, sont redirigées vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="9e433-111">For example, this is useful in a scenario where you do not have a mouse, and special key combinations such as ALT+TAB are being redirected to the server.</span></span> <span data-ttu-id="9e433-112">Dans ce cas, vous n’avez pas de moyen de ramener le focus clavier sur le bureau local.</span><span class="sxs-lookup"><span data-stu-id="9e433-112">In this case, you do not have a way to return the keyboard focus back to the local desktop.</span></span> <span data-ttu-id="9e433-113">Toutefois, avec la combinaison de touches CTRL + ALT + gauche ou CTRL + ALT + flèche droite, le conteneur ActiveX peut écouter cet événement et y répondre en désoccupant le focus du contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9e433-113">However, with the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination, the ActiveX container can listen for this event and respond by taking focus away from the ActiveX control.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e433-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e433-114">Syntax</span></span>


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a><span data-ttu-id="9e433-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e433-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e433-116">*iDirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e433-116">*iDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e433-117">Paramètre de direction de 1 (CTRL + ALT + flèche droite) ou 1 (CTRL + ALT + flèche gauche).</span><span class="sxs-lookup"><span data-stu-id="9e433-117">The direction parameter of 1 (CTRL+ALT+RIGHT ARROW) or  1 (CTRL+ALT+LEFT ARROW).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e433-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e433-118">Return value</span></span>

<span data-ttu-id="9e433-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9e433-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e433-120">Notes</span><span class="sxs-lookup"><span data-stu-id="9e433-120">Remarks</span></span>

<span data-ttu-id="9e433-121">Cet événement est disponible lorsque Connexion Bureau à distance 6,0 est utilisé sur le client.</span><span class="sxs-lookup"><span data-stu-id="9e433-121">This event is available when Remote Desktop Connection 6.0 is used on the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e433-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e433-122">Requirements</span></span>



| <span data-ttu-id="9e433-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e433-123">Requirement</span></span> | <span data-ttu-id="9e433-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e433-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e433-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e433-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9e433-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e433-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9e433-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e433-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9e433-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e433-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9e433-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9e433-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e433-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e433-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e433-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9e433-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e433-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e433-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e433-133">IID</span><span class="sxs-lookup"><span data-stu-id="9e433-133">IID</span></span><br/>                      | <span data-ttu-id="9e433-134">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9e433-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9e433-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e433-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e433-136">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9e433-136">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





