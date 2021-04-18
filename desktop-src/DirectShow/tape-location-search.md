---
description: Recherche de l’emplacement de la bande
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Recherche de l’emplacement de la bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519469"
---
# <a name="tape-location-search"></a><span data-ttu-id="01e8e-103">Recherche de l’emplacement de la bande</span><span class="sxs-lookup"><span data-stu-id="01e8e-103">Tape Location Search</span></span>

<span data-ttu-id="01e8e-104">Bien que les périphériques DV prennent en charge une commande permettant d’effectuer des recherches par code de temps ou par le biais de la fonction ATN (Absolute Number), le pilote MSDV ne dispose pas d’une méthode standard, indépendante du périphérique pour accéder à ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="01e8e-104">Although DV devices support a command to search by time code or by absolute track number (ATN), the MSDV driver does not have a standard, device-independent way to access these functions.</span></span> <span data-ttu-id="01e8e-105">La seule option consiste à envoyer une commande AV/C brute au pilote, comme décrit dans la rubrique [émission de commandes AV/c brutes](issuing-raw-av-c-commands.md).</span><span class="sxs-lookup"><span data-stu-id="01e8e-105">The only option is to send a raw AV/C command to the driver as described in the topic [Issuing Raw AV/C Commands](issuing-raw-av-c-commands.md).</span></span>

<span data-ttu-id="01e8e-106">Le pilote UVC prend en charge un jeu de propriétés pour les recherches d’emplacement de bande.</span><span class="sxs-lookup"><span data-stu-id="01e8e-106">The UVC driver supports a property set for tape location searches.</span></span> <span data-ttu-id="01e8e-107">Pour envoyer une commande de recherche, utilisez l’interface **IKsControl** et définissez la \_ propriété de transport PROPSETID ext \_ .</span><span class="sxs-lookup"><span data-stu-id="01e8e-107">To send a search command, use the **IKsControl** interface and set the PROPSETID\_EXT\_TRANSPORT property.</span></span> <span data-ttu-id="01e8e-108">L’utilisation d’un jeu de propriétés est plus sûre que l’envoi de commandes AV/C brutes à l’appareil, car les commandes AV/C ignorent le filtre et accèdent directement au pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="01e8e-108">Using a property set is safer than sending raw AV/C commands to the device, because AV/C commands bypass the filter and go directly to the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01e8e-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01e8e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01e8e-110">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="01e8e-110">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="01e8e-111">Ensemble de propriétés de transport d’appareil externe</span><span class="sxs-lookup"><span data-stu-id="01e8e-111">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



