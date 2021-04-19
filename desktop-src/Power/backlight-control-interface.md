---
description: L’interface de contrôle du rétroéclairage est une interface IOCTL standardisée pour contrôler la luminosité du rétroéclairage de l’écran LCD.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interface de contrôle de rétroéclairage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518257"
---
# <a name="backlight-control-interface"></a><span data-ttu-id="6a13b-103">Interface de contrôle de rétroéclairage</span><span class="sxs-lookup"><span data-stu-id="6a13b-103">Backlight Control Interface</span></span>

<span data-ttu-id="6a13b-104">L’interface de contrôle du rétroéclairage est une interface IOCTL standardisée pour contrôler la luminosité du rétroéclairage de l’écran LCD.</span><span class="sxs-lookup"><span data-stu-id="6a13b-104">The backlight control interface is a standardized IOCTL interface for controlling the brightness of the LCD backlight.</span></span>

<span data-ttu-id="6a13b-105">Les applications qui requièrent le contrôle par programmation de la luminosité du rétroéclairage ou fournissent des contrôles pour l’utilisateur doivent utiliser cette interface plutôt qu’une interface propriétaire. dans le cas contraire, le système ne peut pas interroger la luminosité matérielle actuelle et risque de ne plus être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="6a13b-105">Applications that require programmatic control of the backlight brightness or provide controls for the user to do so should use this interface rather than a proprietary interface; otherwise, the system cannot query the current hardware brightness and may become unsynchronized.</span></span>

<span data-ttu-id="6a13b-106">La première étape consiste à interroger l’appareil pour la luminosité prise en charge à l’aide du code de contrôle de [**\_ \_ \_ \_ luminosité pris en charge pour la requête de vidéo IOCTL**](ioctl-video-query-supported-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="6a13b-106">The first step is to query the device for the supported brightness using the [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md) control code.</span></span> <span data-ttu-id="6a13b-107">Cette opération retourne une mémoire tampon qui spécifie les niveaux de luminosité disponibles.</span><span class="sxs-lookup"><span data-stu-id="6a13b-107">This operation returns a buffer that specifies the available brightness levels.</span></span> <span data-ttu-id="6a13b-108">Ensuite, vous pouvez interroger l’appareil pour la luminosité actuelle de l’affichage à l’aide du code de contrôle luminosité de l' [**\_ affichage des requêtes de vidéo \_ \_ \_ IOCTL**](ioctl-video-query-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="6a13b-108">Next, you can query the device for the current display brightness using the [**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**](ioctl-video-query-display-brightness.md) control code.</span></span> <span data-ttu-id="6a13b-109">Cette opération renvoie les paramètres actuels pour la luminosité de l’alternance (AC), la luminosité du courant direct (DC) et l’état de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="6a13b-109">This operation returns the current settings for alternating current (AC) brightness, direct current (DC) brightness, and the power state.</span></span>

<span data-ttu-id="6a13b-110">Pour modifier la luminosité de l’affichage, utilisez le jeu de vidéos IOCTL code de contrôle de [**\_ \_ \_ \_ luminosité**](ioctl-video-set-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="6a13b-110">To change the display brightness, use the [**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**](ioctl-video-set-display-brightness.md) control code.</span></span> <span data-ttu-id="6a13b-111">Vous pouvez définir la luminosité de l’alimentation, la luminosité du contrôleur de périphérique ou les deux.</span><span class="sxs-lookup"><span data-stu-id="6a13b-111">You can set the AC brightness, the DC brightness, or both.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a13b-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a13b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a13b-113">À propos de la gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="6a13b-113">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



