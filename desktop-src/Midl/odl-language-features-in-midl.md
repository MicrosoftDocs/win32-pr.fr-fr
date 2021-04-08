---
title: Fonctionnalités du langage ODL dans MIDL
description: Attributs ODL (Object Description Language), Mots clés, instructions et directives qui font partie de MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL et ODL MIDL, fonctionnalités de langage
- ODL MIDL, en MIDL
- ODL MIDL, attributs
- ODL MIDL, Mots clés
- ODL MIDL, instructions
- ODL MIDL, directives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e525322eb185e38303b387dc4aa0007322e713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840614"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="ca257-109">Fonctionnalités du langage ODL dans MIDL</span><span class="sxs-lookup"><span data-stu-id="ca257-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="ca257-110">L’outil Mktyplib.exe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="ca257-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="ca257-111">Utilisez plutôt le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="ca257-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="ca257-112">Les rubriques suivantes répertorient les attributs ODL (Object Description Language), les mots clés, les instructions et les directives qui font désormais partie du Microsoft Interface Definition Language (MIDL) :</span><span class="sxs-lookup"><span data-stu-id="ca257-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="ca257-113">Attributs ODL</span><span class="sxs-lookup"><span data-stu-id="ca257-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="ca257-114">Mots clés, instructions et directives ODL</span><span class="sxs-lookup"><span data-stu-id="ca257-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="ca257-115">Attributs ODL</span><span class="sxs-lookup"><span data-stu-id="ca257-115">ODL Attributes</span></span>



|                                            |                                        |
|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="ca257-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-116">\[[**appobject**](appobject.md)\]</span></span>         | <span data-ttu-id="ca257-117">\[[**pouvant être liée**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-117">\[[**bindable**](bindable.md)\]</span></span>       |
| <span data-ttu-id="ca257-118">\[[**régulation**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-118">\[[**control**](control.md)\]</span></span>             | <span data-ttu-id="ca257-119">\[[**valeurs**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-119">\[[**default**](default.md)\]</span></span>         |
| <span data-ttu-id="ca257-120">\[[**DefaultValue**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>   | <span data-ttu-id="ca257-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-121">\[[**displaybind**](displaybind.md)\]</span></span> |
| <span data-ttu-id="ca257-122">\[[**DllName**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-122">\[[**dllname**](dllname-str-.md)\]</span></span>        | <span data-ttu-id="ca257-123">\[[**double**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-123">\[[**dual**](dual.md)\]</span></span>               |
| <span data-ttu-id="ca257-124">\[[**mention**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-124">\[[**entry**](entry.md)\]</span></span>                 | <span data-ttu-id="ca257-125">\[[**HelpContext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-125">\[[**helpcontext**](helpcontext.md)\]</span></span> |
| <span data-ttu-id="ca257-126">\[[**HelpString**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-126">\[[**helpstring**](helpstring.md)\]</span></span>       | <span data-ttu-id="ca257-127">\[[**HelpFile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-127">\[[**helpfile**](helpfile.md)\]</span></span>       |
| <span data-ttu-id="ca257-128">\[[**masquer**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-128">\[[**hidden**](hidden.md)\]</span></span>               | <span data-ttu-id="ca257-129">\[[**identifi**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-129">\[[**id**](id.md)\]</span></span>                   |
| <span data-ttu-id="ca257-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-130">\[[**immediatebind**](immediatebind.md)\]</span></span> | <span data-ttu-id="ca257-131">\[[**dans**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-131">\[[**in**](in.md)\]</span></span>                   |
| <span data-ttu-id="ca257-132">\[[**LCID**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-132">\[[**lcid**](lcid.md)\]</span></span>                   | <span data-ttu-id="ca257-133">\[[**accordée**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-133">\[[**licensed**](licensed.md)\]</span></span>       |
| <span data-ttu-id="ca257-134">\[[**PerformanceCategory**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-134">\[[**nonextensible**](nonextensible.md)\]</span></span> | <span data-ttu-id="ca257-135">\[[**ODL**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-135">\[[**odl**](odl.md)\]</span></span>                 |
| <span data-ttu-id="ca257-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-136">\[[**oleautomation**](oleautomation.md)\]</span></span> | <span data-ttu-id="ca257-137">\[[**facultatif**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-137">\[[**optional**](optional.md)\]</span></span>       |
| <span data-ttu-id="ca257-138">\[[**à**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-138">\[[**out**](out-idl.md)\]</span></span>                 | <span data-ttu-id="ca257-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-139">\[[**propget**](propget.md)\]</span></span>         |
| <span data-ttu-id="ca257-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-140">\[[**propput**](propput.md)\]</span></span>             | <span data-ttu-id="ca257-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-141">\[[**propputref**](propputref.md)\]</span></span>   |
| <span data-ttu-id="ca257-142">\[[**publique**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-142">\[[**public**](public.md)\]</span></span>               | <span data-ttu-id="ca257-143">\[[ **lecture seule**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-143">\[ [**readonly**](readonly.md)\]</span></span>      |
| <span data-ttu-id="ca257-144">\[[**modification**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-144">\[[**requestedit**](requestedit.md)\]</span></span>     | <span data-ttu-id="ca257-145">\[[**sensible**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-145">\[[**restricted**](restricted.md)\]</span></span>   |
| <span data-ttu-id="ca257-146">\[[**retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-146">\[[**retval**](retval.md)\]</span></span>               | <span data-ttu-id="ca257-147">\[[**code**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-147">\[[**source**](source.md)\]</span></span>           |
| <span data-ttu-id="ca257-148">\[[**universel**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-148">\[[**uuid**](uuid.md)\]</span></span>                   | <span data-ttu-id="ca257-149">[**vararg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-149">[**vararg**](vararg.md)\]</span></span>             |
| <span data-ttu-id="ca257-150">\[[**Version**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-150">\[[**version**](version.md)\]</span></span>             | <span data-ttu-id="ca257-151">Â</span><span class="sxs-lookup"><span data-stu-id="ca257-151">Â</span></span>                                      |



 

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="ca257-152">Mots clés, instructions et directives ODL</span><span class="sxs-lookup"><span data-stu-id="ca257-152">ODL Keywords, Statements, and Directives</span></span>



|                                        |
|----------------------------------------|
| [<span data-ttu-id="ca257-153">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="ca257-153">**coclass**</span></span>](coclass.md)             |
| [<span data-ttu-id="ca257-154">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="ca257-154">**dispinterface**</span></span>](dispinterface.md) |
| [<span data-ttu-id="ca257-155">**variables**</span><span class="sxs-lookup"><span data-stu-id="ca257-155">**enum**</span></span>](enum.md)                   |
| <span data-ttu-id="ca257-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="ca257-156">\[[**importlib**](importlib.md)\]</span></span>     |
| [<span data-ttu-id="ca257-157">**interface**</span><span class="sxs-lookup"><span data-stu-id="ca257-157">**interface**</span></span>](interface.md)         |
| [<span data-ttu-id="ca257-158">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="ca257-158">**library**</span></span>](library.md)             |
| [<span data-ttu-id="ca257-159">**modules**</span><span class="sxs-lookup"><span data-stu-id="ca257-159">**module**</span></span>](module.md)               |
| [<span data-ttu-id="ca257-160">**modélis**</span><span class="sxs-lookup"><span data-stu-id="ca257-160">**struct**</span></span>](struct.md)               |
| [<span data-ttu-id="ca257-161">**typedef**</span><span class="sxs-lookup"><span data-stu-id="ca257-161">**typedef**</span></span>](typedef.md)             |
| [<span data-ttu-id="ca257-162">**UE**</span><span class="sxs-lookup"><span data-stu-id="ca257-162">**union**</span></span>](union.md)                 |



 

<span data-ttu-id="ca257-163">Pour plus d’informations sur la façon de marshaler des types OLE Automation, tels que **BSTR**, **Variant** et **SAFEARRAY**, consultez [marshaling de types de données OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="ca257-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




