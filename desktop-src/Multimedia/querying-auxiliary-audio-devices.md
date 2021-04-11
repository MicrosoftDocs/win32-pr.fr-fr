---
title: Interrogation des périphériques audio auxiliaires
description: Interrogation des périphériques audio auxiliaires
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- audio Wave, interrogation des périphériques audio auxiliaires
- audio auxiliaire, interrogation des appareils
- interface audio auxiliaire
- périphériques audio auxiliaires, interrogation
- interrogation des périphériques audio auxiliaires
- audio auxiliaire, interface
- audio auxiliaire, appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d7de949c304cdd6941be87277f2eef1711ada24
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031121"
---
# <a name="querying-auxiliary-audio-devices"></a><span data-ttu-id="026f5-110">Interrogation des périphériques audio auxiliaires</span><span class="sxs-lookup"><span data-stu-id="026f5-110">Querying Auxiliary Audio Devices</span></span>

<span data-ttu-id="026f5-111">Tous les systèmes multimédias n’ont pas de prise en charge audio auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="026f5-111">Not all multimedia systems have auxiliary audio support.</span></span> <span data-ttu-id="026f5-112">Vous pouvez utiliser la fonction [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) pour déterminer le nombre d’appareils auxiliaires contrôlable présents dans un système.</span><span class="sxs-lookup"><span data-stu-id="026f5-112">You can use the [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) function to determine the number of controllable auxiliary devices present in a system.</span></span>

<span data-ttu-id="026f5-113">Pour obtenir des informations sur un périphérique audio auxiliaire particulier, utilisez la fonction [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="026f5-113">To get information about a particular auxiliary audio device, use the [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) function.</span></span> <span data-ttu-id="026f5-114">Cette fonction remplit une structure [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) avec des informations sur les fonctionnalités d’un appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="026f5-114">This function fills an [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="026f5-115">Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote d’appareil.</span><span class="sxs-lookup"><span data-stu-id="026f5-115">This information includes the manufacturer and product identifiers, a product name for the device, and the device-driver version number.</span></span>

 

 