---
description: L’interface IMediaLocator fournit des méthodes pour valider des noms de fichiers dans les services de modification DirectShow (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interface IMediaLocator (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532527"
---
# <a name="imedialocator-interface"></a><span data-ttu-id="a3cf5-103">Interface IMediaLocator</span><span class="sxs-lookup"><span data-stu-id="a3cf5-103">IMediaLocator interface</span></span>

> [!Note]  
> <span data-ttu-id="a3cf5-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-104">\[Deprecated.</span></span> <span data-ttu-id="a3cf5-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3cf5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a3cf5-106">L' `IMediaLocator` interface fournit des méthodes pour valider des noms de fichiers dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="a3cf5-106">The `IMediaLocator` interface provides methods for validating file names in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="a3cf5-107">Utilisez cette interface pour vous assurer qu’un nom de fichier et un chemin d’accès donnés correspondent à un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-107">Use this interface to ensure that a given file name and path correspond to an existing file.</span></span> <span data-ttu-id="a3cf5-108">Cette interface fournit également un moyen de rechercher le fichier à d’autres emplacements et d’afficher une boîte de dialogue **ouvrir** afin que l’utilisateur puisse localiser le fichier.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-108">This interface also provides a way to search for the file at other locations, and to display an **Open** dialog box so that the user can locate the file.</span></span>

<span data-ttu-id="a3cf5-109">Le localisateur de média implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-109">The media locator implements this interface.</span></span> <span data-ttu-id="a3cf5-110">La chronologie et le moteur de rendu prennent également en charge la validation des noms de fichiers par le biais des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3cf5-110">The timeline and the render engine also support file name validation through the following methods:</span></span>

-   <span data-ttu-id="a3cf5-111">[**IAMTimeline :: ValidateSourceNames**](iamtimeline-validatesourcenames.md): valide et met à jour les noms de fichiers dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-111">[**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md): Validates and updates file names in the timeline.</span></span>
-   <span data-ttu-id="a3cf5-112">[**IRenderEngine :: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): spécifie la manière dont le moteur de rendu valide les noms de fichiers au moment du rendu.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-112">[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): Specifies how the render engine validates file names at rendering time.</span></span>

<span data-ttu-id="a3cf5-113">En règle générale, une application DES appellera ces méthodes au lieu de créer directement une instance du localisateur de média.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-113">Typically, a DES application will call these methods rather than directly create an instance of the media locator.</span></span> <span data-ttu-id="a3cf5-114">Pour plus d’informations, consultez [utilisation du localisateur de média](using-the-media-locator.md).</span><span class="sxs-lookup"><span data-stu-id="a3cf5-114">For more information, see [Using the Media Locator](using-the-media-locator.md).</span></span>

## <a name="members"></a><span data-ttu-id="a3cf5-115">Membres</span><span class="sxs-lookup"><span data-stu-id="a3cf5-115">Members</span></span>

<span data-ttu-id="a3cf5-116">L’interface **IMediaLocator** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a3cf5-116">The **IMediaLocator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a3cf5-117">**IMediaLocator** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a3cf5-117">**IMediaLocator** also has these types of members:</span></span>

-   [<span data-ttu-id="a3cf5-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3cf5-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a3cf5-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3cf5-119">Methods</span></span>

<span data-ttu-id="a3cf5-120">L’interface **IMediaLocator** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-120">The **IMediaLocator** interface has these methods.</span></span>



| <span data-ttu-id="a3cf5-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="a3cf5-121">Method</span></span>                                                     | <span data-ttu-id="a3cf5-122">Description</span><span class="sxs-lookup"><span data-stu-id="a3cf5-122">Description</span></span>                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a3cf5-123">**AddFoundLocation**</span><span class="sxs-lookup"><span data-stu-id="a3cf5-123">**AddFoundLocation**</span></span>](imedialocator-addfoundlocation.md) | <span data-ttu-id="a3cf5-124">Ajoute un répertoire au cache de répertoire.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-124">Adds a directory to the directory cache.</span></span><br/>                                |
| [<span data-ttu-id="a3cf5-125">**FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="a3cf5-125">**FindMediaFile**</span></span>](imedialocator-findmediafile.md)       | <span data-ttu-id="a3cf5-126">Recherche un fichier et, en cas de réussite, récupère le chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-126">Searches for a file and, if successful, retrieves the path to the file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3cf5-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a3cf5-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a3cf5-128">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a3cf5-129">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a3cf5-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a3cf5-130">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a3cf5-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3cf5-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3cf5-131">Requirements</span></span>



| <span data-ttu-id="a3cf5-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3cf5-132">Requirement</span></span> | <span data-ttu-id="a3cf5-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3cf5-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3cf5-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3cf5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a3cf5-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3cf5-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a3cf5-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3cf5-136">Library</span></span><br/> | <dl> <span data-ttu-id="a3cf5-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3cf5-137"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
