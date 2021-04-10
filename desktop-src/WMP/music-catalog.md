---
title: Catalogue musical
description: Catalogue musical
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player Online stores, catalogues musicaux
- magasins en ligne, catalogues musicaux
- tapez 1 magasins en ligne, catalogues musicaux
- Magasins en ligne du lecteur Windows Media, compilateur de catalogue
- magasins en ligne, compilateur de catalogue
- magasins en ligne de type 1, compilateur de catalogue
- catalogues musicaux
- compilateur de catalogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030774"
---
# <a name="music-catalog"></a><span data-ttu-id="f470a-111">Catalogue musical</span><span class="sxs-lookup"><span data-stu-id="f470a-111">Music Catalog</span></span>

<span data-ttu-id="f470a-112">Un magasin en ligne de type 1 crée son catalogue musical sous la forme d’un ensemble de fichiers TSV (valeurs séparées par des tabulations).</span><span class="sxs-lookup"><span data-stu-id="f470a-112">A type 1 online store creates its music catalog as a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="f470a-113">Ensuite, le magasin en ligne utilise le [compilateur de catalogue](catalog-compiler-for-type-1-online-stores.md) de Microsoft pour compiler les fichiers TSV dans un catalogue compressé qui peut être téléchargé par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f470a-113">Then the online store uses Microsoft's [catalog compiler](catalog-compiler-for-type-1-online-stores.md) to compile the TSV files into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="f470a-114">Le lecteur Windows Media peut télécharger des fichiers de catalogue complets ou des fichiers de mise à jour de catalogue.</span><span class="sxs-lookup"><span data-stu-id="f470a-114">Windows Media Player can download full catalog files or catalog update files.</span></span> <span data-ttu-id="f470a-115">Les mises à jour du catalogue contiennent uniquement les informations du catalogue qui ont été modifiées depuis la dernière mise à jour du catalogue.</span><span class="sxs-lookup"><span data-stu-id="f470a-115">Catalog updates contain only the catalog information that has changed since the last catalog update.</span></span> <span data-ttu-id="f470a-116">Il revient au plug-in de partenaire de contenu de déterminer s’il faut télécharger un catalogue complet ou une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f470a-116">It is up to the content partner plug-in to determine whether to download a full catalog or an update.</span></span> <span data-ttu-id="f470a-117">Dans les deux cas, le lecteur Windows Media applique les modifications au catalogue en cours lors de la notification du plug-in.</span><span class="sxs-lookup"><span data-stu-id="f470a-117">In either case, Windows Media Player applies the changes to the current catalog upon notification from the plug-in.</span></span>

<span data-ttu-id="f470a-118">Si un nouveau catalogue est préparé pour le magasin en ligne, le plug-in peut notifier le lecteur en appelant [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) et en passant wmpcnNewCatalogAvailable comme valeur pour le paramètre de *type* .</span><span class="sxs-lookup"><span data-stu-id="f470a-118">If the online store has a new catalog prepared, the plug-in can notify the Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) and passing wmpcnNewCatalogAvailable as the value for the *type* parameter.</span></span>

<span data-ttu-id="f470a-119">Lorsque le lecteur Windows Media est prêt à télécharger un catalogue ou une mise à jour, le lecteur appelle [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="f470a-119">When Windows Media Player is ready to download a catalog or update, the Player calls [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> <span data-ttu-id="f470a-120">Cette méthode fournit le plug-in contenant des informations sur le catalogue actuel, telles que la version du catalogue et l’identificateur des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="f470a-120">This method provides the plug-in with information about the current catalog, such as the catalog version and locale identifier.</span></span> <span data-ttu-id="f470a-121">Le plug-in répond en fournissant l’URL (Uniform Resource Locator) du catalogue complet correct ou de la mise à jour, ainsi qu’un numéro de version et une date d’expiration mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f470a-121">The plug-in responds by supplying the uniform resource locator (URL) of the correct full catalog or update, as well as an updated version number and expiration date.</span></span> <span data-ttu-id="f470a-122">Le lecteur Windows Media demande périodiquement des mises à jour du catalogue en fonction des informations fournies par le plug-in dans **GetCatalogURL**.</span><span class="sxs-lookup"><span data-stu-id="f470a-122">Windows Media Player will periodically request catalog updates based upon the information provided by the plug-in in **GetCatalogURL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f470a-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f470a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f470a-124">**À propos des magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="f470a-124">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f470a-125">**Compilateur de catalogue pour les magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="f470a-125">**Catalog Compiler for Type 1 Online Stores**</span></span>](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f470a-126">**Interface IWMPContentPartner**</span><span class="sxs-lookup"><span data-stu-id="f470a-126">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




