---
description: Titre de l’élément.
ms.assetid: 8fb948d6-2677-4e5d-b283-8757c3df574d
title: System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee57037a35c08fd3a6be4f4a0ce7a8475f82cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524459"
---
# <a name="systemtitle"></a><span data-ttu-id="38b44-103">System.Title</span><span class="sxs-lookup"><span data-stu-id="38b44-103">System.Title</span></span>

<span data-ttu-id="38b44-104">Titre de l’élément.</span><span class="sxs-lookup"><span data-stu-id="38b44-104">The title of the item.</span></span> <span data-ttu-id="38b44-105">Par exemple, le titre d'un document, l'objet d'un message, la légende d'une photo ou le nom d'une piste de musique.</span><span class="sxs-lookup"><span data-stu-id="38b44-105">For example, the title of a document, the subject of a message, the caption of a photo, or the name of a music track.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="38b44-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38b44-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Title
   shellPKey = PKEY_Title
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="38b44-107">Notes</span><span class="sxs-lookup"><span data-stu-id="38b44-107">Remarks</span></span>

<span data-ttu-id="38b44-108">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="38b44-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="38b44-109">Cette propriété est mappée au *titre* de la propriété de document OLE.</span><span class="sxs-lookup"><span data-stu-id="38b44-109">This property maps to the OLE document property *Title*.</span></span> <span data-ttu-id="38b44-110">[System. title]() est une propriété couramment utilisée, en particulier dans des listes hétérogènes d’éléments où les éléments peuvent être de nombreux types différents.</span><span class="sxs-lookup"><span data-stu-id="38b44-110">[System.Title]() is a commonly used property, particularly in heterogeneous lists of items where the items can be of many different types.</span></span> <span data-ttu-id="38b44-111">Par conséquent, il est recommandé que les gestionnaires de propriétés remplissent cette propriété même si elle est redondante ; par exemple, un message électronique, qui remplirait à la fois System. title et [System. Subject](./props-system-subject.md) avec la même valeur.</span><span class="sxs-lookup"><span data-stu-id="38b44-111">Therefore, it is recommended that property handlers populate this property even if it is redundant; for example, an e-mail, which would populate both System.Title and [System.Subject](./props-system-subject.md) with the same value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38b44-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38b44-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b44-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="38b44-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="38b44-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="38b44-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="38b44-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="38b44-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="38b44-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="38b44-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="38b44-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="38b44-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="38b44-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="38b44-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="38b44-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="38b44-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="38b44-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="38b44-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="38b44-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="38b44-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="38b44-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="38b44-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="38b44-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="38b44-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="38b44-124">editControl</span><span class="sxs-lookup"><span data-stu-id="38b44-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="38b44-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="38b44-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="38b44-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="38b44-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
