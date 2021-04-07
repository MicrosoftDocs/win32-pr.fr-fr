---
title: Versions DRM
description: Versions DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media Format SDK, versions DRM
- gestion des droits numériques (DRM), versions
- DRM (gestion des droits numériques), versions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939821"
---
# <a name="drm-versions"></a><span data-ttu-id="20537-106">Versions DRM</span><span class="sxs-lookup"><span data-stu-id="20537-106">DRM Versions</span></span>

<span data-ttu-id="20537-107">Il existe plusieurs versions de la gestion des droits numériques (DRM) Windows Media.</span><span class="sxs-lookup"><span data-stu-id="20537-107">There are several versions of Windows Media digital rights management (DRM).</span></span> <span data-ttu-id="20537-108">La version 1 de la gestion des droits relatifs à l’exception est souvent différente des autres versions de cette documentation, car elle est implémentée à l’aide de techniques différentes de celles des versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="20537-108">DRM version 1 is often set apart from the other versions in this documentation, because it is implemented using techniques that are different from the later versions.</span></span> <span data-ttu-id="20537-109">La deuxième génération de Windows Media DRM est appelée DRM version 7, car elle a été introduite dans le cadre du kit de développement logiciel (SDK) Windows Media Format 7.</span><span class="sxs-lookup"><span data-stu-id="20537-109">The second generation of Windows Media DRM is called DRM version 7 because it was introduced as part of the Windows Media Format 7 SDK.</span></span> <span data-ttu-id="20537-110">Il est parfois appelé DRM version 2.</span><span class="sxs-lookup"><span data-stu-id="20537-110">It is sometimes called DRM version 2.</span></span> <span data-ttu-id="20537-111">Les versions ultérieures de Windows Media DRM, DRM version 9 et le nouveau Windows Media DRM 10, sont des extensions de la version 7 de DRM et utilisent les mêmes procédures pour l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="20537-111">The later versions of Windows Media DRM, DRM version 9 and the new Windows Media DRM 10, are extensions of DRM version 7 and use the same procedures for implementation.</span></span> <span data-ttu-id="20537-112">Toutes les versions de Windows Media DRM utilisent les mêmes routines de chiffrement. les différences entre les versions sont liées aux fonctionnalités de licence.</span><span class="sxs-lookup"><span data-stu-id="20537-112">All versions of Windows Media DRM use the same encryption routines; the differences between versions have to do with license features.</span></span>

<span data-ttu-id="20537-113">Lorsque vous créez des fichiers protégés à l’aide des objets du kit de développement logiciel (SDK) Windows Media format, vous devez prendre en charge la version 1 et la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="20537-113">When you create protected files by using the objects of the Windows Media Format SDK, you should support both version 1 and the most current version.</span></span> <span data-ttu-id="20537-114">Les fichiers protégés par DRM version 1 diffèrent des fichiers protégés par les versions ultérieures uniquement dans le contenu de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="20537-114">Files protected by DRM version 1 differ from files protected by later versions only in the contents of the header.</span></span> <span data-ttu-id="20537-115">Les fichiers les plus récents qui contiennent les informations d’en-tête supplémentaires peuvent toujours être utilisés sur les clients qui affichent uniquement le contenu de la version 1.</span><span class="sxs-lookup"><span data-stu-id="20537-115">Newer files that contain the additional header information can still be used on clients that render only version 1 content.</span></span> <span data-ttu-id="20537-116">Alors que les versions ultérieures de DRM offrent un plus haut niveau de sécurité et des fonctionnalités supplémentaires, il existe toujours de nombreux lecteurs qui utilisent uniquement la version 1.</span><span class="sxs-lookup"><span data-stu-id="20537-116">While later versions of DRM offer a higher level of security and additional features, there are still many players that use only version 1.</span></span>

<span data-ttu-id="20537-117">Pour plus d’informations sur les versions DRM, consultez la documentation du kit de développement logiciel (SDK) Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="20537-117">For more information on DRM versions, see the Windows Media Rights Manager SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="20537-118">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="20537-118">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="20537-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20537-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20537-120">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="20537-120">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="20537-121">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="20537-121">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




