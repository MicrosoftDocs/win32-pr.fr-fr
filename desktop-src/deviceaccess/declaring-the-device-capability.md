---
title: Déclaration de la fonctionnalité de l’appareil
description: Cette rubrique explique comment déclarer le GUID des fonctionnalités de l’appareil.
ms.assetid: C663F8D2-2CB6-4C3C-A1EB-A3D93AA71FC8
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 0b1f98717c7e9487874aa71691beefbac635660a
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103941452"
---
# <a name="declaring-the-device-capability"></a><span data-ttu-id="49377-103">Déclaration de la fonctionnalité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="49377-103">Declaring the Device Capability</span></span>

<span data-ttu-id="49377-104">Cette rubrique explique comment déclarer le GUID des fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="49377-104">This topic explains how to declare the device capability GUID.</span></span> <span data-ttu-id="49377-105">Toutes les applications qui ciblent des pilotes personnalisés doivent déclarer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="49377-105">All applications that target custom drivers must declare this capability.</span></span>

<span data-ttu-id="49377-106">Dans votre manifeste d’application, vous devez ajouter une fonctionnalité de périphérique, comme suit :</span><span class="sxs-lookup"><span data-stu-id="49377-106">In your application manifest, you'll need to add a device capability, as follows:</span></span>

<span data-ttu-id="49377-107">Il s’agit d’un exemple de déclaration de fonctionnalité pour un appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="49377-107">This is an example of a capability declaration for a custom device.</span></span> <span data-ttu-id="49377-108">Le GUID est le GUID de la classe d’interface de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="49377-108">The GUID is the GUID of the device interface class.</span></span>

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a><span data-ttu-id="49377-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49377-109">Related topics</span></span>

<span data-ttu-id="49377-110">[Exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications pour appareils UWP pour appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="49377-110">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
