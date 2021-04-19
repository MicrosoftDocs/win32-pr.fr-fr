---
description: L’objet DeviceInfo permet d’accéder aux propriétés d’un périphérique matériel WIA (Windows Image Acquisition).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Objet DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525066"
---
# <a name="deviceinfo-object"></a><span data-ttu-id="1e59a-103">Objet DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="1e59a-103">DeviceInfo object</span></span>

<span data-ttu-id="1e59a-104">L’objet **DeviceInfo** permet d’accéder aux propriétés d’un périphérique matériel WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="1e59a-104">The **DeviceInfo** object provides access to the properties of a Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="1e59a-105">En outre, par le biais de sa méthode de [**création**](-wia-iwiadeviceinfo-create.md) , permet à l’application ou au script de se connecter à l’appareil et d’obtenir un objet d' [**élément**](-wia-item.md) qui représente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1e59a-105">It also, through its [**Create**](-wia-iwiadeviceinfo-create.md) method, provides a way for the application or script to connect to the device and obtain an [**Item**](-wia-item.md) object that represents the device.</span></span> <span data-ttu-id="1e59a-106">Utilisez la méthode [**Devices**](-wia-iwia-devices.md) pour obtenir une collection d’objets **DeviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="1e59a-106">Use the [**Devices**](-wia-iwia-devices.md) method to obtain a collection of **DeviceInfo** objects.</span></span>

## <a name="members"></a><span data-ttu-id="1e59a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1e59a-107">Members</span></span>

<span data-ttu-id="1e59a-108">L’objet **DeviceInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1e59a-108">The **DeviceInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="1e59a-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1e59a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1e59a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1e59a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1e59a-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1e59a-111">Methods</span></span>

<span data-ttu-id="1e59a-112">L’objet **DeviceInfo** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1e59a-112">The **DeviceInfo** object has these methods.</span></span>



| <span data-ttu-id="1e59a-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="1e59a-113">Method</span></span>                                                 | <span data-ttu-id="1e59a-114">Description</span><span class="sxs-lookup"><span data-stu-id="1e59a-114">Description</span></span>                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e59a-115">**Créés**</span><span class="sxs-lookup"><span data-stu-id="1e59a-115">**Create**</span></span>](-wia-iwiadeviceinfo-create.md)           | <span data-ttu-id="1e59a-116">La méthode [**Create**](-wia-iwiadeviceinfo-create.md) de l’objet **DeviceInfo** établit une connexion au périphérique WIA spécifié par l’objet **DeviceInfo** et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1e59a-116">The [**Create**](-wia-iwiadeviceinfo-create.md) method of the **DeviceInfo** object makes a connection to the WIA device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |
| [<span data-ttu-id="1e59a-117">**GetPropById**</span><span class="sxs-lookup"><span data-stu-id="1e59a-117">**GetPropById**</span></span>](-wia-iwiadeviceinfo-getpropbyid.md) | <span data-ttu-id="1e59a-118">La méthode [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) de l’objet **DEVICEINFO** utilise l’ID d’une propriété d’appareil pour retourner sa valeur.</span><span class="sxs-lookup"><span data-stu-id="1e59a-118">The [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) method of the **DeviceInfo** object uses a device property's ID to return its value.</span></span><br/>                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="1e59a-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1e59a-119">Properties</span></span>

<span data-ttu-id="1e59a-120">L’objet **DeviceInfo** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1e59a-120">The **DeviceInfo** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1e59a-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="1e59a-121">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1e59a-122">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="1e59a-122">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1e59a-123">Description</span><span class="sxs-lookup"><span data-stu-id="1e59a-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1e59a-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Identifi</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e59a-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e59a-125">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-126">Récupère l’ID du périphérique matériel WIA.</span><span class="sxs-lookup"><span data-stu-id="1e59a-126">Retrieves the ID of the WIA hardware device.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1e59a-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Fabricant</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e59a-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e59a-128">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-129">Récupère le nom du fabricant de cet appareil matériel.</span><span class="sxs-lookup"><span data-stu-id="1e59a-129">Retrieves the name of the manufacturer of this hardware device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1e59a-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Nom</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e59a-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e59a-131">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-132">Nom du périphérique matériel WIA tel qu’il apparaît dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e59a-132">The name of the WIA hardware device as it appears in the UI.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1e59a-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e59a-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e59a-134">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-135">Récupère le port auquel le périphérique matériel WIA est connecté.</span><span class="sxs-lookup"><span data-stu-id="1e59a-135">Retrieves the port to which the WIA hardware device is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1e59a-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Entrer</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e59a-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e59a-137">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-138">Récupère le type d’appareil matériel WIA.</span><span class="sxs-lookup"><span data-stu-id="1e59a-138">Retrieves the type of WIA hardware device.</span></span> <span data-ttu-id="1e59a-139">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e59a-139">Possible values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="1e59a-140">DigitalCamera</span><span class="sxs-lookup"><span data-stu-id="1e59a-140">DigitalCamera</span></span></li>
<li><span data-ttu-id="1e59a-141">Scanneur</span><span class="sxs-lookup"><span data-stu-id="1e59a-141">Scanner</span></span></li>
<li><span data-ttu-id="1e59a-142">StreamingVideo</span><span class="sxs-lookup"><span data-stu-id="1e59a-142">StreamingVideo</span></span></li>
<li><span data-ttu-id="1e59a-143">Default</span><span class="sxs-lookup"><span data-stu-id="1e59a-143">Default</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1e59a-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e59a-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e59a-145">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1e59a-146">Récupère l’ID de classe de l’interface utilisateur fournie par le fabricant pour cet appareil matériel WIA.</span><span class="sxs-lookup"><span data-stu-id="1e59a-146">Retrieves the class id of the manufacturer-provided user interface for this WIA hardware device.</span></span> <span data-ttu-id="1e59a-147">La valeur est une représentation sous forme de chaîne d’un GUID.</span><span class="sxs-lookup"><span data-stu-id="1e59a-147">The value is a string representation of a GUID.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1e59a-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e59a-148">Requirements</span></span>



| <span data-ttu-id="1e59a-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e59a-149">Requirement</span></span> | <span data-ttu-id="1e59a-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e59a-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e59a-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e59a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="1e59a-152">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e59a-152">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e59a-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e59a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="1e59a-154">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e59a-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1e59a-155">DLL</span><span class="sxs-lookup"><span data-stu-id="1e59a-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e59a-156"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1e59a-156"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




