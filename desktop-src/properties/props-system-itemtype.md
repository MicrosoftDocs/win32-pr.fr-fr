---
description: Type canonique de l’élément.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210324"
---
# <a name="systemitemtype"></a><span data-ttu-id="f8440-103">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="f8440-103">System.ItemType</span></span>

<span data-ttu-id="f8440-104">Type canonique de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f8440-104">The canonical type of the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="f8440-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8440-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="f8440-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f8440-106">Remarks</span></span>

<span data-ttu-id="f8440-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="f8440-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="f8440-108">La valeur de System. ItemType est conçue pour être analysée par programmation et peut être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8440-108">The value for System.ItemType is intended to be programmatically parsed, and can be either:</span></span>

-   <span data-ttu-id="f8440-109">Extension de fichier qui pointe vers une valeur ProgID ( \_ racine de classes HKEY \_ \\ <ProgID> ) contenant le nom complet du type.</span><span class="sxs-lookup"><span data-stu-id="f8440-109">A file extension that points to a ProgID value (HKEY\_CLASSES\_ROOT\\<ProgID>) holding the display name for the type.</span></span>
-   <span data-ttu-id="f8440-110">Valeur ProgID (classes HKEY \_ \_ RROOT \\ <ProgID> ), contenant le nom complet du type.</span><span class="sxs-lookup"><span data-stu-id="f8440-110">A ProgID value (HKEY\_CLASSES\_RROOT\\<ProgID>), containing the display name for the type.</span></span>

<span data-ttu-id="f8440-111">L’élément FriendlyTypeName d’un ProgID doit être une version localisée du nom de l’application ( @winword.dll ,-42), tandis que la valeur par défaut de la clé ProgID est un nom non localisé (Word.Document. 12).</span><span class="sxs-lookup"><span data-stu-id="f8440-111">The FriendlyTypeName element of a ProgID should be a localized version of the application name (@winword.dll,-42), while the default value of the ProgID key is a non-localized name (Word.Document.12).</span></span>

<span data-ttu-id="f8440-112">S’il n’existe aucun type canonique, la valeur est VT \_ vide.</span><span class="sxs-lookup"><span data-stu-id="f8440-112">If there is no canonical type, the value is VT\_EMPTY.</span></span> <span data-ttu-id="f8440-113">Si l’élément est un fichier ([System. FileName](./props-system-filename.md) n’est pas de VT \_ vide), la valeur est la même que celle de [System. FileExtension](./props-system-fileextension.md).</span><span class="sxs-lookup"><span data-stu-id="f8440-113">If the item is a file ([System.FileName](./props-system-filename.md) is not VT\_EMPTY), the value is the same as [System.FileExtension](./props-system-fileextension.md).</span></span> <span data-ttu-id="f8440-114">Utilisez [System. ItemTypeText](./props-system-itemtypetext.md) lorsque vous souhaitez afficher le type pour les utilisateurs finaux dans une vue.</span><span class="sxs-lookup"><span data-stu-id="f8440-114">Use [System.ItemTypeText](./props-system-itemtypetext.md) when you want to display the type to end users in a view.</span></span>

> [!Note]  
> <span data-ttu-id="f8440-115">Si l’élément est un fichier, le passage de la valeur [System. ItemType]() à [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) entraîne la même valeur que [System. ItemTypeText](./props-system-itemtypetext.md).</span><span class="sxs-lookup"><span data-stu-id="f8440-115">If the item is a file, passing the [System.ItemType]() value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) results in the same value as [System.ItemTypeText](./props-system-itemtypetext.md).</span></span>

 

<span data-ttu-id="f8440-116">Exemples de valeurs</span><span class="sxs-lookup"><span data-stu-id="f8440-116">Example values:</span></span>



| <span data-ttu-id="f8440-117">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f8440-117">Path</span></span>                                   | <span data-ttu-id="f8440-118">itemType</span><span class="sxs-lookup"><span data-stu-id="f8440-118">ItemType</span></span>         |
|----------------------------------------|------------------|
| <span data-ttu-id="f8440-119">c : \\hello.txt de la \\ barre mydir \\</span><span class="sxs-lookup"><span data-stu-id="f8440-119">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="f8440-120">.txt</span><span class="sxs-lookup"><span data-stu-id="f8440-120">.txt</span></span>             |
| <span data-ttu-id="f8440-121">\\\\goodnews.doc du partage de serveur \\ \\ mydir \\</span><span class="sxs-lookup"><span data-stu-id="f8440-121">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="f8440-122">.doc</span><span class="sxs-lookup"><span data-stu-id="f8440-122">.doc</span></span>             |
| <span data-ttu-id="f8440-123">\\\\\\dossier partage du serveur \\</span><span class="sxs-lookup"><span data-stu-id="f8440-123">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="f8440-124">Répertoire</span><span class="sxs-lookup"><span data-stu-id="f8440-124">Directory</span></span>        |
| <span data-ttu-id="f8440-125">c : \\ mydir \\ mondossier</span><span class="sxs-lookup"><span data-stu-id="f8440-125">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="f8440-126">Répertoire</span><span class="sxs-lookup"><span data-stu-id="f8440-126">Directory</span></span>        |
| <span data-ttu-id="f8440-127">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8440-127">\[desktop\]</span></span>                            | <span data-ttu-id="f8440-128">Dossier</span><span class="sxs-lookup"><span data-stu-id="f8440-128">Folder</span></span>           |
| <span data-ttu-id="f8440-129">Compte/Mailbox/boîte de réception/'re : Bonjour ! '</span><span class="sxs-lookup"><span data-stu-id="f8440-129">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="f8440-130">MAPI/IPM. Message</span><span class="sxs-lookup"><span data-stu-id="f8440-130">MAPI/IPM.Message</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f8440-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f8440-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8440-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f8440-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f8440-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f8440-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f8440-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f8440-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f8440-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f8440-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f8440-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f8440-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f8440-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f8440-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f8440-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f8440-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f8440-139">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f8440-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f8440-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f8440-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f8440-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f8440-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f8440-142">drawControl</span><span class="sxs-lookup"><span data-stu-id="f8440-142">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f8440-143">editControl</span><span class="sxs-lookup"><span data-stu-id="f8440-143">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f8440-144">filterControl</span><span class="sxs-lookup"><span data-stu-id="f8440-144">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f8440-145">queryControl</span><span class="sxs-lookup"><span data-stu-id="f8440-145">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="f8440-146">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="f8440-146">Programmatic Identifiers</span></span>](../shell/fa-progids.md)
</dt> </dl>

 

 
