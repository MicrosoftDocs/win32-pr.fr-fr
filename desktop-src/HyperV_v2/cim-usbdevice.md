---
description: Caractéristiques de gestion d’un périphérique USB.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: Classe CIM_USBDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519047"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="baf4a-103">Classe CIM_USBDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="baf4a-103">CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="baf4a-104">Caractéristiques de gestion d’un périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="baf4a-104">The management characteristics of a USB device.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf4a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="baf4a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a><span data-ttu-id="baf4a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="baf4a-106">Members</span></span>

<span data-ttu-id="baf4a-107">La classe **CIM \_ USBDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="baf4a-107">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="baf4a-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="baf4a-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="baf4a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="baf4a-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="baf4a-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="baf4a-110">Methods</span></span>

<span data-ttu-id="baf4a-111">La classe **CIM \_ USBDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="baf4a-111">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="baf4a-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="baf4a-112">Method</span></span>                                               | <span data-ttu-id="baf4a-113">Description</span><span class="sxs-lookup"><span data-stu-id="baf4a-113">Description</span></span>                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [<span data-ttu-id="baf4a-114">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="baf4a-114">**GetDescriptor**</span></span>](cim-usbdevice-getdescriptor.md) | <span data-ttu-id="baf4a-115">Récupère un descripteur de périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="baf4a-115">Retrieves a USB device descriptor.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="baf4a-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="baf4a-116">Properties</span></span>

<span data-ttu-id="baf4a-117">La classe **CIM \_ USBDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="baf4a-117">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="baf4a-118">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="baf4a-118">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-119">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="baf4a-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-121">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bDeviceClass")</span><span class="sxs-lookup"><span data-stu-id="baf4a-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceClass")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-122">Code de la classe USB.</span><span class="sxs-lookup"><span data-stu-id="baf4a-122">The USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-123">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="baf4a-123">**CommandTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-124">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="baf4a-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-126">Intervalle de délai d’attente configurable par les applications de gestion qui prennent en charge la redirection USB.</span><span class="sxs-lookup"><span data-stu-id="baf4a-126">A timeout interval that is configurable by management applications that support USB redirection.</span></span> <span data-ttu-id="baf4a-127">Lorsque le service de redirection redirige une commande de périphérique USB vers un périphérique distant et que le périphérique distant ne répond pas avant l’intervalle de délai d’attente, le service de redirection émule un événement d’éjection de support.</span><span class="sxs-lookup"><span data-stu-id="baf4a-127">When the redirection service redirects a USB device command to a remote device, and the remote device does not respond before timeout interval, the redirection service will emulate a media eject event.</span></span> <span data-ttu-id="baf4a-128">En outre, le service peut essayer à nouveau la commande ou essayer de rétablir la connexion au périphérique distant.</span><span class="sxs-lookup"><span data-stu-id="baf4a-128">In addition, the service may re-try the command or try to re-establish the connection to the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-129">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="baf4a-129">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-130">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="baf4a-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-132">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="baf4a-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-133">Tableau qui contient les autres paramètres pour chaque interface dans la configuration actuelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="baf4a-133">An array that contains the alternate settings for each interface in the current configuration of the device.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-134">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="baf4a-134">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-135">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="baf4a-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-137">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="baf4a-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-138">Configuration actuellement sélectionnée pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="baf4a-138">The configuration currently selected for the device.</span></span> <span data-ttu-id="baf4a-139">Si cette valeur est égale à zéro, l’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="baf4a-139">If this value is zero, the Device is not configured.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-140">**DeviceReleaseNumber**</span><span class="sxs-lookup"><span data-stu-id="baf4a-140">**DeviceReleaseNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-141">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="baf4a-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-143">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bcdDevice")</span><span class="sxs-lookup"><span data-stu-id="baf4a-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdDevice")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-144">Numéro de version de l’appareil au format BCD.</span><span class="sxs-lookup"><span data-stu-id="baf4a-144">The device release number in BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-145">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="baf4a-145">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="baf4a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| iManufacturer")</span><span class="sxs-lookup"><span data-stu-id="baf4a-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iManufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-149">Chaîne du fabricant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="baf4a-149">The manufacturer string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-150">**MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="baf4a-150">**MaxPacketSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-151">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="baf4a-151">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-153">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bMaxPacketSize")</span><span class="sxs-lookup"><span data-stu-id="baf4a-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bMaxPacketSize")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-154">Taille de paquet maximale pour le point de terminaison de zéro USB.</span><span class="sxs-lookup"><span data-stu-id="baf4a-154">The maximum packet size for the USB zero endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-155">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="baf4a-155">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-156">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="baf4a-156">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-158">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bNumConfigurations")</span><span class="sxs-lookup"><span data-stu-id="baf4a-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bNumConfigurations")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-159">Nombre de configurations d’appareil définies pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="baf4a-159">The number of device configurations that are defined for the Device.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-160">**Produit**</span><span class="sxs-lookup"><span data-stu-id="baf4a-160">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="baf4a-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-163">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| iProduct")</span><span class="sxs-lookup"><span data-stu-id="baf4a-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iProduct")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-164">Chaîne de produit de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="baf4a-164">The product string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-165">**IDProduit**</span><span class="sxs-lookup"><span data-stu-id="baf4a-165">**ProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-166">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="baf4a-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-168">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| idProduct")</span><span class="sxs-lookup"><span data-stu-id="baf4a-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idProduct")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-169">ID de produit affecté à l’appareil par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="baf4a-169">The product ID assigned to the device by manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-170">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="baf4a-170">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-171">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="baf4a-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-173">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bDeviceProtocol")</span><span class="sxs-lookup"><span data-stu-id="baf4a-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-174">Code du protocole USB.</span><span class="sxs-lookup"><span data-stu-id="baf4a-174">The USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-175">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="baf4a-175">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="baf4a-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-178">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| iSerialNumber")</span><span class="sxs-lookup"><span data-stu-id="baf4a-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iSerialNumber")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-179">Numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="baf4a-179">The serial number of the device.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-180">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="baf4a-180">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-181">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="baf4a-181">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-183">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bDeviceSubClass")</span><span class="sxs-lookup"><span data-stu-id="baf4a-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceSubClass")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-184">Code de sous-classe USB.</span><span class="sxs-lookup"><span data-stu-id="baf4a-184">The USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-185">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="baf4a-185">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-186">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="baf4a-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-188">Version USB la plus récente prise en charge par le périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="baf4a-188">The latest USB Version supported by the USB Device.</span></span> <span data-ttu-id="baf4a-189">La propriété est exprimée sous la forme d’une valeur décimale codée binaire (BCD) qui contient une virgule décimale entre le 2e et le 3e chiffre.</span><span class="sxs-lookup"><span data-stu-id="baf4a-189">The property is expressed as a binary-coded decimal (BCD) that contains a decimal point between the 2nd and 3rd digits.</span></span> <span data-ttu-id="baf4a-190">Par exemple, la valeur 0x201 indique que la version 2,01 est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="baf4a-190">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-191">**USBVersionInBCD**</span><span class="sxs-lookup"><span data-stu-id="baf4a-191">**USBVersionInBCD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-192">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="baf4a-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-194">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bcdUSB")</span><span class="sxs-lookup"><span data-stu-id="baf4a-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdUSB")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-195">Numéro de la spécification USB avec lequel l’appareil est conforme.</span><span class="sxs-lookup"><span data-stu-id="baf4a-195">The USB specification number that the device complies with.</span></span> <span data-ttu-id="baf4a-196">Cette propriété est mise en forme avec le format BCD.</span><span class="sxs-lookup"><span data-stu-id="baf4a-196">This property is formatted with BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="baf4a-197">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="baf4a-197">**VendorID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baf4a-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="baf4a-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baf4a-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baf4a-200">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| idVendor")</span><span class="sxs-lookup"><span data-stu-id="baf4a-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idVendor")</span></span>
</dt> </dl>

<span data-ttu-id="baf4a-201">ID de fournisseur affecté à l’appareil par USB.org.</span><span class="sxs-lookup"><span data-stu-id="baf4a-201">The vendor ID assigned to the device by USB.org.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="baf4a-202">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="baf4a-202">Requirements</span></span>



| <span data-ttu-id="baf4a-203">Condition requise</span><span class="sxs-lookup"><span data-stu-id="baf4a-203">Requirement</span></span> | <span data-ttu-id="baf4a-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="baf4a-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baf4a-205">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="baf4a-205">Minimum supported client</span></span><br/> | <span data-ttu-id="baf4a-206">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="baf4a-206">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="baf4a-207">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="baf4a-207">Minimum supported server</span></span><br/> | <span data-ttu-id="baf4a-208">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="baf4a-208">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="baf4a-209">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="baf4a-209">Namespace</span></span><br/>                | <span data-ttu-id="baf4a-210">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="baf4a-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="baf4a-211">MOF</span><span class="sxs-lookup"><span data-stu-id="baf4a-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="baf4a-212"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="baf4a-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="baf4a-213">DLL</span><span class="sxs-lookup"><span data-stu-id="baf4a-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baf4a-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="baf4a-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="baf4a-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baf4a-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf4a-216">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="baf4a-216">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

