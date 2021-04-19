---
description: Les spécificateurs de type d’appareil WIA (Windows Image Acquisition) sont des constantes qui indiquent le type d’appareil attaché à l’ordinateur d’un utilisateur.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Spécificateurs de type d’appareil WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513424"
---
# <a name="wia-device-type-specifiers"></a><span data-ttu-id="d6eaa-103">Spécificateurs de type d’appareil WIA</span><span class="sxs-lookup"><span data-stu-id="d6eaa-103">WIA Device Type Specifiers</span></span>

<span data-ttu-id="d6eaa-104">Les spécificateurs de type d’appareil WIA (Windows Image Acquisition) sont des constantes qui indiquent le type d’appareil attaché à l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-104">Windows Image Acquisition (WIA) Device Type Specifiers are constants that indicate the type of device attached to a user's computer.</span></span> <span data-ttu-id="d6eaa-105">Utilisez la macro obtenir le \_ \_ type STIDEVICE pour obtenir ces valeurs à partir de la propriété type d’appareil WIA.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-105">Use the GET\_STIDEVICE\_TYPE macro to obtain these values from the WIA device type property.</span></span> <span data-ttu-id="d6eaa-106">Les spécificateurs de type d’appareil WIA valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d6eaa-106">The following are valid WIA Device Type Specifiers:</span></span> 

| <span data-ttu-id="d6eaa-107">Type d’appareil</span><span class="sxs-lookup"><span data-stu-id="d6eaa-107">Device Type</span></span>                 | <span data-ttu-id="d6eaa-108">Signification</span><span class="sxs-lookup"><span data-stu-id="d6eaa-108">Meaning</span></span>                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6eaa-109">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="d6eaa-109">StiDeviceTypeDefault</span></span>        | <span data-ttu-id="d6eaa-110">Appareil WIA générique.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-110">Generic WIA device.</span></span> <span data-ttu-id="d6eaa-111">Pendant les énumérations d’appareils, cette constante est utilisée pour énumérer tous les périphériques WIA.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-111">During device enumerations, this constant is used to enumerate all WIA devices.</span></span>                         |
| <span data-ttu-id="d6eaa-112">StiDeviceTypeDigitalCamera</span><span class="sxs-lookup"><span data-stu-id="d6eaa-112">StiDeviceTypeDigitalCamera</span></span>  | <span data-ttu-id="d6eaa-113">L’appareil est une caméra.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-113">The device is a camera.</span></span> <span data-ttu-id="d6eaa-114">*Ce spécificateur n’est pas pris en charge par* Windows Vista *et versions ultérieures.*</span><span class="sxs-lookup"><span data-stu-id="d6eaa-114">*This specifier is not supported by* Windows Vista *and later.*</span></span>                                     |
| <span data-ttu-id="d6eaa-115">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="d6eaa-115">StiDeviceTypeScanner</span></span>        | <span data-ttu-id="d6eaa-116">L’appareil est un scanneur.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-116">The device is a scanner.</span></span>                                                                                                    |
| <span data-ttu-id="d6eaa-117">StiDeviceTypeStreamingVideo</span><span class="sxs-lookup"><span data-stu-id="d6eaa-117">StiDeviceTypeStreamingVideo</span></span> | <span data-ttu-id="d6eaa-118">L’appareil contient une vidéo de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-118">The device contains streaming video.</span></span> <span data-ttu-id="d6eaa-119">*Ce spécificateur n’est pas pris en charge par* Windows Server 2003 *,* Windows Vista *ou version ultérieure.*</span><span class="sxs-lookup"><span data-stu-id="d6eaa-119">*This specifier is not supported by* Windows Server 2003 *,* Windows Vista, *or later.*</span></span> |



 

 

 



