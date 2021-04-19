---
description: OpenXPS est le format Open XML Paper Specification pour les documents, et il est basé sur la spécification standard ECMA (European cartons Association).
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: Prise en charge des applications pour l’impression OpenXPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518226"
---
# <a name="app-support-for-openxps-printing"></a><span data-ttu-id="928af-103">Prise en charge des applications pour l’impression OpenXPS</span><span class="sxs-lookup"><span data-stu-id="928af-103">App Support for OpenXPS Printing</span></span>

<span data-ttu-id="928af-104">OpenXPS est le format Open XML Paper Specification pour les documents, qui est basé sur la spécification standard ECMA (European Computer Manufacturers Association).</span><span class="sxs-lookup"><span data-stu-id="928af-104">OpenXPS is the Open XML Paper Specification format for documents, and it’s based on the European Computer Manufacturers Association (ECMA) standard specification.</span></span>

<span data-ttu-id="928af-105">Windows 8 prend entièrement en charge l’impression OpenXPS via le modèle de pilote d’imprimante v4, côte à côte avec la prise en charge continue du format Microsoft XPS.</span><span class="sxs-lookup"><span data-stu-id="928af-105">Windows 8 provides full support for OpenXPS printing via the v4 print driver model, side-by-side with continued support for the Microsoft XPS format.</span></span> <span data-ttu-id="928af-106">Et cette rubrique se concentre sur la partie de cette prise en charge qui s’applique aux développeurs d’applications Windows.</span><span class="sxs-lookup"><span data-stu-id="928af-106">And this topic focuses on the portion of this support that is relevant to Windows application developers.</span></span> <span data-ttu-id="928af-107">Pour plus d’informations sur la configuration requise du pilote pour la prise en charge de OpenXPS, consultez [prise en charge des pilotes pour OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span><span class="sxs-lookup"><span data-stu-id="928af-107">For information about driver requirements for OpenXPS support, see [Driver Support for OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span></span>

## <a name="sending-xps-data-to-the-print-system"></a><span data-ttu-id="928af-108">Envoi de données XPS au système d’impression</span><span class="sxs-lookup"><span data-stu-id="928af-108">Sending XPS data to the Print System</span></span>

<span data-ttu-id="928af-109">Nous vous recommandons d’utiliser [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) pour l’envoi de tous les travaux d’impression XPS au système d’impression.</span><span class="sxs-lookup"><span data-stu-id="928af-109">We recommend that you use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for sending all XPS print jobs to the print system.</span></span> <span data-ttu-id="928af-110">**IPrintDocumentPackageTarget** accepte le modèle d’objet XPS (OM) sans sérialisation et permet d’améliorer les performances globales.</span><span class="sxs-lookup"><span data-stu-id="928af-110">**IPrintDocumentPackageTarget** accepts the XPS object model (OM) without serialization, and that helps to improve the overall performance.</span></span>

<span data-ttu-id="928af-111">Voici un bref résumé de l’interface **IPrintDocumentPackageTarget** :</span><span class="sxs-lookup"><span data-stu-id="928af-111">Here's a brief summary of the **IPrintDocumentPackageTarget** interface:</span></span>

-   <span data-ttu-id="928af-112">Cette interface prend en charge l’impression à partir de solutions personnalisées, ainsi que d’applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="928af-112">This interface supports printing from tailored solutions as well as desktop applications.</span></span>

-   <span data-ttu-id="928af-113">Pour les applications de bureau, cette fonctionnalité peut être utilisée à la place de [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span><span class="sxs-lookup"><span data-stu-id="928af-113">For desktops apps, this can be used in place of [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span></span>

-   <span data-ttu-id="928af-114">Disponible sur Windows 7 avec Service Pack 1 (SP1) + mise à jour de la plateforme et Windows 8.</span><span class="sxs-lookup"><span data-stu-id="928af-114">Available on Windows 7 with Service Pack 1 (SP1) + Platform Update, and Windows 8.</span></span>

-   <span data-ttu-id="928af-115">Incluez *DocumentTarget. h* dans les projets pour utiliser ces API.</span><span class="sxs-lookup"><span data-stu-id="928af-115">Include *DocumentTarget.h* in projects to use these APIs.</span></span>

<span data-ttu-id="928af-116">Les applications qui utilisent des documents OpenXPS doivent noter que le type MIME pour OpenXPS est le suivant :</span><span class="sxs-lookup"><span data-stu-id="928af-116">Applications that consume OpenXPS documents should note that the MIME type for OpenXPS is as follows:</span></span>

<dl> <span data-ttu-id="928af-117">oxps de l’application \\</span><span class="sxs-lookup"><span data-stu-id="928af-117">application\\oxps</span></span>  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a><span data-ttu-id="928af-118">Envoi de données OpenXPS à l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="928af-118">Sending OpenXPS data to the XPS Print API</span></span>

<span data-ttu-id="928af-119">Spécifique à OpenXPS, XPS OM accepte à la fois MSXPS et OpenXPS, et fournit des méthodes pour la conversion et la sérialisation dans l’un ou l’autre format.</span><span class="sxs-lookup"><span data-stu-id="928af-119">Specific to OpenXPS, XPS OM accepts both MSXPS and OpenXPS, and provides methods for conversion and serialization to either format.</span></span> <span data-ttu-id="928af-120">Cela permet aux développeurs d’applications d’être agnostiques du pilote cible, s’ils le souhaitent.</span><span class="sxs-lookup"><span data-stu-id="928af-120">This allows application developers to be agnostic of the target driver, if they want.</span></span> <span data-ttu-id="928af-121">Cela signifie également que les développeurs d’applications peuvent toujours envoyer des travaux d’impression en tant que modèle OM XPS à StartXpsPrintJob1 ou IDocumentPackageTarget, sachant que le système d’impression gère toutes les conversions nécessaires.</span><span class="sxs-lookup"><span data-stu-id="928af-121">This also means that app developers can always submit print jobs as XPS OM to either StartXpsPrintJob1 or IDocumentPackageTarget, knowing that the print system will handle any necessary conversion.</span></span>

<span data-ttu-id="928af-122">Bien entendu, la prévention de la conversion entre les formats XPS améliorera les performances de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="928af-122">Of course, preventing conversion between XPS formats will improve end-to-end performance.</span></span> <span data-ttu-id="928af-123">À partir de l’application, le développeur peut vérifier la clé de Registre suivante pour déterminer le format XPS préféré du pilote d’impression ciblé :</span><span class="sxs-lookup"><span data-stu-id="928af-123">From the application, the developer can check the following registry key to determine the preferred XPS format of the targeted print driver:</span></span>

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

<span data-ttu-id="928af-124">Une fois le format XPS préféré déterminé, l’application peut fournir des objets OM XPS qui ne nécessitent pas de conversion.</span><span class="sxs-lookup"><span data-stu-id="928af-124">Once the preferred XPS format has been determined, the application can provide XPS OM objects that will not require conversion.</span></span> <span data-ttu-id="928af-125">Une note particulière est l’utilisation de la photo HD dans MSXPS et JPEGXR dans OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="928af-125">Of particular note is the use of HD Photo in MSXPS and JPEGXR in OpenXPS.</span></span> <span data-ttu-id="928af-126">La conversion de JPEGXR en photo HD est relativement légère puisque la principale différence dans cette conversion est que la photo HD ignore 4 bits de contrôle requis par JPEGXR.</span><span class="sxs-lookup"><span data-stu-id="928af-126">Converting from JPEGXR to HD Photo is relatively lightweight since the primary difference in this conversion is that HD Photo ignores 4 control bits that JPEGXR requires.</span></span> <span data-ttu-id="928af-127">Toutefois, la conversion de la photo HD en JPEGXR nécessite que la totalité de l’image soit à nouveau codée afin de générer les bits de contrôle requis.</span><span class="sxs-lookup"><span data-stu-id="928af-127">However, converting from HD Photo to JPEGXR requires the entire image to be re-encoded in order to generate the required control bits.</span></span> <span data-ttu-id="928af-128">Ainsi, le fait de fournir des images JPEGXR pour les images haute résolution garantit la compatibilité avec OpenXPS et réduit le coût de conversion de l’image pour MSXPS.</span><span class="sxs-lookup"><span data-stu-id="928af-128">Thus, providing JPEGXR images for high-resolution images will ensure compatibility with OpenXPS and minimize the conversion cost of the image for MSXPS.</span></span>

<span data-ttu-id="928af-129">L’en-tête *Xpsobjectmodel \_ 1. h* définit les API et les objets supplémentaires pour OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="928af-129">The *Xpsobjectmodel\_1.h* header defines the additional APIs and objects for OpenXPS.</span></span> <span data-ttu-id="928af-130">L’interface IXpsOMObjectFactory1 fournit des méthodes supplémentaires pour la conversion d’images.</span><span class="sxs-lookup"><span data-stu-id="928af-130">And the IXpsOMObjectFactory1 interface provides additional methods for image conversion.</span></span> <span data-ttu-id="928af-131">Voici la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="928af-131">Here's the syntax:</span></span>


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



<span data-ttu-id="928af-132">Windows 8 fournit les énumérations nouvelles et mises à jour suivantes.</span><span class="sxs-lookup"><span data-stu-id="928af-132">Windows 8 provides the following new and updated enumerations.</span></span>

<span data-ttu-id="928af-133">Nouvelle énumération :</span><span class="sxs-lookup"><span data-stu-id="928af-133">New enumeration:</span></span>

<dl>

[<span data-ttu-id="928af-134">**\_type de document XPS \_**</span><span class="sxs-lookup"><span data-stu-id="928af-134">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

<span data-ttu-id="928af-135">Énumération mise à jour</span><span class="sxs-lookup"><span data-stu-id="928af-135">Updated enumeration</span></span>

<dl>

[<span data-ttu-id="928af-136">**\_type d’image XPS \_**</span><span class="sxs-lookup"><span data-stu-id="928af-136">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

<span data-ttu-id="928af-137">Les nouvelles méthodes GetDocumentType, permettent à une application de déterminer le format de document XPS.</span><span class="sxs-lookup"><span data-stu-id="928af-137">The new GetDocumentType methods allow an application to determine the XPS format of documents.</span></span> <span data-ttu-id="928af-138">Celles-ci sont disponibles dans [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)et [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span><span class="sxs-lookup"><span data-stu-id="928af-138">These are available in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1), and [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span></span> <span data-ttu-id="928af-139">Voici une liste des méthodes.</span><span class="sxs-lookup"><span data-stu-id="928af-139">Here's a list of the methods.</span></span>

<dl>

[<span data-ttu-id="928af-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="928af-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[<span data-ttu-id="928af-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="928af-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[<span data-ttu-id="928af-142">**IXpsOMPackage1 :: GetDocumentType,**</span><span class="sxs-lookup"><span data-stu-id="928af-142">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[<span data-ttu-id="928af-143">**IXpsOMPage1 :: GetDocumentType,**</span><span class="sxs-lookup"><span data-stu-id="928af-143">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

<span data-ttu-id="928af-144">Windows 8 fournit les nouveaux codes d’erreur suivants pour la prise en charge de OpenXPS :</span><span class="sxs-lookup"><span data-stu-id="928af-144">Windows 8 provides the following new error codes in support of OpenXPS:</span></span>

<dl> <span data-ttu-id="928af-145">\_espace de \_ noms incompatible avec XPS E \_ .</span><span class="sxs-lookup"><span data-stu-id="928af-145">XPS\_E\_MISMATCHED\_NAMESPACE.</span></span> <dl> <span data-ttu-id="928af-146">Cette erreur est retournée s’il existe un espace de noms incompatible.</span><span class="sxs-lookup"><span data-stu-id="928af-146">This error is returned, if there is a mismatched namespace.</span></span>  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> <span data-ttu-id="928af-147">Cette erreur est retournée si MSXPS utilise des URI absolus dans les références internes ou s’il tente d’utiliser des références internes pour sérialiser dans le flux.</span><span class="sxs-lookup"><span data-stu-id="928af-147">This error is returned if MSXPS uses absolute URIs in internal references, or attempts to use internal references to serialize in the stream.</span></span> <span data-ttu-id="928af-148">Cela est dû au fait que XPS OM génère des URI relatifs.</span><span class="sxs-lookup"><span data-stu-id="928af-148">That is because XPS OM generates relative URIs.</span></span> <span data-ttu-id="928af-149">Et bien que MSXPS prenne en charge les URI relatifs et absolus, OpenXPS requiert des URI relatifs.</span><span class="sxs-lookup"><span data-stu-id="928af-149">And although MSXPS supports both relative and absolute URIs, OpenXPS requires relative URIs.</span></span>  
</dl> </dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="928af-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="928af-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="928af-151">Prise en charge des pilotes pour OpenXPS</span><span class="sxs-lookup"><span data-stu-id="928af-151">Driver Support for OpenXPS</span></span>](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[<span data-ttu-id="928af-152">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="928af-152">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[<span data-ttu-id="928af-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="928af-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[<span data-ttu-id="928af-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="928af-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[<span data-ttu-id="928af-155">**IXpsOMPackage1 :: GetDocumentType,**</span><span class="sxs-lookup"><span data-stu-id="928af-155">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="928af-156">**IXpsOMPage1 :: GetDocumentType,**</span><span class="sxs-lookup"><span data-stu-id="928af-156">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="928af-157">**\_type de document XPS \_**</span><span class="sxs-lookup"><span data-stu-id="928af-157">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[<span data-ttu-id="928af-158">**\_type d’image XPS \_**</span><span class="sxs-lookup"><span data-stu-id="928af-158">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
