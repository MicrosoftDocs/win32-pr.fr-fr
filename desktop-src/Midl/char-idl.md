---
title: Char (attribut)
description: Le mot clé char spécifie un élément de données de 8 bits.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- attribut char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841477"
---
# <a name="char-attribute"></a><span data-ttu-id="6b445-104">Char (attribut)</span><span class="sxs-lookup"><span data-stu-id="6b445-104">char attribute</span></span>

<span data-ttu-id="6b445-105">Le mot clé **char** spécifie un élément de données de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="6b445-105">The **char** keyword specifies an 8-bit data item.</span></span>

``` syntax
char identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="6b445-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b445-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b445-107">*identificateur-nom*</span><span class="sxs-lookup"><span data-stu-id="6b445-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6b445-108">Spécifie un identificateur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="6b445-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="6b445-109">Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="6b445-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b445-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6b445-110">Remarks</span></span>

<span data-ttu-id="6b445-111">Le mot clé **char** identifie un élément de données qui contient 8 bits.</span><span class="sxs-lookup"><span data-stu-id="6b445-111">The keyword **char** identifies a data item that has 8 bits.</span></span> <span data-ttu-id="6b445-112">Pour le compilateur MIDL, un **caractère** est non signé par défaut et est synonyme de type [**unsigned**](unsigned.md) **char**.</span><span class="sxs-lookup"><span data-stu-id="6b445-112">To the MIDL compiler, a **char** is unsigned by default and is synonymous with [**unsigned**](unsigned.md) **char**.</span></span>

<span data-ttu-id="6b445-113">Dans cette version de Microsoft RPC, les tables de conversion de caractères qui convertissent entre ASCII et EBCDIC sont intégrées dans les bibliothèques Runtime et ne peuvent pas être modifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b445-113">In this version of Microsoft RPC, the character translation tables that convert between ASCII and EBCDIC are built into the run-time libraries and cannot be changed by the user.</span></span>

<span data-ttu-id="6b445-114">Le type **char** est l’un des types de base du langage IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="6b445-114">The **char** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="6b445-115">Le type **char** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et spécificateur de type de paramètre).</span><span class="sxs-lookup"><span data-stu-id="6b445-115">The **char** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="6b445-116">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="6b445-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="6b445-117">Les compilateurs IDL DCE n’acceptent pas le mot clé [**signed**](signed.md) appliqué aux types **char** .</span><span class="sxs-lookup"><span data-stu-id="6b445-117">DCE IDL compilers do not accept the keyword [**signed**](signed.md) applied to **char** types.</span></span> <span data-ttu-id="6b445-118">Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur [**/OSF**](-osf.md) du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="6b445-118">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b445-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b445-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b445-120">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="6b445-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="6b445-121">**poids**</span><span class="sxs-lookup"><span data-stu-id="6b445-121">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="6b445-122">**/Char**</span><span class="sxs-lookup"><span data-stu-id="6b445-122">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="6b445-123">**const**</span><span class="sxs-lookup"><span data-stu-id="6b445-123">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="6b445-124">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="6b445-124">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6b445-125">**/osf**</span><span class="sxs-lookup"><span data-stu-id="6b445-125">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="6b445-126">**abonné**</span><span class="sxs-lookup"><span data-stu-id="6b445-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="6b445-127">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b445-127">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="6b445-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="6b445-128">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="6b445-129">**non signé**</span><span class="sxs-lookup"><span data-stu-id="6b445-129">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="6b445-130">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="6b445-130">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




