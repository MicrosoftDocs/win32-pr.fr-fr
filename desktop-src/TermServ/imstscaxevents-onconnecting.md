---
title: Méthode IMsTscAxEvents OnConnecting
description: Appelé lorsque le contrôle client commence à se connecter à un serveur en réponse à un appel à IMsTscAx Connect.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnConnecting
- Méthode OnConnecting Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnConnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383875"
---
# <a name="imstscaxeventsonconnecting-method"></a><span data-ttu-id="34e0b-106">IMsTscAxEvents :: OnConnecting, méthode</span><span class="sxs-lookup"><span data-stu-id="34e0b-106">IMsTscAxEvents::OnConnecting method</span></span>

<span data-ttu-id="34e0b-107">Appelé lorsque le contrôle client commence à se connecter à un serveur en réponse à un appel à [**IMsTscAx :: Connect**](imstscax-connect.md).</span><span class="sxs-lookup"><span data-stu-id="34e0b-107">Called when the client control begins connecting to a server in response to a call to [**IMsTscAx::Connect**](imstscax-connect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34e0b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34e0b-108">Syntax</span></span>


```C++
void OnConnecting();
```



## <a name="parameters"></a><span data-ttu-id="34e0b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34e0b-109">Parameters</span></span>

<span data-ttu-id="34e0b-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="34e0b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34e0b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34e0b-111">Return value</span></span>

<span data-ttu-id="34e0b-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="34e0b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e0b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="34e0b-113">Remarks</span></span>

<span data-ttu-id="34e0b-114">Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le contrôle a commencé à se connecter.</span><span class="sxs-lookup"><span data-stu-id="34e0b-114">Implement this method in your event sink to receive notification that the control has begun connecting.</span></span>

## <a name="examples"></a><span data-ttu-id="34e0b-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="34e0b-115">Examples</span></span>

<span data-ttu-id="34e0b-116">L’exemple suivant montre comment gérer cet événement avec Visual Basic Code de script.</span><span class="sxs-lookup"><span data-stu-id="34e0b-116">The following example shows how to handle this event with Visual Basic Scripting code.</span></span> <span data-ttu-id="34e0b-117">Dans cet exemple, l’hypothèse est que votre objet de contrôle est nommé « MsRdpClient ».</span><span class="sxs-lookup"><span data-stu-id="34e0b-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="34e0b-118">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="34e0b-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



## <a name="requirements"></a><span data-ttu-id="34e0b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34e0b-119">Requirements</span></span>



| <span data-ttu-id="34e0b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34e0b-120">Requirement</span></span> | <span data-ttu-id="34e0b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="34e0b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34e0b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34e0b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="34e0b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34e0b-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="34e0b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34e0b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="34e0b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34e0b-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="34e0b-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="34e0b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="34e0b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34e0b-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="34e0b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="34e0b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34e0b-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34e0b-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="34e0b-130">IID</span><span class="sxs-lookup"><span data-stu-id="34e0b-130">IID</span></span><br/>                      | <span data-ttu-id="34e0b-131">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="34e0b-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="34e0b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34e0b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e0b-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="34e0b-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





