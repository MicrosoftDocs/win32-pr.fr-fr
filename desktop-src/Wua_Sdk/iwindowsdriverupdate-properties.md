---
description: L’interface IWindowsDriverUpdate définit les propriétés suivantes.
ms.assetid: 2177c5e0-47db-44ae-a0ce-2544ff2d0855
title: Propriétés IWindowsDriverUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291d7933cf3e73dee6f47edab3240c4ebd14f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515874"
---
# <a name="iwindowsdriverupdate-properties"></a><span data-ttu-id="42f76-103">Propriétés IWindowsDriverUpdate</span><span class="sxs-lookup"><span data-stu-id="42f76-103">IWindowsDriverUpdate Properties</span></span>

<span data-ttu-id="42f76-104">L’interface [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="42f76-104">The [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="42f76-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="42f76-105">Property</span></span>                                                                                                    | <span data-ttu-id="42f76-106">Description</span><span class="sxs-lookup"><span data-stu-id="42f76-106">Description</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f76-107">[](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Adresse** DeviceProblemNumber](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span><span class="sxs-lookup"><span data-stu-id="42f76-107">[**DeviceProblemNumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Address**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span></span> | <span data-ttu-id="42f76-108">Obtient le numéro de problème de l’appareil correspondant à la mise à jour du pilote Windows.</span><span class="sxs-lookup"><span data-stu-id="42f76-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                     |
| [<span data-ttu-id="42f76-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="42f76-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_devicestatus)                                                   | <span data-ttu-id="42f76-110">Obtient l’état de l’appareil correspondant à la mise à jour du pilote Windows.</span><span class="sxs-lookup"><span data-stu-id="42f76-110">Gets the status of the device that matches for the Windows driver update.</span></span>                             |
| [<span data-ttu-id="42f76-111">**DriverClass**</span><span class="sxs-lookup"><span data-stu-id="42f76-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverclass)                                                     | <span data-ttu-id="42f76-112">Obtient la classe de la mise à jour du pilote Windows.</span><span class="sxs-lookup"><span data-stu-id="42f76-112">Gets the class of the Windows driver update.</span></span>                                                          |
| [<span data-ttu-id="42f76-113">**DriverHardwareID**</span><span class="sxs-lookup"><span data-stu-id="42f76-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverhardwareid)                                           | <span data-ttu-id="42f76-114">Obtient l’ID matériel ou l’ID compatible que la mise à jour du pilote Windows doit mettre en correspondance pour pouvoir être installée.</span><span class="sxs-lookup"><span data-stu-id="42f76-114">Gets the hardware ID or compatible ID that the Windows driver update must match to be installable.</span></span>    |
| [<span data-ttu-id="42f76-115">**DriverManufacturer**</span><span class="sxs-lookup"><span data-stu-id="42f76-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermanufacturer)                                       | <span data-ttu-id="42f76-116">Obtient le nom invariant du langage du fabricant de la mise à jour du pilote Windows.</span><span class="sxs-lookup"><span data-stu-id="42f76-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                    |
| [<span data-ttu-id="42f76-117">**DriverModel**</span><span class="sxs-lookup"><span data-stu-id="42f76-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermodel)                                                     | <span data-ttu-id="42f76-118">Obtient le nom de modèle de l’appareil pour lequel la mise à jour du pilote Windows est prévue.</span><span class="sxs-lookup"><span data-stu-id="42f76-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span> |
| [<span data-ttu-id="42f76-119">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="42f76-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverprovider)                                               | <span data-ttu-id="42f76-120">Obtient le nom invariant du langage du fournisseur de la mise à jour du pilote Windows.</span><span class="sxs-lookup"><span data-stu-id="42f76-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                        |
| [<span data-ttu-id="42f76-121">**DriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="42f76-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driververdate)                                                 | <span data-ttu-id="42f76-122">Obtient la date de version du pilote de la mise à jour du pilote Windows.</span><span class="sxs-lookup"><span data-stu-id="42f76-122">Gets the driver version date of the Windows driver update.</span></span>                                            |



 

 

 



