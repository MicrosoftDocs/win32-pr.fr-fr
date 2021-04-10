---
title: Fournir une interface utilisateur
description: Fournir une interface utilisateur
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés
- plug-ins, pages de propriétés
- plug-ins de traitement de signal numérique, pages de propriétés
- Plug-ins DSP, pages de propriétés
- plug-ins de traitement de signal numérique, interface utilisateur
- Plug-ins DSP, interface utilisateur
- pages de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197182"
---
# <a name="providing-a-user-interface"></a><span data-ttu-id="edb45-110">Fournir une interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="edb45-110">Providing a User Interface</span></span>

<span data-ttu-id="edb45-111">Les plug-ins DSP peuvent fournir une page de propriétés pour créer une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="edb45-111">DSP plug-ins can provide a property page to create a user interface.</span></span> <span data-ttu-id="edb45-112">Pour ce faire, le plug-in doit inclure un objet page de propriétés qui fournit une implémentation d’une interface **IPropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="edb45-112">To do this, the plug-in must include a property page object that provides an implementation of an **IPropertyPage** interface.</span></span> <span data-ttu-id="edb45-113">L’objet de plug-in DSP doit implémenter **ISpecifyPropertyPages :: GetPages**, qui permet au lecteur Windows Media de localiser et d’identifier la page de propriétés appropriée pour le plug-in.</span><span class="sxs-lookup"><span data-stu-id="edb45-113">The DSP plug-in object must implement **ISpecifyPropertyPages::GetPages**, which allows Windows Media Player to locate and identify the correct property page for the plug-in.</span></span>

<span data-ttu-id="edb45-114">**Affichage d’un graphique d’État**</span><span class="sxs-lookup"><span data-stu-id="edb45-114">**Displaying a Status Graphic**</span></span>

<span data-ttu-id="edb45-115">Les plug-ins DSP peuvent afficher un petit graphique ou une série de graphiques dans la zone État du lecteur Windows Media pour informer l’utilisateur qu’un plug-in est actif.</span><span class="sxs-lookup"><span data-stu-id="edb45-115">DSP plug-ins can display a small graphic, or series of graphics, in the Windows Media Player status area to notify the user that a plug-in is active.</span></span> <span data-ttu-id="edb45-116">Pour prendre en charge cette fonctionnalité, le plug-in doit implémenter l’interface **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="edb45-116">To support this feature, the plug-in must implement the **IPropertyBag** interface.</span></span> <span data-ttu-id="edb45-117">Le lecteur Windows Media appelle **IPropertyBag :: Read**, en fournissant un pointeur vers le nom de la propriété demandée « IconStreams », qui respecte la casse, et un pointeur vers une structure **Variant** qui reçoit les données du graphique.</span><span class="sxs-lookup"><span data-stu-id="edb45-117">Windows Media Player calls **IPropertyBag::Read**, providing a pointer to the requested property name "IconStreams", which is case-sensitive, and a pointer to a **VARIANT** structure that receives the data for the graphic.</span></span> <span data-ttu-id="edb45-118">Le plug-in crée un objet **IStream** (ou un SAFEARRAY d’objets **IStream** s’il y a plusieurs graphiques), puis charge les données graphiques, y compris les informations d’en-tête, dans le flux, puis retourne un pointeur vers l’objet **IStream** à l’aide du membre **punkVal** de la structure **Variant** .</span><span class="sxs-lookup"><span data-stu-id="edb45-118">The plug-in creates an **IStream** object (or a SAFEARRAY of **IStream** objects if there are multiple graphics), then loads the graphic data, including header information, into the stream, and then returns a pointer to the **IStream** object using the **punkVal** member of the **VARIANT** structure.</span></span> <span data-ttu-id="edb45-119">Si le plug-in ne fournit qu’un graphique, il spécifie le membre **VT** de la structure **Variant** comme VT \_ inconnu.</span><span class="sxs-lookup"><span data-stu-id="edb45-119">If the plug-in supplies only one graphic, it specifies the **vt** member of the **VARIANT** structure as VT\_UNKNOWN.</span></span> <span data-ttu-id="edb45-120">Si le plug-in fournit plusieurs objets Graphics **IStream** à l’aide d’un SafeArray, il spécifie le membre **VT** de la structure **Variant** en tant que \_ tableau VT.</span><span class="sxs-lookup"><span data-stu-id="edb45-120">If the plug-in supplies multiple graphic **IStream** objects using a SAFEARRAY, it specifies the **vt** member of the **VARIANT** structure as VT\_ARRAY.</span></span>

<span data-ttu-id="edb45-121">Les graphiques peuvent être stockés dans différents formats de fichiers, notamment :</span><span class="sxs-lookup"><span data-stu-id="edb45-121">Graphics can be stored in a variety of file formats, including:</span></span>

<span data-ttu-id="edb45-122">**BMP**</span><span class="sxs-lookup"><span data-stu-id="edb45-122">**BMP**</span></span>

<span data-ttu-id="edb45-123">Les images bitmap Microsoft Windows ne sont pas compressées.</span><span class="sxs-lookup"><span data-stu-id="edb45-123">Microsoft Windows Bitmap images are uncompressed.</span></span>

<span data-ttu-id="edb45-124">**JPEG**</span><span class="sxs-lookup"><span data-stu-id="edb45-124">**JPEG**</span></span>

<span data-ttu-id="edb45-125">Format d’image compressé couramment utilisé pour les pages Web.</span><span class="sxs-lookup"><span data-stu-id="edb45-125">Compressed image format commonly used for webpages.</span></span> <span data-ttu-id="edb45-126">Les fichiers de format JPEG ont généralement des extensions de nom de fichier. jpg.</span><span class="sxs-lookup"><span data-stu-id="edb45-126">JPEG format files usually have .jpg file name extensions.</span></span>

<span data-ttu-id="edb45-127">**FORMATS**</span><span class="sxs-lookup"><span data-stu-id="edb45-127">**GIF**</span></span>

<span data-ttu-id="edb45-128">Format d’image compressé couramment utilisé pour les pages Web.</span><span class="sxs-lookup"><span data-stu-id="edb45-128">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="edb45-129">**FORMAT**</span><span class="sxs-lookup"><span data-stu-id="edb45-129">**PNG**</span></span>

<span data-ttu-id="edb45-130">Format d’image compressé couramment utilisé pour les pages Web.</span><span class="sxs-lookup"><span data-stu-id="edb45-130">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="edb45-131">Les dimensions maximales pour les graphiques de plug-in DSP sont de 38 pixels de large et de 14 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="edb45-131">The maximum dimensions for DSP plug-in graphics are 38 pixels wide and 14 pixels high.</span></span>

<span data-ttu-id="edb45-132">Le flux d’octets **IStream** contenant le graphique d’État doit inclure des informations d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="edb45-132">The **IStream** byte stream containing the status graphic must include header information.</span></span> <span data-ttu-id="edb45-133">Sans informations d’en-tête, le lecteur Windows Media ne peut pas identifier correctement le type de graphique et, par conséquent, ne charge pas l’image.</span><span class="sxs-lookup"><span data-stu-id="edb45-133">Without header information, Windows Media Player cannot properly identify the type of graphic and therefore will not load the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edb45-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="edb45-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edb45-135">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="edb45-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




