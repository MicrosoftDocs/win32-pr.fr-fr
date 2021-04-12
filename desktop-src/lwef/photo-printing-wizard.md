---
title: Assistant impression de photos
description: L’Assistant impression de photos aide les utilisateurs à imprimer des photos en fournissant une interface d’assistant facile à utiliser.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Assistant impression de photos
- IDropTarget, Assistant impression de photos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381932"
---
# <a name="photo-printing-wizard"></a><span data-ttu-id="27c55-105">Assistant impression de photos</span><span class="sxs-lookup"><span data-stu-id="27c55-105">Photo Printing Wizard</span></span>

<span data-ttu-id="27c55-106">L’Assistant impression de photos aide les utilisateurs à imprimer des photos en fournissant une interface d’assistant facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="27c55-106">The Photo Printing Wizard helps users print photos by providing an easy-to-use wizard interface.</span></span> <span data-ttu-id="27c55-107">L’Assistant permet à l’utilisateur de spécifier des tailles d’impression photo et d’autres options d’impression, puis envoie les photos à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="27c55-107">The wizard enables the user to specify photo print sizes and other print options, and then sends the photos to the printer.</span></span> <span data-ttu-id="27c55-108">L’Assistant est conçu afin de pouvoir être appelé par programme par une application qui souhaite offrir aux utilisateurs la possibilité d’imprimer des photos et de spécifier le dimensionnement et d’autres options d’impression.</span><span class="sxs-lookup"><span data-stu-id="27c55-108">The wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to print photos and specify sizing and other print options.</span></span> <span data-ttu-id="27c55-109">L’Assistant impression de photos est disponible sur Windows XP et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="27c55-109">The Photo Printing Wizard is available on Windows XP and Windows Vista.</span></span>

-   [<span data-ttu-id="27c55-110">Fonctionnalités fournies par l’Assistant impression de photos</span><span class="sxs-lookup"><span data-stu-id="27c55-110">Features Provided by the Photo Print Wizard</span></span>](#features-provided-by-the-photo-print-wizard)
-   [<span data-ttu-id="27c55-111">Formats de fichier photo pris en charge</span><span class="sxs-lookup"><span data-stu-id="27c55-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="27c55-112">Lancement de l’Assistant impression de photos par programmation</span><span class="sxs-lookup"><span data-stu-id="27c55-112">Programmatically Launching the Photo Print Wizard</span></span>](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a><span data-ttu-id="27c55-113">Fonctionnalités fournies par l’Assistant impression de photos</span><span class="sxs-lookup"><span data-stu-id="27c55-113">Features Provided by the Photo Print Wizard</span></span>

<span data-ttu-id="27c55-114">L’Assistant impression de photos offre plusieurs options qui peuvent ne pas être disponibles dans les boîtes de dialogue d’imprimante courantes, telles que les modèles à plusieurs dispositions avec des dimensions précises.</span><span class="sxs-lookup"><span data-stu-id="27c55-114">The Photo Printing Wizard offers several options that may not be available on common printer dialogs, such as multi-layout templates with accurate dimensions.</span></span> <span data-ttu-id="27c55-115">Les modèles de disposition permettent aux utilisateurs de tirer le meilleur parti de l’espace disponible sur le papier d’impression photographique.</span><span class="sxs-lookup"><span data-stu-id="27c55-115">The layout templates enable users to make the most efficient use of the space available on photographic printing paper.</span></span> <span data-ttu-id="27c55-116">Les autres options qui peuvent être spécifiées ou accessibles via l’Assistant impression de photos sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="27c55-116">Other options that can be specified or accessed through the Photo Print Wizard include:</span></span>

-   <span data-ttu-id="27c55-117">Sélection d’une imprimante dans une liste d’imprimantes disponibles ou de destinations d’impression virtuelles (par exemple, Microsoft XPS document Writer).</span><span class="sxs-lookup"><span data-stu-id="27c55-117">Selecting a printer from a list of available printers or virtual printing destinations (for example, Microsoft XPS Document Writer).</span></span> <span data-ttu-id="27c55-118">Sur Windows Vista, les options suivantes peuvent être disponibles, en fonction des fonctionnalités de l’imprimante ou de la destination d’impression virtuelle :</span><span class="sxs-lookup"><span data-stu-id="27c55-118">On Windows Vista, the following options may be available, depending on the capabilities of the printer or virtual printing destination:</span></span>
    -   <span data-ttu-id="27c55-119">Format du papier.</span><span class="sxs-lookup"><span data-stu-id="27c55-119">Paper size.</span></span> <span data-ttu-id="27c55-120">Par exemple, « letter », « Legal », « a3 ».</span><span class="sxs-lookup"><span data-stu-id="27c55-120">For example, "Letter", "Legal", "A3".</span></span>
    -   <span data-ttu-id="27c55-121">Qualité d’impression, en termes de résolutions de points par pouce (dpi) prises en charge.</span><span class="sxs-lookup"><span data-stu-id="27c55-121">Print quality, in terms of supported dots per inch (dpi) resolutions.</span></span>
    -   <span data-ttu-id="27c55-122">Type de papier.</span><span class="sxs-lookup"><span data-stu-id="27c55-122">Paper type.</span></span> <span data-ttu-id="27c55-123">Par exemple, « plain » ou « brillante ».</span><span class="sxs-lookup"><span data-stu-id="27c55-123">For example, "Plain" or "Glossy".</span></span>
-   <span data-ttu-id="27c55-124">Lancement des préférences et des propriétés d’impression pour une imprimante particulière.</span><span class="sxs-lookup"><span data-stu-id="27c55-124">Launching the printing preferences and properties for a particular printer.</span></span>
-   <span data-ttu-id="27c55-125">Définir les **copies de chaque image** (sur Windows Vista) ou le **nombre d’utilisations de chaque image** (sur Windows XP) valeurs de la zone de sélection numérique.</span><span class="sxs-lookup"><span data-stu-id="27c55-125">Setting the **Copies of each picture** (on Windows Vista) or **Number of times to use each picture** (on Windows XP) spin box values.</span></span>
-   <span data-ttu-id="27c55-126">Spécification d’un modèle de mise en page.</span><span class="sxs-lookup"><span data-stu-id="27c55-126">Specifying a print layout template.</span></span> <span data-ttu-id="27c55-127">Par exemple, les **photos en pleine page** ou les **tirages Wallet**.</span><span class="sxs-lookup"><span data-stu-id="27c55-127">For example, **Full page photo** or **Wallet prints**.</span></span>
-   <span data-ttu-id="27c55-128">Sélection de l’option **adapter l’image au cadre** (disponible sur Windows Vista uniquement).</span><span class="sxs-lookup"><span data-stu-id="27c55-128">Selecting the **Fit picture to frame** option (available on Windows Vista only).</span></span>
-   <span data-ttu-id="27c55-129">Aperçu de la photo imprimée avec les options actuellement spécifiées.</span><span class="sxs-lookup"><span data-stu-id="27c55-129">Previewing the printed photo with the currently specified options.</span></span>
-   <span data-ttu-id="27c55-130">Accès aux options d’impression avancées, telles que la **netteté pour l’impression** et la **gestion des couleurs** (disponible sur Windows Vista uniquement).</span><span class="sxs-lookup"><span data-stu-id="27c55-130">Accesssing advanced print options, such as **Sharpen for printing** and **Color management** (available on Windows Vista only).</span></span>

<span data-ttu-id="27c55-131">Toute application peut bénéficier de la fonctionnalité d’impression de photos et de fonctionnalités offerte par l’Assistant impression de photos.</span><span class="sxs-lookup"><span data-stu-id="27c55-131">Any application can benefit from the features and photo printing capability offered by the Photo Printing Wizard.</span></span> <span data-ttu-id="27c55-132">Une application peut transmettre les fichiers à imprimer.</span><span class="sxs-lookup"><span data-stu-id="27c55-132">An application can pass in the files to be printed.</span></span> <span data-ttu-id="27c55-133">L’Assistant impression de photos prend alors soin de préparer le fichier pour l’impression en fonction des options spécifiées par l’utilisateur et envoie les fichiers préparés à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="27c55-133">The Photo Printing Wizard then takes care of preparing the file for printing based on the options specified by the user and sends the prepared files to the printer.</span></span>

<span data-ttu-id="27c55-134">L’illustration suivante montre l’interface de l’Assistant impression de photos sur Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27c55-134">The following figure shows the Photo Printing Wizard interface on Windows Vista</span></span>

![Assistant impression de photos sur Windows Vista](images/ppw-vista.png)

<span data-ttu-id="27c55-136">L’illustration suivante montre l’interface de l’Assistant impression de photos sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="27c55-136">The following figure shows the Photo Printing Wizard interface on Windows XP</span></span>

![Assistant impression de photos sur Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="27c55-138">Formats de fichier photo pris en charge</span><span class="sxs-lookup"><span data-stu-id="27c55-138">Supported Photo File Formats</span></span>

<span data-ttu-id="27c55-139">Sur Windows XP, l’Assistant impression de photos prend en charge tous les formats de fichiers graphiques pris en charge par Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="27c55-139">On Windows XP, the Photo Print Wizard supports all graphics file formats that are supported by Windows GDI+.</span></span> <span data-ttu-id="27c55-140">Actuellement, ces formats de fichier sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="27c55-140">Currently, these file formats include:</span></span>

-   <span data-ttu-id="27c55-141">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="27c55-141">Bitmap (BMP)</span></span>
-   <span data-ttu-id="27c55-142">format GIF (Graphics Interchange Format)</span><span class="sxs-lookup"><span data-stu-id="27c55-142">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="27c55-143">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="27c55-143">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="27c55-144">Fichier image d’échange (EXIF)</span><span class="sxs-lookup"><span data-stu-id="27c55-144">Exchangeable Image File (EXIF)</span></span>
-   <span data-ttu-id="27c55-145">format PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="27c55-145">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="27c55-146">format TIFF (Tagged Image File Format)</span><span class="sxs-lookup"><span data-stu-id="27c55-146">Tagged Image File Format (TIFF)</span></span>

<span data-ttu-id="27c55-147">Pour plus d’informations sur les formats de fichiers graphiques pris en charge par GDI+, consultez [types de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span><span class="sxs-lookup"><span data-stu-id="27c55-147">For more information about graphics file formats supported by GDI+, see [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span></span>

<span data-ttu-id="27c55-148">Sur Windows Vista, l’Assistant impression de photos prend en charge tout format de fichier image pour lequel un codec WIC (Windows Imaging Component) est installé.</span><span class="sxs-lookup"><span data-stu-id="27c55-148">On Windows Vista, the Photo Print Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="27c55-149">WIC fournit plusieurs codecs standard, notamment :</span><span class="sxs-lookup"><span data-stu-id="27c55-149">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="27c55-150">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="27c55-150">Bitmap (BMP)</span></span>
-   <span data-ttu-id="27c55-151">GIF</span><span class="sxs-lookup"><span data-stu-id="27c55-151">GIF</span></span>
-   <span data-ttu-id="27c55-152">Format d’icône (ICO)</span><span class="sxs-lookup"><span data-stu-id="27c55-152">Icon Format (ICO)</span></span>
-   <span data-ttu-id="27c55-153">JPEG</span><span class="sxs-lookup"><span data-stu-id="27c55-153">JPEG</span></span>
-   <span data-ttu-id="27c55-154">PNG</span><span class="sxs-lookup"><span data-stu-id="27c55-154">PNG</span></span>
-   <span data-ttu-id="27c55-155">TIFF</span><span class="sxs-lookup"><span data-stu-id="27c55-155">TIFF</span></span>
-   <span data-ttu-id="27c55-156">Format Windows Media Photo</span><span class="sxs-lookup"><span data-stu-id="27c55-156">Windows Media Photo format</span></span>

<span data-ttu-id="27c55-157">Pour plus d’informations sur les codecs WIC et WIC, consultez [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="27c55-157">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span></span>

## <a name="programmatically-launching-the-photo-print-wizard"></a><span data-ttu-id="27c55-158">Lancement de l’Assistant impression de photos par programmation</span><span class="sxs-lookup"><span data-stu-id="27c55-158">Programmatically Launching the Photo Print Wizard</span></span>

<span data-ttu-id="27c55-159">Pour appeler l’Assistant impression de photos, appelez l’interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) avec l’identificateur de classe (CLSID) suivant :</span><span class="sxs-lookup"><span data-stu-id="27c55-159">To invoke the Photo Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



<span data-ttu-id="27c55-160">Les fichiers à traiter par l’Assistant impression de photos sont spécifiés dans un objet [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="27c55-160">The files to be processed by the Photo Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="27c55-161">L’exemple de code suivant montre comment appeler l’Assistant impression de photos.</span><span class="sxs-lookup"><span data-stu-id="27c55-161">The following code example demonstrates how to invoke the Photo Printing Wizard.</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 