---
title: IMsRdpClientNonScriptable7, interface
description: Fournit l’accès aux propriétés non scriptables de la session à distance d’un client sur le contrôle ActiveX Bureau à distance. Dérive de l’interface IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable7
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable7, Description
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "106514066"
---
# <a name="imsrdpclientnonscriptable7-interface"></a><span data-ttu-id="28df0-106">IMsRdpClientNonScriptable7, interface</span><span class="sxs-lookup"><span data-stu-id="28df0-106">IMsRdpClientNonScriptable7 interface</span></span>

<span data-ttu-id="28df0-107">Fournit l’accès aux propriétés non scriptables de la session à distance d’un client sur le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="28df0-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="28df0-108">Dérive de l’interface [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) .</span><span class="sxs-lookup"><span data-stu-id="28df0-108">Derives from the [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) interface.</span></span> <span data-ttu-id="28df0-109">Les méthodes de cette interface sont accessibles uniquement par le biais de la vtable ; ils ne peuvent pas être utilisés pour des clients scriptables.</span><span class="sxs-lookup"><span data-stu-id="28df0-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="28df0-110">Une instance de cette interface est obtenue en appelant [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet [**IMsTscAx**](imstscax-interface.md) , en passant **IID \_ IMsRdpClientNonScriptable7**.</span><span class="sxs-lookup"><span data-stu-id="28df0-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable7**.</span></span>

## <a name="members"></a><span data-ttu-id="28df0-111">Membres</span><span class="sxs-lookup"><span data-stu-id="28df0-111">Members</span></span>

<span data-ttu-id="28df0-112">L’interface **IMsRdpClientNonScriptable7** hérite de [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="28df0-112">The **IMsRdpClientNonScriptable7** interface inherits from [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="28df0-113">**IMsRdpClientNonScriptable7** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="28df0-113">**IMsRdpClientNonScriptable7** also has these types of members:</span></span>

- [<span data-ttu-id="28df0-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="28df0-114">Methods</span></span>](#methods)
- [<span data-ttu-id="28df0-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="28df0-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="28df0-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="28df0-116">Methods</span></span>

<span data-ttu-id="28df0-117">L’interface **IMsRdpClientNonScriptable7** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="28df0-117">The **IMsRdpClientNonScriptable7** interface has these methods.</span></span>


| <span data-ttu-id="28df0-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="28df0-118">Method</span></span>            | <span data-ttu-id="28df0-119">Description</span><span class="sxs-lookup"><span data-stu-id="28df0-119">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="28df0-120">**DisableDpiCursorScalingForProcess**</span><span class="sxs-lookup"><span data-stu-id="28df0-120">**DisableDpiCursorScalingForProcess**</span></span>](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  <span data-ttu-id="28df0-121">Désactive la mise à l’échelle locale du curseur de la souris reçue du serveur, garantissant ainsi un rendu correct de la forme du curseur sans modification.</span><span class="sxs-lookup"><span data-stu-id="28df0-121">Disables local scaling of the mouse cursor received from the server, ensuring that the cursor shape is rendered correctly without modification.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="28df0-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="28df0-122">Properties</span></span>

<span data-ttu-id="28df0-123">L’interface **IMsRdpClientNonScriptable7** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="28df0-123">The **IMsRdpClientNonScriptable7** interface has these properties.</span></span>

| <span data-ttu-id="28df0-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="28df0-124">Property</span></span>         | <span data-ttu-id="28df0-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="28df0-125">Access type</span></span>           | <span data-ttu-id="28df0-126">Description</span><span class="sxs-lookup"><span data-stu-id="28df0-126">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="28df0-127">**CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="28df0-127">**CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | <span data-ttu-id="28df0-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28df0-128">Read-only</span></span> |  <span data-ttu-id="28df0-129">Obtient la collection des appareils photo (et les configurations associées) qui sont disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="28df0-129">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>   |
| [<span data-ttu-id="28df0-130">**Papier**</span><span class="sxs-lookup"><span data-stu-id="28df0-130">**Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)                       | <span data-ttu-id="28df0-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28df0-131">Read-only</span></span> |    <span data-ttu-id="28df0-132">Obtient le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée.</span><span class="sxs-lookup"><span data-stu-id="28df0-132">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="28df0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28df0-133">Requirements</span></span>

| <span data-ttu-id="28df0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28df0-134">Requirement</span></span> | <span data-ttu-id="28df0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="28df0-135">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="28df0-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28df0-136">Minimum supported client</span></span>| <span data-ttu-id="28df0-137">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="28df0-137">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="28df0-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="28df0-138">Type library</span></span>            | <span data-ttu-id="28df0-139">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="28df0-139">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="28df0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="28df0-140">DLL</span></span>                  | <span data-ttu-id="28df0-141">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="28df0-141">MsTscAx.dll</span></span>     |
| <span data-ttu-id="28df0-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="28df0-142">CLSID</span></span>                    | <span data-ttu-id="28df0-143">Le CLSID \_ MsRdpClient12 est défini en tant que 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="28df0-143">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="28df0-144">Le CLSID \_ MsRdpClient12NotSafeForScripting est défini en tant que 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="28df0-144">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="28df0-145">Le CLSID \_ MsRdpClient11 est défini en tant que 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="28df0-145">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="28df0-146">Le CLSID \_ MsRdpClient11NotSafeForScripting est défini en tant que 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="28df0-146">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="28df0-147">IID</span><span class="sxs-lookup"><span data-stu-id="28df0-147">IID</span></span>                      | <span data-ttu-id="28df0-148">IID \_ IMsRdpClientNonScriptable7 est défini en tant que 71B4A60A-fe21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="28df0-148">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>            |

## <a name="see-also"></a><span data-ttu-id="28df0-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28df0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28df0-150">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="28df0-150">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
