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
ms.openlocfilehash: 3766d6c2fdc46b36350e9259e0e988f3a276cee6376d02de349abbe83bf8031b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427729"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a>Classe CIM_USBDevice (gestion Hyper-V)

Caractéristiques de gestion d’un périphérique USB.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe **CIM \_ USBDevice** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **CIM \_ USBDevice** possède ces méthodes.



| Méthode                                               | Description                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**GetDescriptor**](cim-usbdevice-getdescriptor.md) | Récupère un descripteur de périphérique USB.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **CIM \_ USBDevice** possède les propriétés suivantes.

<dl> <dt>

**ClassCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bDeviceClass")
</dt> </dl>

Code de la classe USB.

</dd> <dt>

**CommandTimeout**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de délai d’attente configurable par les applications de gestion qui prennent en charge la redirection USB. Lorsque le service de redirection redirige une commande de périphérique USB vers un périphérique distant et que le périphérique distant ne répond pas avant l’intervalle de délai d’attente, le service de redirection émule un événement d’éjection de support. En outre, le service peut essayer à nouveau la commande ou essayer de rétablir la connexion au périphérique distant.

</dd> <dt>

**CurrentAlternateSettings**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")
</dt> </dl>

Tableau qui contient les autres paramètres pour chaque interface dans la configuration actuelle de l’appareil.

</dd> <dt>

**CurrentConfigValue**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")
</dt> </dl>

Configuration actuellement sélectionnée pour l’appareil. Si cette valeur est égale à zéro, l’appareil n’est pas configuré.

</dd> <dt>

**DeviceReleaseNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bcdDevice")
</dt> </dl>

Numéro de version de l’appareil au format BCD.

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| iManufacturer")
</dt> </dl>

Chaîne du fabricant de l’appareil.

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bMaxPacketSize")
</dt> </dl>

Taille de paquet maximale pour le point de terminaison de zéro USB.

</dd> <dt>

**NumberOfConfigs**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bNumConfigurations")
</dt> </dl>

Nombre de configurations d’appareil définies pour l’appareil.

</dd> <dt>

**Produit**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| iProduct")
</dt> </dl>

Chaîne de produit de l’appareil.

</dd> <dt>

**IDProduit**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| idProduct")
</dt> </dl>

ID de produit affecté à l’appareil par le fabricant.

</dd> <dt>

**ProtocolCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bDeviceProtocol")
</dt> </dl>

Code du protocole USB.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| iSerialNumber")
</dt> </dl>

Numéro de série de l’appareil.

</dd> <dt>

**SubclassCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bDeviceSubClass")
</dt> </dl>

Code de sous-classe USB.

</dd> <dt>

**USBVersion**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version USB la plus récente prise en charge par le périphérique USB. La propriété est exprimée sous la forme d’une valeur décimale codée binaire (BCD) qui contient une virgule décimale entre le 2e et le 3e chiffre. Par exemple, la valeur 0x201 indique que la version 2,01 est prise en charge.

</dd> <dt>

**USBVersionInBCD**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| bcdUSB")
</dt> </dl>

Numéro de la spécification USB avec lequel l’appareil est conforme. Cette propriété est mise en forme avec le format BCD.

</dd> <dt>

**VendorID**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("spécification du bus de série universel. USB-if \| standard descripteur de l’appareil \| idVendor")
</dt> </dl>

ID de fournisseur affecté à l’appareil par USB.org.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

