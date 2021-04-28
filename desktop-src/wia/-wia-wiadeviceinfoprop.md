---
description: 'Constantes de propriété d’informations sur l’appareil : les propriétés des informations de périphérique sont des propriétés qui décrivent la configuration et l’installation de l’appareil.'
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Constantes de propriété d’informations sur l’appareil (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aec37ae84eed6b15bc10a4e979a5d95d21be3423
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097237"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="0f2e4-103">Constantes de propriété d’informations sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="0f2e4-103">Device Information Property Constants</span></span>

<span data-ttu-id="0f2e4-104">Les propriétés d’informations de périphérique sont des propriétés qui décrivent l’installation et l’installation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="0f2e4-105">Ces propriétés sont disponibles par le biais des interfaces [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , ainsi que par le biais de l’élément racine.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="0f2e4-106">Les propriétés d’informations sur l’appareil sont précédées de « WIA \_ DIP \_ » (propriété d’informations de périphérique) et sont fournies par l’acquisition d’image Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="0f2e4-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="0f2e4-107">À des fins de script, ces constantes utilisent le préfixe « DeviceInfo » et font partie du type énuméré [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="0f2e4-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="0f2e4-108">Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0f2e4-109">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="0f2e4-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0f2e4-110">Description</span><span class="sxs-lookup"><span data-stu-id="0f2e4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="0f2e4-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f2e4-112">Chaîne d’ID de l’appareil pour le minipilote WIA.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="0f2e4-113">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="0f2e4-114">Type : VT_BSTR, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="0f2e4-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f2e4-116">Chaîne de description du fournisseur pour le minipilote WIA.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="0f2e4-117">La description du fournisseur est obtenue à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="0f2e4-118">Une application lit cette propriété pour obtenir une description du fournisseur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="0f2e4-119">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="0f2e4-120">Type : VT_BSTR, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="0f2e4-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f2e4-122">Chaîne de description de l’appareil pour le minipilote WIA.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="0f2e4-123">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-124">La chaîne de description de l’appareil que cette propriété contient est obtenue à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="0f2e4-125">Une application lit cette propriété pour obtenir une description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="0f2e4-126">Type : VT_BSTR, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="0f2e4-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f2e4-128">Type d’appareil et sous-type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-128">The device type and device subtype.</span></span> <span data-ttu-id="0f2e4-129">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-130">Utilisez la macro GET_STIDEVICE_TYPE pour récupérer le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="0f2e4-131">Le type et le sous-type d’appareil sont obtenus à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="0f2e4-132">Une application lit cette propriété pour déterminer si elle utilise un scanneur, un appareil photo ou un périphérique vidéo.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="0f2e4-133">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="0f2e4-134">Actuellement, les types d’appareils sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="0f2e4-135">L’astérisque \* indique que le type d’appareil n’est pas pris en charge par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="0f2e4-136">Le double astérisque \* \* indique que le type d’appareil n’est pas pris en charge par Windows Server 2003, Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0f2e4-137">Type</span><span class="sxs-lookup"><span data-stu-id="0f2e4-137">Type</span></span></th>
<th><span data-ttu-id="0f2e4-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f2e4-138">Value</span></span></th>
<th><span data-ttu-id="0f2e4-139">Définition</span><span class="sxs-lookup"><span data-stu-id="0f2e4-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f2e4-140">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="0f2e4-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="0f2e4-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="0f2e4-141">0x0000</span></span></td>
<td><span data-ttu-id="0f2e4-142">Appareil par défaut</span><span class="sxs-lookup"><span data-stu-id="0f2e4-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f2e4-143">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="0f2e4-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="0f2e4-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="0f2e4-144">0x0001</span></span></td>
<td><span data-ttu-id="0f2e4-145">Périphérique scanneur (voir le <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> pour déterminer si le scanneur est à plat ou feuille.)</span><span class="sxs-lookup"><span data-stu-id="0f2e4-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f2e4-146">StiDeviceTypeDigitalCamera\*</span><span class="sxs-lookup"><span data-stu-id="0f2e4-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="0f2e4-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="0f2e4-147">0x0002</span></span></td>
<td><span data-ttu-id="0f2e4-148">Appareil photo</span><span class="sxs-lookup"><span data-stu-id="0f2e4-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f2e4-149">StiDeviceTypeStreamingVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="0f2e4-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="0f2e4-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="0f2e4-150">0x0003</span></span></td>
<td><span data-ttu-id="0f2e4-151">Périphérique vidéo</span><span class="sxs-lookup"><span data-stu-id="0f2e4-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="0f2e4-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-153">Nom du port de l’appareil installé, affecté par le pilote en mode noyau qui exécute l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="0f2e4-154">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-155">Une application lit cette propriété pour déterminer le nom du port.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="0f2e4-156">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="0f2e4-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-158">Nom de l’appareil</span><span class="sxs-lookup"><span data-stu-id="0f2e4-158">The name of the device.</span></span> <span data-ttu-id="0f2e4-159">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-160">Le nom de l’appareil contenu dans cette propriété est obtenu à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="0f2e4-161">Une application lit cette propriété pour obtenir le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="0f2e4-162">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="0f2e4-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-164">Nom du serveur sur lequel s’exécute le minipilote WIA.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="0f2e4-165">Cette propriété est facultative pour Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="0f2e4-166">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="0f2e4-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-168">L’ID d’appareil de l’appareil WIA qui est installé sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="0f2e4-169">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-170">Elle est utilisée uniquement en interne par le service WIA.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="0f2e4-171">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="0f2e4-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-173">CLSID fourni par le fournisseur pour tout objet COM d’extension d’interface utilisateur installé avec le minipilote WIA.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="0f2e4-174">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-175">La valeur du CLSID de l’interface utilisateur contenue dans cette propriété est obtenue à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="0f2e4-176">Si aucun CLSID d’interface utilisateur n’est spécifié, le service WIA fournit une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="0f2e4-177">Cette propriété est utilisée uniquement en interne par le service WIA lorsque l’interface utilisateur est affichée.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="0f2e4-178">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="0f2e4-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-180">Type de connexion utilisé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-180">The type of connection that the device is using.</span></span> <span data-ttu-id="0f2e4-181">Le service WIA crée et gère cette propriété, et seul le service WIA peut la modifier.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="0f2e4-182">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0f2e4-183">La propriété peut avoir les valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0f2e4-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f2e4-184">Value</span></span></th>
<th><span data-ttu-id="0f2e4-185">Définition</span><span class="sxs-lookup"><span data-stu-id="0f2e4-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f2e4-186">1</span><span class="sxs-lookup"><span data-stu-id="0f2e4-186">1</span></span></td>
<td><span data-ttu-id="0f2e4-187">Périphérique WDM générique</span><span class="sxs-lookup"><span data-stu-id="0f2e4-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f2e4-188">2</span><span class="sxs-lookup"><span data-stu-id="0f2e4-188">2</span></span></td>
<td><span data-ttu-id="0f2e4-189">Périphérique SCSI</span><span class="sxs-lookup"><span data-stu-id="0f2e4-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f2e4-190">4</span><span class="sxs-lookup"><span data-stu-id="0f2e4-190">4</span></span></td>
<td><span data-ttu-id="0f2e4-191">Périphérique USB</span><span class="sxs-lookup"><span data-stu-id="0f2e4-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f2e4-192">8</span><span class="sxs-lookup"><span data-stu-id="0f2e4-192">8</span></span></td>
<td><span data-ttu-id="0f2e4-193">Appareil série</span><span class="sxs-lookup"><span data-stu-id="0f2e4-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f2e4-194">16</span><span class="sxs-lookup"><span data-stu-id="0f2e4-194">16</span></span></td>
<td><span data-ttu-id="0f2e4-195">Appareil parallèle</span><span class="sxs-lookup"><span data-stu-id="0f2e4-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="0f2e4-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-197">Paramètre de vitesse en bauds actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="0f2e4-198">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-199">La valeur doit être &quot; vide &quot; si l’appareil n’est pas connecté par un câble série.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="0f2e4-200">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="0f2e4-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-202">Les fonctionnalités STI génériques pour l’appareil obtenues à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="0f2e4-203">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-204">Une application lit cette propriété pour déterminer les fonctionnalités de STI génériques de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="0f2e4-205">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="0f2e4-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-207">Nombre (sous forme de chaîne) de la version WIA actuelle qui est installée sur le système.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="0f2e4-208">Une application lit cette propriété pour déterminer la version de WIA qui est installée sur le système.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="0f2e4-209">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-210">Cette propriété est disponible dans Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="0f2e4-211">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="0f2e4-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-213">Version actuelle de la DLL du minipilote WIA.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="0f2e4-214">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-215">Cette propriété est disponible dans Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="0f2e4-216">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="0f2e4-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-218">ID PnP actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-218">The current PnP id for the device.</span></span> <span data-ttu-id="0f2e4-219">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-220">Cette propriété est disponible dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="0f2e4-221">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="0f2e4-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="0f2e4-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0f2e4-223">Version du pilote STI générique.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-223">The generic STI driver version.</span></span> <span data-ttu-id="0f2e4-224">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="0f2e4-225">Une application lit cette propriété pour déterminer la version du pilote STI générique.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="0f2e4-226">Cette propriété est disponible dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f2e4-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="0f2e4-227">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0f2e4-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="0f2e4-228">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f2e4-228">Requirements</span></span>



| <span data-ttu-id="0f2e4-229">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f2e4-229">Requirement</span></span> | <span data-ttu-id="0f2e4-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f2e4-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f2e4-231">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f2e4-231">Minimum supported client</span></span><br/> | <span data-ttu-id="0f2e4-232">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f2e4-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0f2e4-233">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f2e4-233">Minimum supported server</span></span><br/> | <span data-ttu-id="0f2e4-234">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f2e4-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f2e4-235">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f2e4-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f2e4-236"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f2e4-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




