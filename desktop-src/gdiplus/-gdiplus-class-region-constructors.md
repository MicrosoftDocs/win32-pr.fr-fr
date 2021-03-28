---
description: Cette rubrique répertorie les constructeurs de la classe Region. Pour obtenir une liste complète des classes, consultez region, classe.
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Constructeurs Region. Region
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98663587fab3722d689c9d34578d60daad922a2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115250"
---
# <a name="regionregion-constructors"></a><span data-ttu-id="baf6f-104">Constructeurs Region. Region</span><span class="sxs-lookup"><span data-stu-id="baf6f-104">Region.Region constructors</span></span>

<span data-ttu-id="baf6f-105">Cette rubrique répertorie les constructeurs de la classe [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) .</span><span class="sxs-lookup"><span data-stu-id="baf6f-105">This topic lists the constructors of the [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) class.</span></span> <span data-ttu-id="baf6f-106">Pour obtenir une liste complète des classes, consultez **Region, classe**.</span><span class="sxs-lookup"><span data-stu-id="baf6f-106">For a complete class listing, see **Region Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="baf6f-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="baf6f-107">Overload list</span></span>



| <span data-ttu-id="baf6f-108">Constructeur</span><span class="sxs-lookup"><span data-stu-id="baf6f-108">Constructor</span></span>                                                                 | <span data-ttu-id="baf6f-109">Description</span><span class="sxs-lookup"><span data-stu-id="baf6f-109">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baf6f-110">[**Région (HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span><span class="sxs-lookup"><span data-stu-id="baf6f-110">[**Region(HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span></span>                  | <span data-ttu-id="baf6f-111">Crée une région qui est identique à la région spécifiée par un handle vers une région GDI.</span><span class="sxs-lookup"><span data-stu-id="baf6f-111">Creates a region that is identical to the region that is specified by a handle to a GDI region.</span></span><br/>                                                                                       |
| <span data-ttu-id="baf6f-112">[**Region (Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="baf6f-112">[**Region(Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span></span>            | <span data-ttu-id="baf6f-113">Crée une région qui est définie par un rectangle.</span><span class="sxs-lookup"><span data-stu-id="baf6f-113">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="baf6f-114">[**Region (RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="baf6f-114">[**Region(RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span></span>          | <span data-ttu-id="baf6f-115">Crée une région qui est définie par un rectangle.</span><span class="sxs-lookup"><span data-stu-id="baf6f-115">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="baf6f-116">[**Region (BYTE \* , int)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span><span class="sxs-lookup"><span data-stu-id="baf6f-116">[**Region(BYTE\*,INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span></span> | <span data-ttu-id="baf6f-117">Crée une région qui est définie par les données obtenues à partir d’une autre région.</span><span class="sxs-lookup"><span data-stu-id="baf6f-117">Creates a region that is defined by data obtained from another region.</span></span> <br/>                                                                                                               |
| <span data-ttu-id="baf6f-118">[**Région (GraphicsPath \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span><span class="sxs-lookup"><span data-stu-id="baf6f-118">[**Region(GraphicsPath\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span></span>        | <span data-ttu-id="baf6f-119">Crée une région qui est définie par un chemin d’accès (objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) ) et possède un mode de remplissage contenu dans l’objet **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="baf6f-119">Creates a region that is defined by a path (a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object) and has a fill mode that is contained in the **GraphicsPath** object.</span></span><br/> |
| <span data-ttu-id="baf6f-120">[**Région ()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span><span class="sxs-lookup"><span data-stu-id="baf6f-120">[**Region()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span></span>                           | <span data-ttu-id="baf6f-121">Crée une région qui est infinie.</span><span class="sxs-lookup"><span data-stu-id="baf6f-121">Creates a region that is infinite.</span></span> <span data-ttu-id="baf6f-122">Il s'agit du constructeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="baf6f-122">This is the default constructor.</span></span> <br/>                                                                                                                  |



 

 
