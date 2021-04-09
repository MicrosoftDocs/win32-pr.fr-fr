---
description: L’interface IWiaDevMgr2 est utilisée pour créer et gérer des appareils d’acquisition d’images et pour s’inscrire afin de recevoir des événements d’appareil.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Interface IWiaDevMgr2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865246"
---
# <a name="iwiadevmgr2-interface"></a><span data-ttu-id="0bf47-103">Interface IWiaDevMgr2</span><span class="sxs-lookup"><span data-stu-id="0bf47-103">IWiaDevMgr2 interface</span></span>

<span data-ttu-id="0bf47-104">L’interface **IWiaDevMgr2** est utilisée pour créer et gérer des appareils d’acquisition d’images et pour s’inscrire afin de recevoir des événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="0bf47-104">The **IWiaDevMgr2** interface is used to create and manage image acquisition devices and to register to receive device events.</span></span>

## <a name="members"></a><span data-ttu-id="0bf47-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0bf47-105">Members</span></span>

<span data-ttu-id="0bf47-106">L’interface **IWiaDevMgr2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0bf47-106">The **IWiaDevMgr2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0bf47-107">**IWiaDevMgr2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0bf47-107">**IWiaDevMgr2** also has these types of members:</span></span>

-   [<span data-ttu-id="0bf47-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0bf47-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0bf47-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0bf47-109">Methods</span></span>

<span data-ttu-id="0bf47-110">L’interface **IWiaDevMgr2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0bf47-110">The **IWiaDevMgr2** interface has these methods.</span></span>



| <span data-ttu-id="0bf47-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="0bf47-111">Method</span></span>                                                                                    | <span data-ttu-id="0bf47-112">Description</span><span class="sxs-lookup"><span data-stu-id="0bf47-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bf47-113">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="0bf47-113">**CreateDevice**</span></span>](-wia-iwiadevmgr2-createdevice.md)                                     | <span data-ttu-id="0bf47-114">Crée une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) pour un appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0bf47-114">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="0bf47-115">**EnumDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="0bf47-115">**EnumDeviceInfo**</span></span>](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | <span data-ttu-id="0bf47-116">Crée un énumérateur d’informations de propriété pour chaque appareil WIA 2,0 disponible.</span><span class="sxs-lookup"><span data-stu-id="0bf47-116">Creates an enumerator of property information for each available WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="0bf47-117">**GetImageDlg**</span><span class="sxs-lookup"><span data-stu-id="0bf47-117">**GetImageDlg**</span></span>](-wia-iwiadevmgr2-getimagedlg.md)                                       | <span data-ttu-id="0bf47-118">La méthode [**IWiaDevMgr2 :: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) affiche une ou plusieurs boîtes de dialogue qui permettent à un utilisateur d’acquérir une image à partir d’un appareil WIA 2,0 et d’écrire l’image dans un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="0bf47-118">The [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method displays one or more dialog boxes that enable a user to acquire an image from a WIA 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="0bf47-119">Cette méthode étend les fonctionnalités de [**IWiaDevMgr2 :: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) pour encapsuler l’acquisition d’images dans un seul appel d’API.</span><span class="sxs-lookup"><span data-stu-id="0bf47-119">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span> <br/> |
| [<span data-ttu-id="0bf47-120">**RegisterEventCallbackCLSID**</span><span class="sxs-lookup"><span data-stu-id="0bf47-120">**RegisterEventCallbackCLSID**</span></span>](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | <span data-ttu-id="0bf47-121">La méthode [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) inscrit une application pour recevoir des événements même si l’application n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0bf47-121">The [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) method registers an application to receive events even if the application is not running.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="0bf47-122">**RegisterEventCallbackInterface**</span><span class="sxs-lookup"><span data-stu-id="0bf47-122">**RegisterEventCallbackInterface**</span></span>](-wia-iwiadevmgr2-registereventcallbackinterface.md) | <span data-ttu-id="0bf47-123">Inscrit une application en cours d’exécution pour la notification d’événements WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0bf47-123">Registers a running application for WIA 2.0 event notification.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="0bf47-124">**RegisterEventCallbackProgram**</span><span class="sxs-lookup"><span data-stu-id="0bf47-124">**RegisterEventCallbackProgram**</span></span>](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | <span data-ttu-id="0bf47-125">La méthode [**IWiaDevMgr2 :: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) inscrit une application pour recevoir des événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="0bf47-125">The [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method registers an application to receive device events.</span></span> <span data-ttu-id="0bf47-126">Il est principalement fourni pour la compatibilité descendante avec les applications qui n’ont pas été écrites pour WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0bf47-126">It is primarily provided for backward compatibility with applications that were not written for WIA 2.0.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="0bf47-127">**SelectDeviceDlg**</span><span class="sxs-lookup"><span data-stu-id="0bf47-127">**SelectDeviceDlg**</span></span>](-wia-iwiadevmgr2-selectdevicedlg.md)                               | <span data-ttu-id="0bf47-128">Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="0bf47-128">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="0bf47-129">**SelectDeviceDlgID**</span><span class="sxs-lookup"><span data-stu-id="0bf47-129">**SelectDeviceDlgID**</span></span>](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | <span data-ttu-id="0bf47-130">Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="0bf47-130">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="0bf47-131">Notes</span><span class="sxs-lookup"><span data-stu-id="0bf47-131">Remarks</span></span>

<span data-ttu-id="0bf47-132">L’interface **IWiaDevMgr2** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0bf47-132">The **IWiaDevMgr2** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="0bf47-133">Méthodes IUnknown</span><span class="sxs-lookup"><span data-stu-id="0bf47-133">IUnknown Methods</span></span>                                        | <span data-ttu-id="0bf47-134">Description</span><span class="sxs-lookup"><span data-stu-id="0bf47-134">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0bf47-135">[IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="0bf47-135">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="0bf47-136">Retourne des pointeurs aux interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0bf47-136">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="0bf47-137">IUnknown :: AddRef</span><span class="sxs-lookup"><span data-stu-id="0bf47-137">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="0bf47-138">Incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="0bf47-138">Increments reference count.</span></span>               |
| [<span data-ttu-id="0bf47-139">IUnknown :: Release</span><span class="sxs-lookup"><span data-stu-id="0bf47-139">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="0bf47-140">Décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="0bf47-140">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="0bf47-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bf47-141">Requirements</span></span>



| <span data-ttu-id="0bf47-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bf47-142">Requirement</span></span> | <span data-ttu-id="0bf47-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bf47-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf47-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bf47-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf47-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bf47-145">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0bf47-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bf47-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf47-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bf47-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0bf47-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bf47-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bf47-149"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bf47-149"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="0bf47-150">MIDL</span><span class="sxs-lookup"><span data-stu-id="0bf47-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0bf47-151"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0bf47-151"><dt>Wia.idl</dt></span></span> </dl> |



 

 
