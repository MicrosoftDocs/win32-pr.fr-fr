---
title: Méthode IMsTscAxEvents OnLoginComplete
description: Appelé lorsque le contrôle client s’est correctement connecté à un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance), en suivant l’affichage de la boîte de dialogue ouverture de session Windows.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnLoginComplete
- Méthode OnLoginComplete Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnLoginComplete
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508761"
---
# <a name="imstscaxeventsonlogincomplete-method"></a><span data-ttu-id="88363-106">IMsTscAxEvents :: OnLoginComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="88363-106">IMsTscAxEvents::OnLoginComplete method</span></span>

<span data-ttu-id="88363-107">Appelé lorsque le contrôle client s’est correctement connecté à un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance), en suivant l’affichage de la boîte de dialogue ouverture de session Windows.</span><span class="sxs-lookup"><span data-stu-id="88363-107">Called when the client control has successfully logged on to a Remote Desktop Session Host (RD Session Host) server, following the display of the Windows Logon dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="88363-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88363-108">Syntax</span></span>


```C++
void OnLoginComplete();
```



## <a name="parameters"></a><span data-ttu-id="88363-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88363-109">Parameters</span></span>

<span data-ttu-id="88363-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="88363-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88363-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88363-111">Return value</span></span>

<span data-ttu-id="88363-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="88363-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88363-113">Notes</span><span class="sxs-lookup"><span data-stu-id="88363-113">Remarks</span></span>

<span data-ttu-id="88363-114">Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le contrôle a terminé l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="88363-114">Implement this method in your event sink to receive notification that the control has completed logon.</span></span>

## <a name="examples"></a><span data-ttu-id="88363-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="88363-115">Examples</span></span>

<span data-ttu-id="88363-116">L’exemple suivant montre comment gérer cet événement à l’aide de Visual Basic Code de script.</span><span class="sxs-lookup"><span data-stu-id="88363-116">The following example shows how to handle this event by using Visual Basic Scripting code.</span></span> <span data-ttu-id="88363-117">Dans cet exemple, l’hypothèse est que votre objet de contrôle est nommé « MsRdpClient ».</span><span class="sxs-lookup"><span data-stu-id="88363-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="88363-118">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="88363-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a><span data-ttu-id="88363-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88363-119">Requirements</span></span>



| <span data-ttu-id="88363-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88363-120">Requirement</span></span> | <span data-ttu-id="88363-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="88363-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88363-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88363-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88363-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88363-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="88363-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88363-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88363-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88363-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="88363-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="88363-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="88363-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88363-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="88363-128">DLL</span><span class="sxs-lookup"><span data-stu-id="88363-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88363-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88363-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="88363-130">IID</span><span class="sxs-lookup"><span data-stu-id="88363-130">IID</span></span><br/>                      | <span data-ttu-id="88363-131">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="88363-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="88363-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88363-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88363-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="88363-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





