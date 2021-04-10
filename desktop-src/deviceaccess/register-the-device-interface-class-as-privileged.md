---
title: Inscrire l’interface de l’appareil comme restreint aux applications privilégiées
description: Cette rubrique montre comment ajouter la propriété Restricted qui indique que seules les applications privilégiées peuvent accéder à une classe d’interface d’appareil.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: e23f8b7f2cc1884e2f878739f56507e79eb1bb69
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032054"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a><span data-ttu-id="34b8b-103">Inscrire l’interface de l’appareil comme restreint aux applications privilégiées</span><span class="sxs-lookup"><span data-stu-id="34b8b-103">Register the device interface as restricted to privileged apps</span></span>

<span data-ttu-id="34b8b-104">L’accès aux fonctionnalités du pilote personnalisé est refusé aux applications, à moins qu’elles reçoivent des autorisations via des métadonnées de périphérique signées.</span><span class="sxs-lookup"><span data-stu-id="34b8b-104">Applications are denied access to custom driver functionality, unless they're granted permissions through signed device metadata.</span></span> <span data-ttu-id="34b8b-105">Cette rubrique montre comment ajouter la propriété **Restricted** qui indique que seules les applications privilégiées peuvent accéder à une classe d’interface d’appareil.</span><span class="sxs-lookup"><span data-stu-id="34b8b-105">This topic shows how to add the **Restricted** property that indicates that only privileged apps can access a device interface class.</span></span> <span data-ttu-id="34b8b-106">Les pilotes de périphérique personnalisés doivent avoir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="34b8b-106">Custom device drivers must have this property.</span></span>

## <a name="instructions"></a><span data-ttu-id="34b8b-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="34b8b-107">Instructions</span></span>

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a><span data-ttu-id="34b8b-108">Définition de la propriété Restricted dans un fichier d’informations (INF)</span><span class="sxs-lookup"><span data-stu-id="34b8b-108">Setting the Restricted property in an information (INF) file</span></span>

<span data-ttu-id="34b8b-109">Dans la `InterfaceInstall32` section, le GUID de la classe d’interface d’appareil est inscrit.</span><span class="sxs-lookup"><span data-stu-id="34b8b-109">In the `InterfaceInstall32` section, the GUID of the device interface class is registered.</span></span>

<span data-ttu-id="34b8b-110">Les lignes de la directive **AddProperty** définissent les propriétés de la classe de périphérique.</span><span class="sxs-lookup"><span data-stu-id="34b8b-110">The lines under the **AddProperty** directive set the device class properties.</span></span> <span data-ttu-id="34b8b-111">La deuxième ligne définit une propriété personnalisée dans une catégorie de propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="34b8b-111">The second line sets a custom property in a custom property category.</span></span> <span data-ttu-id="34b8b-112">Le GUID de la catégorie de propriété est **14c83a99-0B3F-44b7-BE4C-a178d3990564** et l’identificateur de propriété est **2**.</span><span class="sxs-lookup"><span data-stu-id="34b8b-112">The property-category GUID is **14c83a99-0b3f-44b7-be4c-a178d3990564**, and the property identifier is **2**.</span></span> <span data-ttu-id="34b8b-113">La `Flags` valeur d’entrée facultative n’est pas présente et le type est **17** (**DEVPROP_TYPE_BOOLEAN**).</span><span class="sxs-lookup"><span data-stu-id="34b8b-113">The optional `Flags` entry value is not present, and the type is **17** (**DEVPROP_TYPE_BOOLEAN**).</span></span> <span data-ttu-id="34b8b-114">La valeur de la propriété est **1**.</span><span class="sxs-lookup"><span data-stu-id="34b8b-114">The value of the property is **1**.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="34b8b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="34b8b-115">Remarks</span></span>

<span data-ttu-id="34b8b-116">Au lieu de la directive **AddInterface** , le pilote peut également appeler la routine [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) pour inscrire la classe d’interface de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="34b8b-116">Instead of the **AddInterface** directive, the driver can also call the [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine to register the device interface class.</span></span>

<span data-ttu-id="34b8b-117">Vous pouvez également définir la propriété d’interface restreinte en appelant la routine [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .</span><span class="sxs-lookup"><span data-stu-id="34b8b-117">You can also set the restricted interface property by calling the [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34b8b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34b8b-118">Related topics</span></span>

<span data-ttu-id="34b8b-119">[Exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications pour appareils UWP pour appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="34b8b-119">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
