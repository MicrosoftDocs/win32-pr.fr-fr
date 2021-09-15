---
title: Inscrire l’interface de l’appareil comme restreint aux applications privilégiées
description: Cette rubrique montre comment ajouter la propriété Restricted qui indique que seules les applications privilégiées peuvent accéder à une classe d’interface d’appareil.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: e23f8b7f2cc1884e2f878739f56507e79eb1bb69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521781"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Inscrire l’interface de l’appareil comme restreint aux applications privilégiées

L’accès aux fonctionnalités du pilote personnalisé est refusé aux applications, à moins qu’elles reçoivent des autorisations via des métadonnées de périphérique signées. Cette rubrique montre comment ajouter la propriété **Restricted** qui indique que seules les applications privilégiées peuvent accéder à une classe d’interface d’appareil. Les pilotes de périphérique personnalisés doivent avoir cette propriété.

## <a name="instructions"></a>Instructions

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Définition de la propriété Restricted dans un fichier d’informations (INF)

Dans la `InterfaceInstall32` section, le GUID de la classe d’interface d’appareil est inscrit.

Les lignes de la directive **AddProperty** définissent les propriétés de la classe de périphérique. La deuxième ligne définit une propriété personnalisée dans une catégorie de propriété personnalisée. Le GUID de la catégorie de propriété est **14c83a99-0B3F-44b7-BE4C-a178d3990564** et l’identificateur de propriété est **2**. La `Flags` valeur d’entrée facultative n’est pas présente et le type est **17** (**DEVPROP_TYPE_BOOLEAN**). La valeur de la propriété est **1**.

```Text
; Below, {11111111-0000-1111-0000-111111111111} is the GUID of the
; new device interface class in an AddInterface directive



; -- Interface installation
[InterfaceInstall32]
{11111111-0000-1111-0000-111111111111}=NewInterfaceInstall

[NewInterfaceInstall]
AddProperty=PrivilegedProperties

[PrivilegedProperties]
; DEVPKey_DeviceInterfaceClass_Restricted
{14c83a99-0b3f-44b7-be4c-a178d3990564}, 2, 17,,1 ; -- non-zero indicates privileged
```

## <a name="remarks"></a>Notes

Au lieu de la directive **AddInterface** , le pilote peut également appeler la routine [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) pour inscrire la classe d’interface de l’appareil.

Vous pouvez également définir la propriété d’interface restreinte en appelant la routine [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .

## <a name="related-topics"></a>Rubriques connexes

[exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)
