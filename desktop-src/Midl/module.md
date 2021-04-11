---
title: attribut de module
description: L’instruction module définit un groupe de fonctions, en général un ensemble de points d’entrée de DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- attribut de module MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314879"
---
# <a name="module-attribute"></a><span data-ttu-id="d808a-104">attribut de module</span><span class="sxs-lookup"><span data-stu-id="d808a-104">module attribute</span></span>

<span data-ttu-id="d808a-105">L’instruction **module** définit un groupe de fonctions, en général un ensemble de points d’entrée de dll.</span><span class="sxs-lookup"><span data-stu-id="d808a-105">The **module** statement defines a group of functions, typically a set of DLL entry points.</span></span>

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="d808a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d808a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d808a-107">*attributes*</span><span class="sxs-lookup"><span data-stu-id="d808a-107">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d808a-108">Les \[ attributs [**UUID**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**helpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] et \[ [**DllName**](dllname-str-.md) \] sont acceptés avant une instruction **module** .</span><span class="sxs-lookup"><span data-stu-id="d808a-108">The \[[**uuid**](uuid.md)\], \[[**version**](version.md)\], \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**hidden**](hidden.md)\], and \[[**dllname**](dllname-str-.md)\] attributes are accepted before a **module** statement.</span></span> <span data-ttu-id="d808a-109">Pour plus d’informations sur les attributs acceptés avant une définition de module, consultez [descriptions d’attributs](/previous-versions/windows/desktop/automat/attribute-descriptions)dans le livre OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="d808a-109">See [Attribute Descriptions](/previous-versions/windows/desktop/automat/attribute-descriptions), in the OLE Automation book, for more information on the attributes accepted before a module definition.</span></span> <span data-ttu-id="d808a-110">L' \[ attribut **DllName** \] est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d808a-110">The \[**dllname**\] attribute is required.</span></span> <span data-ttu-id="d808a-111">Si l' \[  \] attribut UUID est omis, le module n’est pas spécifié de manière unique dans le système.</span><span class="sxs-lookup"><span data-stu-id="d808a-111">If the \[**uuid**\] attribute is omitted, the module is not uniquely specified in the system.</span></span>

</dd> <dt>

<span data-ttu-id="d808a-112">*NomModule*</span><span class="sxs-lookup"><span data-stu-id="d808a-112">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="d808a-113">Nom du module.</span><span class="sxs-lookup"><span data-stu-id="d808a-113">The name of the module.</span></span>

</dd> <dt>

<span data-ttu-id="d808a-114">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="d808a-114">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="d808a-115">Liste des définitions de constantes et des prototypes de fonction pour chaque fonction dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="d808a-115">List of constant definitions and function prototypes for each function in the DLL.</span></span> <span data-ttu-id="d808a-116">Un nombre quelconque de définitions de fonction peuvent apparaître dans la liste de fonctions.</span><span class="sxs-lookup"><span data-stu-id="d808a-116">Any number of function definitions can appear in the function list.</span></span> <span data-ttu-id="d808a-117">Une fonction dans la liste de fonctions se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="d808a-117">A function in the function list has the following form:</span></span>

<span data-ttu-id="d808a-118">\[*attributs* \] *ReturnType* \[ *Convention d’appel funcname* \] (*params*);</span><span class="sxs-lookup"><span data-stu-id="d808a-118">\[*attributes*\] *returntype* \[*calling convention funcname*\](*params*);</span></span>

<span data-ttu-id="d808a-119">\[*attributs* \] [**const**](const.md) constantType *constname*  =  *constval*;</span><span class="sxs-lookup"><span data-stu-id="d808a-119">\[*attributes*\] [**const**](const.md) constanttype *constname* = *constval*;</span></span>

<span data-ttu-id="d808a-120">Seuls les \[ [](helpstring.md) \] attributs HelpString et \[ [**HelpContext**](helpcontext.md) \] sont acceptés pour une [**constante const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="d808a-120">Only the \[[**helpstring**](helpstring.md)\] and \[[**helpcontext**](helpcontext.md)\] attributes are accepted for a [**const**](const.md).</span></span>

<span data-ttu-id="d808a-121">Les attributs suivants sont acceptés sur une fonction d’un module : \[ [**helpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**propput**](propput.md) \] , \[ [**PROPPUTREF**](propputref.md) \] et \[ [**vararg**](vararg.md) \] .</span><span class="sxs-lookup"><span data-stu-id="d808a-121">The following attributes are accepted on a function in a module: \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**string**](string.md)\], \[[**entry**](entry.md)\], \[[**propget**](propget.md)\], \[[**propput**](propput.md)\], \[[**propputref**](propputref.md)\], and \[[**vararg**](vararg.md)\].</span></span> <span data-ttu-id="d808a-122">Si \[ **vararg** \] est spécifié, le dernier paramètre doit être un tableau sécurisé de type **Variant** .</span><span class="sxs-lookup"><span data-stu-id="d808a-122">If \[**vararg**\] is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="d808a-123">La Convention d’appel facultative peut être \_ \_ Pascal/ \_ Pascal/Pascal, \_ \_ cdecl/ \_ cdecl/cdecl, ou \_ \_ StdCall/ \_ StdCall/StdCall.</span><span class="sxs-lookup"><span data-stu-id="d808a-123">The optional calling convention can be one of \_\_pascal/\_pascal/pascal, \_\_cdecl/\_cdecl/cdecl, or \_\_stdcall/\_stdcall/stdcall.</span></span> <span data-ttu-id="d808a-124">Le *type de convention d’appel paramName* peut inclure jusqu’à deux traits de soulignement de début.</span><span class="sxs-lookup"><span data-stu-id="d808a-124">The *calling convention type paramname* can include up to two leading underscores.</span></span>

<span data-ttu-id="d808a-125">La liste de paramètres est une liste délimitée par des virgules de :</span><span class="sxs-lookup"><span data-stu-id="d808a-125">The parameter list is a comma-delimited list of:</span></span>

<span data-ttu-id="d808a-126">\[*attributs*\]</span><span class="sxs-lookup"><span data-stu-id="d808a-126">\[*attributes*\]</span></span>

<span data-ttu-id="d808a-127">Le type peut être n’importe quel type précédemment déclaré ou type intégré, un pointeur vers tout type ou un pointeur vers un type intégré.</span><span class="sxs-lookup"><span data-stu-id="d808a-127">The type can be any previously declared type or built-in type, a pointer to any type, or a pointer to a built-in type.</span></span> <span data-ttu-id="d808a-128">Les attributs sur les paramètres sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d808a-128">Attributes on parameters are:</span></span>

<span data-ttu-id="d808a-129">\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**facultatif**](optional.md) \] .</span><span class="sxs-lookup"><span data-stu-id="d808a-129">\[[**in**](in.md)\], \[[**out**](out-idl.md)\], \[[**optional**](optional.md)\].</span></span>

<span data-ttu-id="d808a-130">Si \[ [](optional.md) \] cette option est utilisée, les types de ces paramètres doivent être **Variant** ou **Variant** \* .</span><span class="sxs-lookup"><span data-stu-id="d808a-130">If \[[**optional**](optional.md)\] is used, the types of those parameters must be **VARIANT** or **VARIANT**\*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d808a-131">Notes</span><span class="sxs-lookup"><span data-stu-id="d808a-131">Remarks</span></span>

<span data-ttu-id="d808a-132">La sortie du fichier d’en-tête (. h) pour les modules est une série de prototypes de fonction.</span><span class="sxs-lookup"><span data-stu-id="d808a-132">The header file (.h) output for modules is a series of function prototypes.</span></span> <span data-ttu-id="d808a-133">Le mot clé **module** et les crochets environnants sont supprimés de la sortie du fichier d’en-tête (. h), mais un commentaire (// *modulename* du **module** ) est inséré avant les prototypes.</span><span class="sxs-lookup"><span data-stu-id="d808a-133">The **module** keyword and surrounding brackets are stripped from the header (.h) file output, but a comment (// **module** *modulename*) is inserted before the prototypes.</span></span> <span data-ttu-id="d808a-134">Le mot clé **extern** est inséré avant les déclarations.</span><span class="sxs-lookup"><span data-stu-id="d808a-134">The keyword **extern** is inserted before the declarations.</span></span>

## <a name="examples"></a><span data-ttu-id="d808a-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="d808a-135">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a><span data-ttu-id="d808a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d808a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d808a-137">**const**</span><span class="sxs-lookup"><span data-stu-id="d808a-137">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="d808a-138">Contenu d’une bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d808a-138">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="d808a-139">**DllName**</span><span class="sxs-lookup"><span data-stu-id="d808a-139">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="d808a-140">**mention**</span><span class="sxs-lookup"><span data-stu-id="d808a-140">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="d808a-141">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="d808a-141">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="d808a-142">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="d808a-142">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="d808a-143">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="d808a-143">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="d808a-144">**masquer**</span><span class="sxs-lookup"><span data-stu-id="d808a-144">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="d808a-145">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="d808a-145">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d808a-146">**propget**</span><span class="sxs-lookup"><span data-stu-id="d808a-146">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="d808a-147">**propput**</span><span class="sxs-lookup"><span data-stu-id="d808a-147">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="d808a-148">**propputref**</span><span class="sxs-lookup"><span data-stu-id="d808a-148">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="d808a-149">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="d808a-149">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="d808a-150">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="d808a-150">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="d808a-151">**universel**</span><span class="sxs-lookup"><span data-stu-id="d808a-151">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="d808a-152">**vararg**</span><span class="sxs-lookup"><span data-stu-id="d808a-152">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="d808a-153">**Version**</span><span class="sxs-lookup"><span data-stu-id="d808a-153">**version**</span></span>](version.md)
</dt> </dl>

 

 