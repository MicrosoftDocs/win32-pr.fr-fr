---
title: attribut wchar_t
description: Le \_ mot clé WCHAR t désigne un type à caractères larges.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t MIDL de l’attribut
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2020
ms.locfileid: "104030896"
---
# <a name="wchar_t-attribute"></a><span data-ttu-id="e7542-104">WCHAR \_ t (attribut)</span><span class="sxs-lookup"><span data-stu-id="e7542-104">wchar\_t attribute</span></span>

<span data-ttu-id="e7542-105">Le mot clé **WCHAR \_ t** désigne un type à caractères larges.</span><span class="sxs-lookup"><span data-stu-id="e7542-105">The **wchar\_t** keyword designates a wide-character type.</span></span>

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="e7542-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7542-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7542-107">*identificateur-nom*</span><span class="sxs-lookup"><span data-stu-id="e7542-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e7542-108">Spécifie un identificateur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="e7542-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="e7542-109">Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="e7542-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7542-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e7542-110">Remarks</span></span>

<span data-ttu-id="e7542-111">Le type de **WCHAR \_ t** est défini par MIDL comme un objet de données [**short**](short.md) (16 bits) [**non signé**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="e7542-111">The **wchar\_t** type is defined by MIDL as an [**unsigned**](unsigned.md) [**short**](short.md) (16-bit) data object.</span></span>

<span data-ttu-id="e7542-112">Le compilateur MIDL permet la redéfinition de **WCHAR \_ t**, mais uniquement s’il est cohérent avec la définition précédente.</span><span class="sxs-lookup"><span data-stu-id="e7542-112">The MIDL compiler allows redefinition of **wchar\_t**, but only if it is consistent with the preceding definition.</span></span>

<span data-ttu-id="e7542-113">Le type à caractères larges est l’un des types prédéfinis de MIDL.</span><span class="sxs-lookup"><span data-stu-id="e7542-113">The wide-character type is one of the predefined types of MIDL.</span></span> <span data-ttu-id="e7542-114">Le type à caractères larges peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type de retour de fonction et en tant que spécificateur de type de paramètre).</span><span class="sxs-lookup"><span data-stu-id="e7542-114">The wide-character type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="e7542-115">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="e7542-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="e7542-116">L’attribut de **\[ chaîne \]** peut être appliqué à un pointeur ou à un tableau de type **WCHAR \_ t**.</span><span class="sxs-lookup"><span data-stu-id="e7542-116">The **\[string\]** attribute can be applied to a pointer or array of type **wchar\_t**.</span></span>

<span data-ttu-id="e7542-117">Utilisez le caractère **l** avant un caractère ou une constante de chaîne pour désigner la constante de type à caractères larges.</span><span class="sxs-lookup"><span data-stu-id="e7542-117">Use the **L** character before a character or a string constant to designate the wide character type constant.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7542-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7542-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7542-119">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="e7542-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e7542-120">**Char**</span><span class="sxs-lookup"><span data-stu-id="e7542-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="e7542-121">**const**</span><span class="sxs-lookup"><span data-stu-id="e7542-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e7542-122">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="e7542-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e7542-123">**short**</span><span class="sxs-lookup"><span data-stu-id="e7542-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="e7542-124">**typedef**</span><span class="sxs-lookup"><span data-stu-id="e7542-124">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="e7542-125">**non signé**</span><span class="sxs-lookup"><span data-stu-id="e7542-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




