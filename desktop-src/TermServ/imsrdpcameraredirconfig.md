---
title: IMsRdpCameraRedirConfig, interface
description: Représente les configurations pour une caméra qui est disponible pour la redirection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, Description
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520308"
---
# <a name="imsrdpcameraredirconfig-interface"></a><span data-ttu-id="b7eb0-105">IMsRdpCameraRedirConfig, interface</span><span class="sxs-lookup"><span data-stu-id="b7eb0-105">IMsRdpCameraRedirConfig interface</span></span>

<span data-ttu-id="b7eb0-106">Représente les configurations pour une caméra qui est disponible pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-106">Represents the configurations for a camera that is available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="b7eb0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b7eb0-107">Members</span></span>

<span data-ttu-id="b7eb0-108">L’interface **IMsRdpCameraRedirConfig** hérite de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-108">The **IMsRdpCameraRedirConfig** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="b7eb0-109">**IMsRdpCameraRedirConfig** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7eb0-109">**IMsRdpCameraRedirConfig** also has these types of members:</span></span>

- [<span data-ttu-id="b7eb0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7eb0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7eb0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7eb0-111">Properties</span></span>

<span data-ttu-id="b7eb0-112">L’interface **IMsRdpCameraRedirConfig** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-112">The **IMsRdpCameraRedirConfig** interface has these properties.</span></span>

| <span data-ttu-id="b7eb0-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7eb0-113">Property</span></span>         | <span data-ttu-id="b7eb0-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b7eb0-114">Access type</span></span>           | <span data-ttu-id="b7eb0-115">Description</span><span class="sxs-lookup"><span data-stu-id="b7eb0-115">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="b7eb0-116">**DeviceExists**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-116">**DeviceExists**</span></span>](imsrdpcameraredirconfig-deviceexists.md)      | <span data-ttu-id="b7eb0-117">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7eb0-117">Read-only</span></span> | <span data-ttu-id="b7eb0-118">Spécifie si le périphérique de l’appareil photo existe actuellement (c’est-à-dire que l’appareil photo est connecté).</span><span class="sxs-lookup"><span data-stu-id="b7eb0-118">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>   |
| [<span data-ttu-id="b7eb0-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-119">**FriendlyName**</span></span>](imsrdpcameraredirconfig-friendlyname.md)                       | <span data-ttu-id="b7eb0-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7eb0-120">Read-only</span></span> |    <span data-ttu-id="b7eb0-121">Obtient le nom convivial de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-121">Gets the camera’s friendly name.</span></span>    |
| [<span data-ttu-id="b7eb0-122">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-122">**InstanceId**</span></span>](imsrdpcameraredirconfig-instanceid.md)      | <span data-ttu-id="b7eb0-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7eb0-123">Read-only</span></span> |  <span data-ttu-id="b7eb0-124">Obtient l’ID d’instance de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-124">Gets the instance ID of the camera.</span></span>  |
| [<span data-ttu-id="b7eb0-125">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-125">**ParentInstanceId**</span></span>](imsrdpcameraredirconfig-parentinstanceid.md)                       | <span data-ttu-id="b7eb0-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7eb0-126">Read-only</span></span> |    <span data-ttu-id="b7eb0-127">Obtient l’ID d’instance d’appareil parent de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-127">Gets the parent device instance ID of the camera.</span></span>   |
| [<span data-ttu-id="b7eb0-128">**Redirected**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-128">**Redirected**</span></span>](imsrdpcameraredirconfig-redirected.md)      | <span data-ttu-id="b7eb0-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b7eb0-129">Read/Write</span></span> |  <span data-ttu-id="b7eb0-130">Spécifie si l’appareil photo est redirigé.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-130">Specifies whether or not the camera is redirected.</span></span>  |
| [<span data-ttu-id="b7eb0-131">**SymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-131">**SymbolicLink**</span></span>](imsrdpcameraredirconfig-symboliclink.md)                       | <span data-ttu-id="b7eb0-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7eb0-132">Read-only</span></span> |   <span data-ttu-id="b7eb0-133">Obtient le lien symbolique de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-133">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>   |

## <a name="requirements"></a><span data-ttu-id="b7eb0-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7eb0-134">Requirements</span></span>

| <span data-ttu-id="b7eb0-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7eb0-135">Requirement</span></span> | <span data-ttu-id="b7eb0-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7eb0-136">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="b7eb0-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7eb0-137">Minimum supported client</span></span>| <span data-ttu-id="b7eb0-138">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="b7eb0-138">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="b7eb0-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b7eb0-139">Type library</span></span>            | <span data-ttu-id="b7eb0-140">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b7eb0-140">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="b7eb0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b7eb0-141">DLL</span></span>                  | <span data-ttu-id="b7eb0-142">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b7eb0-142">MsTscAx.dll</span></span>     |
| <span data-ttu-id="b7eb0-143">IID</span><span class="sxs-lookup"><span data-stu-id="b7eb0-143">IID</span></span>                      | <span data-ttu-id="b7eb0-144">IID \_ IMsRdpCameraRedirConfig est défini comme 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="b7eb0-144">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="b7eb0-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7eb0-145">See also</span></span>

- [<span data-ttu-id="b7eb0-146">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-146">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
- [<span data-ttu-id="b7eb0-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)