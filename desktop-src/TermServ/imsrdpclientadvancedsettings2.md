---
title: Interface IMsRdpClientAdvancedSettings2
description: Gère les paramètres client avancés. Dérive de l’interface IMsRdpClientAdvancedSettings.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317326"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a><span data-ttu-id="b1266-106">Interface IMsRdpClientAdvancedSettings2</span><span class="sxs-lookup"><span data-stu-id="b1266-106">IMsRdpClientAdvancedSettings2 interface</span></span>

<span data-ttu-id="b1266-107">Gère les paramètres client avancés.</span><span class="sxs-lookup"><span data-stu-id="b1266-107">Manages advanced client settings.</span></span> <span data-ttu-id="b1266-108">Dérive de l’interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="b1266-108">Derives from the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="b1266-109">Cette interface comprend des méthodes pour récupérer et définir des propriétés avancées (facultatives) pour le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b1266-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="b1266-110">Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="b1266-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="b1266-111">Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings2** à **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="b1266-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings2** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="b1266-112">Membres</span><span class="sxs-lookup"><span data-stu-id="b1266-112">Members</span></span>

<span data-ttu-id="b1266-113">L’interface **IMsRdpClientAdvancedSettings2** hérite de [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b1266-113">The **IMsRdpClientAdvancedSettings2** interface inherits from [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span></span> <span data-ttu-id="b1266-114">**IMsRdpClientAdvancedSettings2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b1266-114">**IMsRdpClientAdvancedSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="b1266-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b1266-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1266-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b1266-116">Properties</span></span>

<span data-ttu-id="b1266-117">L’interface **IMsRdpClientAdvancedSettings2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b1266-117">The **IMsRdpClientAdvancedSettings2** interface has these properties.</span></span>



| <span data-ttu-id="b1266-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="b1266-118">Property</span></span>                                                                                      | <span data-ttu-id="b1266-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b1266-119">Access type</span></span>           | <span data-ttu-id="b1266-120">Description</span><span class="sxs-lookup"><span data-stu-id="b1266-120">Description</span></span>                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1266-121">**CanAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="b1266-121">**CanAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | <span data-ttu-id="b1266-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1266-122">Read-only</span></span><br/>  | <span data-ttu-id="b1266-123">Spécifie si le contrôle client peut se reconnecter automatiquement à la session active en cas de déconnexion réseau.</span><span class="sxs-lookup"><span data-stu-id="b1266-123">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span><br/>    |
| [<span data-ttu-id="b1266-124">**EnableAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="b1266-124">**EnableAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | <span data-ttu-id="b1266-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b1266-125">Read/write</span></span><br/> | <span data-ttu-id="b1266-126">Spécifie s’il faut activer le contrôle client pour qu’il se reconnecte automatiquement à une session en cas de déconnexion d’un réseau.</span><span class="sxs-lookup"><span data-stu-id="b1266-126">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span><br/>            |
| [<span data-ttu-id="b1266-127">**MaxReconnectAttempts**</span><span class="sxs-lookup"><span data-stu-id="b1266-127">**MaxReconnectAttempts**</span></span>](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | <span data-ttu-id="b1266-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b1266-128">Read/write</span></span><br/> | <span data-ttu-id="b1266-129">Spécifie le nombre de tentatives de connexion lors de la reconnexion automatique.</span><span class="sxs-lookup"><span data-stu-id="b1266-129">Specifies the number of times to try to reconnect during automatic reconnection.</span></span> <span data-ttu-id="b1266-130">Les valeurs valides de cette propriété sont comprises entre 0 et 200 inclus.</span><span class="sxs-lookup"><span data-stu-id="b1266-130">The valid values of this property are 0 to 200 inclusive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1266-131">Notes</span><span class="sxs-lookup"><span data-stu-id="b1266-131">Remarks</span></span>

<span data-ttu-id="b1266-132">Cette interface a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :</span><span class="sxs-lookup"><span data-stu-id="b1266-132">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="b1266-133">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b1266-133">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
-   [<span data-ttu-id="b1266-134">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b1266-134">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="b1266-135">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b1266-135">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="b1266-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b1266-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="b1266-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b1266-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="b1266-138">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b1266-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1266-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1266-139">Requirements</span></span>



| <span data-ttu-id="b1266-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1266-140">Requirement</span></span> | <span data-ttu-id="b1266-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1266-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1266-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1266-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b1266-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1266-143">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="b1266-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1266-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b1266-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1266-145">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="b1266-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b1266-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1266-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1266-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b1266-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b1266-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1266-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1266-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b1266-150">IID</span><span class="sxs-lookup"><span data-stu-id="b1266-150">IID</span></span><br/>                      | <span data-ttu-id="b1266-151">IID \_ IMsRdpClientAdvancedSettings2 est défini en tant que 9ac42117-2b76-4320-AA44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="b1266-151">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1266-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1266-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1266-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b1266-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b1266-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b1266-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b1266-155">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="b1266-155">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

