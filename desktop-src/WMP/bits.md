---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Windows Media Player Online stores, Service de transfert intelligent en arrière-plan (BITS)
- magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- type 2 magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan (BITS)
- BITS (Service de transfert intelligent en arrière-plan)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315473"
---
# <a name="bits"></a><span data-ttu-id="3aaae-108">BITS</span><span class="sxs-lookup"><span data-stu-id="3aaae-108">BITS</span></span>

<span data-ttu-id="3aaae-109">Le [service de transfert intelligent en arrière-plan](/windows/desktop/Bits/background-intelligent-transfer-service-portal) est une fonctionnalité du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="3aaae-109">The [Background Intelligent Transfer Service](/windows/desktop/Bits/background-intelligent-transfer-service-portal) is a feature of the Windows operating system.</span></span> <span data-ttu-id="3aaae-110">BITS transfère les fichiers (téléchargements ou chargements) entre un client et un serveur, et fournit des informations de progression relatives aux transferts.</span><span class="sxs-lookup"><span data-stu-id="3aaae-110">BITS transfers files (downloads or uploads) between a client and server, and provides progress information related to the transfers.</span></span> <span data-ttu-id="3aaae-111">Si vous souhaitez transférer des fichiers à l’aide de code C++, le service BITS est la technologie appropriée à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3aaae-111">If you want to transfer files using C++ code, BITS is the correct technology to use.</span></span> <span data-ttu-id="3aaae-112">Si vous souhaitez transférer des fichiers à l’aide du code JScript dans votre page Web de boutique en ligne, utilisez le gestionnaire de téléchargement à la place.</span><span class="sxs-lookup"><span data-stu-id="3aaae-112">If you want to transfer files using JScript code in your online store webpage, use the Download Manager instead.</span></span>

<span data-ttu-id="3aaae-113">Étant donné que le gestionnaire de téléchargement du lecteur Windows Media utilise le service BITS, vous pouvez prendre les mesures nécessaires pour configurer vos travaux de copie BITS de telle sorte que le lecteur Windows Media gère les tâches pour vous.</span><span class="sxs-lookup"><span data-stu-id="3aaae-113">Because the Windows Media Player Download Manager uses BITS, you can take steps to configure your BITS copy jobs in such a way that Windows Media Player manages the jobs for you.</span></span> <span data-ttu-id="3aaae-114">Pour ce faire, vous devez suivre la convention décrite dans la section [Convention du travail bits du lecteur Windows Media](windows-media-player-bits-job-convention.md) lorsque vous ajoutez vos travaux à la file d’attente de transfert bits.</span><span class="sxs-lookup"><span data-stu-id="3aaae-114">To do this, you must follow the convention described in the [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md) section when adding your jobs to the BITS transfer queue.</span></span> <span data-ttu-id="3aaae-115">Cette section décrit également un mécanisme permettant de récupérer des informations sur vos travaux BITS à partir de votre page Web de magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="3aaae-115">This section also describes a mechanism for retrieving information about your BITS jobs from your online stores webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3aaae-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3aaae-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aaae-117">**Utilisation du gestionnaire de téléchargement**</span><span class="sxs-lookup"><span data-stu-id="3aaae-117">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> <dt>

[<span data-ttu-id="3aaae-118">**À propos des magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="3aaae-118">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> </dl>

 

 