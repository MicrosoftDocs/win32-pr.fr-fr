---
title: Vitesse de transmission
description: Vitesse de transmission
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK, vitesses de transmission
- ASF (Advanced Systems Format), vitesses de transmission
- ASF (format des systèmes avancés), vitesses de transmission
- vitesses de transmission, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675341"
---
# <a name="bit-rate"></a><span data-ttu-id="6d980-107">Vitesse de transmission</span><span class="sxs-lookup"><span data-stu-id="6d980-107">Bit Rate</span></span>

<span data-ttu-id="6d980-108">La vitesse de transmission fait référence à la quantité de données par seconde qui est fournie à partir d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="6d980-108">Bit rate refers to the amount of data per second that is delivered from an ASF file.</span></span> <span data-ttu-id="6d980-109">Les mesures de la vitesse de transmission sont exprimées en bits par seconde (BPS) ou en kilobits par seconde (Kbits/s).</span><span class="sxs-lookup"><span data-stu-id="6d980-109">Bit rate measurements are in bits per second (bps) or kilobits per second (Kbps).</span></span> <span data-ttu-id="6d980-110">La vitesse de transmission est souvent confondue avec la bande passante, qui est une mesure de la capacité de transfert de données d’un réseau.</span><span class="sxs-lookup"><span data-stu-id="6d980-110">Bit rate is often confused with bandwidth, which is a measurement of the data transfer capacity of a network.</span></span> <span data-ttu-id="6d980-111">La bande passante est également mesurée en BPS et en Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="6d980-111">Bandwidth is also measured in bps and Kbps.</span></span>

<span data-ttu-id="6d980-112">Le kit de développement logiciel (SDK) Windows Media format peut être utilisé pour créer des applications qui diffusent du contenu Windows Media en continu à partir d’emplacements Internet ou intranet.</span><span class="sxs-lookup"><span data-stu-id="6d980-112">The Windows Media Format SDK can be used to create applications that deliver streaming Windows Media-based content from Internet or intranet locations.</span></span> <span data-ttu-id="6d980-113">Lorsque vous diffusez des données sur un réseau ou sur Internet, le taux d’échantillonnage revêt une importance vitale pour l’expérience de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="6d980-113">When you are streaming data across a network or the Internet, the bit rate is of vital importance to the end-user experience.</span></span> <span data-ttu-id="6d980-114">Si la bande passante disponible sur le réseau est inférieure à la vitesse de transmission du fichier ASF, la lecture du fichier sera interrompue d’une certaine manière.</span><span class="sxs-lookup"><span data-stu-id="6d980-114">If the bandwidth available to the network is less than the bit rate of the ASF file, the playback of the file will be interrupted in some way.</span></span> <span data-ttu-id="6d980-115">En règle générale, une bande passante insuffisante entraîne l’omission des exemples ou la suspension de la lecture, tandis que davantage de données sont mises en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6d980-115">Usually, insufficient bandwidth will result in either samples being skipped, or a pause in playback while more data is buffered.</span></span>

<span data-ttu-id="6d980-116">Chaque fichier ASF reçoit une valeur de vitesse de transmission au moment de la création, en fonction du type et du nombre de flux inclus dans le profil utilisé.</span><span class="sxs-lookup"><span data-stu-id="6d980-116">Every ASF file is assigned a bit rate value at the time of creation, based upon the type and number of streams that are included in the profile used.</span></span> <span data-ttu-id="6d980-117">Les flux individuels ont leurs propres vitesses de transmission.</span><span class="sxs-lookup"><span data-stu-id="6d980-117">Individual streams have their own bit rates.</span></span> <span data-ttu-id="6d980-118">Les vitesses de transmission peuvent être constantes (les données d’origine sont compressées de façon à conserver un flot constant de données à approximativement la même vitesse) ou variable (les données d’origine sont compressées de façon à conserver la même qualité dans tout, même si cela peut entraîner un flot de données inégal).</span><span class="sxs-lookup"><span data-stu-id="6d980-118">Bit rates can be constant (the original data is compressed in such a way as to maintain a constant flow of data at approximately the same rate) or variable (the original data is compressed in such a way as to maintain the same quality throughout, even though this may mean uneven data flow).</span></span> <span data-ttu-id="6d980-119">Différents types de taux de bits peuvent être appliqués à différents flux dans le même fichier.</span><span class="sxs-lookup"><span data-stu-id="6d980-119">Different bit rate types can be applied to different streams within the same file.</span></span>

<span data-ttu-id="6d980-120">Vous pouvez encoder le même contenu dans plusieurs flux différents, chacun avec une vitesse de transmission différente.</span><span class="sxs-lookup"><span data-stu-id="6d980-120">You can encode the same content to several different streams, each with a different bit rate.</span></span> <span data-ttu-id="6d980-121">Vous pouvez ensuite configurer les flux afin qu’ils s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="6d980-121">Then you can configure the streams so that they are mutually exclusive.</span></span> <span data-ttu-id="6d980-122">Cela vous permet de créer un fichier unique qui peut être transmis en continu aux utilisateurs avec des bandes passantes différentes.</span><span class="sxs-lookup"><span data-stu-id="6d980-122">This enables you to create a single file that can be streamed to users with different bandwidths.</span></span> <span data-ttu-id="6d980-123">Cette fonctionnalité est appelée débit binaire multiple, ou MBR.</span><span class="sxs-lookup"><span data-stu-id="6d980-123">This feature is called multiple bit rate, or MBR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d980-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d980-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d980-125">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="6d980-125">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="6d980-126">**Encodage à débit binaire constant (CBR)**</span><span class="sxs-lookup"><span data-stu-id="6d980-126">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="6d980-127">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="6d980-127">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="6d980-128">**Profils**</span><span class="sxs-lookup"><span data-stu-id="6d980-128">**Profiles**</span></span>](profiles.md)
</dt> <dt>

[<span data-ttu-id="6d980-129">**Encodage à vitesse de transmission variable (VBR)**</span><span class="sxs-lookup"><span data-stu-id="6d980-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




