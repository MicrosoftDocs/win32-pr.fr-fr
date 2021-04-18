---
title: attribut enum
description: Le mot clé enum identifie un type énuméré.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- énumération MIDL d’attribut
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312220"
---
# <a name="enum-attribute"></a><span data-ttu-id="380ef-104">attribut enum</span><span class="sxs-lookup"><span data-stu-id="380ef-104">enum attribute</span></span>

<span data-ttu-id="380ef-105">Le mot clé **enum** identifie un type énuméré.</span><span class="sxs-lookup"><span data-stu-id="380ef-105">The keyword **enum** identifies an enumerated type.</span></span>

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a><span data-ttu-id="380ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="380ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380ef-107">*tag*</span><span class="sxs-lookup"><span data-stu-id="380ef-107">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="380ef-108">Spécifie une balise facultative pour le type énuméré.</span><span class="sxs-lookup"><span data-stu-id="380ef-108">Specifies an optional tag for the enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="380ef-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="380ef-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="380ef-110">Spécifie l’énumération particulière.</span><span class="sxs-lookup"><span data-stu-id="380ef-110">Specifies the particular enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="380ef-111">*valeur entière*</span><span class="sxs-lookup"><span data-stu-id="380ef-111">*integer-value*</span></span> 
</dt> <dd>

<span data-ttu-id="380ef-112">Spécifie une valeur entière constante.</span><span class="sxs-lookup"><span data-stu-id="380ef-112">Specifies a constant integer value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="380ef-113">Notes</span><span class="sxs-lookup"><span data-stu-id="380ef-113">Remarks</span></span>

<span data-ttu-id="380ef-114">les types **enum** peuvent apparaître en tant que spécificateurs de type dans les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que fonction-Return-type ou en tant que spécificateur de type paramètre).</span><span class="sxs-lookup"><span data-stu-id="380ef-114">**enum** types can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (either as the function-return-type or as a parameter-type specifier).</span></span> <span data-ttu-id="380ef-115">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="380ef-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="380ef-116">Dans le mode par défaut du compilateur MIDL, vous pouvez assigner des valeurs entières à des énumérateurs.</span><span class="sxs-lookup"><span data-stu-id="380ef-116">In the MIDL compiler's default mode, you can assign integer values to enumerators.</span></span> <span data-ttu-id="380ef-117">(Cette fonctionnalité n’est pas disponible quand vous compilez avec le commutateur [**/OSF**](-osf.md) .) Comme avec les énumérateurs de langage C, les noms d’énumérateur doivent être uniques, mais les valeurs d’énumérateur n’ont pas besoin d’être.</span><span class="sxs-lookup"><span data-stu-id="380ef-117">(This feature is not available when you compile with the [**/osf**](-osf.md) switch.) As with C-language enumerators, enumerator names must be unique, but the enumerator values need not be.</span></span>

<span data-ttu-id="380ef-118">Lorsque les opérateurs d’assignation ne sont pas fournis, les identificateurs sont mappés à des entiers consécutifs de gauche à droite, en commençant par zéro.</span><span class="sxs-lookup"><span data-stu-id="380ef-118">When assignment operators are not provided, identifiers are mapped to consecutive integers from left to right, starting with zero.</span></span> <span data-ttu-id="380ef-119">Lorsque des opérateurs d’assignation sont fournis, les valeurs affectées commencent à partir de la dernière valeur assignée.</span><span class="sxs-lookup"><span data-stu-id="380ef-119">When assignment operators are provided, assigned values start from the most recently assigned value.</span></span>

<span data-ttu-id="380ef-120">Le nombre maximal d’identificateurs est 65 535.</span><span class="sxs-lookup"><span data-stu-id="380ef-120">The maximum number of identifiers is 65,535.</span></span>

<span data-ttu-id="380ef-121">Les objets de type **enum** sont des types [**int**](int.md) et leur taille est dépendante du système.</span><span class="sxs-lookup"><span data-stu-id="380ef-121">Objects of type **enum** are [**int**](int.md) types, and their size is system-dependent.</span></span> <span data-ttu-id="380ef-122">Par défaut, les objets de types **enum** sont traités comme des objets 16 bits de type [**unsigned**](unsigned.md) [**short**](short.md) lorsqu’ils sont transmis sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="380ef-122">By default, objects of **enum** types are treated as 16-bit objects of type [**unsigned**](unsigned.md) [**short**](short.md) when transmitted over a network.</span></span> <span data-ttu-id="380ef-123">Les valeurs situées en dehors de la plage 0 à 32 767 provoquent la \_ valeur enum X RPC de l’exception Runtime \_ \_ \_ hors \_ \_ limites.</span><span class="sxs-lookup"><span data-stu-id="380ef-123">Values outside the range 0 - 32,767 cause the run-time exception RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="380ef-124">Pour transmettre des objets en tant qu’entités 32 bits, appliquez l' **\[** attribut [**\_ enum v1**](v1-enum.md) **\]** au typedef **enum** .</span><span class="sxs-lookup"><span data-stu-id="380ef-124">To transmit objects as 32-bit entities, apply the **\[**[**v1\_enum**](v1-enum.md)**\]** attribute to the **enum** typedef.</span></span>

## <a name="examples"></a><span data-ttu-id="380ef-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="380ef-125">Examples</span></span>

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a><span data-ttu-id="380ef-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="380ef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380ef-127">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="380ef-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="380ef-128">**int**</span><span class="sxs-lookup"><span data-stu-id="380ef-128">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="380ef-129">**short**</span><span class="sxs-lookup"><span data-stu-id="380ef-129">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="380ef-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="380ef-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="380ef-131">**non signé**</span><span class="sxs-lookup"><span data-stu-id="380ef-131">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="380ef-132">**\_enum v1**</span><span class="sxs-lookup"><span data-stu-id="380ef-132">**v1\_enum**</span></span>](v1-enum.md)
</dt> </dl>

 

 




