---
title: Requêtes d’appareil de mixage
description: Requêtes d’appareil de mixage
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- audio multimédia, requêtes d’appareil de mixage
- audio, requêtes d’appareil de mixage
- mixages audio, requêtes d’appareil
- mixages, requêtes d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031179"
---
# <a name="mixer-device-queries"></a><span data-ttu-id="b0fa3-107">Requêtes d’appareil de mixage</span><span class="sxs-lookup"><span data-stu-id="b0fa3-107">Mixer Device Queries</span></span>

<span data-ttu-id="b0fa3-108">Les services de mixage fournissent des fonctions permettant de déterminer le nombre d’appareils de mixage présents dans le système et les fonctionnalités des appareils.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-108">The mixer services provide functions for determining the number of mixer devices present in the system and the capabilities of the devices.</span></span> <span data-ttu-id="b0fa3-109">Vous pouvez également utiliser une fonction de service de mixage pour déterminer l’identificateur d’appareil pour un appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-109">You can also use a mixer services function to determine the device identifier for a mixer device.</span></span>

<span data-ttu-id="b0fa3-110">Vous pouvez utiliser la fonction [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) pour déterminer le nombre de périphériques de mixage présents dans le système.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-110">You can use the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function to determine how many mixer devices are present in the system.</span></span> <span data-ttu-id="b0fa3-111">Les appareils de mixage sont identifiés par un identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-111">Mixer devices are identified by a device identifier.</span></span> <span data-ttu-id="b0fa3-112">Les identificateurs d’appareil sont déterminés implicitement à partir du nombre d’appareils présents dans un système donné.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-112">Device identifiers are determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="b0fa3-113">Elles sont comprises entre zéro et un de moins que le nombre d’appareils présents.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-113">They range from zero through one less than the number of devices present.</span></span>

<span data-ttu-id="b0fa3-114">Avant d’utiliser un appareil de mixage, vous devez déterminer ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-114">Before using a mixer device, you must determine its capabilities.</span></span> <span data-ttu-id="b0fa3-115">Les fonctionnalités audio peuvent varier d’un ordinateur multimédia à un autre, de sorte que les applications doivent fonctionner avec un large éventail de matériel audio.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-115">Audio capabilities can vary from one multimedia computer to another, so applications need to work with a variety of audio hardware.</span></span>

<span data-ttu-id="b0fa3-116">Vous pouvez utiliser la fonction [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) pour déterminer les fonctionnalités des appareils de mixage.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-116">You can use the [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) function to determine the capabilities of mixer devices.</span></span> <span data-ttu-id="b0fa3-117">Cette fonction remplit une structure [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) avec des informations sur les fonctionnalités d’un appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-117">This function fills a [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) structure with information about the capabilities of a specified device.</span></span>

<span data-ttu-id="b0fa3-118">La fonction [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) récupère l’identificateur d’appareil de mixage audio associé à un handle de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-118">The [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) function retrieves the audio mixer device identifier associated with a specified device handle.</span></span> <span data-ttu-id="b0fa3-119">Par exemple, vous pouvez utiliser cette fonction pour récupérer l’identificateur d’appareil pour un mélangeur audio, puis utiliser l’identificateur d’appareil pour ajuster le volume ou pour afficher un autre contrôle.</span><span class="sxs-lookup"><span data-stu-id="b0fa3-119">For example, you could use this function to retrieve the device identifier for an audio mixer and then use the device identifier to adjust the volume or to display another control.</span></span>

 

 