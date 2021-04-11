---
title: Assistant impression en ligne
description: L’Assistant impression en ligne de Windows Vista aide les utilisateurs à commander des photos des revendeurs d’impression en ligne.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Assistant impression en ligne
- icônes, Assistant impression en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315095"
---
# <a name="online-printing-wizard"></a><span data-ttu-id="0ecaa-105">Assistant impression en ligne</span><span class="sxs-lookup"><span data-stu-id="0ecaa-105">Online Printing Wizard</span></span>

<span data-ttu-id="0ecaa-106">L’Assistant impression en ligne de Windows Vista aide les utilisateurs à commander des photos des revendeurs d’impression en ligne.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-106">The Windows Vista Online Printing Wizard helps users order prints of photos from participating online printing retailers.</span></span> <span data-ttu-id="0ecaa-107">Cet Assistant est conçu afin de pouvoir être appelé par programme par toute application qui souhaite offrir aux utilisateurs la possibilité de commander des impressions de photos.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-107">This wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to order prints of photos.</span></span> <span data-ttu-id="0ecaa-108">L’Assistant impression de photos est disponible sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-108">The Photo Printing Wizard is available on Windows Vista.</span></span> <span data-ttu-id="0ecaa-109">PIX pour Windows</span><span class="sxs-lookup"><span data-stu-id="0ecaa-109">PIX for Windows</span></span>

-   [<span data-ttu-id="0ecaa-110">Fonctionnalités fournies par l’Assistant impression en ligne</span><span class="sxs-lookup"><span data-stu-id="0ecaa-110">Features Provided by the Online Print Wizard</span></span>](#features-provided-by-the-online-print-wizard)
-   [<span data-ttu-id="0ecaa-111">Formats de fichier photo pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ecaa-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="0ecaa-112">Lancement de l’Assistant impression en ligne par programmation</span><span class="sxs-lookup"><span data-stu-id="0ecaa-112">Programmatically Launching the Online Print Wizard</span></span>](#programmatically-launching-the-online-print-wizard)
-   [<span data-ttu-id="0ecaa-113">Accès à l’icône de l’Assistant impression en ligne</span><span class="sxs-lookup"><span data-stu-id="0ecaa-113">Accessing the Online Print Wizard Icon</span></span>](#accessing-the-online-print-wizard-icon)
-   [<span data-ttu-id="0ecaa-114">Propriétés MRU de l’Assistant impression en ligne</span><span class="sxs-lookup"><span data-stu-id="0ecaa-114">Online Print Wizard MRU Properties</span></span>](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a><span data-ttu-id="0ecaa-115">Fonctionnalités fournies par l’Assistant impression en ligne</span><span class="sxs-lookup"><span data-stu-id="0ecaa-115">Features Provided by the Online Print Wizard</span></span>

<span data-ttu-id="0ecaa-116">L’Assistant impression en ligne de Windows Vista permet aux utilisateurs de commander des tirages à partir d’une sélection de détaillants en ligne participant à l’impression.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-116">The Windows Vista Online Printing Wizard enables users to order prints from a selection of participating online printing retailers.</span></span> <span data-ttu-id="0ecaa-117">Lorsqu’il est appelé, l’Assistant :</span><span class="sxs-lookup"><span data-stu-id="0ecaa-117">When invoked, the wizard:</span></span>

1.  <span data-ttu-id="0ecaa-118">Accepte un fichier ou une liste de fichiers pour lesquels des impressions doivent être classées.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-118">Accepts a file or list of files for which prints are to be ordered.</span></span>
2.  <span data-ttu-id="0ecaa-119">Récupère automatiquement la liste actuelle des revendeurs d’impression en ligne participante et permet à l’utilisateur de sélectionner le détaillant à partir duquel acheter les photos.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-119">Automatically retrieves the current list of participating online printing retailers, and enables the user to select the retailer from which to purchase the photo prints.</span></span>
3.  <span data-ttu-id="0ecaa-120">Guide l’utilisateur tout au long du processus ou de l’ordre des impressions.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-120">Guides the user through the process or ordering prints.</span></span>

<span data-ttu-id="0ecaa-121">Toute application peut tirer parti des fonctionnalités offertes par l’Assistant impression en ligne de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-121">Any application can benefit from the features offered by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="0ecaa-122">Une application n’a besoin que de transmettre le ou les fichiers pour lesquels les tirage sont triés, et l’Assistant guide l’utilisateur tout au long du processus de commande.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-122">An application need only pass in the file or files for which prints will be ordered, and the wizard guides the user through the ordering process.</span></span>

<span data-ttu-id="0ecaa-123">L’illustration suivante montre l’Assistant impression en ligne de Windows Vista affichant un exemple de liste des détaillants en ligne participant à l’impression.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-123">The following figure shows the Windows Vista Online Printing Wizard displaying an example list of participating online printing retailers.</span></span>

![Assistant impression en ligne Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="0ecaa-125">Formats de fichier photo pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ecaa-125">Supported Photo File Formats</span></span>

<span data-ttu-id="0ecaa-126">L’Assistant impression en ligne de Windows Vista prend en charge tout format de fichier image pour lequel un codec WIC (Windows Imaging Component) est installé.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-126">The Windows Vista Online Printing Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="0ecaa-127">WIC fournit plusieurs codecs standard, notamment :</span><span class="sxs-lookup"><span data-stu-id="0ecaa-127">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="0ecaa-128">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="0ecaa-128">Bitmap (BMP)</span></span>
-   <span data-ttu-id="0ecaa-129">format GIF (Graphics Interchange Format)</span><span class="sxs-lookup"><span data-stu-id="0ecaa-129">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="0ecaa-130">Format d’icône (ICO)</span><span class="sxs-lookup"><span data-stu-id="0ecaa-130">Icon Format (ICO)</span></span>
-   <span data-ttu-id="0ecaa-131">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="0ecaa-131">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="0ecaa-132">format PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="0ecaa-132">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="0ecaa-133">format TIFF (Tagged Image File Format)</span><span class="sxs-lookup"><span data-stu-id="0ecaa-133">Tagged Image File Format (TIFF)</span></span>
-   <span data-ttu-id="0ecaa-134">Format Windows Media Photo</span><span class="sxs-lookup"><span data-stu-id="0ecaa-134">Windows Media Photo format</span></span>

<span data-ttu-id="0ecaa-135">Pour plus d’informations sur les codecs WIC et WIC, consultez [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0ecaa-135">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span></span>

<span data-ttu-id="0ecaa-136">Les formats de fichier pris en charge par les revendeurs d’impression en ligne varient d’un détaillant à l’autres. Il est possible qu’un détaillant particulier ne prenne pas en charge tous les formats de fichier pris en charge par l’Assistant impression en ligne de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-136">File formats supported by online printing retailers vary from retailer to retailer; it is possible that a particular retailer may not support all of the file formats supported by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="0ecaa-137">Si l’utilisateur tente de commander des impressions dans un format qui n’est pas pris en charge par le détaillant sélectionné, l’Assistant impression en ligne de Windows Vista avertit l’utilisateur que le détaillant sélectionné ne prend pas en charge le format de fichier envoyé.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-137">If the user attempts to order prints in a format that is not supported by the selected retailer, the Windows Vista Online Printing Wizard notifies the user that the selected retailer does not support the submitted file format.</span></span>

## <a name="programmatically-launching-the-online-print-wizard"></a><span data-ttu-id="0ecaa-138">Lancement de l’Assistant impression en ligne par programmation</span><span class="sxs-lookup"><span data-stu-id="0ecaa-138">Programmatically Launching the Online Print Wizard</span></span>

<span data-ttu-id="0ecaa-139">Pour appeler l’Assistant impression en ligne de Windows Vista, appelez l’interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) avec l’identificateur de classe (CLSID) suivant :</span><span class="sxs-lookup"><span data-stu-id="0ecaa-139">To invoke the Windows Vista Online Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
CLSID_PublishDropTarget
```



<span data-ttu-id="0ecaa-140">Ce CLSID est défini dans ShObjIdl. h et ShObjIdl. idl.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-140">This CLSID is defined in Shobjidl.h and Shobjidl.idl.</span></span> <span data-ttu-id="0ecaa-141">Les fichiers à traiter par l’Assistant impression en ligne de Windows Vista sont spécifiés dans un objet [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="0ecaa-141">The files to be processed by the Windows Vista Online Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="0ecaa-142">L’exemple de code suivant montre comment appeler l’Assistant impression en ligne de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-142">The following code example demonstrates how to invoke the Windows Vista Online Printing Wizard.</span></span>


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a><span data-ttu-id="0ecaa-143">Accès à l’icône de l’Assistant impression en ligne</span><span class="sxs-lookup"><span data-stu-id="0ecaa-143">Accessing the Online Print Wizard Icon</span></span>

<span data-ttu-id="0ecaa-144">L’Assistant impression en ligne de Windows Vista exporte une icône accessible et affichée par les applications qui l’appellent.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-144">The Windows Vista Online Printing Wizard exports an icon that can be accessed and displayed by applications which call it.</span></span> <span data-ttu-id="0ecaa-145">L’illustration suivante montre l’icône de l’Assistant impression en ligne de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-145">The following figure shows the Windows Vista Online Printing Wizard icon.</span></span>

![icône de l’Assistant impression en ligne de Windows Vista](images/opw-icon.png)

<span data-ttu-id="0ecaa-147">L’exemple de code suivant montre comment récupérer l’index de l’icône de l’Assistant impression en ligne de Windows Vista en lisant la propriété **OPWIcon** .</span><span class="sxs-lookup"><span data-stu-id="0ecaa-147">The following code example demonstrates how to retrieve the index for the Windows Vista Online Printing Wizard icon by reading the **OPWIcon** property.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a><span data-ttu-id="0ecaa-148">Propriétés MRU de l’Assistant impression en ligne</span><span class="sxs-lookup"><span data-stu-id="0ecaa-148">Online Print Wizard MRU Properties</span></span>

<span data-ttu-id="0ecaa-149">L’Assistant impression en ligne de Windows Vista définit trois propriétés qui sont liées au détaillant d’impression en ligne (MRU) le plus récemment utilisé.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-149">The Windows Vista Online Printing Wizard defines three properties that are related to the most recently used (MRU) online printing retailer.</span></span>



| <span data-ttu-id="0ecaa-150">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="0ecaa-150">Property Name</span></span> | <span data-ttu-id="0ecaa-151">Valeur/fonction de la propriété</span><span class="sxs-lookup"><span data-stu-id="0ecaa-151">Property Value/Function</span></span>                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ecaa-152">**MRUIcon**</span><span class="sxs-lookup"><span data-stu-id="0ecaa-152">**MRUIcon**</span></span>   | <span data-ttu-id="0ecaa-153">L’index de l’icône du détaillant d’impression en ligne utilisé le plus récemment peut être lu à partir de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-153">The index of the icon for the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="0ecaa-154">**MRUName**</span><span class="sxs-lookup"><span data-stu-id="0ecaa-154">**MRUName**</span></span>   | <span data-ttu-id="0ecaa-155">Le nom du détaillant d’impression en ligne utilisé le plus récemment peut être lu à partir de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-155">The name of the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="0ecaa-156">**UseMRU**</span><span class="sxs-lookup"><span data-stu-id="0ecaa-156">**UseMRU**</span></span>    | <span data-ttu-id="0ecaa-157">Valeur de **variante** **VT \_ booléenne** indiquant si l’Assistant doit ignorer la page de sélection du détaillant pour l’impression en ligne, et utiliser le plus récemment le détaillant d’impression en ligne utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-157">A **VARIANT** **VT\_BOOL** value indicating whether the wizard should skip the online printing retailer selection page, and just use the most recently used online printing retailer instead.</span></span> <span data-ttu-id="0ecaa-158">Affectez à cette propriété la **\_ valeur variant true** pour ignorer la page de sélection du détaillant.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-158">Set this property to **VARIANT\_TRUE** to skip the retailer selection page.</span></span> |



 

<span data-ttu-id="0ecaa-159">L’exemple de code suivant montre comment définir la propriété UseMRU pour que l’Assistant impression en ligne de Windows Vista ignore la page de sélection du détaillant pour l’impression en ligne et sélectionne automatiquement le dernier détaillant utilisé.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-159">The following code example demonstrates how to set the UseMRU property so the Windows Vista Online Printing Wizard bypasses the online printing retailer selection page and automatically selects the most recently used retailer.</span></span>


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



<span data-ttu-id="0ecaa-160">L’exemple de code suivant montre comment lire les propriétés MRUName et MRUIcon.</span><span class="sxs-lookup"><span data-stu-id="0ecaa-160">The following code example demonstrates how to read the MRUName and MRUIcon properties.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 