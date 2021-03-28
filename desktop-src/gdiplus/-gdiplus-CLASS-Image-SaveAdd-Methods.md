---
description: Cette rubrique répertorie les méthodes SaveAdd de la classe image. Pour obtenir la liste complète des méthodes de la classe image, consultez Méthodes d’image.
ms.assetid: e597f6e6-6e07-4afb-8905-26e4af961685
title: Méthodes image. SaveAdd (Gdiplusheaders. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a2b65c6fe56507538f092edc7128497de5cb2f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973030"
---
# <a name="imagesaveadd-methods"></a><span data-ttu-id="ee554-104">Méthodes image. SaveAdd</span><span class="sxs-lookup"><span data-stu-id="ee554-104">Image.SaveAdd methods</span></span>

<span data-ttu-id="ee554-105">Cette rubrique répertorie les méthodes SaveAdd de la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="ee554-105">This topic lists the SaveAdd methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="ee554-106">Pour obtenir la liste complète des méthodes de la classe **image** , consultez [méthodes d’image](-gdiplus-class-image-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ee554-106">For a complete list of methods for the **Image** class, see [Image Methods](-gdiplus-class-image-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="ee554-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="ee554-107">Overload list</span></span>



| <span data-ttu-id="ee554-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="ee554-108">Method</span></span>                                                                                               | <span data-ttu-id="ee554-109">Description</span><span class="sxs-lookup"><span data-stu-id="ee554-109">Description</span></span>                                                                                                                                                                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee554-110">[**SaveAdd (EncoderParameters \* )**](/previous-versions//ms535408(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee554-110">[**SaveAdd(EncoderParameters\*)**](/previous-versions//ms535408(v=vs.85))</span></span>                  | <span data-ttu-id="ee554-111">La méthode [**image :: SaveAdd**](/previous-versions//ms535408(v=vs.85)) ajoute un frame à un fichier ou à un flux spécifié dans un appel précédent à la méthode **Save** .</span><span class="sxs-lookup"><span data-stu-id="ee554-111">The [**Image::SaveAdd**](/previous-versions//ms535408(v=vs.85)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span> <span data-ttu-id="ee554-112">Utilisez cette méthode pour enregistrer les frames sélectionnés d'une image à plusieurs frames dans une autre image à plusieurs frames.</span><span class="sxs-lookup"><span data-stu-id="ee554-112">Use this method to save selected frames from a multiple-frame image to another multiple-frame image.</span></span><br/> |
| <span data-ttu-id="ee554-113">[**SaveAdd (image \* , EncoderParameters \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span><span class="sxs-lookup"><span data-stu-id="ee554-113">[**SaveAdd(Image\*,EncoderParameters\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span></span> | <span data-ttu-id="ee554-114">La méthode [**image :: SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) ajoute un frame à un fichier ou à un flux spécifié dans un appel précédent à la méthode **Save** .</span><span class="sxs-lookup"><span data-stu-id="ee554-114">The [**Image::SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span><br/>                                                                                             |



## <a name="requirements"></a><span data-ttu-id="ee554-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ee554-115">Requirements</span></span>



| <span data-ttu-id="ee554-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee554-116">Requirement</span></span> | <span data-ttu-id="ee554-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee554-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee554-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee554-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee554-119">Windows XP, applications de bureau Windows 2000 professionnel \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee554-119">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ee554-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee554-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee554-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee554-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ee554-122">Produit</span><span class="sxs-lookup"><span data-stu-id="ee554-122">Product</span></span><br/>                  | <span data-ttu-id="ee554-123">GDI+ 1,0</span><span class="sxs-lookup"><span data-stu-id="ee554-123">GDI+ 1.0</span></span><br/>                                                                                             |
| <span data-ttu-id="ee554-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee554-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee554-125"><dt>Gdiplusheaders. h (inclure Gdiplus. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee554-125"><dt>Gdiplusheaders.h (include Gdiplus.h)</dt></span></span> </dl> |
| <span data-ttu-id="ee554-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee554-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee554-127"><dt>Gdiplus. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee554-127"><dt>Gdiplus.lib</dt></span></span> </dl>                          |



 

 
