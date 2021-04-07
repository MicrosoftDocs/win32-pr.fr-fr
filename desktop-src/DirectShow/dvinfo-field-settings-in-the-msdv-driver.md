---
description: Paramètres de champ DVINFO dans le pilote MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Paramètres de champ DVINFO dans le pilote MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746668"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a><span data-ttu-id="f3e42-103">Paramètres de champ DVINFO dans le pilote MSDV</span><span class="sxs-lookup"><span data-stu-id="f3e42-103">DVINFO Field Settings in the MSDV Driver</span></span>

<span data-ttu-id="f3e42-104">Cette section décrit comment le pilote MSDV remplit la structure [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="f3e42-104">This section describes how the MSDV driver fills in the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="f3e42-105">La `DVINFO` structure définit le bloc de format pour les connexions de code confidentiel entre MSDV et d’autres filtres.</span><span class="sxs-lookup"><span data-stu-id="f3e42-105">The `DVINFO` structure defines the format block for pin connections between MSDV and other filters.</span></span> <span data-ttu-id="f3e42-106">Par défaut, le filtre de séparateur DV est utilisé lors de la capture à partir d’un périphérique DV et le filtre MUX DV est utilisé lors de la transmission à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f3e42-106">By default, the DV Splitter filter is used when capturing from a DV device, and the DV Mux filter is used when transmitting to the device.</span></span> <span data-ttu-id="f3e42-107">Toutefois, les applications peuvent fournir leurs propres filtres personnalisés. il est donc utile de comprendre comment MSDV remplit le `DVINFO` bloc de format.</span><span class="sxs-lookup"><span data-stu-id="f3e42-107">However, applications may provide their own custom filters, so it is useful to understand how MSDV populates the `DVINFO` format block.</span></span>

<span data-ttu-id="f3e42-108">La `DVINFO` structure contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3e42-108">The `DVINFO` structure contains the following information:</span></span>

-   <span data-ttu-id="f3e42-109">Deux packs sources audio auxiliaires (AAUX) pour les premier et deuxième blocs audio.</span><span class="sxs-lookup"><span data-stu-id="f3e42-109">Two audio auxiliary (AAUX) source packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="f3e42-110">Deux packs de contrôle de code source AAUX pour les premier et deuxième blocs audio.</span><span class="sxs-lookup"><span data-stu-id="f3e42-110">Two AAUX source control packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="f3e42-111">Un pack source VAUX (Video auxiliaire).</span><span class="sxs-lookup"><span data-stu-id="f3e42-111">A video auxiliary (VAUX) source pack.</span></span>
-   <span data-ttu-id="f3e42-112">Un pack de contrôle de code source VAUX.</span><span class="sxs-lookup"><span data-stu-id="f3e42-112">A VAUX source control pack.</span></span>

<span data-ttu-id="f3e42-113">Chaque trame dans un flux DV contient des packs AAUX et VAUX.</span><span class="sxs-lookup"><span data-stu-id="f3e42-113">Every frame in a DV stream contains AAUX and VAUX packs.</span></span> <span data-ttu-id="f3e42-114">Toutefois, le `DVINFO` bloc de format est statique et n’est utilisé que pour établir la connexion de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f3e42-114">However, the `DVINFO` format block is static, and is only used to establish the pin connection.</span></span> <span data-ttu-id="f3e42-115">Lorsque le pilote MSDV se connecte, il n’examine pas les packs AAUX ou VAUX dans le flux.</span><span class="sxs-lookup"><span data-stu-id="f3e42-115">When the MSDV driver connects, it does not examine any of the AAUX or VAUX packs in the stream.</span></span> <span data-ttu-id="f3e42-116">Au lieu de cela, il utilise un ensemble de valeurs par défaut, en fonction des caractéristiques suivantes du périphérique DV :</span><span class="sxs-lookup"><span data-stu-id="f3e42-116">Instead, it uses a set of default values, based on the following characteristics of the DV device:</span></span>

-   <span data-ttu-id="f3e42-117">Si l’appareil prend en charge un format de consommateur (magnétoscope) ou un format professionnel (DVCPRO)</span><span class="sxs-lookup"><span data-stu-id="f3e42-117">Whether the device supports a consumer format (DVCR) or professional format (DVCPRO)</span></span>
-   <span data-ttu-id="f3e42-118">Type de signal</span><span class="sxs-lookup"><span data-stu-id="f3e42-118">The signal type</span></span>
-   <span data-ttu-id="f3e42-119">Indique si le format est NTSC ou PAL.</span><span class="sxs-lookup"><span data-stu-id="f3e42-119">Whether the format is NTSC or PAL.</span></span> <span data-ttu-id="f3e42-120">(Si l’appareil ne signale pas ces informations, MSDV utilise par défaut les paramètres NTSC)</span><span class="sxs-lookup"><span data-stu-id="f3e42-120">(If the device does not report this information, MSDV defaults to the NTSC settings)</span></span>

<span data-ttu-id="f3e42-121">Une fois que la diffusion en continu commence, il est de la responsabilité des filtres en mode utilisateur, tels que le séparateur DV, d’examiner le contenu réel de chaque image DV.</span><span class="sxs-lookup"><span data-stu-id="f3e42-121">Once streaming begins, it is the responsibility of the user-mode filters, such as the DV Splitter, to examine the actual contents of each DV frame.</span></span> <span data-ttu-id="f3e42-122">Comme les informations peuvent changer d’une image à l’autres, il se peut que le filtre doive effectuer une modification de format dynamique.</span><span class="sxs-lookup"><span data-stu-id="f3e42-122">Because the information can change from frame to frame, the filter may need to perform a dynamic format change.</span></span> <span data-ttu-id="f3e42-123">Par exemple, si le débit audio change, il se peut que le filtre doive renégocier le type audio.</span><span class="sxs-lookup"><span data-stu-id="f3e42-123">For example, if the audio rate changes, the filter might need to renegotiate the audio type.</span></span>

<span data-ttu-id="f3e42-124">Si vous capturez un fichier DV de type 1, la `DVINFO` structure est écrite dans le fichier en tant que bloc de format de flux ('Strf').</span><span class="sxs-lookup"><span data-stu-id="f3e42-124">If you capture a type-1 DV file, the `DVINFO` structure is written into the file as the stream format ('strf') chunk.</span></span> <span data-ttu-id="f3e42-125">Ces données sont extraites directement du bloc de format fourni par MSDV.</span><span class="sxs-lookup"><span data-stu-id="f3e42-125">This data is taken directly from the format block provided by MSDV.</span></span> <span data-ttu-id="f3e42-126">Comme indiqué, le contenu réel du flux peut être différent.</span><span class="sxs-lookup"><span data-stu-id="f3e42-126">As noted, the actual content of the stream might be different.</span></span> <span data-ttu-id="f3e42-127">Il incombe à l’application d’examiner les AAUX et les packs VAUX dans chaque frame.</span><span class="sxs-lookup"><span data-stu-id="f3e42-127">It is the application's responsibility to examine the AAUX and VAUX packs in each frame.</span></span>

<span data-ttu-id="f3e42-128">Dans les rubriques suivantes, vous pouvez trouver des tables qui répertorient tous les champs utilisés par MSDV.</span><span class="sxs-lookup"><span data-stu-id="f3e42-128">In the following topics, you can find tables listing all of the fields used by MSDV.</span></span>

-   [<span data-ttu-id="f3e42-129">Pack source AAUX (AS)</span><span class="sxs-lookup"><span data-stu-id="f3e42-129">AAUX Source (AS) Pack</span></span>](aaux-source--as--pack.md)
-   [<span data-ttu-id="f3e42-130">Pack de contrôle de code source AAUX (ASC)</span><span class="sxs-lookup"><span data-stu-id="f3e42-130">AAUX Source Control (ASC) Pack</span></span>](aaux-source-control--asc--pack.md)
-   [<span data-ttu-id="f3e42-131">Pack source VAUX (VS)</span><span class="sxs-lookup"><span data-stu-id="f3e42-131">VAUX Source (VS) Pack</span></span>](vaux-source--vs--pack.md)
-   [<span data-ttu-id="f3e42-132">Pack de contrôle de code source VAUX (VSC)</span><span class="sxs-lookup"><span data-stu-id="f3e42-132">VAUX Source Control (VSC) Pack</span></span>](vaux-source-control--vsc--pack.md)

<span data-ttu-id="f3e42-133">Lors de la lecture de ces tables, consultez les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3e42-133">When reading these tables, please consult the following specifications:</span></span>

-   <span data-ttu-id="f3e42-134">IEC 61834</span><span class="sxs-lookup"><span data-stu-id="f3e42-134">IEC 61834</span></span>
-   <span data-ttu-id="f3e42-135">314M SMPTE</span><span class="sxs-lookup"><span data-stu-id="f3e42-135">SMPTE 314M</span></span>
-   <span data-ttu-id="f3e42-136">SMPTE 370</span><span class="sxs-lookup"><span data-stu-id="f3e42-136">SMPTE 370</span></span>

<span data-ttu-id="f3e42-137">Dans chaque table, la première colonne indique le code de champ, suivi du nombre de bits (entre parenthèses).</span><span class="sxs-lookup"><span data-stu-id="f3e42-137">In each table, the first column gives the field code, followed by the number of bits (in parentheses).</span></span> <span data-ttu-id="f3e42-138">Les colonnes restantes fournissent les valeurs de champ.</span><span class="sxs-lookup"><span data-stu-id="f3e42-138">The remaining columns give the field values.</span></span> <span data-ttu-id="f3e42-139">La plupart des champs AAUX et VAUX ne sont pas pertinents pour la connexion de code confidentiel, auquel cas MSDV définit une valeur factice.</span><span class="sxs-lookup"><span data-stu-id="f3e42-139">Many of the AAUX and VAUX fields are not relevant for the pin connection, in which case MSDV sets a dummy value.</span></span> <span data-ttu-id="f3e42-140">La valeur numérique de l’ensemble du Pack est indiquée au bas de chaque table.</span><span class="sxs-lookup"><span data-stu-id="f3e42-140">The numeric value of the entire pack is listed at the bottom of each table.</span></span>

<span data-ttu-id="f3e42-141">Les remarques après chaque tableau fournissent des informations supplémentaires sur les champs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f3e42-141">The notes after each table give more information about selected fields.</span></span> <span data-ttu-id="f3e42-142">Pour obtenir une description complète, reportez-vous aux spécifications.</span><span class="sxs-lookup"><span data-stu-id="f3e42-142">For complete descriptions, refer to the specifications.</span></span> <span data-ttu-id="f3e42-143">En outre, certains champs n’ont pas la même signification dans SMPTE 314M/SMPTE 370 que dans IEC 61834.</span><span class="sxs-lookup"><span data-stu-id="f3e42-143">Also, some fields do not have the same meaning in SMPTE 314M/SMPTE 370 as they do in IEC 61834.</span></span>

> [!Note]  
> <span data-ttu-id="f3e42-144">Actuellement, DirectShow ne prend pas en charge les formats DVCPRO.</span><span class="sxs-lookup"><span data-stu-id="f3e42-144">Currently, DirectShow does not support DVCPRO formats.</span></span> <span data-ttu-id="f3e42-145">Les valeurs répertoriées pour les formats DVCPRO sont définies pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f3e42-145">The values listed for the DVCPRO formats are defined for future use.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3e42-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3e42-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3e42-147">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="f3e42-147">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f3e42-148">Données DV au format de fichier AVI</span><span class="sxs-lookup"><span data-stu-id="f3e42-148">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[<span data-ttu-id="f3e42-149">Pilote MSDV</span><span class="sxs-lookup"><span data-stu-id="f3e42-149">MSDV Driver</span></span>](msdv-driver.md)
</dt> </dl>

 

 



