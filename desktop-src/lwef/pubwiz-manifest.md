---
title: Utilisation du manifeste de transfert
description: L’Assistant Publication de sites Web et l’Assistant commande d’impression en ligne utilisent le manifeste de transfert pour communiquer les détails du transfert de données entre l’ordinateur client et le site serveur.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Assistant Publication de sites Web, manifeste de transfert
- Assistant commande d’impression en ligne, manifeste de transfert
- transférer le manifeste
- manifest
- Window. external, manifeste de transfert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842274"
---
# <a name="using-the-transfer-manifest"></a><span data-ttu-id="b35d2-108">Utilisation du manifeste de transfert</span><span class="sxs-lookup"><span data-stu-id="b35d2-108">Using the Transfer Manifest</span></span>

<span data-ttu-id="b35d2-109">L’Assistant Publication de sites Web et l’Assistant commande d’impression en ligne utilisent le manifeste de transfert pour communiquer les détails du transfert de données entre l’ordinateur client et le site serveur.</span><span class="sxs-lookup"><span data-stu-id="b35d2-109">The Web Publishing Wizard and Online Print Ordering Wizard use the transfer manifest to communicate details of data transfer between the client computer and the server site.</span></span>

## <a name="the-purpose-of-the-transfer-manifest"></a><span data-ttu-id="b35d2-110">Objectif du manifeste de transfert</span><span class="sxs-lookup"><span data-stu-id="b35d2-110">The Purpose of the Transfer Manifest</span></span>

<span data-ttu-id="b35d2-111">Le manifeste de transfert décrit les fichiers impliqués dans le transfert, y compris les détails tels que la hiérarchie de destination et les métadonnées du fichier.</span><span class="sxs-lookup"><span data-stu-id="b35d2-111">The transfer manifest describes files involved in the transfer, including details such as the destination hierarchy and the file's metadata.</span></span> <span data-ttu-id="b35d2-112">Le script côté serveur peut modifier le manifeste en supprimant les fichiers inappropriés de la liste et en ajoutant des informations sur le mode et l’emplacement de transfert des fichiers.</span><span class="sxs-lookup"><span data-stu-id="b35d2-112">Server-side script can modify the manifest by removing inappropriate files from the list and adding information about how and where the files should be transferred.</span></span>

<span data-ttu-id="b35d2-113">Le manifeste est exposé en tant que propriété **Window. external. Property ("TransferManifest")**, Document XML Document Object Model (DOM).</span><span class="sxs-lookup"><span data-stu-id="b35d2-113">The manifest is exposed as the property **window.external.Property("TransferManifest")**, an XML Document Object Model (DOM) document.</span></span> <span data-ttu-id="b35d2-114">Pour plus d’informations sur le modèle DOM XML, consultez la documentation MSDN relative à [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b35d2-114">For more information on the XML DOM, see the MSDN documentation for [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span></span>

<span data-ttu-id="b35d2-115">L’organisation de niveau supérieur du manifeste de transfert est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b35d2-115">The top-level organization of the transfer manifest is as follows:</span></span>


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



<span data-ttu-id="b35d2-116">La page HTML côté serveur peut utiliser les nœuds du manifeste pour obtenir certaines informations sur les fichiers à copier, puis modifier l’interface utilisateur du service en conséquence.</span><span class="sxs-lookup"><span data-stu-id="b35d2-116">The server-side HTML page can use the nodes in the manifest to obtain certain information about the files to be copied and then modify the service's UI accordingly.</span></span> <span data-ttu-id="b35d2-117">Par exemple, un site d’impression de photos peut utiliser les informations pour afficher des miniatures des images choisies, alors qu’un site de stockage peut utiliser ces informations pour s’assurer qu’un espace de stockage suffisant est disponible pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b35d2-117">For instance, a photo printing site might use the information to display thumbnails of the chosen images, while a storage site might use the information to ensure that sufficient storage space is available for that user.</span></span> <span data-ttu-id="b35d2-118">Pour obtenir des informations complètes sur les nœuds et les attributs du manifeste de transfert, consultez [transférer le schéma de manifeste](/windows/desktop/shell/interfaces).</span><span class="sxs-lookup"><span data-stu-id="b35d2-118">For complete information on the transfer manifest nodes and attributes, see [Transfer Manifest Schema](/windows/desktop/shell/interfaces).</span></span>

<span data-ttu-id="b35d2-119">Le schéma de manifeste de transfert est écrit sous la forme d’un modèle ouvert, de sorte que les éléments qui ne sont pas spécifiquement définis dans le schéma peuvent apparaître dans le manifeste de transfert.</span><span class="sxs-lookup"><span data-stu-id="b35d2-119">The transfer manifest schema is written as an open model so that elements not specifically defined in the schema may appear in the transfer manifest.</span></span> <span data-ttu-id="b35d2-120">Par conséquent, un site de fournisseur peut ajouter des éléments propriétaires pour sa propre utilisation sans perturber la validité du manifeste.</span><span class="sxs-lookup"><span data-stu-id="b35d2-120">Therefore, a provider site might add proprietary elements for its own use without disturbing the validity of the manifest.</span></span> <span data-ttu-id="b35d2-121">Le schéma est également défini de sorte que l’ordre des éléments ne soit pas limité.</span><span class="sxs-lookup"><span data-stu-id="b35d2-121">The schema is also defined so that the order of elements is not restricted.</span></span>

> [!Note]  
> <span data-ttu-id="b35d2-122">Le manifeste est recréé chaque fois qu’un nouveau fournisseur est choisi afin que le fournisseur puisse stocker les informations de site dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="b35d2-122">The manifest is re-created each time a new provider is chosen so that the provider has a chance to store site information in the manifest.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b35d2-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b35d2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b35d2-124">Schéma de manifeste de transfert</span><span class="sxs-lookup"><span data-stu-id="b35d2-124">Transfer Manifest Schema</span></span>](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 