---
description: De nombreuses applications du panneau de configuration affichent une feuille de propriétés de propriétés pour permettre aux utilisateurs d’afficher et de modifier divers paramètres de périphérique et système.
title: Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour une application du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864917"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="04893-103">Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour une application du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="04893-103">How to Register and Implement a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="04893-104">De nombreuses applications du panneau de configuration affichent une feuille de propriétés de propriétés pour permettre aux utilisateurs d’afficher et de modifier divers paramètres de périphérique et système.</span><span class="sxs-lookup"><span data-stu-id="04893-104">Many Control Panel applications display a Properties property sheet to enable users to view and modify various device and system settings.</span></span> <span data-ttu-id="04893-105">Deux de ces applications (souris et affichage) permettent aux gestionnaires de feuille de propriétés de remplacer une ou plusieurs de leurs pages par une page personnalisée.</span><span class="sxs-lookup"><span data-stu-id="04893-105">Two of these applications—Mouse and Display—allow property sheet handlers to replace one or more of their pages with a custom page.</span></span> <span data-ttu-id="04893-106">La capture d’écran suivante montre la feuille de propriétés propriétés de la **souris** .</span><span class="sxs-lookup"><span data-stu-id="04893-106">The following screen shot shows the **Mouse Properties** property sheet.</span></span>

![feuille de propriétés propriétés de la souris](images/propsheethandler3.jpg)

<span data-ttu-id="04893-108">Les gestionnaires de feuille de propriétés pour les applications du panneau de configuration sont similaires à ceux des types de fichiers, avec deux exceptions principales :</span><span class="sxs-lookup"><span data-stu-id="04893-108">Property sheet handlers for Control Panel applications are similar to those for file types, with two primary exceptions:</span></span>

-   <span data-ttu-id="04893-109">Elles sont appelées par une application du panneau de configuration, et non par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="04893-109">They are called by a Control Panel application, not the Shell.</span></span>
-   <span data-ttu-id="04893-110">Ils sont enregistrés différemment.</span><span class="sxs-lookup"><span data-stu-id="04893-110">They are registered differently.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="04893-111">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="04893-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="04893-112">Technologies</span><span class="sxs-lookup"><span data-stu-id="04893-112">Technologies</span></span>

-   <span data-ttu-id="04893-113">Shell</span><span class="sxs-lookup"><span data-stu-id="04893-113">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="04893-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="04893-114">Prerequisites</span></span>

-   <span data-ttu-id="04893-115">Comprendre le panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="04893-115">An understanding of the Control Panel</span></span>
-   <span data-ttu-id="04893-116">Compréhension des menus contextuels</span><span class="sxs-lookup"><span data-stu-id="04893-116">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="04893-117">Instructions</span><span class="sxs-lookup"><span data-stu-id="04893-117">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="04893-118">Étape 1 : inscription d’un gestionnaire de feuille de propriétés pour une application du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="04893-118">Step 1: Registering a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="04893-119">Un gestionnaire de feuille de propriétés d’application du panneau de configuration doit être inscrit sous la sous-clé du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="04893-119">A Control Panel application property sheet handler must be registered under the Control Panel subkey.</span></span> <span data-ttu-id="04893-120">Cette clé peut être dans l’un des deux emplacements, selon que le gestionnaire doit être par utilisateur ou par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="04893-120">This key can be in either of two locations, depending on whether the handler is to be per-user or per-computer.</span></span> <span data-ttu-id="04893-121">Pour l’inscription par utilisateur, la sous-clé du panneau de configuration est **HKEY \_ Current \_ User** \\ **Control Panel**.</span><span class="sxs-lookup"><span data-stu-id="04893-121">For per-user registration, the Control Panel subkey is **HKEY\_CURRENT\_USER**\\**Control Panel**.</span></span> <span data-ttu-id="04893-122">La macro REGSTR \_ chemin d’accès \_ ControlPanel, telle que définie dans REGSTR. h, peut être utilisée dans le code à la place de « panneau de configuration ».</span><span class="sxs-lookup"><span data-stu-id="04893-122">The macro REGSTR\_PATH\_CONTROLPANEL as defined in Regstr.h can be used in code in place of "Control Panel".</span></span> <span data-ttu-id="04893-123">Pour l’inscription par ordinateur, l’emplacement est le suivant :</span><span class="sxs-lookup"><span data-stu-id="04893-123">For per-computer registration, the location is:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

<span data-ttu-id="04893-124">Ce chemin d’accès peut être référencé dans le code sous la forme HKEY \_ local \_ machine \\ REGSTR \_ path \_ CONTROLSFOLDER, à l’aide de la \_ \_ macro CONTROLSFOLDER Path REGSTR définie dans REGSTR. h.</span><span class="sxs-lookup"><span data-stu-id="04893-124">This path can be referred to in code as HKEY\_LOCAL\_MACHINE\\REGSTR\_PATH\_CONTROLSFOLDER, using the REGSTR\_PATH\_CONTROLSFOLDER macro that is defined in Regstr.h.</span></span>

<span data-ttu-id="04893-125">Les applications du panneau de configuration qui permettent aux gestionnaires de feuille de propriétés de remplacer des pages ont une sous-clé sous la sous-clé du panneau de configuration, nommée pour l’application, telle que la souris et l’affichage.</span><span class="sxs-lookup"><span data-stu-id="04893-125">The Control Panel applications that allow property sheet handlers to replace pages have a subkey under the Control Panel's subkey, named for the application, such as Mouse and Display.</span></span> <span data-ttu-id="04893-126">La sous-clé de l’application doit avoir une sous-clé **shellex** avec une sous-clé **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="04893-126">The application's subkey must have a **shellex** subkey with a **PropertySheetHandlers** subkey.</span></span> <span data-ttu-id="04893-127">Pour inscrire un gestionnaire de feuilles de propriétés, ajoutez son GUID à la sous-clé **PropertySheetHandlers** associée à l’application du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="04893-127">To register a property sheet handler, add its GUID to the **PropertySheetHandlers** subkey that is associated with the Control Panel application.</span></span> <span data-ttu-id="04893-128">Pour ce faire, créez une sous-clé de la sous-clé **PropertySheetHandlers** , nommée pour le gestionnaire de feuille de propriétés, et définissez sa valeur par défaut sur la forme de chaîne du GUID du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="04893-128">To do so, create a subkey of the **PropertySheetHandlers** subkey, named for the property sheet handler, and set its default value to the string form of the handler's GUID.</span></span>

<span data-ttu-id="04893-129">L’exemple suivant inscrit un gestionnaire de feuille de propriétés pour l’application du panneau de configuration de la souris sur chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="04893-129">The following example registers a property sheet handler for the Mouse Control Panel application on a per-computer basis.</span></span> <span data-ttu-id="04893-130">Pour l’inscrire au niveau de chaque utilisateur, remplacez **HKEY \_ local \_ machine** \\ **REGSTR \_ path \_ CONTROLSFOLDER** par **HKEY \_ Current \_ User** \\ **REGSTR \_ path \_ ControlPanel**.</span><span class="sxs-lookup"><span data-stu-id="04893-130">To register it on a per-user basis, replace **HKEY\_LOCAL\_MACHINE**\\**REGSTR\_PATH\_CONTROLSFOLDER** with **HKEY\_CURRENT\_USER**\\**REGSTR\_PATH\_CONTROLPANEL**.</span></span>

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="04893-131">Étape 2 : implémentation d’un gestionnaire de feuille de propriétés pour une application du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="04893-131">Step 2: Implementing a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="04893-132">La procédure d’implémentation d’un gestionnaire de feuilles de propriétés du panneau de configuration est très similaire à celle décrite dans [comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="04893-132">The procedure for implementing a Control Panel property sheet handler is very similar to that discussed in [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span> <span data-ttu-id="04893-133">La principale différence est que désormais, [**IShellPropSheetExt :: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) a besoin d’une implémentation sans jeton au lieu de [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="04893-133">The primary difference is that now [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) needs a nontoken implementation instead of [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span>

<span data-ttu-id="04893-134">Quand une application du panneau de configuration est sur le présent d’afficher sa feuille de propriétés, elle appelle la méthode [**IShellPropSheetExt :: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) du gestionnaire de feuilles de propriétés une fois pour chaque page qui peut être remplacée.</span><span class="sxs-lookup"><span data-stu-id="04893-134">When a Control Panel application is about to display its property sheet, it calls the property sheet handler's [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) method once for each page that can be replaced.</span></span> <span data-ttu-id="04893-135">Le paramètre *uPageID* est défini sur l’ID de la page.</span><span class="sxs-lookup"><span data-stu-id="04893-135">The *uPageID* parameter is set to the page's ID.</span></span> <span data-ttu-id="04893-136">Les ID des pages disponibles sont définis dans Cplext. h.</span><span class="sxs-lookup"><span data-stu-id="04893-136">The IDs for the available pages are defined in Cplext.h.</span></span> <span data-ttu-id="04893-137">Les ID actuellement disponibles sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="04893-137">The currently available IDs are listed in the following table.</span></span> 

| <span data-ttu-id="04893-138">ID de page</span><span class="sxs-lookup"><span data-stu-id="04893-138">Page ID</span></span>                      | <span data-ttu-id="04893-139">Description</span><span class="sxs-lookup"><span data-stu-id="04893-139">Description</span></span>         | <span data-ttu-id="04893-140">Application du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="04893-140">Control Panel application</span></span> |
|------------------------------|---------------------|---------------------------|
| <span data-ttu-id="04893-141">CPLPAGE \_ boutons de la souris \_</span><span class="sxs-lookup"><span data-stu-id="04893-141">CPLPAGE\_MOUSE\_BUTTONS</span></span>      | <span data-ttu-id="04893-142">Page boutons</span><span class="sxs-lookup"><span data-stu-id="04893-142">The Buttons page</span></span>    | <span data-ttu-id="04893-143">Souris</span><span class="sxs-lookup"><span data-stu-id="04893-143">Mouse</span></span>                     |
| <span data-ttu-id="04893-144">CPLPAGE \_ souris \_ PTRMOTION</span><span class="sxs-lookup"><span data-stu-id="04893-144">CPLPAGE\_MOUSE\_PTRMOTION</span></span>    | <span data-ttu-id="04893-145">La page de mouvement</span><span class="sxs-lookup"><span data-stu-id="04893-145">The Motion page</span></span>     | <span data-ttu-id="04893-146">Souris</span><span class="sxs-lookup"><span data-stu-id="04893-146">Mouse</span></span>                     |
| <span data-ttu-id="04893-147">\_roulette de la souris CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="04893-147">CPLPAGE\_MOUSE\_WHEEL</span></span>        | <span data-ttu-id="04893-148">Page de la roulette</span><span class="sxs-lookup"><span data-stu-id="04893-148">The Wheel page</span></span>      | <span data-ttu-id="04893-149">Souris</span><span class="sxs-lookup"><span data-stu-id="04893-149">Mouse</span></span>                     |
| <span data-ttu-id="04893-150">\_Vitesse du clavier CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="04893-150">CPLPAGE\_KEYBOARD\_SPEED</span></span>     | <span data-ttu-id="04893-151">Page Vitesse</span><span class="sxs-lookup"><span data-stu-id="04893-151">The Speed page</span></span>      | <span data-ttu-id="04893-152">Clavier</span><span class="sxs-lookup"><span data-stu-id="04893-152">Keyboard</span></span>                  |
| <span data-ttu-id="04893-153">\_ \_ arrière-plan d’affichage CPLPAGE</span><span class="sxs-lookup"><span data-stu-id="04893-153">CPLPAGE\_DISPLAY\_BACKGROUND</span></span> | <span data-ttu-id="04893-154">Page d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="04893-154">The Background page</span></span> | <span data-ttu-id="04893-155">Afficher</span><span class="sxs-lookup"><span data-stu-id="04893-155">Display</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="04893-156">Notes</span><span class="sxs-lookup"><span data-stu-id="04893-156">Remarks</span></span>

<span data-ttu-id="04893-157">La procédure de création et de remplacement d’une page est identique à celle de l’ajout d’une page.</span><span class="sxs-lookup"><span data-stu-id="04893-157">The procedure for creating and replacing a page is identical to that for adding a page.</span></span> <span data-ttu-id="04893-158">Pour plus d’informations, consultez [comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="04893-158">For more information, see [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span>

 

 



