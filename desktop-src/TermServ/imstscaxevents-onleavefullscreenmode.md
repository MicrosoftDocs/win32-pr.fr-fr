---
title: Méthode IMsTscAxEvents OnLeaveFullScreenMode
description: Appelé lorsque le client quitte le mode plein écran. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de raccourci du mode plein écran (CTRL + ALT + ATTN).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnLeaveFullScreenMode
- Méthode OnLeaveFullScreenMode Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnLeaveFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4ee414f2dceba35a17ff86bce03c83d75aab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033003"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a><span data-ttu-id="289c9-107">IMsTscAxEvents :: OnLeaveFullScreenMode, méthode</span><span class="sxs-lookup"><span data-stu-id="289c9-107">IMsTscAxEvents::OnLeaveFullScreenMode method</span></span>

<span data-ttu-id="289c9-108">Appelé lorsque le client quitte le mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="289c9-108">Called when the client leaves full-screen mode.</span></span> <span data-ttu-id="289c9-109">Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de [raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).</span><span class="sxs-lookup"><span data-stu-id="289c9-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="289c9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="289c9-110">Syntax</span></span>


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="289c9-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="289c9-111">Parameters</span></span>

<span data-ttu-id="289c9-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="289c9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="289c9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="289c9-113">Return value</span></span>

<span data-ttu-id="289c9-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="289c9-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="289c9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="289c9-115">Remarks</span></span>

<span data-ttu-id="289c9-116">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="289c9-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="289c9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="289c9-117">Requirements</span></span>



| <span data-ttu-id="289c9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="289c9-118">Requirement</span></span> | <span data-ttu-id="289c9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="289c9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="289c9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="289c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="289c9-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="289c9-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="289c9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="289c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="289c9-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="289c9-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="289c9-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="289c9-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="289c9-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="289c9-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="289c9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="289c9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="289c9-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="289c9-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="289c9-128">IID</span><span class="sxs-lookup"><span data-stu-id="289c9-128">IID</span></span><br/>                      | <span data-ttu-id="289c9-129">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="289c9-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="289c9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="289c9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289c9-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="289c9-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





