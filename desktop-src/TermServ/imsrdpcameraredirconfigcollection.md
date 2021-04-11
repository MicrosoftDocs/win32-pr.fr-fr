---
title: IMsRdpCameraRedirConfigCollection, interface
description: Représente la collection d’appareils photo (et les configurations associées) qui sont disponibles pour la redirection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, Description
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108355"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a><span data-ttu-id="6ddd3-105">IMsRdpCameraRedirConfigCollection, interface</span><span class="sxs-lookup"><span data-stu-id="6ddd3-105">IMsRdpCameraRedirConfigCollection interface</span></span>

 <span data-ttu-id="6ddd3-106">Représente la collection d’appareils photo (et les configurations associées) qui sont disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-106">Represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="6ddd3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6ddd3-107">Members</span></span>

<span data-ttu-id="6ddd3-108">L’interface **IMsRdpCameraRedirConfigCollection** hérite de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-108">The **IMsRdpCameraRedirConfigCollection** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="6ddd3-109">**IMsRdpCameraRedirConfigCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6ddd3-109">**IMsRdpCameraRedirConfigCollection** also has these types of members:</span></span>

- [<span data-ttu-id="6ddd3-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6ddd3-110">Methods</span></span>](#methods)
- [<span data-ttu-id="6ddd3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ddd3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6ddd3-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6ddd3-112">Methods</span></span>

<span data-ttu-id="6ddd3-113">L’interface **IMsRdpCameraRedirConfigCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-113">The **IMsRdpCameraRedirConfigCollection** interface has these methods.</span></span>

| <span data-ttu-id="6ddd3-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="6ddd3-114">Method</span></span>            | <span data-ttu-id="6ddd3-115">Description</span><span class="sxs-lookup"><span data-stu-id="6ddd3-115">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="6ddd3-116">**AddConfig**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-116">**AddConfig**</span></span>](imsrdpcameraredirconfigcollection-addconfig.md)       |  <span data-ttu-id="6ddd3-117">Ajoute un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à la collection (la caméra correspondante n’a pas besoin d’être connectée).</span><span class="sxs-lookup"><span data-stu-id="6ddd3-117">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>                   |
| [<span data-ttu-id="6ddd3-118">**Relancer**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-118">**Rescan**</span></span>](imsrdpcameraredirconfigcollection-rescan.md)       |  <span data-ttu-id="6ddd3-119">Énumère les appareils photo connectés.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-119">Enumerates connected camera devices.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="6ddd3-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ddd3-120">Properties</span></span>

<span data-ttu-id="6ddd3-121">L’interface **IMsRdpCameraRedirConfigCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-121">The **IMsRdpCameraRedirConfigCollection** interface has these properties.</span></span>

| <span data-ttu-id="6ddd3-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="6ddd3-122">Property</span></span>         | <span data-ttu-id="6ddd3-123">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="6ddd3-123">Access type</span></span>           | <span data-ttu-id="6ddd3-124">Description</span><span class="sxs-lookup"><span data-stu-id="6ddd3-124">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="6ddd3-125">**ByIndex**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-125">**ByIndex**</span></span>](imsrdpcameraredirconfigcollection-byindex.md)      | <span data-ttu-id="6ddd3-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ddd3-126">Read-only</span></span> |  <span data-ttu-id="6ddd3-127">Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) par son index dans la collection.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-127">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>   |
| [<span data-ttu-id="6ddd3-128">**ByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-128">**ByInstanceId**</span></span>](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | <span data-ttu-id="6ddd3-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ddd3-129">Read-only</span></span> |    <span data-ttu-id="6ddd3-130">Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la collection qui correspond à l’ID d’instance spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-130">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>    |
| [<span data-ttu-id="6ddd3-131">**BySymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-131">**BySymbolicLink**</span></span>](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | <span data-ttu-id="6ddd3-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ddd3-132">Read-only</span></span> |  <span data-ttu-id="6ddd3-133">Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la collection qui correspond au lien symbolique donné de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-133">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>  |
| [<span data-ttu-id="6ddd3-134">**Saut**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-134">**Count**</span></span>](imsrdpcameraredirconfigcollection-count.md)                       | <span data-ttu-id="6ddd3-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ddd3-135">Read-only</span></span> |    <span data-ttu-id="6ddd3-136">Retourne le nombre d’objets [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-136">Returns the number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>   |
| [<span data-ttu-id="6ddd3-137">**EncodeVideo**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-137">**EncodeVideo**</span></span>](imsrdpcameraredirconfigcollection-encodevideo.md)      | <span data-ttu-id="6ddd3-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6ddd3-138">Read/Write</span></span> |  <span data-ttu-id="6ddd3-139">Spécifie si le flux vidéo est au format H. 264 encodé.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-139">Specifies whether or not the video stream is H.264 encoded.</span></span>  |
| [<span data-ttu-id="6ddd3-140">**EncodingQuality**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-140">**EncodingQuality**</span></span>](imsrdpcameraredirconfigcollection-encodingquality.md)                       | <span data-ttu-id="6ddd3-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6ddd3-141">Read/Write</span></span> |    <span data-ttu-id="6ddd3-142">Spécifie la qualité d’encodage (vitesse de transmission).</span><span class="sxs-lookup"><span data-stu-id="6ddd3-142">Specifies the encoding quality (bit rate).</span></span>   |
| [<span data-ttu-id="6ddd3-143">**RedirectByDefault**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-143">**RedirectByDefault**</span></span>](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | <span data-ttu-id="6ddd3-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6ddd3-144">Read/Write</span></span> |   <span data-ttu-id="6ddd3-145">Spécifie si une nouvelle caméra est redirigée par défaut.</span><span class="sxs-lookup"><span data-stu-id="6ddd3-145">Specifies whether or not any new camera gets redirected by default.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="6ddd3-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ddd3-146">Requirements</span></span>

| <span data-ttu-id="6ddd3-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ddd3-147">Requirement</span></span> | <span data-ttu-id="6ddd3-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ddd3-148">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="6ddd3-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ddd3-149">Minimum supported client</span></span>| <span data-ttu-id="6ddd3-150">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="6ddd3-150">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="6ddd3-151">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6ddd3-151">Type library</span></span>            | <span data-ttu-id="6ddd3-152">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="6ddd3-152">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="6ddd3-153">DLL</span><span class="sxs-lookup"><span data-stu-id="6ddd3-153">DLL</span></span>                  | <span data-ttu-id="6ddd3-154">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="6ddd3-154">MsTscAx.dll</span></span>     |
| <span data-ttu-id="6ddd3-155">IID</span><span class="sxs-lookup"><span data-stu-id="6ddd3-155">IID</span></span>                      | <span data-ttu-id="6ddd3-156">IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="6ddd3-156">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>            |

## <a name="see-also"></a><span data-ttu-id="6ddd3-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ddd3-157">See also</span></span>

- [<span data-ttu-id="6ddd3-158">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-158">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
- [<span data-ttu-id="6ddd3-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="6ddd3-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
