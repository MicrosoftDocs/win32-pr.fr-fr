---
description: Détecteur de média (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Détecteur de média (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116058"
---
# <a name="media-detector-mediadet"></a><span data-ttu-id="e1b93-103">Détecteur de média (MediaDet)</span><span class="sxs-lookup"><span data-stu-id="e1b93-103">Media Detector (MediaDet)</span></span>

> [!Note]  
> <span data-ttu-id="e1b93-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e1b93-104">\[Deprecated.</span></span> <span data-ttu-id="e1b93-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1b93-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e1b93-106">L’objet détecteur de média (MediaDet) récupère les informations de format et les images fixes des sources de fichier.</span><span class="sxs-lookup"><span data-stu-id="e1b93-106">The Media Detector (MediaDet) object retrieves format information and still frames from file sources.</span></span> <span data-ttu-id="e1b93-107">Le détecteur de média ne nécessite pas le fonctionnement du gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1b93-107">The Media Detector does not require the Filter Graph Manager to function.</span></span> <span data-ttu-id="e1b93-108">Pour créer cet objet, appelez **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e1b93-108">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="e1b93-109">L’identificateur de classe est CLSID \_ MediaDet.</span><span class="sxs-lookup"><span data-stu-id="e1b93-109">The class identifier is CLSID\_MediaDet.</span></span>

<span data-ttu-id="e1b93-110">Pour lire des fichiers Windows Media™, l’application doit fournir un certificat logiciel, également appelé clé.</span><span class="sxs-lookup"><span data-stu-id="e1b93-110">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="e1b93-111">Inscrivez l’application en tant que fournisseur de clé via l’interface **IObjectWithSite** du détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="e1b93-111">Register the application as a key provider through the Media Detector's **IObjectWithSite** interface.</span></span> <span data-ttu-id="e1b93-112">Pour plus d’informations, consultez [déverrouillage du kit de développement logiciel (SDK) de format Windows Media](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="e1b93-112">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="e1b93-113">L’objet MediaDet expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1b93-113">The MediaDet object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="e1b93-114">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="e1b93-114">**IMediaDet**</span></span>](imediadet.md)
-   <span data-ttu-id="e1b93-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="e1b93-115">**IObjectWithSite**</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1b93-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1b93-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1b93-117">Utilisation des sources</span><span class="sxs-lookup"><span data-stu-id="e1b93-117">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



