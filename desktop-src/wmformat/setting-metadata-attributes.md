---
title: Définition des attributs de métadonnées
description: Définition des attributs de métadonnées
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media Format SDK, définition des attributs de métadonnées
- ASF (Advanced Systems Format), définition des attributs de métadonnées
- ASF (format des systèmes avancés), définition des attributs de métadonnées
- métadonnées, définir des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381547"
---
# <a name="setting-metadata-attributes"></a><span data-ttu-id="f0251-107">Définition des attributs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="f0251-107">Setting Metadata Attributes</span></span>

<span data-ttu-id="f0251-108">Les attributs de métadonnées sont définis à l’aide de la méthode [**IWMHeaderInfo3 :: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .</span><span class="sxs-lookup"><span data-stu-id="f0251-108">Metadata attributes are set by using the [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) method.</span></span>

<span data-ttu-id="f0251-109">Une langue est attribuée à tous les attributs dans la liste des langues du fichier.</span><span class="sxs-lookup"><span data-stu-id="f0251-109">All attributes are assigned a language from the language list for the file.</span></span> <span data-ttu-id="f0251-110">Vous pouvez accéder à la liste des langues à l’aide de l’interface [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) .</span><span class="sxs-lookup"><span data-stu-id="f0251-110">You can access the language list by using the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface.</span></span> <span data-ttu-id="f0251-111">Pour obtenir un pointeur vers une interface **IWMLanguageList** , appelez **QueryInterface** sur toute interface de l’objet à partir duquel vous avez obtenu [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span><span class="sxs-lookup"><span data-stu-id="f0251-111">To get a pointer to an **IWMLanguageList** interface, call **QueryInterface** on any interface of the object from which you have obtained [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span></span>

<span data-ttu-id="f0251-112">Vous pouvez ajouter des attributs avec n’importe quel nom de votre choix.</span><span class="sxs-lookup"><span data-stu-id="f0251-112">You can add attributes with any name you like.</span></span> <span data-ttu-id="f0251-113">Toutefois, l’utilisation de noms d’attribut qui ne sont pas des noms standard pris en charge par le kit de développement logiciel (SDK) Windows Media format peut compliquer la découverte des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="f0251-113">However, using attribute names that are not standard names supported by the Windows Media Format SDK can make your metadata difficult for users to discover.</span></span> <span data-ttu-id="f0251-114">La plupart des applications qui jouent sur des médias vérifient les valeurs standard.</span><span class="sxs-lookup"><span data-stu-id="f0251-114">Most media-playing applications will check for standard values.</span></span> <span data-ttu-id="f0251-115">Pour plus d’informations, consultez [métadonnées personnalisées](custom-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="f0251-115">For more information, see [Custom Metadata](custom-metadata.md).</span></span>

<span data-ttu-id="f0251-116">Vous ne pouvez pas utiliser le nombre de flux 0xFFFF pour ajouter un attribut globalement.</span><span class="sxs-lookup"><span data-stu-id="f0251-116">You cannot use stream number 0xFFFF to add an attribute globally.</span></span> <span data-ttu-id="f0251-117">Vous devez assigner chaque attribut à un numéro de flux spécifique, ou le flux 0 pour les attributs de niveau fichier.</span><span class="sxs-lookup"><span data-stu-id="f0251-117">You must assign each attribute to a specific stream number, or stream 0 for file-level attributes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0251-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0251-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0251-119">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="f0251-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




