---
title: Interface IMsTscSecuredSettings
description: Comprend des méthodes pour récupérer et définir des propriétés du contrôle ActiveX Bureau à distance qui sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques. | Interface IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsTscSecuredSettings
- Services Bureau à distance de l’interface IMsTscSecuredSettings, Description
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531774"
---
# <a name="imstscsecuredsettings-interface"></a><span data-ttu-id="26846-106">Interface IMsTscSecuredSettings</span><span class="sxs-lookup"><span data-stu-id="26846-106">IMsTscSecuredSettings interface</span></span>

<span data-ttu-id="26846-107">Comprend des méthodes pour récupérer et définir des propriétés du contrôle ActiveX Bureau à distance qui sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques.</span><span class="sxs-lookup"><span data-stu-id="26846-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="26846-108">Les propriétés incluent celles qui spécifient le mode du contrôle client (mode plein écran ou mode fenêtre) et le programme à démarrer lors de la connexion au serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="26846-108">Properties include those that specify the mode of the client control (full-screen mode or window mode) and the program to start upon connection to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="26846-109">Ces méthodes sont également disponibles via l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="26846-109">These methods are also available through the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="26846-110">Membres</span><span class="sxs-lookup"><span data-stu-id="26846-110">Members</span></span>

<span data-ttu-id="26846-111">L’interface **IMsTscSecuredSettings** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="26846-111">The **IMsTscSecuredSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="26846-112">**IMsTscSecuredSettings** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26846-112">**IMsTscSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="26846-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26846-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26846-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26846-114">Properties</span></span>

<span data-ttu-id="26846-115">L’interface **IMsTscSecuredSettings** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="26846-115">The **IMsTscSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="26846-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="26846-116">Property</span></span>                                                              | <span data-ttu-id="26846-117">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="26846-117">Access type</span></span>           | <span data-ttu-id="26846-118">Description</span><span class="sxs-lookup"><span data-stu-id="26846-118">Description</span></span>                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="26846-119">**FullScreen**</span><span class="sxs-lookup"><span data-stu-id="26846-119">**FullScreen**</span></span>](imstscsecuredsettings-fullscreen.md)<br/>     | <span data-ttu-id="26846-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="26846-120">Read/write</span></span><br/> | <span data-ttu-id="26846-121">État plein écran du contrôle client.</span><span class="sxs-lookup"><span data-stu-id="26846-121">The full-screen state of the client control.</span></span><br/>                    |
| [<span data-ttu-id="26846-122">**StartProgram**</span><span class="sxs-lookup"><span data-stu-id="26846-122">**StartProgram**</span></span>](imstscsecuredsettings-startprogram.md)<br/> | <span data-ttu-id="26846-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="26846-123">Read/write</span></span><br/> | <span data-ttu-id="26846-124">Programme à démarrer sur le serveur distant lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="26846-124">The program to be started on the remote server upon connection.</span></span><br/> |
| [<span data-ttu-id="26846-125">**WorkDir**</span><span class="sxs-lookup"><span data-stu-id="26846-125">**WorkDir**</span></span>](imstscsecuredsettings-workdir.md)<br/>           | <span data-ttu-id="26846-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="26846-126">Read/write</span></span><br/> | <span data-ttu-id="26846-127">Répertoire de travail du programme de démarrage.</span><span class="sxs-lookup"><span data-stu-id="26846-127">The working directory of the start program.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="26846-128">Notes</span><span class="sxs-lookup"><span data-stu-id="26846-128">Remarks</span></span>

<span data-ttu-id="26846-129">Pour plus d’informations sur les méthodes de cette interface, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="26846-129">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="26846-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="26846-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26846-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26846-131">Requirements</span></span>



| <span data-ttu-id="26846-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26846-132">Requirement</span></span> | <span data-ttu-id="26846-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="26846-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26846-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26846-134">Minimum supported client</span></span><br/> | <span data-ttu-id="26846-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26846-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="26846-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26846-136">Minimum supported server</span></span><br/> | <span data-ttu-id="26846-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26846-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="26846-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="26846-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="26846-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26846-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="26846-140">DLL</span><span class="sxs-lookup"><span data-stu-id="26846-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26846-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26846-141"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26846-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26846-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26846-143">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="26846-143">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="26846-144">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="26846-144">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

