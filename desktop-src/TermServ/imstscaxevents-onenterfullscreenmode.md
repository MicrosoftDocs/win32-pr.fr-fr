---
title: Méthode IMsTscAxEvents OnEnterFullScreenMode
description: Appelé lorsque le client passe en mode plein écran. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de raccourci du mode plein écran (CTRL + ALT + ATTN).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnEnterFullScreenMode
- Méthode OnEnterFullScreenMode Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnEnterFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226054fc7b1371bb088deb70ec9e87ea5a340b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942328"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a><span data-ttu-id="1d891-107">IMsTscAxEvents :: OnEnterFullScreenMode, méthode</span><span class="sxs-lookup"><span data-stu-id="1d891-107">IMsTscAxEvents::OnEnterFullScreenMode method</span></span>

<span data-ttu-id="1d891-108">Appelé lorsque le client passe en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="1d891-108">Called when the client enters full-screen mode.</span></span> <span data-ttu-id="1d891-109">Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de [raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).</span><span class="sxs-lookup"><span data-stu-id="1d891-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d891-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d891-110">Syntax</span></span>


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="1d891-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d891-111">Parameters</span></span>

<span data-ttu-id="1d891-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1d891-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d891-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d891-113">Return value</span></span>

<span data-ttu-id="1d891-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1d891-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d891-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1d891-115">Remarks</span></span>

<span data-ttu-id="1d891-116">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1d891-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d891-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d891-117">Requirements</span></span>



| <span data-ttu-id="1d891-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d891-118">Requirement</span></span> | <span data-ttu-id="1d891-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d891-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d891-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d891-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d891-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d891-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1d891-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d891-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d891-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d891-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1d891-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1d891-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d891-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d891-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d891-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1d891-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d891-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d891-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d891-128">IID</span><span class="sxs-lookup"><span data-stu-id="1d891-128">IID</span></span><br/>                      | <span data-ttu-id="1d891-129">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="1d891-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1d891-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d891-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d891-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="1d891-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





