---
title: Modification de la propriété exemple de plug-in DSP audio
description: Modification de la propriété exemple de plug-in DSP audio
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Plug-ins du lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, propriétés audio
- Plug-ins DSP, propriétés audio
- plug-ins DSP audio, propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674322"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a><span data-ttu-id="5cb87-108">Modification de la propriété exemple de plug-in DSP audio</span><span class="sxs-lookup"><span data-stu-id="5cb87-108">Changing the Sample Audio DSP Plug-in Property</span></span>

<span data-ttu-id="5cb87-109">Vous souhaiterez probablement modifier la propriété que l’Assistant de plug-in du lecteur Windows Media crée par défaut.</span><span class="sxs-lookup"><span data-stu-id="5cb87-109">You will probably want to change the property that the Windows Media Player Plug-in Wizard creates by default.</span></span> <span data-ttu-id="5cb87-110">La liste suivante détaille les éléments qui peuvent nécessiter des modifications :</span><span class="sxs-lookup"><span data-stu-id="5cb87-110">The following list details the items that might require changing:</span></span>

-   <span data-ttu-id="5cb87-111">**Ressource de boîte de dialogue.**</span><span class="sxs-lookup"><span data-stu-id="5cb87-111">**The dialog resource.**</span></span> <span data-ttu-id="5cb87-112">Cliquez sur l’onglet **ResourceView** dans la fenêtre espace de travail du projet.</span><span class="sxs-lookup"><span data-stu-id="5cb87-112">Click the **ResourceView** tab in the Project Workspace window.</span></span> <span data-ttu-id="5cb87-113">Développez la liste des dossiers pour ouvrir le dossier boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5cb87-113">Expand the folder list to open the Dialog folder.</span></span> <span data-ttu-id="5cb87-114">Double-cliquez sur la ressource de boîte de dialogue pour ouvrir l’éditeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="5cb87-114">Double-click the dialog resource to open the resource editor.</span></span> <span data-ttu-id="5cb87-115">Vous pouvez apporter des modifications à la boîte de dialogue de la page de propriétés pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="5cb87-115">You can make changes to the property page dialog to fulfill your needs.</span></span> <span data-ttu-id="5cb87-116">Par exemple, vous pouvez modifier le texte de l’étiquette ou remplacer le contrôle d’édition par une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="5cb87-116">For instance, you could change the text in the label or replace the edit control with a checkbox.</span></span>
-   <span data-ttu-id="5cb87-117">**Code objet de la page de propriétés.**</span><span class="sxs-lookup"><span data-stu-id="5cb87-117">**The property page object code.**</span></span> <span data-ttu-id="5cb87-118">L’implémentation par défaut utilise une variable de type double pour stocker le facteur d’échelle.</span><span class="sxs-lookup"><span data-stu-id="5cb87-118">The default implementation uses a variable of type double to store the scale factor.</span></span> <span data-ttu-id="5cb87-119">Vous pouvez avoir besoin d’un type de données différent.</span><span class="sxs-lookup"><span data-stu-id="5cb87-119">You might require a different type of data.</span></span> <span data-ttu-id="5cb87-120">Cela vous obligerait également à modifier le code qui rend les données persistantes dans le registre et à lire les données à partir du Registre (y compris le code qui lit à partir du Registre dans *CProjectName*::**FinalConstruct**).</span><span class="sxs-lookup"><span data-stu-id="5cb87-120">This would also require you to change the code that persists the data to the registry and reads the data from the registry (including the code that reads from the registry in *CProjectName*::**FinalConstruct**).</span></span>
-   <span data-ttu-id="5cb87-121">**Variable membre qui stocke la valeur de propriété.**</span><span class="sxs-lookup"><span data-stu-id="5cb87-121">**The member variable that stores the property value.**</span></span> <span data-ttu-id="5cb87-122">Cette variable est nommée « m \_ fScaleFactor » et est déclarée comme étant de type double.</span><span class="sxs-lookup"><span data-stu-id="5cb87-122">This variable is named "m\_fScaleFactor" and is declared as type double.</span></span> <span data-ttu-id="5cb87-123">Vous pouvez modifier le nom et le type de cette variable tout au long du projet.</span><span class="sxs-lookup"><span data-stu-id="5cb87-123">You may want to change the name and type of this variable throughout the project.</span></span>
-   <span data-ttu-id="5cb87-124">**Méthodes d’extraction et de propriété put.**</span><span class="sxs-lookup"><span data-stu-id="5cb87-124">**The property get and property put methods.**</span></span> <span data-ttu-id="5cb87-125">Vous souhaiterez peut-être modifier les noms, les paramètres et les implémentations de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5cb87-125">You might want to change the names, parameters, and implementations of these methods.</span></span> <span data-ttu-id="5cb87-126">N’oubliez pas également de refléter ces modifications ailleurs dans le projet.</span><span class="sxs-lookup"><span data-stu-id="5cb87-126">Don't forget to also reflect those changes elsewhere in the project.</span></span> <span data-ttu-id="5cb87-127">Par exemple, la méthode **apply** de la page de propriétés appelle **l' \_ échelle** *CProjectName*:: put.</span><span class="sxs-lookup"><span data-stu-id="5cb87-127">For instance, the property page **Apply** method calls *CProjectName*::**put\_scale**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cb87-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5cb87-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cb87-129">**Implémentation d’un plug-in DSP audio**</span><span class="sxs-lookup"><span data-stu-id="5cb87-129">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




