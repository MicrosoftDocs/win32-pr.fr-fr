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
ms.openlocfilehash: db346a664ed7b8f7beeacfe73cc928a924befe10
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119784"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="395e8-109">Fonctionnalités du langage ODL dans MIDL</span><span class="sxs-lookup"><span data-stu-id="395e8-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="395e8-110">L’outil Mktyplib.exe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="395e8-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="395e8-111">Utilisez plutôt le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="395e8-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="395e8-112">Les rubriques suivantes répertorient les attributs ODL (Object Description Language), les mots clés, les instructions et les directives qui font désormais partie du Microsoft Interface Definition Language (MIDL) :</span><span class="sxs-lookup"><span data-stu-id="395e8-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="395e8-113">Attributs ODL</span><span class="sxs-lookup"><span data-stu-id="395e8-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="395e8-114">Mots clés, instructions et directives ODL</span><span class="sxs-lookup"><span data-stu-id="395e8-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="395e8-115">Attributs ODL</span><span class="sxs-lookup"><span data-stu-id="395e8-115">ODL Attributes</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="395e8-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-116">\[[**appobject**](appobject.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-117">\[[**pouvant être liée**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-117">\[[**bindable**](bindable.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-118">\[[**régulation**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-118">\[[**control**](control.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-119">\[[**valeurs**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-119">\[[**default**](default.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-120">\[[**DefaultValue**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-121">\[[**displaybind**](displaybind.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-122">\[[**DllName**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-122">\[[**dllname**](dllname-str-.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-123">\[[**double**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-123">\[[**dual**](dual.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-124">\[[**mention**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-124">\[[**entry**](entry.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-125">\[[**HelpContext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-125">\[[**helpcontext**](helpcontext.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-126">\[[**HelpString**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-126">\[[**helpstring**](helpstring.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-127">\[[**HelpFile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-127">\[[**helpfile**](helpfile.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-128">\[[**masquer**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-128">\[[**hidden**](hidden.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-129">\[[**identifi**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-129">\[[**id**](id.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-130">\[[**immediatebind**](immediatebind.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-131">\[[**dans**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-131">\[[**in**](in.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-132">\[[**LCID**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-132">\[[**lcid**](lcid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-133">\[[**accordée**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-133">\[[**licensed**](licensed.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-134">\[[**PerformanceCategory**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-134">\[[**nonextensible**](nonextensible.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-135">\[[**ODL**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-135">\[[**odl**](odl.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-136">\[[**oleautomation**](oleautomation.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-137">\[[**facultatif**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-137">\[[**optional**](optional.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-138">\[[**à**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-138">\[[**out**](out-idl.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-139">\[[**propget**](propget.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-140">\[[**propput**](propput.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-141">\[[**propputref**](propputref.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-142">\[[**publique**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-142">\[[**public**](public.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-143">\[[ **lecture seule**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-143">\[ [**readonly**](readonly.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-144">\[[**modification**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-144">\[[**requestedit**](requestedit.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-145">\[[**sensible**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-145">\[[**restricted**](restricted.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-146">\[[**retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-146">\[[**retval**](retval.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-147">\[[**code**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-147">\[[**source**](source.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-148">\[[**universel**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-148">\[[**uuid**](uuid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-149">[**vararg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-149">[**vararg**](vararg.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="395e8-150">\[[**Version**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-150">\[[**version**](version.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="395e8-151">Â</span><span class="sxs-lookup"><span data-stu-id="395e8-151">Â</span></span>
    :::column-end:::
:::row-end:::

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="395e8-152">Mots clés, instructions et directives ODL</span><span class="sxs-lookup"><span data-stu-id="395e8-152">ODL Keywords, Statements, and Directives</span></span>

[<span data-ttu-id="395e8-153">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="395e8-153">**coclass**</span></span>](coclass.md)

[<span data-ttu-id="395e8-154">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="395e8-154">**dispinterface**</span></span>](dispinterface.md)

[<span data-ttu-id="395e8-155">**variables**</span><span class="sxs-lookup"><span data-stu-id="395e8-155">**enum**</span></span>](enum.md)

<span data-ttu-id="395e8-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="395e8-156">\[[**importlib**](importlib.md)\]</span></span>

[<span data-ttu-id="395e8-157">**interface**</span><span class="sxs-lookup"><span data-stu-id="395e8-157">**interface**</span></span>](interface.md)

[<span data-ttu-id="395e8-158">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="395e8-158">**library**</span></span>](library.md)

[<span data-ttu-id="395e8-159">**modules**</span><span class="sxs-lookup"><span data-stu-id="395e8-159">**module**</span></span>](module.md)

[<span data-ttu-id="395e8-160">**modélis**</span><span class="sxs-lookup"><span data-stu-id="395e8-160">**struct**</span></span>](struct.md)

[<span data-ttu-id="395e8-161">**typedef**</span><span class="sxs-lookup"><span data-stu-id="395e8-161">**typedef**</span></span>](typedef.md)

[<span data-ttu-id="395e8-162">**UE**</span><span class="sxs-lookup"><span data-stu-id="395e8-162">**union**</span></span>](union.md)

<span data-ttu-id="395e8-163">Pour plus d’informations sur la façon de marshaler des types OLE Automation, tels que **BSTR**, **Variant** et **SAFEARRAY**, consultez [marshaling de types de données OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="395e8-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




