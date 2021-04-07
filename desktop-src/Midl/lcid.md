---
title: LCID (attribut)
description: L’attribut \ LCID \ spécifie un identificateur de paramètres régionaux et active la prise en charge du compilateur MIDL spécifique aux paramètres régionaux.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- attribut LCID MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725093"
---
# <a name="lcid-attribute"></a><span data-ttu-id="02ba2-104">LCID (attribut)</span><span class="sxs-lookup"><span data-stu-id="02ba2-104">lcid attribute</span></span>

<span data-ttu-id="02ba2-105">L’attribut **\[ LCID \]** spécifie un identificateur de paramètres régionaux et active la prise en charge du compilateur MIDL spécifique aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="02ba2-105">The **\[lcid\]** attribute specifies a locale identifier and enables locale-specific MIDL compiler support.</span></span>

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="02ba2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02ba2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ba2-107">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="02ba2-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="02ba2-108">Spécifie un numéro d’identification unique universel pour la [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="02ba2-108">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="02ba2-109">*localeID*</span><span class="sxs-lookup"><span data-stu-id="02ba2-109">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="02ba2-110">Spécifie l’identificateur de paramètres régionaux 32 bits utilisé dans la prise en charge des langues nationales Windows.</span><span class="sxs-lookup"><span data-stu-id="02ba2-110">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="02ba2-111">En général, l’identificateur de paramètres régionaux est fourni au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="02ba2-111">Typically the locale identifier is given in hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="02ba2-112">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="02ba2-112">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02ba2-113">Zéro, un ou plusieurs attributs à appliquer à la [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="02ba2-113">Zero or more attributes to apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="02ba2-114">*nom de la bibliothèque*</span><span class="sxs-lookup"><span data-stu-id="02ba2-114">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02ba2-115">Nom par lequel les composants logiciels font référence à la [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="02ba2-115">The name by which software components refer to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="02ba2-116">*Bibliothèque-définition-instructions*</span><span class="sxs-lookup"><span data-stu-id="02ba2-116">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="02ba2-117">Une ou plusieurs instructions MIDL qui définissent le contenu de la [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="02ba2-117">One or more MIDL statements which define the contents of the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="02ba2-118">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="02ba2-118">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02ba2-119">Spécifie le nom de la fonction dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="02ba2-119">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="02ba2-120">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="02ba2-120">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02ba2-121">Zéro, un ou plusieurs attributs MIDL qui seront appliqués au paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="02ba2-121">Zero or more MIDL attributes that will be applied to the function parameter.</span></span>

</dd> <dt>

<span data-ttu-id="02ba2-122">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="02ba2-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02ba2-123">Spécifie le nom du paramètre dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="02ba2-123">Specifies the name of the parameter in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02ba2-124">Notes</span><span class="sxs-lookup"><span data-stu-id="02ba2-124">Remarks</span></span>

<span data-ttu-id="02ba2-125">La syntaxe **\[ \] LCID** a deux formes différentes ; l’effet de l’attribut dépend de la syntaxe que vous utilisez, à savoir la syntaxe de l’instruction de la [**bibliothèque**](library.md) ou la syntaxe du paramètre.</span><span class="sxs-lookup"><span data-stu-id="02ba2-125">The **\[lcid\]** syntax has two different forms; the effect of the attribute depends on which syntax you use — either the [**library**](library.md) statement syntax or the parameter syntax.</span></span>

<span data-ttu-id="02ba2-126">En cas d’application à l’instruction [**Library**](library.md) , avec un argument LocaleID, comme indiqué dans le premier exemple, l’attribut **\[ LCID \]** identifie les paramètres régionaux d’une bibliothèque de types ou d’un argument de fonction, et vous permet d’utiliser des caractères internationaux dans le bloc de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="02ba2-126">When applied to the [**library**](library.md) statement, along with a localeID argument, as shown in the first example, the **\[lcid\]** attribute identifies the locale for a type library or for a function argument and lets you use international characters inside the library block.</span></span>

<span data-ttu-id="02ba2-127">Efficace avec la version 3.01.75 du compilateur MIDL, l’identificateur de paramètres régionaux fourni par cet attribut décore la bibliothèque de types résultante, mais modifie en fait le comportement du compilateur.</span><span class="sxs-lookup"><span data-stu-id="02ba2-127">Effective with version 3.01.75 of the MIDL compiler, the locale identifier supplied by this attribute not only decorates the resulting type library, but actually changes the behavior of the compiler.</span></span> <span data-ttu-id="02ba2-128">Dans une instruction de [**bibliothèque**](library.md) , à partir du point où l’attribut **\[ LCID \]** est utilisé, MIDL accepte les entrées localisées en fonction des paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="02ba2-128">Within a [**library**](library.md) statement, from the point where the **\[lcid\]** attribute is used, MIDL will accept input localized according to the specified locale.</span></span> <span data-ttu-id="02ba2-129">En particulier, la prise en charge complète des langues asiatiques telles que le japonais, le chinois et le coréen (prise en charge complète des caractères DBCS) est disponible.</span><span class="sxs-lookup"><span data-stu-id="02ba2-129">In particular, full support for Asian languages such as Japanese, Chinese and Korean (full DBCS support) is available.</span></span> <span data-ttu-id="02ba2-130">Les fonctionnalités prises en charge par la localisation sont les suivantes : commentaires, chaînes, HelpStrings et identificateurs.</span><span class="sxs-lookup"><span data-stu-id="02ba2-130">Features supported by the localization are: comments, strings, helpstrings and identifiers.</span></span>

<span data-ttu-id="02ba2-131">Utilisez le commutateur [**/LCID**](-lcid.md) du compilateur pour que cette prise en charge de la localisation soit disponible pour l’ensemble du fichier d’entrée, y compris le nom de fichier et le chemin d’accès au répertoire, plutôt que simplement à l’intérieur du bloc de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="02ba2-131">Use the [**/lcid**](-lcid.md) compiler switch to have this localization support available to the entire input file, including file name and directory path, rather than just inside the library block.</span></span>

<span data-ttu-id="02ba2-132">Lorsqu’il est appliqué à un paramètre, l’attribut **\[ LCID \]** vous permet de passer un identificateur de paramètres régionaux à une fonction, comme indiqué dans le deuxième exemple.</span><span class="sxs-lookup"><span data-stu-id="02ba2-132">When applied to a parameter, the **\[lcid\]** attribute lets you pass a locale identifier to a function, as shown in the second example.</span></span> <span data-ttu-id="02ba2-133">Les restrictions suivantes s’appliquent aux paramètres **\[ LCID \]** :</span><span class="sxs-lookup"><span data-stu-id="02ba2-133">The following restrictions apply to **\[lcid\]** parameters:</span></span>

-   <span data-ttu-id="02ba2-134">Une fonction ne peut avoir qu’un seul paramètre **\[ LCID \]** .</span><span class="sxs-lookup"><span data-stu-id="02ba2-134">A function can have at most one **\[lcid\]** parameter.</span></span>
-   <span data-ttu-id="02ba2-135">Le type de données du paramètre doit être [**long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="02ba2-135">The data type of the parameter must be [**long**](long.md).</span></span>
-   <span data-ttu-id="02ba2-136">La direction du paramètre doit être **\[** [**dans**](in.md) **\]** uniquement.</span><span class="sxs-lookup"><span data-stu-id="02ba2-136">The direction of the parameter must be **\[**[**in**](in.md)**\]** only.</span></span>
-   <span data-ttu-id="02ba2-137">Le paramètre **\[ LCID \]** doit suivre tous les autres paramètres, à l’exception d’un **\[** paramètre [**retVal**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="02ba2-137">The **\[lcid\]** parameter must follow any other parameters, except a **\[**[**retval**](retval.md)**\]** parameter.</span></span>
-   <span data-ttu-id="02ba2-138">Vous ne pouvez pas appliquer l’attribut **\[ LCID \]** à un paramètre [**dispinterface**](dispinterface.md) ou [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="02ba2-138">You cannot apply the **\[lcid\]** attribute to a [**dispinterface**](dispinterface.md) or [**coclass**](coclass.md) parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="02ba2-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="02ba2-139">Examples</span></span>

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a><span data-ttu-id="02ba2-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02ba2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ba2-141">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="02ba2-141">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="02ba2-142">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="02ba2-142">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="02ba2-143">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="02ba2-143">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="02ba2-144">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="02ba2-144">**/lcid**</span></span>](-lcid.md)
</dt> <dt>

[<span data-ttu-id="02ba2-145">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="02ba2-145">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="02ba2-146">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="02ba2-146">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="02ba2-147">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="02ba2-147">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="02ba2-148">**retval**</span><span class="sxs-lookup"><span data-stu-id="02ba2-148">**retval**</span></span>](retval.md)
</dt> </dl>

 

 