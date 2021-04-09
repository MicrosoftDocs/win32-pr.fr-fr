---
title: Hyper Attribute
description: Le mot clé hyper indique un entier 64 bits qui peut être déclaré comme étant signé ou non signé.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- MIDL hyper-attribut
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678246"
---
# <a name="hyper-attribute"></a><span data-ttu-id="ef7dd-104">Hyper Attribute</span><span class="sxs-lookup"><span data-stu-id="ef7dd-104">hyper attribute</span></span>

<span data-ttu-id="ef7dd-105">Le mot clé **hyper** indique un entier 64 bits qui peut être déclaré comme étant signé ou non signé.</span><span class="sxs-lookup"><span data-stu-id="ef7dd-105">The keyword **hyper** indicates a 64-bit integer that can be declared as either signed or unsigned.</span></span>

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="ef7dd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef7dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef7dd-107">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="ef7dd-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ef7dd-108">Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="ef7dd-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="ef7dd-109">(Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="ef7dd-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="ef7dd-110">Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ef7dd-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef7dd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ef7dd-111">Remarks</span></span>

<span data-ttu-id="ef7dd-112">Le type **hyper** est l’un des types de base du langage IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="ef7dd-112">The **hyper** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="ef7dd-113">Le type **hyper** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type de retour de fonction et en tant que spécificateur de type de paramètre).</span><span class="sxs-lookup"><span data-stu-id="ef7dd-113">The **hyper** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="ef7dd-114">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="ef7dd-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="ef7dd-115">Pour les plateformes 16 bits, le compilateur MIDL remplace les entiers hyper signés par des **\_ uhyper MIDL**.</span><span class="sxs-lookup"><span data-stu-id="ef7dd-115">For 16-bit platforms, the MIDL compiler replaces unsigned hyper integers with **MIDL\_uhyper**.</span></span> <span data-ttu-id="ef7dd-116">Cela permet de définir des interfaces avec des entiers hyper signés sur des plateformes qui ne prennent pas directement en charge les entiers 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ef7dd-116">This allows interfaces with unsigned hyper integers to be defined on platforms that do not directly support 64-bit integers.</span></span> <span data-ttu-id="ef7dd-117">**Le \_ uhyper MIDL** est défini dans les fichiers d’en-tête RPC.</span><span class="sxs-lookup"><span data-stu-id="ef7dd-117">**MIDL\_uhyper** is defined in the RPC header files.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ef7dd-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef7dd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef7dd-119">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="ef7dd-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="ef7dd-120">**const**</span><span class="sxs-lookup"><span data-stu-id="ef7dd-120">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="ef7dd-121">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="ef7dd-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ef7dd-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="ef7dd-122">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




