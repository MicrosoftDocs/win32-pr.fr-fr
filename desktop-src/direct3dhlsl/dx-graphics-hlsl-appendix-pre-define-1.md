---
title: '\#define, directive (constante)'
description: Directive de préprocesseur qui affecte un nom explicite à une constante dans votre application.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104030628"
---
# <a name="define-directive-constant"></a><span data-ttu-id="b628b-103">\#define, directive (constante)</span><span class="sxs-lookup"><span data-stu-id="b628b-103">\#define directive (constant)</span></span>

<span data-ttu-id="b628b-104">Directive de préprocesseur qui affecte un nom explicite à une constante dans votre application.</span><span class="sxs-lookup"><span data-stu-id="b628b-104">Preprocessor directive that assigns a meaningful name to a constant in your application.</span></span>



| <span data-ttu-id="b628b-105">\#définir *identifiertoken-chaîne*</span><span class="sxs-lookup"><span data-stu-id="b628b-105">\#define *identifiertoken-string*</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b628b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b628b-106">Parameters</span></span>



| <span data-ttu-id="b628b-107">Élément</span><span class="sxs-lookup"><span data-stu-id="b628b-107">Item</span></span>                                                                                                                       | <span data-ttu-id="b628b-108">Description</span><span class="sxs-lookup"><span data-stu-id="b628b-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b628b-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificateur*</span><span class="sxs-lookup"><span data-stu-id="b628b-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                          | <span data-ttu-id="b628b-110">Identificateur de la constante.</span><span class="sxs-lookup"><span data-stu-id="b628b-110">Identifier of the constant.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b628b-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*jeton-chaîne* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b628b-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[optional\]</span></span><br/> | <span data-ttu-id="b628b-112">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="b628b-112">Value of the constant.</span></span> <span data-ttu-id="b628b-113">Ce paramètre se compose d’une série de jetons, tels que les mots clés, les constantes ou les instructions complètes.</span><span class="sxs-lookup"><span data-stu-id="b628b-113">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="b628b-114">Un ou plusieurs espaces blancs doivent séparer ce paramètre du paramètre *identificateur* ; Cet espace blanc n’est pas considéré comme faisant partie du texte substitué, et n’est pas un espace blanc qui suit le dernier jeton du texte.</span><span class="sxs-lookup"><span data-stu-id="b628b-114">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <br/> <span data-ttu-id="b628b-115">Si vous excluez ce paramètre, toutes les instances du paramètre d' *identificateur* sont supprimées du fichier source.</span><span class="sxs-lookup"><span data-stu-id="b628b-115">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="b628b-116">L’identificateur reste défini et peut être testé à l’aide des directives [ \# If](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef et \# ifndef définies.</span><span class="sxs-lookup"><span data-stu-id="b628b-116">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b628b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b628b-117">Remarks</span></span>

<span data-ttu-id="b628b-118">Toutes les instances du paramètre d' *identificateur* qui se produisent après la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) dans le fichier source sont remplacées par la valeur du paramètre de *chaîne de jeton* .</span><span class="sxs-lookup"><span data-stu-id="b628b-118">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file will be replaced by the value of the *token-string* parameter.</span></span> <span data-ttu-id="b628b-119">L’identificateur est remplacé uniquement lorsqu’il forme un jeton. par exemple, l’identificateur n’est pas remplacé s’il apparaît dans un commentaire, dans une chaîne ou dans le cadre d’un identificateur plus long.</span><span class="sxs-lookup"><span data-stu-id="b628b-119">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="b628b-120">La directive [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) indique au préprocesseur d’oublier la définition d’un identificateur. pour plus d’informations, consultez \# directive undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="b628b-120">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="b628b-121">La définition de constantes avec l’option de compilateur/D a le même effet que l’utilisation de la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) au début de votre fichier.</span><span class="sxs-lookup"><span data-stu-id="b628b-121">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="b628b-122">Il est possible de définir jusqu’à 30 constantes avec l’option/D.</span><span class="sxs-lookup"><span data-stu-id="b628b-122">Up to 30 constants can be defined with the /D option.</span></span> <span data-ttu-id="b628b-123">Pour obtenir un exemple de la façon dont cela peut être utilisé, consultez la section Exemples de [ \# ifdef et)](dx-graphics-hlsl-appendix-pre-ifdef.md).</span><span class="sxs-lookup"><span data-stu-id="b628b-123">For an example of how this can be used, see the Examples section of [\#ifdef and )](dx-graphics-hlsl-appendix-pre-ifdef.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b628b-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="b628b-124">Examples</span></span>

<span data-ttu-id="b628b-125">L’exemple suivant définit la largeur de l’identificateur en tant que constante entière 80, puis définit la longueur en termes de largeur et la constante entière 10.</span><span class="sxs-lookup"><span data-stu-id="b628b-125">The following example defines the identifier WIDTH as the integer constant 80 and then defines LENGTH in terms of WIDTH and the integer constant 10.</span></span>


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



<span data-ttu-id="b628b-126">Chaque instance suivante de LENGTH est remplacée par (WIDTH + 10), et chaque instance suivante de WIDTH + 10 est remplacée par l’expression (80 + 10).</span><span class="sxs-lookup"><span data-stu-id="b628b-126">Every subsequent instance of LENGTH is replaced by (WIDTH + 10), and every subsequent instance of WIDTH + 10 is replaced by the expression (80 + 10).</span></span> <span data-ttu-id="b628b-127">Les parenthèses autour de la largeur + 10 sont importantes car elles contrôlent l’interprétation dans des instructions telles que la suivante.</span><span class="sxs-lookup"><span data-stu-id="b628b-127">The parentheses around WIDTH + 10 are important because they control the interpretation in statements such as the following.</span></span>


```
var = LENGTH * 20;
```



<span data-ttu-id="b628b-128">Après l’étape de prétraitement, l’instruction devient la suivante, qui prend la valeur 1 800.</span><span class="sxs-lookup"><span data-stu-id="b628b-128">After the preprocessing stage the statement becomes the following, which evaluates to 1,800.</span></span>


```
var = ( 80 + 10 ) * 20;
```



<span data-ttu-id="b628b-129">Sans parenthèses, le résultat est le suivant, qui prend la valeur 280.</span><span class="sxs-lookup"><span data-stu-id="b628b-129">Without parentheses, the result would be the following, which evaluates to 280.</span></span>


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a><span data-ttu-id="b628b-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b628b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b628b-131">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b628b-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="b628b-132">\#définir des surcharges</span><span class="sxs-lookup"><span data-stu-id="b628b-132">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="b628b-133">\#undef, directive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b628b-133">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





