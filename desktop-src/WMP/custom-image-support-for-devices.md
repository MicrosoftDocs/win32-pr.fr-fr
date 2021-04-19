---
title: Prise en charge d’images personnalisées pour les appareils
description: Prise en charge d’images personnalisées pour les appareils
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Lecteur Windows Media, prise en charge d’images personnalisées pour les appareils
- Lecteur Windows Media, prise en charge d’images pour les appareils
- prise en charge des images personnalisées par l’appareil
- prise en charge d’images personnalisées pour les appareils
- prise en charge des images pour les appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511699"
---
# <a name="custom-image-support-for-devices"></a><span data-ttu-id="ab868-108">Prise en charge d’images personnalisées pour les appareils</span><span class="sxs-lookup"><span data-stu-id="ab868-108">Custom Image Support for Devices</span></span>

> [!Note]  
> <span data-ttu-id="ab868-109">Cette section décrit une fonctionnalité du lecteur Windows Media 10 qui est disponible lors de l’utilisation du système d’exploitation Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab868-109">This section documents a feature of Windows Media Player 10 that is available when using the Windows XP operating system.</span></span> <span data-ttu-id="ab868-110">Elle n’est peut-être pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ab868-110">It may be unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ab868-111">Les fabricants de périphériques peuvent fournir deux fichiers image spéciaux pour personnaliser la façon dont un appareil est représenté dans l’interface utilisateur du lecteur Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="ab868-111">Device manufacturers can provide two special image files to customize the way a device is represented in the Windows Media Player 10 user interface.</span></span> <span data-ttu-id="ab868-112">Ces deux fichiers sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ab868-112">These two files are:</span></span>

-   <span data-ttu-id="ab868-113">DevIcon. fil.</span><span class="sxs-lookup"><span data-stu-id="ab868-113">DevIcon.fil.</span></span> <span data-ttu-id="ab868-114">Fichier de format d’icône Windows qui représente le matériel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ab868-114">A Windows icon format file that represents the device hardware.</span></span> <span data-ttu-id="ab868-115">Cette image s’affiche dans le lecteur Windows Media 10 partout où une icône est utilisée pour représenter un appareil, comme la liste des appareils dans la fonctionnalité de **synchronisation** .</span><span class="sxs-lookup"><span data-stu-id="ab868-115">This image displays in Windows Media Player 10 anywhere an icon is used to represent a device, such as the device list in the **Sync** feature.</span></span>
-   <span data-ttu-id="ab868-116">Dévlogo. fil.</span><span class="sxs-lookup"><span data-stu-id="ab868-116">DevLogo.fil.</span></span> <span data-ttu-id="ab868-117">Fichier de format PNG qui représente le logo de l’entreprise du fabricant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ab868-117">A PNG format file that represents the corporate logo of the device manufacturer.</span></span> <span data-ttu-id="ab868-118">Cette image s’affiche dans le lecteur Windows Media 10 Anywhere. la personnalisation de l’entreprise est utilisée, telle que la boîte de dialogue Configuration de l' **appareil** .</span><span class="sxs-lookup"><span data-stu-id="ab868-118">This image displays in Windows Media Player 10 anywhere corporate branding is used, such as the **Device Setup** dialog box.</span></span>

## <a name="general-guidelines-for-images"></a><span data-ttu-id="ab868-119">Instructions générales pour les images</span><span class="sxs-lookup"><span data-stu-id="ab868-119">General Guidelines for Images</span></span>

<span data-ttu-id="ab868-120">Les indications suivantes s’appliquent à la prise en charge d’images personnalisées en général :</span><span class="sxs-lookup"><span data-stu-id="ab868-120">The following guidelines apply to custom image support in general:</span></span>

-   <span data-ttu-id="ab868-121">Cette fonctionnalité est facultative.</span><span class="sxs-lookup"><span data-stu-id="ab868-121">This feature is optional.</span></span> <span data-ttu-id="ab868-122">Les appareils qui ne fournissent pas d’images sont représentés par des images par défaut.</span><span class="sxs-lookup"><span data-stu-id="ab868-122">Devices that do not supply images will be represented by default images.</span></span>
-   <span data-ttu-id="ab868-123">Cette fonctionnalité est prise en charge uniquement pour les appareils compatibles MTP.</span><span class="sxs-lookup"><span data-stu-id="ab868-123">This feature is supported for MTP-enabled devices only.</span></span>
-   <span data-ttu-id="ab868-124">Pour empêcher la modification des fichiers, il est recommandé de stocker les fichiers image dans un microprogramme ou un support de stockage protégé, et non avec des fichiers créés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab868-124">To prevent changes to the files, it is recommended that the image files be stored in firmware or a protected storage medium, not with user-created files.</span></span>
-   <span data-ttu-id="ab868-125">Les fichiers ne doivent pas être retournés aux clients Windows Media Gestionnaire de périphériques qui énumèrent le stockage racine de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ab868-125">The files should not be returned to Windows Media Device Manager clients that enumerate the root storage of the device.</span></span> <span data-ttu-id="ab868-126">En outre, la suppression, le déplacement ou le changement de nom des fichiers doivent échouer.</span><span class="sxs-lookup"><span data-stu-id="ab868-126">Also, deleting, moving, or renaming the files should fail.</span></span>
-   <span data-ttu-id="ab868-127">Si l’appareil fournit plus d’un support de stockage, l’appareil doit retourner les fichiers image en réponse aux demandes d’ouverture de fichier à partir de n’importe quel support.</span><span class="sxs-lookup"><span data-stu-id="ab868-127">If the device provides more than one storage medium, the device should return the image files in response to file open requests from any medium.</span></span> <span data-ttu-id="ab868-128">Différentes icônes d’appareil peuvent être retournées à partir de chaque support de stockage.</span><span class="sxs-lookup"><span data-stu-id="ab868-128">Different device icons may be returned from each storage medium.</span></span>
-   <span data-ttu-id="ab868-129">Pour les clients Windows Media Gestionnaire de périphériques 1,2, ces images ont priorité sur les propriétés d’icône fournies par les mécanismes d’installation de Windows, tels que les propriétés de nœud d’appareil.</span><span class="sxs-lookup"><span data-stu-id="ab868-129">For Windows Media Device Manager 1.2-enabled clients, these images will take precedence over icon properties supplied by Windows setup mechanisms, such as device node properties.</span></span>
-   <span data-ttu-id="ab868-130">Les images ne doivent pas contenir d’informations nécessitant une localisation.</span><span class="sxs-lookup"><span data-stu-id="ab868-130">The images must not contain any information that requires localization.</span></span>
-   <span data-ttu-id="ab868-131">Pour les appareils multifonctions, seules les fonctionnalités de lecture musicale de Windows XP utilisent ces images.</span><span class="sxs-lookup"><span data-stu-id="ab868-131">For multi-function devices, only the music playback features of Windows XP will use these images.</span></span>

## <a name="creating-the-device-icon-image"></a><span data-ttu-id="ab868-132">Création de l’image de l’icône d’appareil</span><span class="sxs-lookup"><span data-stu-id="ab868-132">Creating the Device Icon Image</span></span>

<span data-ttu-id="ab868-133">Le fichier image de l’icône de l’appareil, DevIcon. fil, doit contenir un fichier au format icône Windows.</span><span class="sxs-lookup"><span data-stu-id="ab868-133">The device icon image file, DevIcon.fil, must contain a file in Windows icon format.</span></span> <span data-ttu-id="ab868-134">Les icônes de l’article MSDN [dans Win32](/previous-versions/ms997538(v=msdn.10)) décrivent comment créer un fichier de ce type.</span><span class="sxs-lookup"><span data-stu-id="ab868-134">The MSDN article [Icons in Win32](/previous-versions/ms997538(v=msdn.10)) describes how to create such a file.</span></span> <span data-ttu-id="ab868-135">L’article MSDN [création d’icônes Windows XP](/previous-versions/ms997636(v=msdn.10)) fournit des règles de style pour les icônes Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab868-135">The MSDN article [Creating Windows XP Icons](/previous-versions/ms997636(v=msdn.10)) provides style guidelines for Windows XP icons.</span></span> <span data-ttu-id="ab868-136">Le fichier image icône d’appareil intègre douze images dans un fichier unique en fournissant quatre tailles différentes avec trois profondeurs de couleurs différentes.</span><span class="sxs-lookup"><span data-stu-id="ab868-136">The device icon image file incorporates twelve images in a single file by providing four different sizes with three different color depths each.</span></span>

<span data-ttu-id="ab868-137">Veillez à prêter une attention particulière aux recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab868-137">Be certain to pay particular attention to the following guidelines:</span></span>

-   <span data-ttu-id="ab868-138">Les tailles recommandées (en pixels) sont 16x16, 32x32, 48 et 256x256.</span><span class="sxs-lookup"><span data-stu-id="ab868-138">Recommended sizes (in pixels) are 16x16, 32x32, 48x48, and 256x256.</span></span>
-   <span data-ttu-id="ab868-139">Les profondeurs de couleurs recommandés sont 24 bits avec un canal alpha 8 bits, 8 bits avec transparence de 1 bit et 4 bits avec transparence de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="ab868-139">Recommended color depths are 24-bit with 8-bit alpha channel, 8-bit with 1-bit transparency, and 4-bit with 1-bit transparency.</span></span>
-   <span data-ttu-id="ab868-140">Utilisez l’angle de perspective et les recommandations d’ombre portée décrites dans les articles MSDN mentionnés précédemment.</span><span class="sxs-lookup"><span data-stu-id="ab868-140">Use the perspective angle and drop shadow recommendations described in the MSDN articles mentioned previously.</span></span>

<span data-ttu-id="ab868-141">Une fois que vous avez créé le fichier d’icône, il vous suffit de le renommer DevIcon. fil.</span><span class="sxs-lookup"><span data-stu-id="ab868-141">Once you have created the icon file, simply rename it DevIcon.fil.</span></span>

## <a name="creating-the-corporate-logo-image"></a><span data-ttu-id="ab868-142">Création de l’image du logo de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="ab868-142">Creating the Corporate Logo Image</span></span>

<span data-ttu-id="ab868-143">Le fichier image du logo de l’entreprise, devlogo. fil, doit contenir un fichier au format PNG.</span><span class="sxs-lookup"><span data-stu-id="ab868-143">The corporate logo image file, DevLogo.fil, must contain a file in PNG format.</span></span> <span data-ttu-id="ab868-144">Pour créer l’image, suivez les instructions ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ab868-144">Use the following guidelines when creating the image:</span></span>

-   <span data-ttu-id="ab868-145">Les dimensions maximales de l’image sont 150x32 pixels.</span><span class="sxs-lookup"><span data-stu-id="ab868-145">The maximum dimensions for the image are 150x32 pixels.</span></span>
-   <span data-ttu-id="ab868-146">L’image doit prendre en charge la fusion alpha pour permettre une transition sans heurts entre l’interface utilisateur de Windows Media Player 10 et le logo.</span><span class="sxs-lookup"><span data-stu-id="ab868-146">The image should support alpha blending to enable a smooth transition between the Windows Media Player 10 user interface and the logo.</span></span>

<span data-ttu-id="ab868-147">Une fois que vous avez créé le fichier de logo de l’entreprise, il vous suffit de le renommer devlogo. fil.</span><span class="sxs-lookup"><span data-stu-id="ab868-147">Once you have created the corporate logo file, simply rename it DevLogo.fil.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab868-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab868-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab868-149">**Lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ab868-149">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 