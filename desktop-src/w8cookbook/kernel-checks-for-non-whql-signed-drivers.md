---
title: Vérifications du noyau pour les pilotes non signés WHQL
description: Pour les appareils qui nettoient Windows 10, et où le démarrage sécurisé est activé (Notez qu’il s’agit d’une norme pour tous les nouveaux appareils depuis la sortie de Windows 8,0), tous les nouveaux pilotes doivent être signés par WHQL/sysdev plutôt que simplement à l’aide de certificats à signature croisée.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380225"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a><span data-ttu-id="dacb0-103">Vérifications du noyau pour les pilotes non signés WHQL</span><span class="sxs-lookup"><span data-stu-id="dacb0-103">Kernel checks for non-WHQL signed drivers</span></span>

<span data-ttu-id="dacb0-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="dacb0-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dacb0-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="dacb0-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dacb0-106">Pour les appareils qui nettoient Windows 10, et où le démarrage sécurisé est activé (Notez qu’il s’agit d’une norme pour tous les nouveaux appareils depuis la sortie de Windows 8,0), tous les nouveaux pilotes doivent être signés par WHQL/sysdev plutôt que simplement à l’aide de certificats à signature croisée.</span><span class="sxs-lookup"><span data-stu-id="dacb0-106">For devices that clean install Windows 10, and where Secure Boot is on (note that this is standard for all new devices since the release of Windows 8.0), all new drivers must be signed by WHQL/Sysdev rather than just use cross-signed certificates.</span></span> <span data-ttu-id="dacb0-107">Les appareils qui sont mis à niveau et les cas où les pilotes ont été signés avec un certificat croisé avant que cette stratégie soit appliquée sont exclus de cette stratégie pour garantir la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="dacb0-107">Devices that are upgraded and cases where drivers have been signed with a cross-cert before this policy went into effect are excluded from this policy to ensure backwards compatibility.</span></span> <span data-ttu-id="dacb0-108">Cette stratégie a été annoncée le 2015 avril, mais elle sera appliquée avec l’édition anniversaire de Windows, publiée le 2016 août.</span><span class="sxs-lookup"><span data-stu-id="dacb0-108">This policy was announced April 2015, however it will be enforced with the Windows Anniversary Edition, released August 2016.</span></span>

<span data-ttu-id="dacb0-109">Dans les cas où un pilote n’est pas signé correctement, il se manifeste en tant que notification PCA indiquant que le ou les pilotes sont bloqués lorsqu’il ne répond pas aux exigences de signature.</span><span class="sxs-lookup"><span data-stu-id="dacb0-109">In cases where a driver is not signed correctly, it will manifest as a PCA notification that the driver(s) is blocked when it doesn’t pass signature requirements.</span></span> <span data-ttu-id="dacb0-110">Cela empêche une expérience utilisateur déconnectée ultérieure du pilote bloqué dans le noyau en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="dacb0-110">This prevents a later disconnected user experience of the driver being blocked in kernel transparently.</span></span>

<span data-ttu-id="dacb0-111">Pour plus d’informations, consultez ce billet de [blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), qui annonce le changement de signature du pilote.</span><span class="sxs-lookup"><span data-stu-id="dacb0-111">For more information, please refer to [this blog post](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), which announces the driver signing change.</span></span>

 

 




