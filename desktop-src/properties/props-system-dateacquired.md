---
description: Date d’acquisition du fichier ou du support.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210335"
---
# <a name="systemdateacquired"></a><span data-ttu-id="559e4-103">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="559e4-103">System.DateAcquired</span></span>

<span data-ttu-id="559e4-104">Date d’acquisition du fichier ou du support.</span><span class="sxs-lookup"><span data-stu-id="559e4-104">The acquisition date of the file or media.</span></span> <span data-ttu-id="559e4-105">Cette propriété est liée à un utilisateur ou à un groupe d’utilisateurs particulier.</span><span class="sxs-lookup"><span data-stu-id="559e4-105">This property is related to a particular user or group of users.</span></span> <span data-ttu-id="559e4-106">Par exemple, ces données sont utilisées comme axe de tri principal pour le dossier virtuel **New Music**, ce qui permet aux utilisateurs de parcourir les derniers ajouts à leur collection.</span><span class="sxs-lookup"><span data-stu-id="559e4-106">For example, this data is used as the main sorting axis for the virtual folder **New Music**, which enables people to browse the latest additions to their collection.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="559e4-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="559e4-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a><span data-ttu-id="559e4-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="559e4-108">Windows Vista</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a><span data-ttu-id="559e4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="559e4-109">Remarks</span></span>

<span data-ttu-id="559e4-110">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="559e4-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="559e4-111">[DateAcquired]() est stocké en tant que valeur dans le flux principal du fichier, mais il n’est pas toujours présent.</span><span class="sxs-lookup"><span data-stu-id="559e4-111">[DateAcquired]() is stored as a value in the main stream of the file, but it may not always be present.</span></span> <span data-ttu-id="559e4-112">Dans ces cas, la date d’acquisition peut être estimée en fonction d’autres dates connues pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="559e4-112">In those instances, the acquisition date can be approximated based on other known dates for the content.</span></span> <span data-ttu-id="559e4-113">Le gestionnaire de métadonnées doit utiliser un ensemble de règles pour déterminer la date à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="559e4-113">The metadata handler should use a set of rules to determine the date to return.</span></span> <span data-ttu-id="559e4-114">L’exemple suivant illustre cela pour les fichiers musicaux.</span><span class="sxs-lookup"><span data-stu-id="559e4-114">The following example demonstrates this for music files.</span></span>

-   <span data-ttu-id="559e4-115">Pour la musique achetée, l’heure de création du fichier doit être utilisée si aucune date d’acquisition n’est présente.</span><span class="sxs-lookup"><span data-stu-id="559e4-115">For purchased music, the file's creation time should be used if no acquired date is present.</span></span> <span data-ttu-id="559e4-116">Toutefois, le fournisseur de téléchargement doit définir la propriété [DateAcquired]() dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="559e4-116">However, the download provider should set the [DateAcquired]() property in the file.</span></span>
-   <span data-ttu-id="559e4-117">Pour les fichiers musicaux que l’utilisateur ou le groupe « a extraits » (copie de musique ou de vidéo à partir d’un CD ou d’un DVD sur un disque dur), la date d’acquisition doit correspondre à la date à laquelle l’action a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="559e4-117">For music files that the user or group "ripped" (copying music or video from a CD or DVD to a hard disk), the acquisition date should be the date that action took place.</span></span> <span data-ttu-id="559e4-118">Par exemple, l’attribut [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="559e4-118">For instance, the [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) attribute.</span></span>
-   <span data-ttu-id="559e4-119">Pour la musique copiée à partir d’un autre emplacement, l’heure de création du fichier doit être utilisée comme date d’acquisition.</span><span class="sxs-lookup"><span data-stu-id="559e4-119">For music copied from another location, the file's creation time should be used as the acquisition date.</span></span>

<span data-ttu-id="559e4-120">La date et l’heure de l’acquisition d’images à partir d’un appareil photo ou de l’achat de musique en ligne sont des exemples de [System. DateAcquired]() .</span><span class="sxs-lookup"><span data-stu-id="559e4-120">Examples of [System.DateAcquired]() are the date and time when pictures are acquired from a camera or when music is purchased online.</span></span> <span data-ttu-id="559e4-121">Ce n’est pas le même que [System. DateImported](./props-system-dateimported.md).</span><span class="sxs-lookup"><span data-stu-id="559e4-121">This is not the same as [System.DateImported](./props-system-dateimported.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="559e4-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="559e4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="559e4-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="559e4-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="559e4-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="559e4-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="559e4-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="559e4-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="559e4-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="559e4-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="559e4-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="559e4-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="559e4-128">stringFormat</span><span class="sxs-lookup"><span data-stu-id="559e4-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="559e4-129">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="559e4-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="559e4-130">numberFormat</span><span class="sxs-lookup"><span data-stu-id="559e4-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="559e4-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="559e4-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="559e4-132">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="559e4-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="559e4-133">drawControl</span><span class="sxs-lookup"><span data-stu-id="559e4-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="559e4-134">editControl</span><span class="sxs-lookup"><span data-stu-id="559e4-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="559e4-135">filterControl</span><span class="sxs-lookup"><span data-stu-id="559e4-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="559e4-136">queryControl</span><span class="sxs-lookup"><span data-stu-id="559e4-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
