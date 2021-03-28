---
description: Windows Vista utilise plus d’images miniatures spécifiques aux fichiers que les versions antérieures de Windows.
title: Gestionnaires de miniatures
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209933"
---
# <a name="thumbnail-handlers"></a><span data-ttu-id="05d71-103">Gestionnaires de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-103">Thumbnail Handlers</span></span>

<span data-ttu-id="05d71-104">Windows Vista utilise plus d’images miniatures spécifiques aux fichiers que les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="05d71-104">Windows Vista makes greater use of file-specific thumbnail images than earlier versions of Windows.</span></span> <span data-ttu-id="05d71-105">Windows Vista les utilise dans tous les affichages, dans les boîtes de dialogue et dans tout type de fichier qui les fournit.</span><span class="sxs-lookup"><span data-stu-id="05d71-105">Windows Vista uses them in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="05d71-106">D’autres applications peuvent également utiliser votre miniature.</span><span class="sxs-lookup"><span data-stu-id="05d71-106">Other applications can consume your thumbnail as well.</span></span> <span data-ttu-id="05d71-107">L’affichage des miniatures a également changé.</span><span class="sxs-lookup"><span data-stu-id="05d71-107">Thumbnail display has also changed.</span></span> <span data-ttu-id="05d71-108">À présent, un spectre continu de tailles sélectionnables par l’utilisateur est disponible au lieu des tailles discrètes, telles que les icônes et les miniatures fournies dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="05d71-108">Now, a continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails provided in Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="05d71-109">Vous pouvez entendre ces miniatures désignées par le terme « icônes dynamiques ».</span><span class="sxs-lookup"><span data-stu-id="05d71-109">You might hear these thumbnails referred to as Live Icons.</span></span>

 

<span data-ttu-id="05d71-110">Les miniatures de résolution 32 bits et aussi volumineuses que les pixels 256x256 sont souvent utilisées dans l’interface utilisateur de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05d71-110">Thumbnails of 32-bit resolution and as large as 256x256 pixels are often used in Windows Vista UI.</span></span> <span data-ttu-id="05d71-111">Les propriétaires de format de fichier doivent être prêts à afficher leurs miniatures à cette taille.</span><span class="sxs-lookup"><span data-stu-id="05d71-111">File format owners should be prepared to display their thumbnails at that size.</span></span> <span data-ttu-id="05d71-112">Ils doivent également fournir des images non statiques pour leurs miniatures qui reflètent le contenu d’un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="05d71-112">They should also provide non-static images for their thumbnails that reflect the particular file's contents.</span></span> <span data-ttu-id="05d71-113">Par exemple, la miniature d’un fichier texte doit afficher une version miniature du document, y compris son texte.</span><span class="sxs-lookup"><span data-stu-id="05d71-113">For example, a text file's thumbnail should show a miniature version of the document, including its text.</span></span>

<span data-ttu-id="05d71-114">L’interface [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) a été introduite pour rendre une miniature plus facile et plus simple que dans le passé, lorsque [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) aurait été utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="05d71-114">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface has been introduced to make providing a thumbnail easier and more straightforward than in the past, when [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) would have been used instead.</span></span> <span data-ttu-id="05d71-115">Notez que le code existant qui utilise **IExtractImage** est toujours valide sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05d71-115">Note, that existing code that uses **IExtractImage** is still valid under Windows Vista.</span></span> <span data-ttu-id="05d71-116">Toutefois, **IExtractImage** n’est pas pris en charge dans le volet d' **informations** .</span><span class="sxs-lookup"><span data-stu-id="05d71-116">However, **IExtractImage** is not supported in the **Details** pane.</span></span>

<span data-ttu-id="05d71-117">Cette rubrique traite des sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="05d71-117">This topic discusses the following:</span></span>

-   [<span data-ttu-id="05d71-118">Processus de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-118">Thumbnail Processes</span></span>](#thumbnail-processes)
-   [<span data-ttu-id="05d71-119">Cache de miniatures et dimensionnement</span><span class="sxs-lookup"><span data-stu-id="05d71-119">Thumbnail Cache and Sizing</span></span>](#thumbnail-cache-and-sizing)
-   [<span data-ttu-id="05d71-120">Superpositions de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-120">Thumbnail Overlays</span></span>](#thumbnail-overlays)
-   [<span data-ttu-id="05d71-121">Ornements de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-121">Thumbnail Adornments</span></span>](#thumbnail-adornments)
-   [<span data-ttu-id="05d71-122">Inscription de votre gestionnaire de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-122">Registering Your Thumbnail Handler</span></span>](#registering-your-thumbnail-handler)
-   [<span data-ttu-id="05d71-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05d71-123">Related topics</span></span>](#related-topics)

## <a name="thumbnail-processes"></a><span data-ttu-id="05d71-124">Processus de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-124">Thumbnail Processes</span></span>

<span data-ttu-id="05d71-125">Les gestionnaires, y compris les gestionnaires de miniatures, s’exécutent par défaut dans un processus distinct.</span><span class="sxs-lookup"><span data-stu-id="05d71-125">Handlers, including thumbnail handlers, run by default in a separate process.</span></span> <span data-ttu-id="05d71-126">Vous pouvez forcer le gestionnaire à s’exécuter in-process en passant une valeur **null** comme contexte de liaison dans un appel à [**IShellItem :: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="05d71-126">You can force the handler to run in-process by passing a **NULL** value as the bind context in a call to [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) as shown here:</span></span>


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



<span data-ttu-id="05d71-127">Vous pouvez également refuser l’exécution hors processus par défaut en définissant l’entrée DisableProcessIsolation dans le registre, comme indiqué dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="05d71-127">You can also opt out of running out of process by default by setting the DisableProcessIsolation entry in the registry as shown in this example.</span></span> <span data-ttu-id="05d71-128">L’identificateur de classe (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} est le CLSID pour les implémentations de [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .</span><span class="sxs-lookup"><span data-stu-id="05d71-128">The class identifier (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} is the CLSID for [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) implementations.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a><span data-ttu-id="05d71-129">Cache de miniatures et dimensionnement</span><span class="sxs-lookup"><span data-stu-id="05d71-129">Thumbnail Cache and Sizing</span></span>

<span data-ttu-id="05d71-130">Quand une miniature est nécessaire, Windows vérifie d’abord le cache de miniatures pour l’image.</span><span class="sxs-lookup"><span data-stu-id="05d71-130">When a thumbnail is needed, Windows first checks the thumbnail cache for the image.</span></span> <span data-ttu-id="05d71-131">L’extracteur de miniatures est appelé si l’image est introuvable dans le cache.</span><span class="sxs-lookup"><span data-stu-id="05d71-131">The thumbnail extractor is called if the image is not found in the cache.</span></span> <span data-ttu-id="05d71-132">Elle est également appelée lorsque l’heure de la dernière modification de l’image est ultérieure à celle de la copie dans le cache.</span><span class="sxs-lookup"><span data-stu-id="05d71-132">It is also called when the last modified time of the image is later than that of the copy in the cache.</span></span>

<span data-ttu-id="05d71-133">Les images miniatures de ce cache sont stockées dans un ensemble de tailles discrètes.</span><span class="sxs-lookup"><span data-stu-id="05d71-133">The thumbnail images in this cache are stored in a set of discrete sizes.</span></span> <span data-ttu-id="05d71-134">Toutes les tailles sont exprimées en pixels.</span><span class="sxs-lookup"><span data-stu-id="05d71-134">All sizes are given in pixels.</span></span>

-   <span data-ttu-id="05d71-135">32x32</span><span class="sxs-lookup"><span data-stu-id="05d71-135">32x32</span></span>
-   <span data-ttu-id="05d71-136">96 x 96</span><span class="sxs-lookup"><span data-stu-id="05d71-136">96x96</span></span>
-   <span data-ttu-id="05d71-137">256 x 256</span><span class="sxs-lookup"><span data-stu-id="05d71-137">256x256</span></span>
-   <span data-ttu-id="05d71-138">1024x1024</span><span class="sxs-lookup"><span data-stu-id="05d71-138">1024x1024</span></span>

> [!Note]  
> <span data-ttu-id="05d71-139">Ces valeurs sont sujettes à modification.</span><span class="sxs-lookup"><span data-stu-id="05d71-139">These values are subject to change.</span></span> <span data-ttu-id="05d71-140">Vous ne devez pas supposer que toute taille particulière sera toujours utilisée.</span><span class="sxs-lookup"><span data-stu-id="05d71-140">You code should not assume that any particular size will always be used.</span></span>

 

<span data-ttu-id="05d71-141">Si une image n’est pas carrée, vous ne devez pas la remplir vous-même.</span><span class="sxs-lookup"><span data-stu-id="05d71-141">If an image is not square, you should not pad it yourself.</span></span> <span data-ttu-id="05d71-142">Windows est chargé de respecter les proportions d’origine et de remplir l’image à une taille carrée.</span><span class="sxs-lookup"><span data-stu-id="05d71-142">Windows is responsible for respecting the original aspect ratio and padding the image to a square size.</span></span>

<span data-ttu-id="05d71-143">Quand une image d’une taille particulière est demandée, sauf si une correspondance exacte est trouvée, Windows Vista récupère toujours la plus grande image suivante et la met à l’échelle jusqu’à la taille demandée.</span><span class="sxs-lookup"><span data-stu-id="05d71-143">When an image of a particular size is asked for, unless an exact match is found, Windows Vista always retrieves the next largest image and scales it down to the requested size.</span></span> <span data-ttu-id="05d71-144">Une image n’est jamais montée en puissance comme c’était le cas dans les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="05d71-144">An image is never scaled up in size as was the case in previous versions of Windows.</span></span>

<span data-ttu-id="05d71-145">Le tableau suivant donne quelques exemples de la relation entre la taille demandée et la taille disponible.</span><span class="sxs-lookup"><span data-stu-id="05d71-145">The following table gives some examples of the relationship between requested size and available size.</span></span>



| <span data-ttu-id="05d71-146">Taille d’image maximale que vous fournissez</span><span class="sxs-lookup"><span data-stu-id="05d71-146">Maximum Image Size You Provide</span></span> | <span data-ttu-id="05d71-147">Taille demandée par l’extracteur</span><span class="sxs-lookup"><span data-stu-id="05d71-147">Size Requested by the Extractor</span></span> | <span data-ttu-id="05d71-148">Vous fournissez</span><span class="sxs-lookup"><span data-stu-id="05d71-148">You Provide</span></span>                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| <span data-ttu-id="05d71-149">156x120</span><span class="sxs-lookup"><span data-stu-id="05d71-149">156x120</span></span>                        | <span data-ttu-id="05d71-150">256 x 256</span><span class="sxs-lookup"><span data-stu-id="05d71-150">256x256</span></span>                         | <span data-ttu-id="05d71-151">156x120 (ne pas remplir, conserver les proportions)</span><span class="sxs-lookup"><span data-stu-id="05d71-151">156x120 (Do not pad, maintain aspect ratio)</span></span> |
| <span data-ttu-id="05d71-152">2048x1024</span><span class="sxs-lookup"><span data-stu-id="05d71-152">2048x1024</span></span>                      | <span data-ttu-id="05d71-153">256 x 256</span><span class="sxs-lookup"><span data-stu-id="05d71-153">256x256</span></span>                         | <span data-ttu-id="05d71-154">256 x 128 (ne pas remplir, conserver les proportions)</span><span class="sxs-lookup"><span data-stu-id="05d71-154">256x128 (Do not pad, maintain aspect ratio)</span></span> |



 

<span data-ttu-id="05d71-155">Vous pouvez déclarer un point de coupure dans le cadre de l’entrée de l’ID de programme de l’application associée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="05d71-155">You can declare a cutoff point as part of the program ID entry of the associated app in the registry.</span></span> <span data-ttu-id="05d71-156">En dessous de cette taille, les miniatures ne sont pas utilisées.</span><span class="sxs-lookup"><span data-stu-id="05d71-156">Below this size, thumbnails are not used.</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

<span data-ttu-id="05d71-157">L’entrée ThumbnailCutoff est l’une de ces \_ valeurs de Reg DWORD.</span><span class="sxs-lookup"><span data-stu-id="05d71-157">The ThumbnailCutoff entry is one of these REG\_DWORD values.</span></span>

| <span data-ttu-id="05d71-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="05d71-158">Value</span></span> | <span data-ttu-id="05d71-159">Coupure</span><span class="sxs-lookup"><span data-stu-id="05d71-159">Cutoff</span></span> | <span data-ttu-id="05d71-160">HighDPI sensible</span><span class="sxs-lookup"><span data-stu-id="05d71-160">HighDPI Sensitive</span></span> |
|-------|--------|-------------------|
| <span data-ttu-id="05d71-161">0</span><span class="sxs-lookup"><span data-stu-id="05d71-161">0</span></span>     | <span data-ttu-id="05d71-162">32x32</span><span class="sxs-lookup"><span data-stu-id="05d71-162">32x32</span></span>  | <span data-ttu-id="05d71-163">Oui</span><span class="sxs-lookup"><span data-stu-id="05d71-163">Yes</span></span>               |
| <span data-ttu-id="05d71-164">1</span><span class="sxs-lookup"><span data-stu-id="05d71-164">1</span></span>     | <span data-ttu-id="05d71-165">16x16</span><span class="sxs-lookup"><span data-stu-id="05d71-165">16x16</span></span>  | <span data-ttu-id="05d71-166">Oui</span><span class="sxs-lookup"><span data-stu-id="05d71-166">Yes</span></span>               |
| <span data-ttu-id="05d71-167">2</span><span class="sxs-lookup"><span data-stu-id="05d71-167">2</span></span>     | <span data-ttu-id="05d71-168">48 x 48</span><span class="sxs-lookup"><span data-stu-id="05d71-168">48x48</span></span>  | <span data-ttu-id="05d71-169">Oui</span><span class="sxs-lookup"><span data-stu-id="05d71-169">Yes</span></span>               |
| <span data-ttu-id="05d71-170">3</span><span class="sxs-lookup"><span data-stu-id="05d71-170">3</span></span>     | <span data-ttu-id="05d71-171">16x16</span><span class="sxs-lookup"><span data-stu-id="05d71-171">16x16</span></span>  | <span data-ttu-id="05d71-172">Oui</span><span class="sxs-lookup"><span data-stu-id="05d71-172">Yes</span></span>               |


<span data-ttu-id="05d71-173">La sensibilité en points par pouce (dpi) élevée signifie que les dimensions en pixels de la miniature s’ajustent automatiquement pour une résolution supérieure.</span><span class="sxs-lookup"><span data-stu-id="05d71-173">High dots per inch (dpi) sensitivity means that the pixel dimensions of the thumbnail automatically adjust for the greater dpi.</span></span> <span data-ttu-id="05d71-174">Par exemple, une image 32x32 à 96 ppp serait une image 40 x 40 à 120 ppp.</span><span class="sxs-lookup"><span data-stu-id="05d71-174">For instance, a 32x32 image at 96 dpi would be a 40x40 image at 120 dpi.</span></span>

<span data-ttu-id="05d71-175">Si l’entrée ThumbnailCutoff n’est pas spécifiée, la limite par défaut est 20x20 (non-respect de la dpi).</span><span class="sxs-lookup"><span data-stu-id="05d71-175">If the ThumbnailCutoff entry is not specified, the default cutoff is 20x20 (not dpi-sensitive).</span></span>

## <a name="thumbnail-overlays"></a><span data-ttu-id="05d71-176">Superpositions de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-176">Thumbnail Overlays</span></span>

<span data-ttu-id="05d71-177">Les superpositions de miniatures, une petite image affichée dans le coin inférieur droit de la miniature, donnent aux développeurs la possibilité d’appliquer une identification de marques à leurs miniatures.</span><span class="sxs-lookup"><span data-stu-id="05d71-177">Thumbnail overlays, a small image displayed over the lower right corner of the thumbnail, provide an opportunity for developers to apply brand identification to their thumbnails.</span></span> <span data-ttu-id="05d71-178">Les superpositions sont déclarées dans le registre dans le cadre de l’entrée de l’ID de programme de l’application associée, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="05d71-178">Overlays are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

<span data-ttu-id="05d71-179">L’entrée TypeOverlay contient une valeur de REG \_ SZ interprétée comme suit :</span><span class="sxs-lookup"><span data-stu-id="05d71-179">The TypeOverlay entry contains a REG\_SZ value interpreted as follows:</span></span>

-   <span data-ttu-id="05d71-180">Si la valeur est une référence de ressource (un fichier **. ico** incorporé dans la dll) telle que `ISVComponent.dll,-155` , cette image est utilisée comme superposition pour les fichiers avec cette extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="05d71-180">If the value is a resource reference (a **.ico** file embedded in the DLL) such as `ISVComponent.dll,-155`, that image is used as the overlay for files with that file name extension.</span></span> <span data-ttu-id="05d71-181">Notez que dans cet exemple, **155** est l’ID de la ressource, et si la dll n’est pas présente dans un chemin d’accès standard (tel que **C:/Windows/system32**), le chemin d’accès complet est requis au lieu de simplement le nom de la dll.</span><span class="sxs-lookup"><span data-stu-id="05d71-181">Note that in this example, **155** is the resouce ID, and if the DLL is not present in a standard path (such as **C:/Windows/System32**), the full path is required instead of just the DLL name.</span></span>
-   <span data-ttu-id="05d71-182">Si la valeur est une chaîne vide, aucune superposition n’est appliquée à l’image.</span><span class="sxs-lookup"><span data-stu-id="05d71-182">If the value is an empty string, no overlay is applied to the image.</span></span>
-   <span data-ttu-id="05d71-183">Si la valeur n’est pas présente, l’icône par défaut de l’application associée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="05d71-183">If the value is not present, the default icon of the associated application is used.</span></span>

<span data-ttu-id="05d71-184">Les superpositions de vos miniatures doivent uniquement être fournies par le biais de ce mécanisme et appliquées par Windows.</span><span class="sxs-lookup"><span data-stu-id="05d71-184">Overlays for your thumbnails should only be provided through this mechanism and applied by Windows.</span></span> <span data-ttu-id="05d71-185">N’appliquez pas les superpositions vous-même.</span><span class="sxs-lookup"><span data-stu-id="05d71-185">Do not apply overlays yourself.</span></span>

## <a name="thumbnail-adornments"></a><span data-ttu-id="05d71-186">Ornements de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-186">Thumbnail Adornments</span></span>

<span data-ttu-id="05d71-187">Les ornements, tels que les ombres portées, sont appliqués aux miniatures en fonction du thème actuellement sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05d71-187">Adornments such as drop shadows are applied to thumbnails based on the user's currently selected theme.</span></span> <span data-ttu-id="05d71-188">Les ornements sont fournis par Windows ; ne les créez pas vous-même.</span><span class="sxs-lookup"><span data-stu-id="05d71-188">Adornments are provided by Windows; do not create them yourself.</span></span> <span data-ttu-id="05d71-189">Windows peut modifier l’apparence d’ornements particuliers à tout moment. par conséquent, si vous vous êtes assuré, vous risquez de ne pas être synchronisé avec le système.</span><span class="sxs-lookup"><span data-stu-id="05d71-189">Windows could change the look of particular adornments at any time, so if you provided you own you would risk falling out of sync with the system.</span></span> <span data-ttu-id="05d71-190">Vos miniatures peuvent être plus ou moins récentes.</span><span class="sxs-lookup"><span data-stu-id="05d71-190">Your thumbnails could wind up looking dated or out of place.</span></span>

<span data-ttu-id="05d71-191">Les ornements potentiels sont déclarés dans le registre dans le cadre de l’entrée de l’ID de programme de l’application associée, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="05d71-191">Potential adornments are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

<span data-ttu-id="05d71-192">L’entrée de traitement contient une des valeurs de REG \_ DWORD suivantes :</span><span class="sxs-lookup"><span data-stu-id="05d71-192">The Treatment entry contains one of these REG\_DWORD values:</span></span>



| <span data-ttu-id="05d71-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="05d71-193">Value</span></span> | <span data-ttu-id="05d71-194">Signification</span><span class="sxs-lookup"><span data-stu-id="05d71-194">Meaning</span></span>         |
|-------|-----------------|
| <span data-ttu-id="05d71-195">0</span><span class="sxs-lookup"><span data-stu-id="05d71-195">0</span></span>     | <span data-ttu-id="05d71-196">Aucun ornement</span><span class="sxs-lookup"><span data-stu-id="05d71-196">No Adornment</span></span>    |
| <span data-ttu-id="05d71-197">1</span><span class="sxs-lookup"><span data-stu-id="05d71-197">1</span></span>     | <span data-ttu-id="05d71-198">Ombre portée</span><span class="sxs-lookup"><span data-stu-id="05d71-198">Drop Shadow</span></span>     |
| <span data-ttu-id="05d71-199">2</span><span class="sxs-lookup"><span data-stu-id="05d71-199">2</span></span>     | <span data-ttu-id="05d71-200">Bordure photo</span><span class="sxs-lookup"><span data-stu-id="05d71-200">Photo Border</span></span>    |
| <span data-ttu-id="05d71-201">3</span><span class="sxs-lookup"><span data-stu-id="05d71-201">3</span></span>     | <span data-ttu-id="05d71-202">Des fusées vidéo</span><span class="sxs-lookup"><span data-stu-id="05d71-202">Video Sprockets</span></span> |


<span data-ttu-id="05d71-203">Une ombre portée est appliquée aux images par défaut.</span><span class="sxs-lookup"><span data-stu-id="05d71-203">A drop shadow is applied to images by default.</span></span>

## <a name="registering-your-thumbnail-handler"></a><span data-ttu-id="05d71-204">Inscription de votre gestionnaire de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-204">Registering Your Thumbnail Handler</span></span>

<span data-ttu-id="05d71-205">L’inscription d’un gestionnaire de miniatures est basée sur les associations de fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="05d71-205">Registration of a thumbnail handler is based on standard file associations.</span></span>

<span data-ttu-id="05d71-206">Le GUID de l’extension de Shell du gestionnaire de miniatures est `E357FCCD-A995-4576-B01F-234630154E96` .</span><span class="sxs-lookup"><span data-stu-id="05d71-206">The GUID for the thumbnail handler Shell extension is `E357FCCD-A995-4576-B01F-234630154E96`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05d71-207">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05d71-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05d71-208">**IThumbnailProvider**</span><span class="sxs-lookup"><span data-stu-id="05d71-208">**IThumbnailProvider**</span></span>](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[<span data-ttu-id="05d71-209">Création de gestionnaires de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-209">Building Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="05d71-210">Instructions du gestionnaire de miniatures</span><span class="sxs-lookup"><span data-stu-id="05d71-210">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



