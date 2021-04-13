---
title: WM/MediaClassSecondaryID
description: L’attribut WM/MediaClassSecondaryID contient le GUID de la classe de support secondaire.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Format Windows Media WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380903"
---
# <a name="wmmediaclasssecondaryid"></a><span data-ttu-id="28db7-104">WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="28db7-104">WM/MediaClassSecondaryID</span></span>

<span data-ttu-id="28db7-105">L’attribut **WM/MediaClassSecondaryID** contient le GUID de la classe de support secondaire.</span><span class="sxs-lookup"><span data-stu-id="28db7-105">The **WM/MediaClassSecondaryID** attribute contains the GUID of the secondary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="28db7-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="28db7-106">Global Constant</span></span>

<span data-ttu-id="28db7-107">\_wszWMMediaClassSecondaryID g</span><span class="sxs-lookup"><span data-stu-id="28db7-107">g\_wszWMMediaClassSecondaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="28db7-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="28db7-108">Data Type</span></span>

<span data-ttu-id="28db7-109">**\_GUID du type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="28db7-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="28db7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="28db7-110">Remarks</span></span>

<span data-ttu-id="28db7-111">Cet attribut doit être défini sur l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="28db7-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="28db7-112">GUID de la classe secondaire</span><span class="sxs-lookup"><span data-stu-id="28db7-112">Secondary class GUID</span></span>                   | <span data-ttu-id="28db7-113">Description</span><span class="sxs-lookup"><span data-stu-id="28db7-113">Description</span></span>                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28db7-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span><span class="sxs-lookup"><span data-stu-id="28db7-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span></span> | <span data-ttu-id="28db7-115">Utilisez pour les fichiers de livre audio.</span><span class="sxs-lookup"><span data-stu-id="28db7-115">Use for audio book files.</span></span>                                                                                                                                                               |
| <span data-ttu-id="28db7-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span><span class="sxs-lookup"><span data-stu-id="28db7-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span></span> | <span data-ttu-id="28db7-117">Utilisez pour les fichiers audio qui contiennent des mots prononcés, mais qui ne sont pas des livres audio.</span><span class="sxs-lookup"><span data-stu-id="28db7-117">Use for audio files that contain spoken word, but are not audio books.</span></span> <span data-ttu-id="28db7-118">Par exemple, les routines comédie de mise en attente.</span><span class="sxs-lookup"><span data-stu-id="28db7-118">For example, stand-up comedy routines.</span></span>                                                                           |
| <span data-ttu-id="28db7-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span><span class="sxs-lookup"><span data-stu-id="28db7-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span></span> | <span data-ttu-id="28db7-120">Utilisez pour les fichiers audio liés aux actualités.</span><span class="sxs-lookup"><span data-stu-id="28db7-120">Use for audio files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="28db7-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span><span class="sxs-lookup"><span data-stu-id="28db7-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span></span> | <span data-ttu-id="28db7-122">Utilisez pour les fichiers audio avec la fonction parler afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="28db7-122">Use for audio files with talk show content.</span></span>                                                                                                                                             |
| <span data-ttu-id="28db7-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span><span class="sxs-lookup"><span data-stu-id="28db7-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span></span> | <span data-ttu-id="28db7-124">Utilisez pour les fichiers vidéo relatifs aux nouvelles.</span><span class="sxs-lookup"><span data-stu-id="28db7-124">Use for video files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="28db7-125">« D6DE1D88-C77C-4593-BFBC-9C61E8C373E3 »</span><span class="sxs-lookup"><span data-stu-id="28db7-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span></span> | <span data-ttu-id="28db7-126">Utilisez pour les fichiers vidéo contenant des émissions basées sur le Web, des films courts, des codes de fin, etc.</span><span class="sxs-lookup"><span data-stu-id="28db7-126">Use for video files containing Web-based shows, short films, movie trailers, and so on.</span></span> <span data-ttu-id="28db7-127">Il s’agit de l’identificateur général pour les divertissements vidéo qui ne rentre pas dans une autre catégorie.</span><span class="sxs-lookup"><span data-stu-id="28db7-127">This is the general identifier for video entertainment that does not fit into another category.</span></span> |
| <span data-ttu-id="28db7-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span><span class="sxs-lookup"><span data-stu-id="28db7-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span></span> | <span data-ttu-id="28db7-129">Utilisez pour les fichiers audio contenant des clips audio de jeux.</span><span class="sxs-lookup"><span data-stu-id="28db7-129">Use for audio files containing sound clips from games.</span></span>                                                                                                                                  |
| <span data-ttu-id="28db7-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span><span class="sxs-lookup"><span data-stu-id="28db7-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span></span> | <span data-ttu-id="28db7-131">Utilisez pour les fichiers audio contenant des chansons complètes à partir de pistes audio de jeu.</span><span class="sxs-lookup"><span data-stu-id="28db7-131">Use for audio files containing complete songs from game sound tracks.</span></span> <span data-ttu-id="28db7-132">Si seule une partie d’une chanson est encodée dans le fichier, utilisez plutôt l’identificateur pour les clips audio du jeu.</span><span class="sxs-lookup"><span data-stu-id="28db7-132">If only part of a song is encoded in the file, use the identifier for game sound clips instead.</span></span>                   |
| <span data-ttu-id="28db7-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span><span class="sxs-lookup"><span data-stu-id="28db7-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span></span> | <span data-ttu-id="28db7-134">Utilisez pour les fichiers vidéo contenant des vidéos musicales.</span><span class="sxs-lookup"><span data-stu-id="28db7-134">Use for video files containing music videos.</span></span>                                                                                                                                            |
| <span data-ttu-id="28db7-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span><span class="sxs-lookup"><span data-stu-id="28db7-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span></span> | <span data-ttu-id="28db7-136">Utilisez pour les fichiers vidéo contenant une vidéo de démarrage générale.</span><span class="sxs-lookup"><span data-stu-id="28db7-136">Use for video files containing general home video.</span></span>                                                                                                                                      |
| <span data-ttu-id="28db7-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span><span class="sxs-lookup"><span data-stu-id="28db7-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span></span> | <span data-ttu-id="28db7-138">Utilisez pour les fichiers vidéo contenant des films de caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="28db7-138">Use for video files containing feature films.</span></span>                                                                                                                                           |
| <span data-ttu-id="28db7-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span><span class="sxs-lookup"><span data-stu-id="28db7-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span></span> | <span data-ttu-id="28db7-140">Utilisez pour les fichiers vidéo contenant des émissions de télévision.</span><span class="sxs-lookup"><span data-stu-id="28db7-140">Use for video files containing television shows.</span></span> <span data-ttu-id="28db7-141">Pour les diaporamas basés sur le Web, utilisez l’identificateur plus générique.</span><span class="sxs-lookup"><span data-stu-id="28db7-141">For Web-based shows, use the more generic identifier.</span></span>                                                                                  |
| <span data-ttu-id="28db7-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span><span class="sxs-lookup"><span data-stu-id="28db7-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span></span> | <span data-ttu-id="28db7-143">Utilisez pour les fichiers vidéo contenant la vidéo d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="28db7-143">Use for video files containing corporate video.</span></span> <span data-ttu-id="28db7-144">Par exemple, des réunions ou des vidéos de formation enregistrées.</span><span class="sxs-lookup"><span data-stu-id="28db7-144">For example, recorded meetings or training videos.</span></span>                                                                                      |
| <span data-ttu-id="28db7-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span><span class="sxs-lookup"><span data-stu-id="28db7-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span></span> | <span data-ttu-id="28db7-146">Utilisez pour les fichiers vidéo contenant des vidéos familiales à partir de photographies.</span><span class="sxs-lookup"><span data-stu-id="28db7-146">Use for video files containing home video made from photographs.</span></span>                                                                                                                        |



 

<span data-ttu-id="28db7-147">Lorsque vous spécifiez un identificateur de classe secondaire, le fichier doit également contenir un attribut d’identificateur de classe primaire.</span><span class="sxs-lookup"><span data-stu-id="28db7-147">When specifying a secondary class identifier, the file should also contain a primary class identifier attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="28db7-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28db7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28db7-149">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="28db7-149">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="28db7-150">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="28db7-150">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
</dt> </dl>

 

 




