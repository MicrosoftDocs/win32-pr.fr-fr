---
title: attribut const
description: Le mot clé const modifie le type d’une déclaration de type ou le type d’un paramètre de fonction, ce qui empêche la valeur de varier.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- attribut const, MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7095e29daf18dc111caf37038b06b0beff5245a8
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387058"
---
# <a name="const-attribute"></a><span data-ttu-id="b22fa-104">attribut const</span><span class="sxs-lookup"><span data-stu-id="b22fa-104">const attribute</span></span>

<span data-ttu-id="b22fa-105">Le mot clé **const** modifie le type d’une déclaration de type ou le type d’un paramètre de fonction, ce qui empêche la valeur de varier.</span><span class="sxs-lookup"><span data-stu-id="b22fa-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="b22fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b22fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b22fa-107">*const-type*</span><span class="sxs-lookup"><span data-stu-id="b22fa-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-108">Spécifie un entier MIDL, un caractère, une chaîne ou un type booléen valide.</span><span class="sxs-lookup"><span data-stu-id="b22fa-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="b22fa-109">Les types MIDL valides incluent [**Small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), \**\* charÂ* _, [_ *WCHAR \_ t* \*](wchar-t.md), \**WCHAR \_ t \**_, [_ *Byte* \*](byte.md), \**byteÂ \** _ et [_*voidÂ \**_](void.md).</span><span class="sxs-lookup"><span data-stu-id="b22fa-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), \**charÂ \**_, [_ *wchar\_t*\*](wchar-t.md), \**wchar\_tÂ \**_, [_ *byte*\*](byte.md), \**byteÂ \** _, and [_*voidÂ \**_](void.md).</span></span> <span data-ttu-id="b22fa-110">Les types entier et caractère peuvent être [_ *signés* \*](signed.md) ou [**non signés**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="b22fa-110">The integer and character types can be [_ *signed*\*](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="b22fa-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-112">Spécifie un identificateur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="b22fa-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="b22fa-113">Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="b22fa-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-114">*const-expression*</span><span class="sxs-lookup"><span data-stu-id="b22fa-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-115">Spécifie une expression, un identificateur ou une constante numérique ou caractère appropriée pour le type spécifié : littéraux entiers constants ou expressions entières constantes pour les constantes entières ; Expressions booléennes qui peuvent être calculées au moment de la compilation pour les types [**booléens**](boolean.md) ; constantes à caractère unique pour les types [**char**](char-idl.md) ; et constantes de chaîne pour les **\[** [](string.md) **\]** types chaîne.</span><span class="sxs-lookup"><span data-stu-id="b22fa-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="b22fa-116">Le type [ \* *voidÂ \** _](void.md) peut être initialisé uniquement à _ \* null \* \*.</span><span class="sxs-lookup"><span data-stu-id="b22fa-116">The [\**voidÂ \** _](void.md) type can be initialized only to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-117">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="b22fa-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-118">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="b22fa-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-119">*type pointeur*</span><span class="sxs-lookup"><span data-stu-id="b22fa-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-120">Spécifie un type de pointeur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="b22fa-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-121">*déclarateur et déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="b22fa-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-122">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="b22fa-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="b22fa-123">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="b22fa-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="b22fa-124">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="b22fa-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="b22fa-125">L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.</span><span class="sxs-lookup"><span data-stu-id="b22fa-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-126">*function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="b22fa-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-127">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="b22fa-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="b22fa-128">Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b22fa-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-129">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="b22fa-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-130">Spécifie [un \_ type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="b22fa-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="b22fa-131">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="b22fa-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-132">*pointeur-decl*</span><span class="sxs-lookup"><span data-stu-id="b22fa-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-133">Spécifie zéro ou plusieurs déclarateurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="b22fa-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="b22fa-134">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C. Elle est construite à partir de l' **\* *indicateur _, de modificateurs tels que _* Far** et du qualificateur **const**.</span><span class="sxs-lookup"><span data-stu-id="b22fa-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the \**\**_ designator, modifiers such as _\* far\*\*, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-135">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="b22fa-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-136">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="b22fa-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="b22fa-137">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b22fa-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b22fa-138">Spécifie zéro, un ou plusieurs attributs directionnels, attributs de champ, attributs d’utilisation et attributs de pointeur appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="b22fa-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="b22fa-139">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="b22fa-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b22fa-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="b22fa-140">Remarks</span></span>

<span data-ttu-id="b22fa-141">MIDL vous permet de déclarer des types entier constant, caractère, chaîne et booléen dans le corps de l’interface du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="b22fa-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="b22fa-142">Les déclarations de type **const** sont reproduites dans le fichier d’en-tête généré en tant que directives de **\# définition** .</span><span class="sxs-lookup"><span data-stu-id="b22fa-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="b22fa-143">Les compilateurs IDL DCE ne prennent pas en charge les expressions constantes.</span><span class="sxs-lookup"><span data-stu-id="b22fa-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="b22fa-144">Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur [**/OSF**](-osf.md) du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="b22fa-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="b22fa-145">Une constante définie précédemment peut être utilisée comme valeur assignée d’une constante suivante.</span><span class="sxs-lookup"><span data-stu-id="b22fa-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="b22fa-146">La valeur d’une expression intégrale constante est automatiquement convertie en type entier respectif conformément aux règles de conversion C.</span><span class="sxs-lookup"><span data-stu-id="b22fa-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="b22fa-147">La valeur d’une constante caractère doit être un caractère ASCII à guillemet simple.</span><span class="sxs-lookup"><span data-stu-id="b22fa-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="b22fa-148">Lorsque la constante caractère est le caractère de guillemet simple ('), la barre oblique inverse ( \\ ) doit précéder le caractère de guillemet simple, comme dans \\ '.</span><span class="sxs-lookup"><span data-stu-id="b22fa-148">When the character constant is the single-quote character itself ('), the backslash character (\\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="b22fa-149">La valeur d’une constante de chaîne de caractères doit être une chaîne entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="b22fa-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="b22fa-150">Dans une chaîne, la barre oblique inverse ( **\\** ) doit précéder un caractère de guillemet double littéral ( **"** ), comme dans **\\ "**.</span><span class="sxs-lookup"><span data-stu-id="b22fa-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="b22fa-151">Dans une chaîne, la barre oblique inverse ( **\\** ) représente un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="b22fa-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="b22fa-152">Les constantes de chaîne peuvent comporter jusqu’à 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="b22fa-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="b22fa-153">La valeur **null** est la seule valeur valide pour les constantes de type [ \* *voidÂ \** _](void.md).</span><span class="sxs-lookup"><span data-stu-id="b22fa-153">The value **NULL** is the only valid value for constants of type [\**voidÂ \** _](void.md).</span></span> <span data-ttu-id="b22fa-154">Tous les attributs associés à la déclaration _ *const*\* sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b22fa-154">Any attributes associated with the _ *const*\* declaration are ignored.</span></span>

<span data-ttu-id="b22fa-155">Le compilateur MIDL ne vérifie pas les erreurs de plage dans l’initialisation **const** .</span><span class="sxs-lookup"><span data-stu-id="b22fa-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="b22fa-156">Par exemple, lorsque vous spécifiez « const Short x = 0xFFFFFFFF ; », le compilateur MIDL ne signale pas d’erreur et l’initialiseur est reproduit dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="b22fa-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="b22fa-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="b22fa-157">Examples</span></span>

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a><span data-ttu-id="b22fa-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b22fa-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b22fa-159">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="b22fa-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="b22fa-160">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="b22fa-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="b22fa-161">**Expression**</span><span class="sxs-lookup"><span data-stu-id="b22fa-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="b22fa-162">**poids**</span><span class="sxs-lookup"><span data-stu-id="b22fa-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="b22fa-163">**rappel**</span><span class="sxs-lookup"><span data-stu-id="b22fa-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="b22fa-164">**Char**</span><span class="sxs-lookup"><span data-stu-id="b22fa-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="b22fa-165">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="b22fa-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="b22fa-166">**variables**</span><span class="sxs-lookup"><span data-stu-id="b22fa-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="b22fa-167">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="b22fa-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b22fa-168">**tenir**</span><span class="sxs-lookup"><span data-stu-id="b22fa-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="b22fa-169">**localisé**</span><span class="sxs-lookup"><span data-stu-id="b22fa-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="b22fa-170">**long**</span><span class="sxs-lookup"><span data-stu-id="b22fa-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="b22fa-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="b22fa-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="b22fa-172">**ptr**</span><span class="sxs-lookup"><span data-stu-id="b22fa-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="b22fa-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="b22fa-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="b22fa-174">**Résumé**</span><span class="sxs-lookup"><span data-stu-id="b22fa-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="b22fa-175">**abonné**</span><span class="sxs-lookup"><span data-stu-id="b22fa-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="b22fa-176">**Small**</span><span class="sxs-lookup"><span data-stu-id="b22fa-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="b22fa-177">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="b22fa-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="b22fa-178">**modélis**</span><span class="sxs-lookup"><span data-stu-id="b22fa-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="b22fa-179">**UE**</span><span class="sxs-lookup"><span data-stu-id="b22fa-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="b22fa-180">**unique**</span><span class="sxs-lookup"><span data-stu-id="b22fa-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="b22fa-181">**non signé**</span><span class="sxs-lookup"><span data-stu-id="b22fa-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="b22fa-182">**nullité**</span><span class="sxs-lookup"><span data-stu-id="b22fa-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="b22fa-183">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="b22fa-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 