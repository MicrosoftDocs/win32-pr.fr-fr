---
description: Nom complet dans &\# 0034 ; la plus complète&\# 0034 ; formulaire.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753109"
---
# <a name="systemitemnamedisplay"></a><span data-ttu-id="ce941-103">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="ce941-103">System.ItemNameDisplay</span></span>

<span data-ttu-id="ce941-104">Nom complet dans le formulaire « le plus complet ».</span><span class="sxs-lookup"><span data-stu-id="ce941-104">The display name in "most complete" form.</span></span> <span data-ttu-id="ce941-105">Il s’agit de la représentation unique du nom d’élément le plus approprié pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="ce941-105">It is the unique representation of the item name most appropriate for end users.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="ce941-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce941-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="ce941-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ce941-107">Remarks</span></span>

<span data-ttu-id="ce941-108">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="ce941-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="ce941-109">Cette valeur est le concatentation de [System. ItemNamePrefix](./props-system-itemnameprefix.md) et [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="ce941-109">This value is the concatentation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span>

<span data-ttu-id="ce941-110">Si l’élément est un fichier, cette propriété comprend le nom complet comme indiqué dans l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ce941-110">If the item is a file, this property includes the display name as shown in File Explorer.</span></span> <span data-ttu-id="ce941-111">Il existe des cas acceptables lorsque [System. FileName](./props-system-filename.md) est donné, mais la valeur de cette propriété est totalement différente.</span><span class="sxs-lookup"><span data-stu-id="ce941-111">There are acceptable cases when [System.FileName](./props-system-filename.md) is given but the value of this property is completely different.</span></span> <span data-ttu-id="ce941-112">Les messages électroniques sont un bon exemple.</span><span class="sxs-lookup"><span data-stu-id="ce941-112">E-mail messages are a good example.</span></span> <span data-ttu-id="ce941-113">Si l’élément est un message électronique, le nom de l’élément est normalement l’objet.</span><span class="sxs-lookup"><span data-stu-id="ce941-113">If the item is an e-mail message, the item name is normally the subject.</span></span> <span data-ttu-id="ce941-114">Dans ce cas, la valeur doit être la concaténation de [System. ItemNamePrefix](./props-system-itemnameprefix.md) et [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="ce941-114">In that case, the value must be the concatenation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span> <span data-ttu-id="ce941-115">Étant donné que la valeur de System. ItemNamePrefix exclut les espaces de fin, la concaténation doit inclure un espace lors de la génération de [System. ItemNameDisplay]().</span><span class="sxs-lookup"><span data-stu-id="ce941-115">Since the value of System.ItemNamePrefix excludes any trailing spaces, the concatenation must include a space when generating [System.ItemNameDisplay]().</span></span> <span data-ttu-id="ce941-116">Notez que cette propriété n’est pas nécessairement unique, mais qu’elle est conçue pour promouvoir le candidat le plus probable qui peut être unique et qui paraîtra logique pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="ce941-116">Note that this property is not guaranteed to be unique, but is designed to promote the most likely candidate that can be unique and also makes sense to end users.</span></span>

<span data-ttu-id="ce941-117">Par exemple, pour les documents, [System. title](./props-system-title.md) peut être utilisé en tant que [System. ItemNameDisplay](), mais dans la pratique, le titre des documents peut ne pas être utile ou être suffisamment unique pour fonctionner en tant que System. ItemNameDisplay unique.</span><span class="sxs-lookup"><span data-stu-id="ce941-117">For example, for documents, the [System.Title](./props-system-title.md) could be used as the [System.ItemNameDisplay](), but in practice the title of the documents may not be useful or unique enough to function as the sole System.ItemNameDisplay.</span></span> <span data-ttu-id="ce941-118">Au lieu de cela, il est préférable de fournir [System. FileName](./props-system-filename.md) comme valeur de System. ItemNameDisplay.</span><span class="sxs-lookup"><span data-stu-id="ce941-118">Instead, providing [System.FileName](./props-system-filename.md) as the value of System.ItemNameDisplay is a better choice.</span></span> <span data-ttu-id="ce941-119">Dans Windows Mail, le courrier électronique est stocké dans le système de fichiers en tant que fichiers. eml.</span><span class="sxs-lookup"><span data-stu-id="ce941-119">In Windows Mail, e-mail is stored in the file system as .eml files.</span></span> <span data-ttu-id="ce941-120">Les valeurs System. FileName de ces fichiers ne sont pas conviviales, car il s’agit de GUID.</span><span class="sxs-lookup"><span data-stu-id="ce941-120">The System.FileName values for those files are not human-friendly as they are GUIDs.</span></span> <span data-ttu-id="ce941-121">Dans cet exemple, la promotion de [System. Subject](./props-system-subject.md) en tant que System. ItemNameDisplay est plus appropriée.</span><span class="sxs-lookup"><span data-stu-id="ce941-121">In this example, promoting [System.Subject](./props-system-subject.md) as System.ItemNameDisplay makes more sense.</span></span>

<span data-ttu-id="ce941-122">**Remarques sur la compatibilité :**</span><span class="sxs-lookup"><span data-stu-id="ce941-122">**Compatibility notes:**</span></span>

-   <span data-ttu-id="ce941-123">Implémentations de dossiers Shell sur Windows Vista : utilisez \_ le nom de colonne ItemNameDisplay pour la colonne nom lorsque vous souhaitez que l’Explorateur Windows appelle [**IShellFolder :: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN \_ normal) pour obtenir la valeur du nom.</span><span class="sxs-lookup"><span data-stu-id="ce941-123">Shell folder implementations on Windows Vista: use PKEY\_ItemNameDisplay for the name column when you want Windows Explorer to call [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN\_NORMAL) to get the value of the name.</span></span> <span data-ttu-id="ce941-124">Utilisez un autre nom de fichier, tel que \_ le nom du fichier de la base de au format, lorsque vous souhaitez que l’Explorateur Windows appelle la Banque de propriétés du dossier ou [**IShellFolder2 :: GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) pour obtenir la valeur du nom.</span><span class="sxs-lookup"><span data-stu-id="ce941-124">Use another PKEY, such as PKEY\_ItemName, when you want Windows Explorer to call either the folder's property store or [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) to get the value of the name.</span></span>
-   <span data-ttu-id="ce941-125">Implémentations de dossiers Shell sur Windows XP : la première colonne doit être la colonne Name, et l’Explorateur Windows appelle [**IShellFolder :: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) pour récupérer la valeur du nom.</span><span class="sxs-lookup"><span data-stu-id="ce941-125">Shell folder implementations on Windows XP: the first column must be the name column, and Windows Explorer calls [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to get the value of the name.</span></span> <span data-ttu-id="ce941-126">Le SCID/le n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="ce941-126">The PKEY/SCID does not matter.</span></span>



| <span data-ttu-id="ce941-127">Type d’élément</span><span class="sxs-lookup"><span data-stu-id="ce941-127">Item type</span></span>     | <span data-ttu-id="ce941-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="ce941-128">Example</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="ce941-129">Fichier</span><span class="sxs-lookup"><span data-stu-id="ce941-129">File</span></span>          | <span data-ttu-id="ce941-130">hello.txt</span><span class="sxs-lookup"><span data-stu-id="ce941-130">hello.txt</span></span>                 |
| <span data-ttu-id="ce941-131">Message</span><span class="sxs-lookup"><span data-stu-id="ce941-131">Message</span></span>       | <span data-ttu-id="ce941-132">Re : où est la réunion ?</span><span class="sxs-lookup"><span data-stu-id="ce941-132">Re: Where is the meeting?</span></span> |
| <span data-ttu-id="ce941-133">Dossier de l’appareil</span><span class="sxs-lookup"><span data-stu-id="ce941-133">Device folder</span></span> | <span data-ttu-id="ce941-134">chanson. WMA</span><span class="sxs-lookup"><span data-stu-id="ce941-134">song.wma</span></span>                  |
| <span data-ttu-id="ce941-135">Dossier</span><span class="sxs-lookup"><span data-stu-id="ce941-135">Folder</span></span>        | <span data-ttu-id="ce941-136">Documents</span><span class="sxs-lookup"><span data-stu-id="ce941-136">Documents</span></span>                 |



 

## <a name="related-topics"></a><span data-ttu-id="ce941-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce941-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce941-138">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ce941-138">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ce941-139">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ce941-139">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ce941-140">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ce941-140">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ce941-141">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ce941-141">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ce941-142">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ce941-142">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ce941-143">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ce941-143">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ce941-144">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ce941-144">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ce941-145">numberFormat</span><span class="sxs-lookup"><span data-stu-id="ce941-145">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ce941-146">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ce941-146">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ce941-147">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ce941-147">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ce941-148">drawControl</span><span class="sxs-lookup"><span data-stu-id="ce941-148">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ce941-149">editControl</span><span class="sxs-lookup"><span data-stu-id="ce941-149">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ce941-150">filterControl</span><span class="sxs-lookup"><span data-stu-id="ce941-150">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ce941-151">queryControl</span><span class="sxs-lookup"><span data-stu-id="ce941-151">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
