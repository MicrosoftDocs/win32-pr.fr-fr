---
description: Appareils mobiles Windows prend en charge les propriétés d’appareil suivantes.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Propriétés de l’appareil (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 696d5fefd65d194f9bb451b0095ed87b90f8a22c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542401"
---
# <a name="device-properties-portabledeviceh"></a><span data-ttu-id="65992-103">Propriétés de l’appareil (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="65992-103">Device Properties (PortableDevice.h)</span></span>

<span data-ttu-id="65992-104">Appareils mobiles Windows prend en charge les propriétés d’appareil suivantes.</span><span class="sxs-lookup"><span data-stu-id="65992-104">Windows Portable Devices supports the following device properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="65992-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="65992-105">Property</span></span></th>
<th><span data-ttu-id="65992-106">VarType</span><span class="sxs-lookup"><span data-stu-id="65992-106">VarType</span></span></th>
<th><span data-ttu-id="65992-107">Description</span><span class="sxs-lookup"><span data-stu-id="65992-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65992-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span><span class="sxs-lookup"><span data-stu-id="65992-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span></span></td>
<td><span data-ttu-id="65992-109"><strong>VT_DATE</strong></span><span class="sxs-lookup"><span data-stu-id="65992-109"><strong>VT_DATE</strong></span></span></td>
<td><span data-ttu-id="65992-110">Date et heure actuelles sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-110">The current date and time on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span><span class="sxs-lookup"><span data-stu-id="65992-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span></span></td>
<td><span data-ttu-id="65992-112"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="65992-112"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="65992-113">Version du microprogramme de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-113">The device's firmware version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="65992-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="65992-115"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="65992-115"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="65992-116">Identificateur unique de 16 octets qui est commun entre plusieurs transports pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-116">A unique 16-byte identifier that is common across multiple transports supported by the device.</span></span> <span data-ttu-id="65992-117">Si un seul appareil prend en charge plusieurs transports, cette propriété peut être utilisée pour associer les différents pilotes WPD de transport à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-117">If a single device supports multiple transports, this property may be used to associate the various transport WPD drivers with that device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span><span class="sxs-lookup"><span data-stu-id="65992-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span></span></td>
<td><span data-ttu-id="65992-119"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="65992-119"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="65992-120">Nom de fabricant de l’appareil lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65992-120">A human-readable device manufacturer name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span><span class="sxs-lookup"><span data-stu-id="65992-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span></span></td>
<td><span data-ttu-id="65992-122"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="65992-122"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="65992-123">Modèle de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-123">The device model.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="65992-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="65992-125"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="65992-125"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="65992-126">Identificateur unique de 16 octets utilisé pour faire la distinction entre les différents modèles d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-126">A unique 16-byte identifier used to differentiate among different models of a device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span><span class="sxs-lookup"><span data-stu-id="65992-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span></span></td>
<td><span data-ttu-id="65992-128"><strong>VT_UI8</strong></span><span class="sxs-lookup"><span data-stu-id="65992-128"><strong>VT_UI8</strong></span></span></td>
<td><span data-ttu-id="65992-129">Valeur qui spécifie l’identificateur réseau EUI-64 de l’appareil ; Cette propriété est utilisée pour les opérations réseau hors bande. Si l’appareil possède des adresses réseau physiques MAC-48 (en général des réseaux IPv4), l’adresse MAC-48 est encodée dans l’adresse EUI-64, car les deux moitiés de l’adresse MAC-48 sont séparées par FF-FF.</span><span class="sxs-lookup"><span data-stu-id="65992-129">A value that specifies the EUI-64 network identifier of the device; this property is used for out-of-band network operations.If the device has MAC-48 physical network addresses (typical of IPv4 networks), the MAC-48 address is encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span> <span data-ttu-id="65992-130">La valeur EUI-64 est stockée &quot; dans &quot; &quot; un ordre réseau ou Big endian &quot; , où une adresse eui-64 de 01-02-03-ff-ff-04-05-06 serait placée dans le VT_UI8 de manière à ce que la valeur décimale soit 72624942021346566.</span><span class="sxs-lookup"><span data-stu-id="65992-130">The EUI-64 value is stored in &quot;network&quot; or &quot;big-endian&quot; order, where an EUI-64 address of 01-02-03-FF-FF-04-05-06 would be placed in the VT_UI8 such that the decimal value is 72624942021346566.</span></span> <span data-ttu-id="65992-131">Cette propriété est requise sur tous les appareils qui prennent en charge l’authentification nominale ou sécurisée.</span><span class="sxs-lookup"><span data-stu-id="65992-131">This property is required on any device that supports Nominal or Secure Authentication.</span></span> <span data-ttu-id="65992-132">Cette propriété est recommandée sur les appareils qui prennent uniquement en charge l’authentification zéro.</span><span class="sxs-lookup"><span data-stu-id="65992-132">This property is recommended on devices that support only Zero Authentication.</span></span> <span data-ttu-id="65992-133">La valeur peut être utilisée par l’hôte pour établir automatiquement l’accès à l’appareil sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65992-133">The value can be used by the host to automatically establish access to the device without user intervention.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span><span class="sxs-lookup"><span data-stu-id="65992-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span></span></td>
<td><span data-ttu-id="65992-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="65992-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="65992-136">Valeur comprise entre 0 et 100 qui spécifie le niveau de puissance de la batterie de l’appareil, 0 étant aucun et 100 entièrement facturé.</span><span class="sxs-lookup"><span data-stu-id="65992-136">A value from 0 to 100 that specifies the power level of the device's battery, with 0 being none, and 100 being fully charged.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="65992-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span></span></td>
<td><span data-ttu-id="65992-138">VT_UI4</span><span class="sxs-lookup"><span data-stu-id="65992-138">VT_UI4</span></span></td>
<td><span data-ttu-id="65992-139">Énumération <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> qui spécifie la source d’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-139">A <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> enumeration that specifies the power source of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span><span class="sxs-lookup"><span data-stu-id="65992-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span></span></td>
<td><span data-ttu-id="65992-141"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="65992-141"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="65992-142">Protocole d’appareil utilisé.</span><span class="sxs-lookup"><span data-stu-id="65992-142">The device protocol that is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span><span class="sxs-lookup"><span data-stu-id="65992-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span></span></td>
<td><span data-ttu-id="65992-144"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="65992-144"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="65992-145">Numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-145">The device's serial number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span><span class="sxs-lookup"><span data-stu-id="65992-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span></span></td>
<td><span data-ttu-id="65992-147"><strong>VT_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="65992-147"><strong>VT_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="65992-148">Valeur qui spécifie si les formats pris en charge retournés par l’appareil sont dans un ordre de préférence.</span><span class="sxs-lookup"><span data-stu-id="65992-148">A value that specifies whether the supported formats returned from the device are in a preferred order.</span></span> <span data-ttu-id="65992-149">Le premier format de la liste est préféré par l’appareil, tandis que le dernier est le moins recommandé. Les applications peuvent utiliser cette propriété pour déterminer si les formats pris en charge par un appareil sont répertoriés dans un ordre de préférence.</span><span class="sxs-lookup"><span data-stu-id="65992-149">The first format in the list is most preferred by the device, while the last is the least preferred.Applications may use this property to determine whether a device's supported formats are listed in a preferred order.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span><span class="sxs-lookup"><span data-stu-id="65992-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span></span></td>
<td><span data-ttu-id="65992-151"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="65992-151"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="65992-152">Valeur booléenne qui spécifie si les formats pris en charge retournés par l’appareil sont dans un ordre de préférence. autrement dit, le premier format retourné est plus préféré, tandis que le dernier format retourné est le moins recommandé.</span><span class="sxs-lookup"><span data-stu-id="65992-152">A Boolean value that specifies whether the supported formats returned from the device are in a preferred order; that is, the first returned format is most preferred while the last returned format is least preferred.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span><span class="sxs-lookup"><span data-stu-id="65992-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span></span></td>
<td><span data-ttu-id="65992-154"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="65992-154"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="65992-155">Valeur booléenne qui spécifie si l’appareil prend en charge les objets non consommables.</span><span class="sxs-lookup"><span data-stu-id="65992-155">A Boolean value that specifies whether the device supports non-consumable objects.</span></span> <span data-ttu-id="65992-156">Il s’agit d’objets que l’appareil est destiné uniquement à stocker, à ne pas lire ou à utiliser de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="65992-156">These are objects that the device is only meant to store, not play or use in any way.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span><span class="sxs-lookup"><span data-stu-id="65992-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span></span></td>
<td><span data-ttu-id="65992-158"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="65992-158"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="65992-159">Description explicite du <em>partenaire de synchronisation</em>d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-159">A human-readable description of a device's <em>synchronization partner</em>.</span></span> <span data-ttu-id="65992-160">Il s’agit d’un périphérique, d’une application ou d’un serveur avec lequel l’appareil communique pour maintenir un État commun ou un groupe de fichiers entre les deux partenaires.</span><span class="sxs-lookup"><span data-stu-id="65992-160">This is a device, application, or server that the device communicates with to maintain a common state or group of files between both partners.</span></span> <span data-ttu-id="65992-161">Les programmes de messagerie électronique et les bibliothèques musicales en sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="65992-161">Examples include e-mail programs and music libraries.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="65992-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span></span></td>
<td><span data-ttu-id="65992-163"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="65992-163"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="65992-164">Valeur qui représente le nom convivial défini par l’utilisateur sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-164">A value that represents the friendly name set by the user on the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span><span class="sxs-lookup"><span data-stu-id="65992-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span></span></td>
<td><span data-ttu-id="65992-166"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="65992-166"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="65992-167">transport pris en charge par l’appareil, tel que USB, IP ou Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="65992-167">the transport supported by the device, such as USB, IP, or Bluetooth.</span></span> <span data-ttu-id="65992-168">Les valeurs valides sont du type d’énumération <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="65992-168">Valid values are of the <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> enumeration type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65992-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="65992-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span></span></td>
<td><span data-ttu-id="65992-170"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="65992-170"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="65992-171">Valeur qui spécifie le type d’appareil ; les applications utilisent cette propriété à des fins de représentation uniquement.</span><span class="sxs-lookup"><span data-stu-id="65992-171">A value that specifies the device type; applications use this property for representation purposes only.</span></span> <span data-ttu-id="65992-172">Les caractéristiques fonctionnelles de l’appareil sont choisies par le biais d’objets fonctionnels. Les appareils qui ne fournissent pas d’icône d’appareil, par exemple, une <strong>WPD_RESOURCE_ICON</strong> pour l’objet appareil, sont représentés dans l’espace de noms wpd avec une icône générique.</span><span class="sxs-lookup"><span data-stu-id="65992-172">Functional characteristics of the device are decided through functional objects.Devices that do not supply a device icon, for example, a <strong>WPD_RESOURCE_ICON</strong> for the device object, will be represented in the WPD Namespace with a generic icon.</span></span> <span data-ttu-id="65992-173">Cette icône dépend du type de périphérique spécifié, par exemple, si le type d’appareil est un téléphone mobile, l’icône de téléphone générique est utilisée.</span><span class="sxs-lookup"><span data-stu-id="65992-173">This icon will depend on the specified device type, for example, if the device type is a mobile phone, the generic phone icon is used.</span></span> <span data-ttu-id="65992-174">Lors de la première installation de l’appareil, le programme d’installation de la classe WPD interroge cette valeur de propriété et le stocke dans le registre de l’appareil sous la valeur PORTABLE_DEVICE_TYPE en tant que REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="65992-174">On first install of the device, the WPD Class Installer will query this property value and store it in the device registry under the PORTABLE_DEVICE_TYPE value as a REG_DWORD.</span></span><br/> <span data-ttu-id="65992-175">Les valeurs possibles de ce paramètre proviennent de l’énumération <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> définie dans PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="65992-175">This parameter's possible values are from the <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="65992-176">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="65992-176">Values are:</span></span><br/> <dl> <span data-ttu-id="65992-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span><span class="sxs-lookup"><span data-stu-id="65992-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span></span><br /><span data-ttu-id="65992-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span><span class="sxs-lookup"><span data-stu-id="65992-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span></span><br /><span data-ttu-id="65992-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span><span class="sxs-lookup"><span data-stu-id="65992-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span></span><br /><span data-ttu-id="65992-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span><span class="sxs-lookup"><span data-stu-id="65992-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span></span><br /><span data-ttu-id="65992-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="65992-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span></span><br /><span data-ttu-id="65992-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span><span class="sxs-lookup"><span data-stu-id="65992-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span></span><br /><span data-ttu-id="65992-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span><span class="sxs-lookup"><span data-stu-id="65992-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65992-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span><span class="sxs-lookup"><span data-stu-id="65992-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span></span></td>
<td><span data-ttu-id="65992-185"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="65992-185"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="65992-186">Si cette propriété existe et qu’elle a la valeur <strong>true</strong>, l’appareil peut être utilisé avec l’étape de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65992-186">If this property exists and is set to <strong>TRUE</strong>, the device can be used with Device Stage .</span></span> <span data-ttu-id="65992-187">Cela est destiné aux appareils qui ne peuvent pas stocker les métadonnées à l’aide de l' <strong>Metadata service d’appareil</strong>, mais qui fournissent des métadonnées sur les serveurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="65992-187">This is meant for devices that cannot store metadata using the <strong>Device Metadata Service</strong>, but will provide metadata on the Microsoft servers.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="65992-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65992-188">Requirements</span></span>



| <span data-ttu-id="65992-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65992-189">Requirement</span></span> | <span data-ttu-id="65992-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="65992-190">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="65992-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="65992-191">Header</span></span><br/> | <dl> <span data-ttu-id="65992-192"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="65992-192"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65992-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65992-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65992-194">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="65992-194">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




