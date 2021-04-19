---
title: Activation de la synchronisation avec le lecteur Windows Media
description: Activation de la synchronisation avec le lecteur Windows Media
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Gestionnaire de périphériques Windows Media, synchronisation avec le lecteur Windows Media
- Gestionnaire de périphériques, synchronisation avec le lecteur Windows Media
- Guide de programmation, synchronisation avec le lecteur Windows Media
- fournisseurs de services, synchronisation avec le lecteur Windows Media
- création de fournisseurs de services, synchronisation avec le lecteur Windows Media
- synchronisation avec le lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509005"
---
# <a name="enabling-synchronization-with-windows-media-player"></a><span data-ttu-id="83087-109">Activation de la synchronisation avec le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="83087-109">Enabling Synchronization with Windows Media Player</span></span>

<span data-ttu-id="83087-110">Vous pouvez autoriser un appareil à participer à la synchronisation automatique avec le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="83087-110">You can enable a device to participate in automatic synchronization with Windows Media Player.</span></span> <span data-ttu-id="83087-111">La synchronisation automatique signifie que lorsqu’un appareil synchronisé défini par l’utilisateur se connecte à l’ordinateur, le lecteur Windows Media télécharge, met à jour ou supprime automatiquement les fichiers de l’appareil sans nécessiter d’entrée d’utilisateur supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="83087-111">Automatic synchronization means that when a user-designated synchronized device connects to the computer, Windows Media Player will automatically download, update, or delete files from the device without requiring any additional user input.</span></span>

<span data-ttu-id="83087-112">Par défaut, les appareils suivants sont synchronisés avec le lecteur Windows Media :</span><span class="sxs-lookup"><span data-stu-id="83087-112">By default the following devices are synchronized with Windows Media Player:</span></span>

-   <span data-ttu-id="83087-113">Appareils MTP</span><span class="sxs-lookup"><span data-stu-id="83087-113">MTP devices</span></span>
-   <span data-ttu-id="83087-114">Périphériques de stockage de masse</span><span class="sxs-lookup"><span data-stu-id="83087-114">Mass-storage devices</span></span>
-   <span data-ttu-id="83087-115">Appareils Windows CE (Windows Media Player 10 mobile et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="83087-115">Windows CE devices (Windows Media Player 10 Mobile and later)</span></span>

<span data-ttu-id="83087-116">Pour qu’un autre appareil se synchronise avec le lecteur Windows Media, les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="83087-116">For any other device to synchronize with Windows Media Player, the following requirements must met:</span></span>

-   <span data-ttu-id="83087-117">L’appareil doit publier une interface d’appareil PAP qui est {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span><span class="sxs-lookup"><span data-stu-id="83087-117">The device must advertise a PAP device interface that is {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span></span>
-   <span data-ttu-id="83087-118">Les objets d’appareil retournés par le fournisseur de services doivent prendre en charge l’interface **IMDSPDevice3** .</span><span class="sxs-lookup"><span data-stu-id="83087-118">The device objects returned by service provider must support the **IMDSPDevice3** interface.</span></span>
-   <span data-ttu-id="83087-119">Le paramètre d’appareil UseExtendedWmdm doit être défini sur une valeur **DWORD** égale à 1.</span><span class="sxs-lookup"><span data-stu-id="83087-119">The device parameter UseExtendedWmdm must be set to a **DWORD** value of 1.</span></span> <span data-ttu-id="83087-120">Pour plus d’informations, consultez Paramètres de l' [appareil](device-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="83087-120">See [Device Parameters](device-parameters.md) for more information.</span></span>
-   <span data-ttu-id="83087-121">Le fournisseur de services doit implémenter les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="83087-121">The service provider should implement the following interfaces:</span></span>

    [<span data-ttu-id="83087-122">**IMDSPDevice3**</span><span class="sxs-lookup"><span data-stu-id="83087-122">**IMDSPDevice3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [<span data-ttu-id="83087-123">**IMDSPObject2**</span><span class="sxs-lookup"><span data-stu-id="83087-123">**IMDSPObject2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [<span data-ttu-id="83087-124">**IMDSPStorage4**</span><span class="sxs-lookup"><span data-stu-id="83087-124">**IMDSPStorage4**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a><span data-ttu-id="83087-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83087-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83087-126">**Création d’un fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="83087-126">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="83087-127">**Paramètres de l’appareil**</span><span class="sxs-lookup"><span data-stu-id="83087-127">**Device Parameters**</span></span>](device-parameters.md)
</dt> </dl>

 

 




