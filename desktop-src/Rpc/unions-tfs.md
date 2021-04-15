---
title: Unions RPC
description: Les unions encapsulées et sans encapsulées, ainsi que leur format avec appel de procédure distante (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463167"
---
# <a name="rpc-unions"></a><span data-ttu-id="24da5-103">Unions RPC</span><span class="sxs-lookup"><span data-stu-id="24da5-103">RPC unions</span></span>

<span data-ttu-id="24da5-104">Les unions encapsulées et non encapsulées partagent un sélecteur de bras d’Union commun \_ \_<> format :</span><span class="sxs-lookup"><span data-stu-id="24da5-104">Both encapsulated and nonencapsulated unions share a common union\_arm\_selector<> format:</span></span>

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

<span data-ttu-id="24da5-105">Le \_ champ des bras d’union<2> se compose de deux parties.</span><span class="sxs-lookup"><span data-stu-id="24da5-105">The union\_arms<2> field consists of two parts.</span></span> <span data-ttu-id="24da5-106">Si l’Union est une Union de style MIDL 1,0, les 4 bits de poids fort contiennent l’alignement du bras d’Union (alignement du bras le plus aligné).</span><span class="sxs-lookup"><span data-stu-id="24da5-106">If the union is a MIDL 1.0 style union, the upper 4 bits contain the alignment of the union arm (alignment of greatest aligned arm).</span></span> <span data-ttu-id="24da5-107">Sinon, les 4 bits supérieurs sont nuls.</span><span class="sxs-lookup"><span data-stu-id="24da5-107">Otherwise the upper 4 bits are zero.</span></span> <span data-ttu-id="24da5-108">Les 12 bits inférieurs contiennent le nombre de branches dans l’Union.</span><span class="sxs-lookup"><span data-stu-id="24da5-108">The lower 12 bits contain the number of arms in the union.</span></span> <span data-ttu-id="24da5-109">En d’autres termes :</span><span class="sxs-lookup"><span data-stu-id="24da5-109">In other words:</span></span>

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

<span data-ttu-id="24da5-110">La \_ Description de décalage à \_ ARM \_<2> champs contiennent un offset signé relatif à la description de type du ARM.</span><span class="sxs-lookup"><span data-stu-id="24da5-110">The offset\_to\_arm\_description<2> fields contain a relative signed offset to the arm's type description.</span></span> <span data-ttu-id="24da5-111">Toutefois, le champ est surchargé avec l’optimisation pour les types simples.</span><span class="sxs-lookup"><span data-stu-id="24da5-111">However, the field is overloaded with optimization for simple types.</span></span> <span data-ttu-id="24da5-112">Pour ceux-ci, l’octet supérieur de ce champ de décalage est l’octet de l' \_ Union magique FC \_ \_ (0x80) et l’octet de poids faible est le type de caractère de format réel du bras.</span><span class="sxs-lookup"><span data-stu-id="24da5-112">For these, the upper byte of this offset field is FC\_MAGIC\_UNION\_BYTE (0x80) and the lower byte of the short is the actual format character type of the arm.</span></span> <span data-ttu-id="24da5-113">Par conséquent, il existe deux plages pour les valeurs de décalage : « 80 *XX*» signifie que *XX* est une chaîne de format de type ; et tout le reste dans la plage (80 FF..</span><span class="sxs-lookup"><span data-stu-id="24da5-113">As such, there are two ranges for the offset values: "80 *xx*" means that *xx* is a type format string; and everything else within range (80 FF ..</span></span> <span data-ttu-id="24da5-114">7F FF) signifie un décalage réel.</span><span class="sxs-lookup"><span data-stu-id="24da5-114">7f FF) means an actual offset.</span></span> <span data-ttu-id="24da5-115">Cela fait des décalages de la plage <80 00.</span><span class="sxs-lookup"><span data-stu-id="24da5-115">This makes offsets from range <80 00 ..</span></span> <span data-ttu-id="24da5-116">80 FF > non disponible comme décalages.</span><span class="sxs-lookup"><span data-stu-id="24da5-116">80 FF > unavailable as offsets.</span></span> <span data-ttu-id="24da5-117">Le compilateur vérifie que la version de MIDL 5.1.164.</span><span class="sxs-lookup"><span data-stu-id="24da5-117">The compiler checks that as of MIDL version 5.1.164.</span></span>

<span data-ttu-id="24da5-118">Le \_ \_ champ de description ARM<2> par défaut indique le type de bras d’Union pour le bras par défaut, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="24da5-118">The default\_arm\_description<2> field indicates the type of union arm for the default arm, if any.</span></span> <span data-ttu-id="24da5-119">Si aucun ARM par défaut n’est spécifié pour l’Union, la \_ Description du ARM par défaut \_<2> champ est 0xFFFF et une exception est levée si le commutateur \_ est une valeur ne correspond à aucune des valeurs de cas ARM.</span><span class="sxs-lookup"><span data-stu-id="24da5-119">If there is no default arm specified for the union then the default\_arm\_description<2> field is 0xFFFF and an exception is raised if the switch\_is value does not match any of the arm case values.</span></span> <span data-ttu-id="24da5-120">Si le ARM par défaut est spécifié mais vide, la description du ARM par défaut \_ \_<2> champ est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="24da5-120">If the default arm is specified but empty, then the default\_arm\_description<2> field is zero.</span></span> <span data-ttu-id="24da5-121">Dans le cas contraire, la description du ARM par défaut \_ \_<2> champ a la même sémantique que la description du décalage \_ vers \_ ARM \_<2> champs.</span><span class="sxs-lookup"><span data-stu-id="24da5-121">Otherwise the default\_arm\_description<2> field has the same semantics as the offset\_to\_arm\_description<2> fields.</span></span>

<span data-ttu-id="24da5-122">Voici un résumé :</span><span class="sxs-lookup"><span data-stu-id="24da5-122">The following is a summary:</span></span>

-   <span data-ttu-id="24da5-123">0-valeur par défaut vide</span><span class="sxs-lookup"><span data-stu-id="24da5-123">0 - empty default</span></span>
-   <span data-ttu-id="24da5-124">FFFF-pas de valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="24da5-124">FFFF - no default</span></span>
-   <span data-ttu-id="24da5-125">80xx-type simple</span><span class="sxs-lookup"><span data-stu-id="24da5-125">80xx - simple type</span></span>
-   <span data-ttu-id="24da5-126">autre décalage relatif</span><span class="sxs-lookup"><span data-stu-id="24da5-126">other - relative offset</span></span>

## <a name="encapsulated-unions"></a><span data-ttu-id="24da5-127">Unions encapsulées</span><span class="sxs-lookup"><span data-stu-id="24da5-127">Encapsulated Unions</span></span>

<span data-ttu-id="24da5-128">Une Union encapsulée provient d’une syntaxe d’Union spéciale dans IDL.</span><span class="sxs-lookup"><span data-stu-id="24da5-128">An encapsulated union comes from a special union syntax in IDL.</span></span> <span data-ttu-id="24da5-129">En effet, une Union encapsulée est une structure de regroupement avec un champ discriminante au début de la structure et l’Union comme seul autre membre.</span><span class="sxs-lookup"><span data-stu-id="24da5-129">Effectively, an encapsulated union is a bundle structure with a discriminant field at the beginning of the structure and the union as the only other member.</span></span>

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

<span data-ttu-id="24da5-130">Le type de commutateur d’une Union encapsulée \_<1> champ a deux parties.</span><span class="sxs-lookup"><span data-stu-id="24da5-130">An encapsulated union's switch\_type<1> field has two parts.</span></span> <span data-ttu-id="24da5-131">Le Quartet inférieur fournit le type de commutateur réel, et le Quartet supérieur fournit l’incrément de mémoire pour effectuer un pas à pas principal, ce qui indique que le pointeur de la mémoire doit être incrémenté afin de ne pas dépasser le champ du commutateur \_ , ce qui inclut le remplissage entre le champ Switch \_ is () de la structure construite par stub et le champ Union réel.</span><span class="sxs-lookup"><span data-stu-id="24da5-131">The lower nibble provides the actual switch type, and the upper nibble provides the memory increment to step over that is an amount that the memory pointer must be incremented to skip past the switch\_is field, which includes any padding between the switch\_is() field of the stub-constructed structure and the actual union field.</span></span>

<span data-ttu-id="24da5-132">La \_ taille de la mémoire<2> champ est la taille de l’Union uniquement et est identique aux unions non encapsulées.</span><span class="sxs-lookup"><span data-stu-id="24da5-132">The memory\_size<2> field is the size of the union only, and is identical to nonencapsulated unions.</span></span> <span data-ttu-id="24da5-133">Pour obtenir la taille totale de la structure qui contient l’Union, ajoutez la taille de la mémoire \_<2> à l’incrément de mémoire pour effectuer un pas à pas principal, c’est-à-dire au Quartet supérieur du type de commutateur \_<1> champ, puis alignez par l’alignement correspondant à l’incrément.</span><span class="sxs-lookup"><span data-stu-id="24da5-133">To obtain the total size of the structure that contains the union, add memory\_size<2> to memory increment to step over, that is to the upper nibble of the switch\_type<1> field, then align by the alignment corresponding to the increment.</span></span>

## <a name="nonencapsulated-unions"></a><span data-ttu-id="24da5-134">Unions qui ne sont pas encapsulées</span><span class="sxs-lookup"><span data-stu-id="24da5-134">Nonencapsulated Unions</span></span>

<span data-ttu-id="24da5-135">Une Union non encapsulée est une situation classique dans laquelle une Union est un argument ou un champ et le commutateur est un autre argument ou champ, respectivement.</span><span class="sxs-lookup"><span data-stu-id="24da5-135">A nonencapsulated union is a typical situation where a union is one argument or field and the switch is another argument or field, respectively.</span></span>

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

<span data-ttu-id="24da5-136">Où :</span><span class="sxs-lookup"><span data-stu-id="24da5-136">Where:</span></span>

<span data-ttu-id="24da5-137">Le \_ type de commutateur<1> champ est un caractère de format pour le discriminante.</span><span class="sxs-lookup"><span data-stu-id="24da5-137">The switch\_type<1> field is a format character for the discriminant.</span></span>

<span data-ttu-id="24da5-138">Le commutateur \_ est un descripteur \_<> champ est un descripteur de corrélation et a 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="24da5-138">The switch\_is\_descriptor<> field is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="24da5-139">Toutefois, pour le commutateur \_ est la \_ Description<>, si l’Union est incorporée dans une structure, le champ de décalage du commutateur \_ est la \_ Description<> le décalage par \_ rapport au commutateur est le champ de la position de l’Union dans la structure (pas à partir du début de la structure).</span><span class="sxs-lookup"><span data-stu-id="24da5-139">However, for the switch\_is\_description<>, if the union is embedded in a structure, the offset field of the switch\_is\_description<> is the offset to the switch\_is field from the union's position in the structure (not from the beginning of the structure).</span></span>

<span data-ttu-id="24da5-140">La \_ Description offset to \_ size \_ and \_ ARM \_<2> champ donne le décalage à la description de la taille et du ARM de l’Union, ce qui est identique à celui des unions encapsulées et est partagé par toutes les unions non encapsulées du même type :</span><span class="sxs-lookup"><span data-stu-id="24da5-140">The offset\_to\_size\_and\_arm\_description<2> field gives the offset to the union's size and arm description, which is identical to that for encapsulated unions and is shared by all nonencapsulated unions of the same type :</span></span>

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 