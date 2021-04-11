---
title: Interface IRemoteDesktopClientEvents
description: Fournit des méthodes qui reçoivent des informations du serveur qui sont liées aux événements de contrôle du client.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, Description
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032863"
---
# <a name="iremotedesktopclientevents-interface"></a><span data-ttu-id="fddb0-105">Interface IRemoteDesktopClientEvents</span><span class="sxs-lookup"><span data-stu-id="fddb0-105">IRemoteDesktopClientEvents interface</span></span>

<span data-ttu-id="fddb0-106">Fournit des méthodes qui reçoivent des informations du serveur qui sont liées aux événements de contrôle du client.</span><span class="sxs-lookup"><span data-stu-id="fddb0-106">Provides methods that receive information from the server that are related to client control events.</span></span> <span data-ttu-id="fddb0-107">Les événements incluent la connexion et la déconnexion, les demandes en mode plein écran, la réussite de l’ouverture de session et les conditions d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fddb0-107">Events include connecting and disconnecting, full-screen mode requests, successful logon, and error conditions.</span></span>

## <a name="members"></a><span data-ttu-id="fddb0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fddb0-108">Members</span></span>

<span data-ttu-id="fddb0-109">L’interface **IRemoteDesktopClientEvents** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fddb0-109">The **IRemoteDesktopClientEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fddb0-110">**IRemoteDesktopClientEvents** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fddb0-110">**IRemoteDesktopClientEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="fddb0-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fddb0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fddb0-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fddb0-112">Methods</span></span>

<span data-ttu-id="fddb0-113">L’interface **IRemoteDesktopClientEvents** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fddb0-113">The **IRemoteDesktopClientEvents** interface has these methods.</span></span>



| <span data-ttu-id="fddb0-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="fddb0-114">Method</span></span>                                                                                      | <span data-ttu-id="fddb0-115">Description</span><span class="sxs-lookup"><span data-stu-id="fddb0-115">Description</span></span>                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fddb0-116">**OnAdminMessageReceived**</span><span class="sxs-lookup"><span data-stu-id="fddb0-116">**OnAdminMessageReceived**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)         | <span data-ttu-id="fddb0-117">Appelé lorsque le contrôle client reçoit un message d’administration.</span><span class="sxs-lookup"><span data-stu-id="fddb0-117">Called when the client control receives an administrative message.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="fddb0-118">**OnAutoReconnected**</span><span class="sxs-lookup"><span data-stu-id="fddb0-118">**OnAutoReconnected**</span></span>](iremotedesktopclientevents-onautoreconnected.md)                   | <span data-ttu-id="fddb0-119">Appelé lorsque le contrôle client se reconnecte automatiquement à une session à distance.</span><span class="sxs-lookup"><span data-stu-id="fddb0-119">Called when the client control has automatically reconnected to a remote session.</span></span> <br/>                                                                       |
| [<span data-ttu-id="fddb0-120">**OnAutoReconnecting**</span><span class="sxs-lookup"><span data-stu-id="fddb0-120">**OnAutoReconnecting**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)                 | <span data-ttu-id="fddb0-121">Appelé lorsque le contrôle client tente de rétablir automatiquement une connexion à une session à distance.</span><span class="sxs-lookup"><span data-stu-id="fddb0-121">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span> <br/>                                                  |
| [<span data-ttu-id="fddb0-122">**OnConnected**</span><span class="sxs-lookup"><span data-stu-id="fddb0-122">**OnConnected**</span></span>](iremotedesktopclientevents-onconnected.md)                               | <span data-ttu-id="fddb0-123">Appelé lorsque le contrôle client s’est connecté à une session à distance.</span><span class="sxs-lookup"><span data-stu-id="fddb0-123">Called when the client control has connected to a remote session.</span></span><br/>                                                                                        |
| [<span data-ttu-id="fddb0-124">**OnConnecting**</span><span class="sxs-lookup"><span data-stu-id="fddb0-124">**OnConnecting**</span></span>](iremotedesktopclientevents-onconnecting.md)                             | <span data-ttu-id="fddb0-125">Appelé lorsque le contrôle client tente d’établir une connexion à une session à distance.</span><span class="sxs-lookup"><span data-stu-id="fddb0-125">Called when the client control attempts to establish a connection to a remote session.</span></span> <br/>                                                                  |
| [<span data-ttu-id="fddb0-126">**OnDialogDismissed**</span><span class="sxs-lookup"><span data-stu-id="fddb0-126">**OnDialogDismissed**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)                   | <span data-ttu-id="fddb0-127">Appelé après la fermeture d’une boîte de dialogue affichée par le contrôle client.</span><span class="sxs-lookup"><span data-stu-id="fddb0-127">Called after a dialog box displayed by the client control is dismissed.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="fddb0-128">**OnDialogDisplaying**</span><span class="sxs-lookup"><span data-stu-id="fddb0-128">**OnDialogDisplaying**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)                 | <span data-ttu-id="fddb0-129">Appelé avant que le contrôle affiche une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fddb0-129">Called before the control displays a dialog box.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="fddb0-130">**OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="fddb0-130">**OnDisconnected**</span></span>](iremotedesktopclientevents-ondisconnected.md)                         | <span data-ttu-id="fddb0-131">Appelé lorsque le contrôle client a été déconnecté d’une session à distance.</span><span class="sxs-lookup"><span data-stu-id="fddb0-131">Called when the client control has been disconnected from a remote session.</span></span> <br/>                                                                             |
| [<span data-ttu-id="fddb0-132">**OnKeyCombinationPressed**</span><span class="sxs-lookup"><span data-stu-id="fddb0-132">**OnKeyCombinationPressed**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)       | <span data-ttu-id="fddb0-133">Appelé lorsque des combinaisons de touches spéciales sont activées dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="fddb0-133">Called when special key combinations are pressed in the remote session.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="fddb0-134">**OnLoginCompleted**</span><span class="sxs-lookup"><span data-stu-id="fddb0-134">**OnLoginCompleted**</span></span>](iremotedesktopclientevents-onlogincompleted.md)                     | <span data-ttu-id="fddb0-135">Appelé lorsque le contrôle client a réussi à se connecter à une session à distance.</span><span class="sxs-lookup"><span data-stu-id="fddb0-135">Called when the client control has successfully logged on to a remote session.</span></span> <br/>                                                                          |
| [<span data-ttu-id="fddb0-136">**OnNetworkStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="fddb0-136">**OnNetworkStatusChanged**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)         | <span data-ttu-id="fddb0-137">Appelé lorsque l’état du réseau a changé.</span><span class="sxs-lookup"><span data-stu-id="fddb0-137">Called when the network status has changed.</span></span> <br/>                                                                                                             |
| [<span data-ttu-id="fddb0-138">**OnRemoteDesktopSizeChanged**</span><span class="sxs-lookup"><span data-stu-id="fddb0-138">**OnRemoteDesktopSizeChanged**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md) | <span data-ttu-id="fddb0-139">Appelé lorsque la taille du Bureau à distance a changé.</span><span class="sxs-lookup"><span data-stu-id="fddb0-139">Called when the remote desktop size has changed.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="fddb0-140">**OnStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="fddb0-140">**OnStatusChanged**</span></span>](iremotedesktopclientevents-onstatuschanged.md)                       | <span data-ttu-id="fddb0-141">Appelé lorsque le contrôle client a mis à jour son état.</span><span class="sxs-lookup"><span data-stu-id="fddb0-141">Called when the client control has updated its status.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="fddb0-142">**OnTouchPointerCursorMoved**</span><span class="sxs-lookup"><span data-stu-id="fddb0-142">**OnTouchPointerCursorMoved**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)   | <span data-ttu-id="fddb0-143">Appelé lorsque le curseur tactile a été déplacé et que la propriété [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="fddb0-143">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="fddb0-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fddb0-144">Requirements</span></span>



| <span data-ttu-id="fddb0-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fddb0-145">Requirement</span></span> | <span data-ttu-id="fddb0-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="fddb0-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fddb0-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fddb0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="fddb0-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fddb0-148">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="fddb0-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fddb0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="fddb0-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fddb0-150">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="fddb0-151">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fddb0-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="fddb0-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fddb0-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="fddb0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="fddb0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fddb0-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fddb0-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="fddb0-155">CLSID</span><span class="sxs-lookup"><span data-stu-id="fddb0-155">CLSID</span></span><br/>                    | <span data-ttu-id="fddb0-156">Le CLSID \_ RemoteDesktopClient est défini en tant que EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span><span class="sxs-lookup"><span data-stu-id="fddb0-156">CLSID\_RemoteDesktopClient is defined as EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span></span><br/>       |
| <span data-ttu-id="fddb0-157">IID</span><span class="sxs-lookup"><span data-stu-id="fddb0-157">IID</span></span><br/>                      | <span data-ttu-id="fddb0-158">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="fddb0-158">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fddb0-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fddb0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fddb0-160">Référence du contrôle ActiveX Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="fddb0-160">Remote Desktop ActiveX control reference</span></span>](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

