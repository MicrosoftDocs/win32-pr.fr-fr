---
description: L’objet WIA est le point d’entrée pour toutes les fonctionnalités de script WIA (Windows Image Acquisition).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Objet WIA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113263"
---
# <a name="wia-object"></a><span data-ttu-id="7fd1e-103">Objet WIA</span><span class="sxs-lookup"><span data-stu-id="7fd1e-103">Wia object</span></span>

<span data-ttu-id="7fd1e-104">L’objet **WIA** est le point d’entrée pour toutes les fonctionnalités de script WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="7fd1e-104">The **Wia** object is the entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="7fd1e-105">Toute application qui utilise le modèle de script WIA doit créer un objet [**SafeWia**](-wia-safewia.md) ou **WIA** .</span><span class="sxs-lookup"><span data-stu-id="7fd1e-105">Any application that uses the WIA scripting model must create a [**SafeWia**](-wia-safewia.md) or **Wia** object.</span></span> <span data-ttu-id="7fd1e-106">Utilisez cet objet pour énumérer et créer des appareils et recevoir des notifications d’événements matériels.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

> [!Note]  
> <span data-ttu-id="7fd1e-107">Cet objet n’est pas sûr pour l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-107">This object is not safe for scripting.</span></span> <span data-ttu-id="7fd1e-108">Pour obtenir une version de cet objet sécurisée pour les scripts, consultez [**SafeWia**](-wia-safewia.md).</span><span class="sxs-lookup"><span data-stu-id="7fd1e-108">For a version of this object that is safe for scripting, see [**SafeWia**](-wia-safewia.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="7fd1e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7fd1e-109">Members</span></span>

<span data-ttu-id="7fd1e-110">L’objet **WIA** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fd1e-110">The **Wia** object has these types of members:</span></span>

-   [<span data-ttu-id="7fd1e-111">Événements</span><span class="sxs-lookup"><span data-stu-id="7fd1e-111">Events</span></span>](#events)
-   [<span data-ttu-id="7fd1e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7fd1e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7fd1e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7fd1e-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="7fd1e-114">Événements</span><span class="sxs-lookup"><span data-stu-id="7fd1e-114">Events</span></span>

<span data-ttu-id="7fd1e-115">L’objet **WIA** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-115">The **Wia** object has these events.</span></span>



| <span data-ttu-id="7fd1e-116">Événement</span><span class="sxs-lookup"><span data-stu-id="7fd1e-116">Event</span></span>                                                                 | <span data-ttu-id="7fd1e-117">Description</span><span class="sxs-lookup"><span data-stu-id="7fd1e-117">Description</span></span>                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="7fd1e-118">**OnDeviceConnected**</span><span class="sxs-lookup"><span data-stu-id="7fd1e-118">**OnDeviceConnected**</span></span>](-wia--iwiaevents-ondeviceconnected.md)       | <span data-ttu-id="7fd1e-119">Événement qui se produit lorsqu’un nouveau périphérique matériel WIA est connecté.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-119">Event that occurs when a new WIA hardware device is connected.</span></span><br/>    |
| [<span data-ttu-id="7fd1e-120">**OnDeviceDisconnected**</span><span class="sxs-lookup"><span data-stu-id="7fd1e-120">**OnDeviceDisconnected**</span></span>](-wia--iwiaevents-ondevicedisconnected.md) | <span data-ttu-id="7fd1e-121">Événement qui se produit lorsqu’un nouveau périphérique matériel WIA est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-121">Event that occurs when a new WIA hardware device is disconnected.</span></span><br/> |
| [<span data-ttu-id="7fd1e-122">**OnTransferComplete**</span><span class="sxs-lookup"><span data-stu-id="7fd1e-122">**OnTransferComplete**</span></span>](-wia--iwiaevents-ontransfercomplete.md)     | <span data-ttu-id="7fd1e-123">Événement qui se produit lorsqu’un transfert de données est effectué avec succès.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-123">Event that occurs when a data transfer is completed successfully.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="7fd1e-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7fd1e-124">Methods</span></span>

<span data-ttu-id="7fd1e-125">L’objet **WIA** possède les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-125">The **Wia** object has these methods.</span></span>



| <span data-ttu-id="7fd1e-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="7fd1e-126">Method</span></span>                             | <span data-ttu-id="7fd1e-127">Description</span><span class="sxs-lookup"><span data-stu-id="7fd1e-127">Description</span></span>                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fd1e-128">**Créés**</span><span class="sxs-lookup"><span data-stu-id="7fd1e-128">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="7fd1e-129">La méthode [**Create**](-wia-iwia-create.md) de l’objet **WIA** établit une connexion à l’appareil WIA spécifié et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-129">The [**Create**](-wia-iwia-create.md) method of the **Wia** object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7fd1e-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7fd1e-130">Properties</span></span>

<span data-ttu-id="7fd1e-131">L’objet **WIA** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-131">The **Wia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7fd1e-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="7fd1e-132">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7fd1e-133">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="7fd1e-133">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7fd1e-134">Description</span><span class="sxs-lookup"><span data-stu-id="7fd1e-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7fd1e-135"><a href="-wia-iwia-devices.md"><strong>Appareils</strong></a></span><span class="sxs-lookup"><span data-stu-id="7fd1e-135"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7fd1e-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fd1e-136">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7fd1e-137">Collection d’objets <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> qui représentent tous les périphériques installés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-137">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="7fd1e-138">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-138">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7fd1e-139">Cette collection est de base 0.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-139">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="7fd1e-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fd1e-140">Requirements</span></span>



| <span data-ttu-id="7fd1e-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fd1e-141">Requirement</span></span> | <span data-ttu-id="7fd1e-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fd1e-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd1e-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd1e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd1e-144">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fd1e-144">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fd1e-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd1e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd1e-146">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fd1e-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7fd1e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7fd1e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fd1e-148"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="7fd1e-148"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="7fd1e-149">IID</span><span class="sxs-lookup"><span data-stu-id="7fd1e-149">IID</span></span><br/>                      | <span data-ttu-id="7fd1e-150">CLSID \_ WIA</span><span class="sxs-lookup"><span data-stu-id="7fd1e-150">CLSID\_Wia</span></span><br/>                                                                                         |



 

 




