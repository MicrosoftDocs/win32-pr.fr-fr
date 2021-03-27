---
title: Types scalaires
description: Types scalaires
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Types scalaires HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103761894"
---
# <a name="scalar-types"></a><span data-ttu-id="0bb8b-104">Types scalaires</span><span class="sxs-lookup"><span data-stu-id="0bb8b-104">Scalar Types</span></span>


<span data-ttu-id="0bb8b-105">Le langage HLSL prend en charge plusieurs types de données scalaires :</span><span class="sxs-lookup"><span data-stu-id="0bb8b-105">HLSL supports several scalar data types:</span></span>

-   <span data-ttu-id="0bb8b-106">**bool** -true ou false.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-106">**bool** - true or false.</span></span>
-   <span data-ttu-id="0bb8b-107">entier signé **int** -32 bits.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-107">**int** - 32-bit signed integer.</span></span>
-   <span data-ttu-id="0bb8b-108">**uint** -entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-108">**uint** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="0bb8b-109">entier non signé **dword** 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-109">**dword** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="0bb8b-110">valeur à virgule flottante **demi** -16 bits.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-110">**half** - 16-bit floating point value.</span></span> <span data-ttu-id="0bb8b-111">Ce type de données est fourni uniquement pour la compatibilité de langage.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-111">This data type is provided only for language compatibility.</span></span> <span data-ttu-id="0bb8b-112">Les cibles de nuanceur Direct3D 10 mappent tous les deux types de données aux types de données float.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-112">Direct3D 10 shader targets map all half data types to float data types.</span></span> <span data-ttu-id="0bb8b-113">Un type demi-données ne peut pas être utilisé sur une variable globale uniforme (utilisez l’indicateur/GEC si cette fonctionnalité est souhaitée).</span><span class="sxs-lookup"><span data-stu-id="0bb8b-113">A half data type cannot be used on a uniform global variable (use the /Gec flag if this functionality is desired).</span></span>
-   <span data-ttu-id="0bb8b-114">valeur à virgule flottante 32 bits **float** .</span><span class="sxs-lookup"><span data-stu-id="0bb8b-114">**float** - 32-bit floating point value.</span></span>
-   <span data-ttu-id="0bb8b-115">valeur à virgule flottante **double** 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-115">**double** - 64-bit floating point value.</span></span> <span data-ttu-id="0bb8b-116">Vous ne pouvez pas utiliser des valeurs à double précision comme entrées et sorties pour un flux.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-116">You cannot use double precision values as inputs and outputs for a stream.</span></span> <span data-ttu-id="0bb8b-117">Pour passer des valeurs à double précision entre les nuanceurs, déclarez chaque **double** comme une paire de types de données **uint** .</span><span class="sxs-lookup"><span data-stu-id="0bb8b-117">To pass double precision values between shaders, declare each **double** as a pair of **uint** data types.</span></span> <span data-ttu-id="0bb8b-118">Utilisez ensuite la fonction [**asuint**](asuint.md) pour compresser chaque **double** dans la paire **uint** s et la fonction [**AsDouble**](asdouble.md) pour décompresser la paire de **uint** s dans le **double**.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-118">Then, use the [**asuint**](asuint.md) function to pack each **double** into the pair of **uint** s and the [**asdouble**](asdouble.md) function to unpack the pair of **uint** s back into the **double**.</span></span>

<span data-ttu-id="0bb8b-119">À compter de Windows 8 HLSL, il prend également en charge les types de données scalaires de précision minimale.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-119">Starting with Windows 8 HLSL also supports minimum precision scalar data types.</span></span> <span data-ttu-id="0bb8b-120">Les pilotes graphiques peuvent implémenter des types de données scalaires de précision minimale à l’aide d’une précision supérieure ou égale à la précision de bit spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-120">Graphics drivers can implement minimum precision scalar data types by using any precision greater than or equal to their specified bit precision.</span></span> <span data-ttu-id="0bb8b-121">Nous vous recommandons de ne pas compter sur le comportement de verrouillage ou d’habillage qui dépend de la précision sous-jacente spécifique.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-121">We recommend not to rely on clamping or wrapping behavior that depends on specific underlying precision.</span></span> <span data-ttu-id="0bb8b-122">Par exemple, le pilote Graphics peut exécuter une opération arithmétique sur une valeur **min16float** à la précision 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-122">For example, the graphics driver might execute arithmetic on a **min16float** value at full 32-bit precision.</span></span>

-   <span data-ttu-id="0bb8b-123">**min16float** -valeur à virgule flottante 16 bits minimale.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-123">**min16float** - minimum 16-bit floating point value.</span></span>
-   <span data-ttu-id="0bb8b-124">**min10float** -valeur à virgule flottante 10 bits minimale.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-124">**min10float** - minimum 10-bit floating point value.</span></span>
-   <span data-ttu-id="0bb8b-125">**min16int** -entier signé 16 bits minimal.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-125">**min16int** - minimum 16-bit signed integer.</span></span>
-   <span data-ttu-id="0bb8b-126">**min12int** -entier signé 12 bits minimum.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-126">**min12int** - minimum 12-bit signed integer.</span></span>
-   <span data-ttu-id="0bb8b-127">**min16uint** -entier non signé 16 bits minimal.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-127">**min16uint** - minimum 16-bit unsigned integer.</span></span>

<span data-ttu-id="0bb8b-128">Pour plus d’informations sur les littéraux scalaires, consultez [grammaire](dx-graphics-hlsl-appendix-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="0bb8b-128">For more information about scalar literals, see [Grammar](dx-graphics-hlsl-appendix-grammar.md).</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bb8b-129">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="0bb8b-129">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="0bb8b-130">Dans Direct3D 10, les types suivants sont des modificateurs du type float.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-130">In Direct3D 10, the following types are modifiers to the float type.</span></span><br/>
<ul>
<li><span data-ttu-id="0bb8b-131"><strong>monoronfler</strong> - Signée IEEE 32 bits-valeur float normalisée dans la plage comprise entre-1 et 1.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-131"><strong>snorm float</strong> - IEEE 32-bit signed-normalized float in range -1 to 1 inclusive.</span></span></li>
<li><span data-ttu-id="0bb8b-132"><strong>unorm float</strong> - Unsigned-bit non signé IEEE 32 dans la plage comprise entre 0 et 1 inclus.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-132"><strong>unorm float</strong> - IEEE 32-bit unsigned-normalized float in range 0 to 1 inclusive.</span></span></li>
</ul>
<span data-ttu-id="0bb8b-133">Par exemple, voici une déclaration de variable float-normalized-normalized à 4 composants.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-133">For example, here is a 4-component signed-normalized float-variable declaration.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a><span data-ttu-id="0bb8b-134">Type de chaîne</span><span class="sxs-lookup"><span data-stu-id="0bb8b-134">String Type</span></span>

<span data-ttu-id="0bb8b-135">Le langage HLSL prend également en charge un type **chaîne** , qui est une chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-135">HLSL also supports a **string** type, which is an ASCII string.</span></span> <span data-ttu-id="0bb8b-136">Il n’y a pas d’opérations ou d’États acceptant des chaînes, mais les effets peuvent interroger des paramètres de chaîne et des annotations.</span><span class="sxs-lookup"><span data-stu-id="0bb8b-136">There are no operations or states that accept strings, but effects can query string parameters and annotations.</span></span>

## <a name="example"></a><span data-ttu-id="0bb8b-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="0bb8b-137">Example</span></span>

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a><span data-ttu-id="0bb8b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bb8b-138">See also</span></span>



* [<span data-ttu-id="0bb8b-139">Déclaration de types scalaires</span><span class="sxs-lookup"><span data-stu-id="0bb8b-139">Declaring Scalar Types</span></span>](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [<span data-ttu-id="0bb8b-140">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bb8b-140">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)