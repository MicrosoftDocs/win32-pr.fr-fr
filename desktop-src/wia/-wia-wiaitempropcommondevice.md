---
description: En plus des propriétés d’informations de périphérique, les périphériques d’acquisition d’images Windows (WIA) ont des valeurs de propriété stockées dans le registre que les applications lisent et écrivent.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Constantes de propriété d’appareil courantes (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526398"
---
# <a name="common-device-property-constants"></a><span data-ttu-id="94634-103">Constantes de propriété d’appareil courantes</span><span class="sxs-lookup"><span data-stu-id="94634-103">Common Device Property Constants</span></span>

<span data-ttu-id="94634-104">En plus des propriétés d’informations de périphérique, les périphériques d’acquisition d’images Windows (WIA) ont des valeurs de propriété stockées dans le registre que les applications lisent et écrivent.</span><span class="sxs-lookup"><span data-stu-id="94634-104">In addition to device information properties, Windows Image Acquisition (WIA) devices have property values stored in the registry that applications read and write.</span></span> <span data-ttu-id="94634-105">Ils sont associés à l’objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou à l’objet [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="94634-105">They are associated with the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object or [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <span data-ttu-id="94634-106">Les propriétés des appareils représentent des informations sur l’appareil, telles que l’état de la connexion et l’heure de l’appareil</span><span class="sxs-lookup"><span data-stu-id="94634-106">Device properties represent device information such as connection status and device time.</span></span> <span data-ttu-id="94634-107">Chaque propriété d’appareil est associée à une chaîne de propriété d’appareil.</span><span class="sxs-lookup"><span data-stu-id="94634-107">Each device property has an associated device property string.</span></span>

<span data-ttu-id="94634-108">Les constantes de propriété d’appareil répertoriées ici sont communes à la plupart ou à la totalité des périphériques matériels WIA.</span><span class="sxs-lookup"><span data-stu-id="94634-108">The Device Property Constants listed here are common to most or all WIA hardware devices.</span></span>

<span data-ttu-id="94634-109">Le préfixe « WIA \_ DPA \_ » indique une propriété d’appareil pour tous les appareils et est la Convention d’affectation de noms utilisée dans C/C++.</span><span class="sxs-lookup"><span data-stu-id="94634-109">The prefix "WIA\_DPA\_" indicates a Device Property for All devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="94634-110">À des fins de script, ces constantes utilisent le préfixe « Device » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="94634-110">For scripting purposes these constants use the prefix "Device" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="94634-111">Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="94634-111">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="94634-112">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="94634-112">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="94634-113">Description</span><span class="sxs-lookup"><span data-stu-id="94634-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <span data-ttu-id="94634-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="94634-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="94634-115">État actuel de la connexion pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="94634-115">The current connection status for the device.</span></span> <span data-ttu-id="94634-116">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="94634-116">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="94634-117">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="94634-117">Type: <strong>VT_I4</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="94634-118">La propriété peut avoir les valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="94634-118">The property can have the following possible values.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="94634-119">État de connexion</span><span class="sxs-lookup"><span data-stu-id="94634-119">Connect Status</span></span></th>
<th><span data-ttu-id="94634-120">Définition</span><span class="sxs-lookup"><span data-stu-id="94634-120">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94634-121">WIA_DEVICE_NOT_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="94634-121">WIA_DEVICE_NOT_CONNECTED</span></span></td>
<td><span data-ttu-id="94634-122">L’appareil n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="94634-122">Device is not connected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94634-123">WIA_DEVICE_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="94634-123">WIA_DEVICE_CONNECTED</span></span></td>
<td><span data-ttu-id="94634-124">L’appareil est connecté et opérationnel.</span><span class="sxs-lookup"><span data-stu-id="94634-124">Device is connected and operational.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <span data-ttu-id="94634-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span><span class="sxs-lookup"><span data-stu-id="94634-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="94634-126">Heure actuelle de l’horloge stockée sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="94634-126">The current clock time that is stored on the device.</span></span> <span data-ttu-id="94634-127">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="94634-127">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="94634-128">Type : <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="94634-128">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong>, Access: Read/Write or Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="94634-129">Cette propriété est prise en charge uniquement par les appareils qui ont une horloge interne.</span><span class="sxs-lookup"><span data-stu-id="94634-129">This property is supported only by devices that have an internal clock.</span></span> <span data-ttu-id="94634-130">Si l’horloge de l’appareil peut être définie, cette propriété est en lecture/écriture ; dans le cas contraire, il est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="94634-130">If the device clock can be set, this property is Read/Write; otherwise, it is Read-only.</span></span></p>
<p><span data-ttu-id="94634-131">Les appareils WIA signalent l’heure dans une structure <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SystemTime</a> .</span><span class="sxs-lookup"><span data-stu-id="94634-131">WIA devices report time in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <span data-ttu-id="94634-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="94634-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="94634-133">Version du microprogramme de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="94634-133">The device firmware version.</span></span> <span data-ttu-id="94634-134">Cette valeur doit être une valeur de chaîne, telle que &quot; 1.0.4 &quot; ou &quot; 1.0 ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="94634-134">This value must be a string value, such as &quot;1.0.4&quot; or &quot;1.0abc&quot;.</span></span> <span data-ttu-id="94634-135">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="94634-135">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="94634-136">Si le minipilote WIA ne fournit pas de ressource de version, le service WIA fournit la valeur &quot; 0.0.0.0 &quot; comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="94634-136">If the WIA minidriver does not supply a version resource, the WIA service supplies the value &quot;0.0.0.0&quot; as a default.</span></span> <span data-ttu-id="94634-137">Une application lit cette propriété pour déterminer la version de la DLL du minipilote WIA.</span><span class="sxs-lookup"><span data-stu-id="94634-137">An application reads this property to determine the version of the WIA minidriver DLL.</span></span></p>
<p><span data-ttu-id="94634-138">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="94634-138">Type: <strong>VT_BSTR</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="94634-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94634-139">Requirements</span></span>



| <span data-ttu-id="94634-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94634-140">Requirement</span></span> | <span data-ttu-id="94634-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="94634-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94634-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94634-142">Minimum supported client</span></span><br/> | <span data-ttu-id="94634-143">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94634-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="94634-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94634-144">Minimum supported server</span></span><br/> | <span data-ttu-id="94634-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94634-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="94634-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="94634-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="94634-147"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="94634-147"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
