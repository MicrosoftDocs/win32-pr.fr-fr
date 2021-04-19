---
description: Utilisation du profil avancé Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Utilisation du profil avancé Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522879"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a><span data-ttu-id="736ad-103">Utilisation du profil avancé Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="736ad-103">Using the Windows Media Video 9 Advanced Profile</span></span>

<span data-ttu-id="736ad-104">Les procédures vidéo de base décrites dans la section [utilisation de vidéos](workingwithvideo.md) s’appliquent également directement au profil avancé Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="736ad-104">The basic video procedures described in the [Working with Video](workingwithvideo.md) section also apply directly to the Windows Media Video 9 Advanced Profile.</span></span> <span data-ttu-id="736ad-105">Aucune procédure spéciale n’est requise.</span><span class="sxs-lookup"><span data-stu-id="736ad-105">No special procedures are required.</span></span>

<span data-ttu-id="736ad-106">Le profil avancé Windows Media Video 9 est associé aux identificateurs de classe CLSID \_ CWMV9EncMediaObject et CLSID \_ CWMVDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="736ad-106">The Windows Media Video 9 Advanced Profile is associated with the class identifiers CLSID\_CWMV9EncMediaObject and CLSID\_CWMVDecMediaObject.</span></span> <span data-ttu-id="736ad-107">La valeur FOURCC pour les types de média utilisant ce codec est « WVC1 ».</span><span class="sxs-lookup"><span data-stu-id="736ad-107">The FOURCC value for media types using this codec is "WVC1".</span></span>

<span data-ttu-id="736ad-108">Le profil avancé Windows Media Video 9 prend en charge tous les modes d’encodage courants, ainsi que l’encodage entrelacé, le codage mixte entrelacé et progressif, les résolutions qui diffèrent de l’affichage et les fonctionnalités de réduction de plage.</span><span class="sxs-lookup"><span data-stu-id="736ad-108">The Windows Media Video 9 Advanced Profile supports all common encoding modes as well interlaced encoding, mixed interlaced and progressive encoding, resolutions that are different than the display, and range reduction features.</span></span> <span data-ttu-id="736ad-109">Une autre fonctionnalité est la possibilité de stocker des métadonnées de séquence et de frame dans le flux de bits. auparavant, cela nécessitait l’utilisation de l’API ASF et des extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="736ad-109">Another feature is the ability to store sequence and frame metadata in the bit-stream itself; previously this had required use of the ASF and Data Unit Extensions API.</span></span>

<span data-ttu-id="736ad-110">Les propriétés suivantes du profil avancé Windows Media Video 9, qui peuvent être contrôlées à l’aide des paramètres du Registre, n’ont pas de chaînes **IPropertyBag** ou **IPropertyStore** correspondantes :</span><span class="sxs-lookup"><span data-stu-id="736ad-110">The following properties of the Windows Media Video 9 Advanced Profile, which can be controlled using registry settings, do not have corresponding **IPropertyBag** or **IPropertyStore** strings:</span></span>

-   <span data-ttu-id="736ad-111">Option DQuant.</span><span class="sxs-lookup"><span data-stu-id="736ad-111">Dquant Option.</span></span>
-   <span data-ttu-id="736ad-112">Force DQuant.</span><span class="sxs-lookup"><span data-stu-id="736ad-112">Dquant Strength.</span></span>
-   <span data-ttu-id="736ad-113">Chevauchement forcé.</span><span class="sxs-lookup"><span data-stu-id="736ad-113">Force Overlap.</span></span>
-   <span data-ttu-id="736ad-114">Méthode de coût du vecteur de mouvement.</span><span class="sxs-lookup"><span data-stu-id="736ad-114">Motion Vector Cost Method.</span></span>

## <a name="achieving-optimal-visual-quality"></a><span data-ttu-id="736ad-115">Obtenir une qualité visuelle optimale</span><span class="sxs-lookup"><span data-stu-id="736ad-115">Achieving Optimal Visual Quality</span></span>

<span data-ttu-id="736ad-116">Pour la plupart des données vidéo, pour obtenir une qualité visuelle optimale à l’aide du profil avancé Windows Media Video 9, vous pouvez affecter la valeur 1 à la propriété [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="736ad-116">For most video data, to achieve optimal visual quality using the Windows Media Video 9 Advanced Profile, you can set the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property to 1.</span></span>

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a><span data-ttu-id="736ad-117">À propos des codecs de profil avancé Windows Media Video 9 précédents</span><span class="sxs-lookup"><span data-stu-id="736ad-117">About the Previous Windows Media Video 9 Advanced Profile Codecs</span></span>

<span data-ttu-id="736ad-118">La version actuelle du codec de profil avancé Windows Media Video 9 est basée sur la norme SMPTE (The Motion image and Television Engineers) standard pour le profil avancé VC-1 (SMPTE 421M).</span><span class="sxs-lookup"><span data-stu-id="736ad-118">The current version of the Windows Media Video 9 Advanced Profile codec is based on the Society of Motion Picture and Television Engineers (SMPTE) standard for VC-1 (SMPTE 421M) Advanced Profile.</span></span> <span data-ttu-id="736ad-119">Ce codec remplace le codec antérieur de Windows, également appelé codec de profil avancé Windows Media Video 9, identifié par le code FOURCC « WMVA ».</span><span class="sxs-lookup"><span data-stu-id="736ad-119">This codec replaces the earlier codec from Windows also called the Windows Media Video 9 Advanced Profile codec which was identified by the FOURCC code "WMVA".</span></span> <span data-ttu-id="736ad-120">La version précédente du codec VC-1 a été implémentée avant la finalisation de la norme de profil avancé VC-1 et n’est plus prise en charge.</span><span class="sxs-lookup"><span data-stu-id="736ad-120">The previous version of the VC-1 codec was implemented before the VC-1 advanced profile standard was finalized, and is no longer supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="736ad-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="736ad-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="736ad-122">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="736ad-122">Working with Video</span></span>](workingwithvideo.md)
</dt> 
<dt>

[<span data-ttu-id="736ad-123">Utilisation des paramètres avancés du codec de profil avancé Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="736ad-123">Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec</span></span>](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



