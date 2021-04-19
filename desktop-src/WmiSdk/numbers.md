---
description: Dans MOF, les nombres sont des chiffres qui décrivent des valeurs numériques. MOF fournit un large éventail de types de données qui se traduisent par l’automatisation, et permet également à ces nombres d’être dans différents formats. Le tableau suivant répertorie les valeurs numériques prises en charge par MOF.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Nombres (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517219"
---
# <a name="numbers-wmi"></a><span data-ttu-id="a348b-105">Nombres (WMI)</span><span class="sxs-lookup"><span data-stu-id="a348b-105">Numbers (WMI)</span></span>

<span data-ttu-id="a348b-106">Dans MOF, les nombres sont des chiffres qui décrivent des valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="a348b-106">In MOF, numbers are digits that describe numerical values.</span></span> <span data-ttu-id="a348b-107">MOF fournit un large éventail de types de données qui se traduisent par l’automatisation, et permet également à ces nombres d’être dans différents formats.</span><span class="sxs-lookup"><span data-stu-id="a348b-107">MOF provides a variety of data types that translate into Automation, and also allows those numbers to be in different formats.</span></span> <span data-ttu-id="a348b-108">Le tableau suivant répertorie les valeurs numériques prises en charge par MOF.</span><span class="sxs-lookup"><span data-stu-id="a348b-108">The following table lists the numeric values that MOF supports.</span></span>



| <span data-ttu-id="a348b-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="a348b-109">Data type</span></span>  | <span data-ttu-id="a348b-110">Type Automation</span><span class="sxs-lookup"><span data-stu-id="a348b-110">Automation type</span></span> | <span data-ttu-id="a348b-111">Description</span><span class="sxs-lookup"><span data-stu-id="a348b-111">Description</span></span>                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a348b-112">**sint8**</span><span class="sxs-lookup"><span data-stu-id="a348b-112">**sint8**</span></span>  | <span data-ttu-id="a348b-113">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="a348b-113">**VT\_I2**</span></span>      | <span data-ttu-id="a348b-114">Entier 8 bits signé.</span><span class="sxs-lookup"><span data-stu-id="a348b-114">Signed 8-bit integer.</span></span><br/>                                                                                                                                        |
| <span data-ttu-id="a348b-115">**sint16**</span><span class="sxs-lookup"><span data-stu-id="a348b-115">**sint16**</span></span> | <span data-ttu-id="a348b-116">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="a348b-116">**VT\_I2**</span></span>      | <span data-ttu-id="a348b-117">Entier 16 bits signé.</span><span class="sxs-lookup"><span data-stu-id="a348b-117">Signed 16-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="a348b-118">**sint32**</span><span class="sxs-lookup"><span data-stu-id="a348b-118">**sint32**</span></span> | <span data-ttu-id="a348b-119">VT \_</span><span class="sxs-lookup"><span data-stu-id="a348b-119">VT\_I4</span></span>          | <span data-ttu-id="a348b-120">Entier 32 bits signé.</span><span class="sxs-lookup"><span data-stu-id="a348b-120">Signed 32-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="a348b-121">**sint64**</span><span class="sxs-lookup"><span data-stu-id="a348b-121">**sint64**</span></span> | <span data-ttu-id="a348b-122">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a348b-122">**VT\_BSTR**</span></span>    | <span data-ttu-id="a348b-123">Entier 64 bits signé sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a348b-123">Signed 64-bit integer in string form.</span></span> <span data-ttu-id="a348b-124">Ce type suit le format hexadécimal ou décimal en fonction des règles C du American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a348b-124">This type follows hexadecimal or decimal format according to the American National Standards Institute (ANSI) C rules.</span></span><br/> |
| <span data-ttu-id="a348b-125">**real32**</span><span class="sxs-lookup"><span data-stu-id="a348b-125">**real32**</span></span> | <span data-ttu-id="a348b-126">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="a348b-126">**VT\_R4**</span></span>      | <span data-ttu-id="a348b-127">valeur à virgule flottante de 4 octets qui suit la norme IEEE (Institute of Electrical and Electronics Engineers, Inc.).</span><span class="sxs-lookup"><span data-stu-id="a348b-127">4-byte floating-point value that follows the Institute of Electrical and Electronics Engineers, Inc. (IEEE) standard.</span></span><br/>                                        |
| <span data-ttu-id="a348b-128">**real64**</span><span class="sxs-lookup"><span data-stu-id="a348b-128">**real64**</span></span> | <span data-ttu-id="a348b-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="a348b-129">**VT\_R8**</span></span>      | <span data-ttu-id="a348b-130">valeur à virgule flottante de 8 octets qui suit la norme IEEE.</span><span class="sxs-lookup"><span data-stu-id="a348b-130">8-byte floating-point value that follows the IEEE standard.</span></span><br/>                                                                                                  |
| <span data-ttu-id="a348b-131">**destinées**</span><span class="sxs-lookup"><span data-stu-id="a348b-131">**uint8**</span></span>  | <span data-ttu-id="a348b-132">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="a348b-132">**VT\_UI1**</span></span>     | <span data-ttu-id="a348b-133">Entier 8 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="a348b-133">Unsigned 8-bit integer.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a348b-134">**UInt16**</span><span class="sxs-lookup"><span data-stu-id="a348b-134">**uint16**</span></span> | <span data-ttu-id="a348b-135">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="a348b-135">**VT\_I4**</span></span>      | <span data-ttu-id="a348b-136">Entier 16 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="a348b-136">Unsigned 16-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="a348b-137">**uint32**</span><span class="sxs-lookup"><span data-stu-id="a348b-137">**uint32**</span></span> | <span data-ttu-id="a348b-138">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="a348b-138">**VT\_I4**</span></span>      | <span data-ttu-id="a348b-139">Entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a348b-139">Unsigned 32-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="a348b-140">**uint64**</span><span class="sxs-lookup"><span data-stu-id="a348b-140">**uint64**</span></span> | <span data-ttu-id="a348b-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a348b-141">**VT\_BSTR**</span></span>    | <span data-ttu-id="a348b-142">Entier 64 bits non signé sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a348b-142">Unsigned 64-bit integer in string form.</span></span> <span data-ttu-id="a348b-143">Ce type suit le format hexadécimal ou décimal conformément aux règles C ANSI.</span><span class="sxs-lookup"><span data-stu-id="a348b-143">This type follows hexadecimal or decimal format according to ANSI C rules.</span></span><br/>                                           |



 

<span data-ttu-id="a348b-144">Bien que flexible, le code MOF rencontre des modifications lors du traitement de l’automatisation :</span><span class="sxs-lookup"><span data-stu-id="a348b-144">Although flexible, MOF code does encounter some changes when dealing with Automation:</span></span>

-   <span data-ttu-id="a348b-145">Vous devez encoder des entiers 64 bits sous forme de chaînes.</span><span class="sxs-lookup"><span data-stu-id="a348b-145">You must encode 64-bit integers as strings.</span></span>

    <span data-ttu-id="a348b-146">Automation ne prend pas en charge un type intégral 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a348b-146">Automation does not support a 64-bit integral type.</span></span>

-   <span data-ttu-id="a348b-147">Les types Automation ne correspondent pas toujours aux types de données MOF en taille binaire.</span><span class="sxs-lookup"><span data-stu-id="a348b-147">Automation types do not always correspond in bit size to MOF data types.</span></span>

    <span data-ttu-id="a348b-148">Par exemple, Automation utilise VT \_ I4 pour retourner une valeur non signée de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a348b-148">For example, Automation uses VT\_I4 to return an unsigned 16-bit value.</span></span> <span data-ttu-id="a348b-149">Cette différence existe en raison de problèmes d’extension de signature.</span><span class="sxs-lookup"><span data-stu-id="a348b-149">This discrepancy exists because of sign-extension problems.</span></span> <span data-ttu-id="a348b-150">Si Automation a utilisé VT \_ I2 au lieu de VT \_ I4, 65 536 serait la valeur 1, provoquant des problèmes de type et de plage.</span><span class="sxs-lookup"><span data-stu-id="a348b-150">If Automation used VT\_I2 instead of VT\_I4, 65,536 would appear to be the value  1, causing type and range problems.</span></span> <span data-ttu-id="a348b-151">De même, Automation représente le type **UInt32** en tant que VT \_ i4, car il n’existe pas de type entier plus grand pour contenir **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="a348b-151">Similarly, Automation represents the **uint32** type as VT\_I4 because there exists no larger integer type to contain **uint32**.</span></span>

-   <span data-ttu-id="a348b-152">Vous n’avez pas besoin de modifier une représentation pour les types de chiffres 8 bits.</span><span class="sxs-lookup"><span data-stu-id="a348b-152">You do not need to change any representation for 8-bit numeral types.</span></span>

    <span data-ttu-id="a348b-153">Automation prend en charge VT \_ UI1, un type non signé de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="a348b-153">Automation supports VT\_UI1, an unsigned 8-bit type.</span></span>

<span data-ttu-id="a348b-154">MOF prend en charge les constantes longues.</span><span class="sxs-lookup"><span data-stu-id="a348b-154">MOF supports long constants.</span></span> <span data-ttu-id="a348b-155">Vous déclarez une constante longue à l’aide d’une simple série de chiffres avec un signe négatif facultatif.</span><span class="sxs-lookup"><span data-stu-id="a348b-155">You declare a long constant using a simple series of digits with an optional negative sign.</span></span> <span data-ttu-id="a348b-156">Une constante longue ne peut pas dépasser la taille de la variable déclarée pour la conserver.</span><span class="sxs-lookup"><span data-stu-id="a348b-156">A long constant cannot exceed the size of the variable that is declared to hold it.</span></span> <span data-ttu-id="a348b-157">1000 et 12310 sont des exemples de constantes longues.</span><span class="sxs-lookup"><span data-stu-id="a348b-157">Some examples of long constants are 1000 and  12310.</span></span>

<span data-ttu-id="a348b-158">MOF prend également en charge d’autres formats numériques.</span><span class="sxs-lookup"><span data-stu-id="a348b-158">MOF also supports alternate numerical formats.</span></span> <span data-ttu-id="a348b-159">Le tableau suivant répertorie les caractères spéciaux que vous devez utiliser pour décrire les constantes hexadécimales, binaires et octales.</span><span class="sxs-lookup"><span data-stu-id="a348b-159">The following table lists the special characters you must use to describe hexadecimal, binary, and octal constants.</span></span>



| <span data-ttu-id="a348b-160">Constante</span><span class="sxs-lookup"><span data-stu-id="a348b-160">Constant</span></span>               | <span data-ttu-id="a348b-161">Caractère spécial</span><span class="sxs-lookup"><span data-stu-id="a348b-161">Special character</span></span>     | <span data-ttu-id="a348b-162">Exemple</span><span class="sxs-lookup"><span data-stu-id="a348b-162">Example</span></span>                   |
|------------------------|-----------------------|---------------------------|
| <span data-ttu-id="a348b-163">Decimal</span><span class="sxs-lookup"><span data-stu-id="a348b-163">Decimal</span></span><br/>     | <span data-ttu-id="a348b-164">Aucun</span><span class="sxs-lookup"><span data-stu-id="a348b-164">None</span></span><br/>       | <span data-ttu-id="a348b-165">Val = 65</span><span class="sxs-lookup"><span data-stu-id="a348b-165">val = 65</span></span><br/>       |
| <span data-ttu-id="a348b-166">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="a348b-166">Hexadecimal</span></span><br/> | <span data-ttu-id="a348b-167">préfixe 0x</span><span class="sxs-lookup"><span data-stu-id="a348b-167">0x prefix</span></span><br/>  | <span data-ttu-id="a348b-168">Val = 0x41 vers</span><span class="sxs-lookup"><span data-stu-id="a348b-168">val = 0x41</span></span><br/>     |
| <span data-ttu-id="a348b-169">Octal</span><span class="sxs-lookup"><span data-stu-id="a348b-169">Octal</span></span><br/>       | <span data-ttu-id="a348b-170">0 de début</span><span class="sxs-lookup"><span data-stu-id="a348b-170">Leading 0</span></span><br/>  | <span data-ttu-id="a348b-171">Val = 0101</span><span class="sxs-lookup"><span data-stu-id="a348b-171">val = 0101</span></span><br/>     |
| <span data-ttu-id="a348b-172">Binary</span><span class="sxs-lookup"><span data-stu-id="a348b-172">Binary</span></span><br/>      | <span data-ttu-id="a348b-173">Fin B</span><span class="sxs-lookup"><span data-stu-id="a348b-173">Trailing B</span></span><br/> | <span data-ttu-id="a348b-174">Val = 1000001B</span><span class="sxs-lookup"><span data-stu-id="a348b-174">val = 1000001B</span></span><br/> |



 

<span data-ttu-id="a348b-175">Vous pouvez utiliser une constante à virgule flottante pour représenter une notation scientifique et des fractions, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a348b-175">You can use a floating-point constant to represent scientific notation as well as fractions, as shown next:</span></span>

``` syntax
3.14
-3.14
-1.2778E+02
```

<span data-ttu-id="a348b-176">WMI considère les constantes à virgule flottante comme des types **VT \_ R8** pour l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="a348b-176">WMI considers floating-point constants as **VT\_R8** types for Automation.</span></span>

<span data-ttu-id="a348b-177">L’exemple suivant décrit les déclarations de classes et d’instances qui illustrent l’utilisation de chacun des types de données numériques pour définir des propriétés :</span><span class="sxs-lookup"><span data-stu-id="a348b-177">The following example describes class and instance declarations that illustrate how to use each of the numeric data types to set properties:</span></span>

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




