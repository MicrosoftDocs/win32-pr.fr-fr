---
title: dispinterface (attribut)
description: L’instruction dispinterface définit un ensemble de propriétés et de méthodes sur lesquelles vous pouvez appeler IDispatch Invoke.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- MIDL (MIDL), attribut dispinterface
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842266"
---
# <a name="dispinterface-attribute"></a><span data-ttu-id="7cd76-104">dispinterface (attribut)</span><span class="sxs-lookup"><span data-stu-id="7cd76-104">dispinterface attribute</span></span>

<span data-ttu-id="7cd76-105">L’instruction **dispinterface** définit un ensemble de propriétés et de méthodes sur lesquelles vous pouvez appeler **IDispatch :: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="7cd76-105">The **dispinterface** statement defines a set of properties and methods on which you can call **IDispatch::Invoke**.</span></span> <span data-ttu-id="7cd76-106">Une dispinterface peut être définie en répertoriant explicitement l’ensemble des méthodes et des propriétés prises en charge (syntaxe 1), ou en répertoriant une seule interface (syntaxe 2).</span><span class="sxs-lookup"><span data-stu-id="7cd76-106">A dispinterface may be defined by explicitly listing the set of supported methods and properties (Syntax 1), or by listing a single interface (Syntax 2).</span></span>

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a><span data-ttu-id="7cd76-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cd76-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd76-108">*attributes*</span><span class="sxs-lookup"><span data-stu-id="7cd76-108">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7cd76-109">Spécifie les attributs qui s’appliquent à l’ensemble de **dispinterface**.</span><span class="sxs-lookup"><span data-stu-id="7cd76-109">Specifies attributes that apply to the entire **dispinterface**.</span></span> <span data-ttu-id="7cd76-110">Les attributs suivants sont acceptés : **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , non **\[** [**extensible**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** et **\[** [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7cd76-110">The following attributes are accepted: **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**nonextensible**](nonextensible.md)**\]**, **\[**[**oleautomation**](oleautomation.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="7cd76-111">*dispinterface-nom*</span><span class="sxs-lookup"><span data-stu-id="7cd76-111">*dispinterface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7cd76-112">Nom par lequel la **dispinterface** est connue dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="7cd76-112">The name by which the **dispinterface** is known in the type library.</span></span> <span data-ttu-id="7cd76-113">Ce nom doit être unique dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="7cd76-113">This name must be unique within the type library.</span></span>

</dd> <dt>

<span data-ttu-id="7cd76-114">*liste de propriétés*</span><span class="sxs-lookup"><span data-stu-id="7cd76-114">*property-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7cd76-115">(Syntaxe 1) Liste facultative des propriétés prises en charge par l’objet, déclarées sous la forme de variables.</span><span class="sxs-lookup"><span data-stu-id="7cd76-115">(Syntax 1) An optional list of properties supported by the object, declared in the form of variables.</span></span> <span data-ttu-id="7cd76-116">Il s’agit de la forme abrégée de la déclaration des fonctions de propriété dans la liste des méthodes.</span><span class="sxs-lookup"><span data-stu-id="7cd76-116">This is the short form for declaring the property functions in the methods list.</span></span> <span data-ttu-id="7cd76-117">Pour plus d’informations, consultez la section commentaires.</span><span class="sxs-lookup"><span data-stu-id="7cd76-117">See the comments section for details.</span></span>

</dd> <dt>

<span data-ttu-id="7cd76-118">*List, méthode*</span><span class="sxs-lookup"><span data-stu-id="7cd76-118">*method-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7cd76-119">(Syntaxe 1) Liste comprenant un prototype de fonction pour chaque méthode et propriété de **dispinterface**.</span><span class="sxs-lookup"><span data-stu-id="7cd76-119">(Syntax 1) A list comprising a function prototype for each method and property in the **dispinterface**.</span></span> <span data-ttu-id="7cd76-120">Un nombre quelconque de définitions de fonction peuvent apparaître dans *methlist*.</span><span class="sxs-lookup"><span data-stu-id="7cd76-120">Any number of function definitions can appear in *methlist*.</span></span> <span data-ttu-id="7cd76-121">Une fonction dans *methlist* se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="7cd76-121">A function in *methlist* has the following form:</span></span>

<span data-ttu-id="7cd76-122">**\[  attributs \]** *ReturnType methname type paramName ***(*** params \* \* *);**</span><span class="sxs-lookup"><span data-stu-id="7cd76-122">**\[***attributes***\]** *returntype methname type paramname ***(*** params\*\*\*);*\*</span></span>

<span data-ttu-id="7cd76-123">Les attributs suivants sont acceptés sur une méthode dans une **dispinterface**: **\[ helpString \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** , **\[** [**PROPPUTREF**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** et **\[** [**vararg**](vararg.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7cd76-123">The following attributes are accepted on a method in a **dispinterface**: **\[helpstring\]**, **\[helpcontext\]**, **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]**, **\[**[**propputref**](propputref.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**vararg**](vararg.md)**\]**.</span></span> <span data-ttu-id="7cd76-124">Si **\[ vararg \]** est spécifié, le dernier paramètre doit être un tableau sécurisé de type **Variant** .</span><span class="sxs-lookup"><span data-stu-id="7cd76-124">If **\[vararg\]** is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="7cd76-125">La liste de paramètres est une liste délimitée par des virgules, dont chaque élément se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="7cd76-125">The parameter list is a comma-delimited list, each element of which has the following form:</span></span>

<span data-ttu-id="7cd76-126">**\[***attributs***\]**</span><span class="sxs-lookup"><span data-stu-id="7cd76-126">**\[***attributes***\]**</span></span>

<span data-ttu-id="7cd76-127">Le *type* peut être n’importe quel type déclaré ou intégré, ou un pointeur vers n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="7cd76-127">The *type* can be any declared or built-in type, or a pointer to any type.</span></span> <span data-ttu-id="7cd76-128">Les attributs sur les paramètres sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7cd76-128">Attributes on parameters are:</span></span>

<span data-ttu-id="7cd76-129">**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**facultatif**](optional.md) **\]** , **\[ String \]**</span><span class="sxs-lookup"><span data-stu-id="7cd76-129">**\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]**, **\[**[**optional**](optional.md)**\]**, **\[string\]**</span></span>

</dd> <dt>

<span data-ttu-id="7cd76-130">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="7cd76-130">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7cd76-131">(Syntaxe 2) Nom de l’interface à déclarer en tant qu’interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="7cd76-131">(Syntax 2) The name of the interface to declare as an IDispatch interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cd76-132">Notes</span><span class="sxs-lookup"><span data-stu-id="7cd76-132">Remarks</span></span>

<span data-ttu-id="7cd76-133">Le compilateur MIDL accepte l’ordonnancement des paramètres suivant (de gauche à droite) :</span><span class="sxs-lookup"><span data-stu-id="7cd76-133">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="7cd76-134">Paramètres obligatoires (paramètres qui n’ont pas les \[ \] attributs DefaultValue ou \[ facultatifs \] )</span><span class="sxs-lookup"><span data-stu-id="7cd76-134">Required parameters (parameters that do not have the \[defaultvalue\] or \[optional\] attributes),</span></span>
2.  <span data-ttu-id="7cd76-135">paramètres facultatifs avec ou sans \[ l' \] attribut DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="7cd76-135">optional parameters with or without the \[defaultvalue\] attribute,</span></span>
3.  <span data-ttu-id="7cd76-136">paramètres avec l' \[ \] attribut facultatif et sans l' \[ \] attribut DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="7cd76-136">parameters with the \[optional\] attribute and without the \[defaultvalue\] attribute,</span></span>
4.  <span data-ttu-id="7cd76-137">\[paramètre [**LCID**](lcid.md) \] , le cas échéant,</span><span class="sxs-lookup"><span data-stu-id="7cd76-137">\[ [**lcid**](lcid.md)\] parameter, if any,</span></span>
5.  <span data-ttu-id="7cd76-138">\[[**retVal**](retval.md) \] paramètre</span><span class="sxs-lookup"><span data-stu-id="7cd76-138">\[ [**retval**](retval.md)\] parameter</span></span>

<span data-ttu-id="7cd76-139">Les fonctions de méthode sont spécifiées exactement comme décrit dans la page de référence du [**module**](module.md) , sauf que l’attribut d' \[ [**entrée**](entry.md) \] n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="7cd76-139">Method functions are specified exactly as described in the reference page for [**module**](module.md) except that the \[ [**entry**](entry.md)\] attribute is not allowed.</span></span> <span data-ttu-id="7cd76-140">Notez que STDOLE32. TLB (STDOLE. TLB sur les systèmes 16 bits) doit être importé, car une **dispinterface** hérite de IDispatch.</span><span class="sxs-lookup"><span data-stu-id="7cd76-140">Note that STDOLE32.TLB (STDOLE.TLB on 16-bit systems) must be imported, because a **dispinterface** inherits from IDispatch.</span></span>

<span data-ttu-id="7cd76-141">Vous pouvez déclarer des propriétés dans les listes de propriétés ou de méthodes.</span><span class="sxs-lookup"><span data-stu-id="7cd76-141">You can declare properties in either the properties or methods lists.</span></span> <span data-ttu-id="7cd76-142">La déclaration de propriétés dans la liste Propriétés n’indique pas le type d’accès pris en charge par la propriété (c’est-à-dire, l’extraction, la mise en place ou la PutRef).</span><span class="sxs-lookup"><span data-stu-id="7cd76-142">Declaring properties in the properties list does not indicate the type of access the property supports (that is, get, put, or putref).</span></span> <span data-ttu-id="7cd76-143">Spécifiez l' \[ [](readonly.md) \] attribut ReadOnly pour les propriétés qui ne prennent pas en charge put ou PutRef.</span><span class="sxs-lookup"><span data-stu-id="7cd76-143">Specify the \[ [**readonly**](readonly.md)\] attribute for properties that don't support put or putref.</span></span> <span data-ttu-id="7cd76-144">Si vous déclarez les fonctions de propriété dans la liste des méthodes, les fonctions d’une propriété ont toutes le même identificateur.</span><span class="sxs-lookup"><span data-stu-id="7cd76-144">If you declare the property functions in the methods list, functions for one property all have the same identifier.</span></span>

<span data-ttu-id="7cd76-145">À l’aide de la première syntaxe, les balises Properties : et Methods sont requises.</span><span class="sxs-lookup"><span data-stu-id="7cd76-145">Using the first syntax, the properties: and methods: tags are required.</span></span> <span data-ttu-id="7cd76-146">L' \[ attribut [**ID**](id.md) \] est également requis sur chaque membre.</span><span class="sxs-lookup"><span data-stu-id="7cd76-146">The \[ [**id**](id.md)\] attribute is also required on each member.</span></span> <span data-ttu-id="7cd76-147">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7cd76-147">For example:</span></span>

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

<span data-ttu-id="7cd76-148">Contrairement aux membres d’interface, les membres dispinterface ne peuvent pas utiliser l’attribut [**retVal**](retval.md) pour retourner une valeur en plus d’un code d’erreur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7cd76-148">Unlike interface members, dispinterface members cannot use the [**retval**](retval.md) attribute to return a value in addition to an HRESULT error code.</span></span> <span data-ttu-id="7cd76-149">L' \[ [](lcid.md) \] attribut LCID est également non valide pour les dispinterfaces, car IDispatch :: Invoke passe un LCID.</span><span class="sxs-lookup"><span data-stu-id="7cd76-149">The \[ [**lcid**](lcid.md)\] attribute is likewise invalid for dispinterfaces, because IDispatch::Invoke passes an LCID.</span></span> <span data-ttu-id="7cd76-150">Toutefois, il est possible de redéclarer une interface qui utilise ces attributs.</span><span class="sxs-lookup"><span data-stu-id="7cd76-150">However, it is possible to redeclare an interface that uses these attributes.</span></span>

<span data-ttu-id="7cd76-151">À l’aide de la deuxième syntaxe, les interfaces qui prennent en charge IDispatch et sont déclarées précédemment dans un script ODL peuvent être redéclarées comme des interfaces IDispatch comme suit :</span><span class="sxs-lookup"><span data-stu-id="7cd76-151">Using the second syntax, interfaces that support IDispatch and are declared earlier in an ODL script can be redeclared as IDispatch interfaces as follows:</span></span>

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

<span data-ttu-id="7cd76-152">L’exemple précédent déclare tous les membres de Hello et tous les membres que Hello hérite de en prenant en charge IDispatch.</span><span class="sxs-lookup"><span data-stu-id="7cd76-152">The preceding example declares all the members of hello and all the members that hello inherits as supporting IDispatch.</span></span> <span data-ttu-id="7cd76-153">Dans ce cas, si Hello a été déclaré précédemment avec des \[ \] membres LCID et \[ retval \] qui retournaient HRESULT, mktyplib supprimerait chaque \[ \] paramètre LCID et le type de retour HRESULT, et marquera à la place le type de retour comme celui du \[ \] paramètre retval.</span><span class="sxs-lookup"><span data-stu-id="7cd76-153">In this case, if hello were declared earlier with \[lcid\] and \[retval\] members that returned HRESULTs, MkTypLib would remove each \[lcid\] parameter and HRESULT return type, and instead mark the return type as that of the \[retval\] parameter.</span></span>

> [!Note]  
> <span data-ttu-id="7cd76-154">L’outil Mktyplib.exe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7cd76-154">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="7cd76-155">Utilisez plutôt le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="7cd76-155">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="7cd76-156">Les propriétés et les méthodes d’une dispinterface ne font pas partie du VTBL de la dispinterface.</span><span class="sxs-lookup"><span data-stu-id="7cd76-156">The properties and methods of a dispinterface are not part of the VTBL of the dispinterface.</span></span> <span data-ttu-id="7cd76-157">Par conséquent, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) et [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) ne peuvent pas être utilisés pour implémenter IDispatch :: Invoke.</span><span class="sxs-lookup"><span data-stu-id="7cd76-157">Consequently, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) and [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) cannot be used to implement IDispatch::Invoke.</span></span> <span data-ttu-id="7cd76-158">La dispinterface est utilisée lorsqu’une application doit exposer des fonctions non VTBL existantes par le biais de l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="7cd76-158">The dispinterface is used when an application needs to expose existing non-VTBL functions through Automation.</span></span> <span data-ttu-id="7cd76-159">Ces applications peuvent implémenter IDispatch :: Invoke en examinant le paramètre dispidMember et en appelant directement la fonction correspondante.</span><span class="sxs-lookup"><span data-stu-id="7cd76-159">These applications can implement IDispatch::Invoke by examining the dispidMember parameter and directly calling the corresponding function.</span></span>

## <a name="examples"></a><span data-ttu-id="7cd76-160">Exemples</span><span class="sxs-lookup"><span data-stu-id="7cd76-160">Examples</span></span>

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="7cd76-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cd76-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd76-162">**bindable**</span><span class="sxs-lookup"><span data-stu-id="7cd76-162">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="7cd76-163">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="7cd76-163">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="7cd76-164">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="7cd76-164">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="7cd76-165">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="7cd76-165">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="7cd76-166">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="7cd76-166">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="7cd76-167">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="7cd76-167">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="7cd76-168">**masquer**</span><span class="sxs-lookup"><span data-stu-id="7cd76-168">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="7cd76-169">**in**</span><span class="sxs-lookup"><span data-stu-id="7cd76-169">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="7cd76-170">**interface**</span><span class="sxs-lookup"><span data-stu-id="7cd76-170">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="7cd76-171">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="7cd76-171">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="7cd76-172">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7cd76-172">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7cd76-173">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7cd76-173">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7cd76-174">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="7cd76-174">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7cd76-175">**facultatif**</span><span class="sxs-lookup"><span data-stu-id="7cd76-175">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="7cd76-176">**à**</span><span class="sxs-lookup"><span data-stu-id="7cd76-176">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="7cd76-177">**nonextensible**</span><span class="sxs-lookup"><span data-stu-id="7cd76-177">**nonextensible**</span></span>](nonextensible.md)
</dt> <dt>

[<span data-ttu-id="7cd76-178">**propget**</span><span class="sxs-lookup"><span data-stu-id="7cd76-178">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="7cd76-179">**propput**</span><span class="sxs-lookup"><span data-stu-id="7cd76-179">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="7cd76-180">**propputref**</span><span class="sxs-lookup"><span data-stu-id="7cd76-180">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="7cd76-181">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="7cd76-181">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="7cd76-182">**sensible**</span><span class="sxs-lookup"><span data-stu-id="7cd76-182">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="7cd76-183">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="7cd76-183">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="7cd76-184">**universel**</span><span class="sxs-lookup"><span data-stu-id="7cd76-184">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="7cd76-185">**vararg**</span><span class="sxs-lookup"><span data-stu-id="7cd76-185">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="7cd76-186">**Version**</span><span class="sxs-lookup"><span data-stu-id="7cd76-186">**version**</span></span>](version.md)
</dt> </dl>

 

 