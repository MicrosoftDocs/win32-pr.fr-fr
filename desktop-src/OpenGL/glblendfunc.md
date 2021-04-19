---
title: fonction glBlendFunc (GL. h)
description: La fonction glBlendFunc spécifie des opérations arithmétiques sur les pixels.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glBlendFunc fonction OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510972"
---
# <a name="glblendfunc-function"></a><span data-ttu-id="65943-104">glBlendFunc fonction)</span><span class="sxs-lookup"><span data-stu-id="65943-104">glBlendFunc function</span></span>

<span data-ttu-id="65943-105">La fonction **glBlendFunc** spécifie des opérations arithmétiques sur les pixels.</span><span class="sxs-lookup"><span data-stu-id="65943-105">The **glBlendFunc** function specifies pixel arithmetic.</span></span>

## <a name="syntax"></a><span data-ttu-id="65943-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65943-106">Syntax</span></span>


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a><span data-ttu-id="65943-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65943-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65943-108">*sfactor*</span><span class="sxs-lookup"><span data-stu-id="65943-108">*sfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="65943-109">Spécifie la manière dont les facteurs de fusion de source rouge, vert, bleu et alpha sont calculés.</span><span class="sxs-lookup"><span data-stu-id="65943-109">Specifies how the red, green, blue, and alpha source-blending factors are computed.</span></span> <span data-ttu-id="65943-110">Neuf constantes symboliques sont acceptées : \_ zéro GL, GL \_ un, \_ couleur de l’heure d’été GL \_ , GL \_ un moins de couleur de l' \_ heure d' \_ été \_ , GL \_ src \_ alpha, GL \_ One \_ moins \_ src \_ alpha, GL \_ DST \_ alpha, GL \_ un moins d’heure d’été alpha \_ \_ \_ et GL \_ src \_ alpha \_ saturé.</span><span class="sxs-lookup"><span data-stu-id="65943-110">Nine symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_DST\_COLOR, GL\_ONE\_MINUS\_DST\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, GL\_ONE\_MINUS\_DST\_ALPHA, and GL\_SRC\_ALPHA\_SATURATE.</span></span>

</dd> <dt>

<span data-ttu-id="65943-111">*dfactor*</span><span class="sxs-lookup"><span data-stu-id="65943-111">*dfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="65943-112">Spécifie la manière dont les facteurs de fusion de destination rouge, vert, bleu et alpha sont calculés.</span><span class="sxs-lookup"><span data-stu-id="65943-112">Specifies how the red, green, blue, and alpha destination-blending factors are computed.</span></span> <span data-ttu-id="65943-113">Huit constantes symboliques sont acceptées : \_ zéro GL, GL \_ un, \_ couleur de la source GL \_ , GL \_ un \_ moins \_ \_ couleur SRC, GL \_ src \_ alpha, GL \_ un \_ moins \_ src \_ alpha, GL \_ DST \_ alpha et GL \_ 1 \_ moins \_ DST \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="65943-113">Eight symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_SRC\_COLOR, GL\_ONE\_MINUS\_SRC\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, and GL\_ONE\_MINUS\_DST\_ALPHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65943-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65943-114">Return value</span></span>

<span data-ttu-id="65943-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="65943-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65943-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="65943-116">Error codes</span></span>

<span data-ttu-id="65943-117">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="65943-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="65943-118">Nom</span><span class="sxs-lookup"><span data-stu-id="65943-118">Name</span></span>                                                                                                  | <span data-ttu-id="65943-119">Signification</span><span class="sxs-lookup"><span data-stu-id="65943-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="65943-120"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="65943-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="65943-121">*Sfactor* ou *dfactor* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="65943-121">Either *sfactor* or *dfactor* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="65943-122"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="65943-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="65943-123">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="65943-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="65943-124">Notes</span><span class="sxs-lookup"><span data-stu-id="65943-124">Remarks</span></span>

<span data-ttu-id="65943-125">En mode RVB, les pixels peuvent être dessinés à l’aide d’une fonction qui fusionne les valeurs RVBA entrantes (source) avec les valeurs RVBA qui se trouvent déjà dans le trame (valeurs de destination).</span><span class="sxs-lookup"><span data-stu-id="65943-125">In RGB mode, pixels can be drawn using a function that blends the incoming (source) RGBA values with the RGBA values that are already in the framebuffer (the destination values).</span></span> <span data-ttu-id="65943-126">Par défaut, la fusion est désactivée.</span><span class="sxs-lookup"><span data-stu-id="65943-126">By default, blending is disabled.</span></span> <span data-ttu-id="65943-127">Utilisez [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l' \_ argument GL Blend pour activer et désactiver la fusion.</span><span class="sxs-lookup"><span data-stu-id="65943-127">Use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the GL\_BLEND argument to enable and disable blending.</span></span>

<span data-ttu-id="65943-128">Quand cette option est activée, **glBlendFunc** définit l’opération de fusion.</span><span class="sxs-lookup"><span data-stu-id="65943-128">When enabled, **glBlendFunc** defines the operation of blending.</span></span> <span data-ttu-id="65943-129">Le paramètre *sfactor* spécifie laquelle des neuf méthodes est utilisée pour mettre à l’échelle les composants de couleur source.</span><span class="sxs-lookup"><span data-stu-id="65943-129">The *sfactor* parameter specifies which of nine methods is used to scale the source color components.</span></span> <span data-ttu-id="65943-130">Le paramètre *dfactor* spécifie laquelle des huit méthodes est utilisée pour mettre à l’échelle les composants de couleur de destination.</span><span class="sxs-lookup"><span data-stu-id="65943-130">The *dfactor* parameter specifies which of eight methods is used to scale the destination color components.</span></span> <span data-ttu-id="65943-131">Les onze méthodes possibles sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="65943-131">The eleven possible methods are described in the following table.</span></span> <span data-ttu-id="65943-132">Chaque méthode définit quatre facteurs de mise à l’échelle chacun pour les couleurs rouge, vert, bleu et alpha.</span><span class="sxs-lookup"><span data-stu-id="65943-132">Each method defines four scale factors one each for red, green, blue, and alpha.</span></span>

<span data-ttu-id="65943-133">Dans le tableau et dans les équations suivantes, les composants de couleur source et de destination sont appelés (*R*?</span><span class="sxs-lookup"><span data-stu-id="65943-133">In the table and in subsequent equations, source and destination color components are referred to as (*R*?</span></span> <span data-ttu-id="65943-134">, *G*?</span><span class="sxs-lookup"><span data-stu-id="65943-134">, *G*?</span></span> <span data-ttu-id="65943-135">, *B*?</span><span class="sxs-lookup"><span data-stu-id="65943-135">, *B*?</span></span> <span data-ttu-id="65943-136">, *Un*?</span><span class="sxs-lookup"><span data-stu-id="65943-136">, *A*?</span></span> <span data-ttu-id="65943-137">) et (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span><span class="sxs-lookup"><span data-stu-id="65943-137">) and (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span></span> <span data-ttu-id="65943-138">Elles sont comprises comme ayant des valeurs entières comprises entre zéro et (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), où</span><span class="sxs-lookup"><span data-stu-id="65943-138">They are understood to have integer values between zero and (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), where</span></span>

<span data-ttu-id="65943-139">*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1</span><span class="sxs-lookup"><span data-stu-id="65943-139">*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1</span></span>

<span data-ttu-id="65943-140">*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1</span><span class="sxs-lookup"><span data-stu-id="65943-140">*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1</span></span>

<span data-ttu-id="65943-141">*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1</span><span class="sxs-lookup"><span data-stu-id="65943-141">*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1</span></span>

<span data-ttu-id="65943-142">*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1</span><span class="sxs-lookup"><span data-stu-id="65943-142">*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1</span></span>

<span data-ttu-id="65943-143">et (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>a</sub> ) est le nombre de bitplanes rouge, vert, bleu et alpha.</span><span class="sxs-lookup"><span data-stu-id="65943-143">and (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) is the number of red, green, blue, and alpha bitplanes.</span></span>

<span data-ttu-id="65943-144">Les facteurs de mise à l’échelle source et de destination sont appelés (*s*<sub>r</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>a</sub> ) et (*d*<sub>r</sub> , *d*<sub>g</sub> , *d*<sub>b</sub> , *d*<sub>a</sub> ).</span><span class="sxs-lookup"><span data-stu-id="65943-144">Source and destination scale factors are referred to as (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) and (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ).</span></span> <span data-ttu-id="65943-145">Les facteurs d’échelle décrits dans le tableau, dénotés (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), représentent les facteurs source ou de destination.</span><span class="sxs-lookup"><span data-stu-id="65943-145">The scale factors described in the table, denoted (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), represent either source or destination factors.</span></span> <span data-ttu-id="65943-146">Tous les facteurs de mise à l’échelle sont compris entre \[ 0 et 1 \] .</span><span class="sxs-lookup"><span data-stu-id="65943-146">All scale factors have range \[0,1\].</span></span>



| <span data-ttu-id="65943-147">Paramètre</span><span class="sxs-lookup"><span data-stu-id="65943-147">Parameter</span></span>                  | <span data-ttu-id="65943-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span><span class="sxs-lookup"><span data-stu-id="65943-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span></span>                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65943-149">\_zéro GL</span><span class="sxs-lookup"><span data-stu-id="65943-149">GL\_ZERO</span></span>                   | <span data-ttu-id="65943-150">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="65943-150">(0,0,0,0)</span></span>                                                                                                                                                    |
| <span data-ttu-id="65943-151">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="65943-151">GL\_ONE</span></span>                    | <span data-ttu-id="65943-152">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="65943-152">(1,1,1,1)</span></span>                                                                                                                                                    |
| <span data-ttu-id="65943-153">couleur de la source du GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="65943-153">GL\_SRC\_COLOR</span></span>             | <span data-ttu-id="65943-154">(*R*?</span><span class="sxs-lookup"><span data-stu-id="65943-154">(*R*?</span></span><span data-ttu-id="65943-155"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="65943-155"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="65943-156"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="65943-156"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="65943-157"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="65943-157"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="65943-158"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-158"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="65943-159">GL \_ un \_ moins \_ \_ couleur SRC</span><span class="sxs-lookup"><span data-stu-id="65943-159">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="65943-160">(1, 1, 1, 1)-(*R*?</span><span class="sxs-lookup"><span data-stu-id="65943-160">(1,1,1,1) - (*R*?</span></span><span data-ttu-id="65943-161"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="65943-161"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="65943-162"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="65943-162"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="65943-163"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="65943-163"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="65943-164"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-164"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="65943-165">couleur de l' \_ heure d’été GL \_</span><span class="sxs-lookup"><span data-stu-id="65943-165">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="65943-166">(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub></sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-166">(*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="65943-167">\_couleur GL 1 \_ moins \_ DST \_</span><span class="sxs-lookup"><span data-stu-id="65943-167">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="65943-168">(1, 1, 1, 1)-(*r*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-168">(1,1,1,1) - (*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="65943-169">source de la \_ source GL \_</span><span class="sxs-lookup"><span data-stu-id="65943-169">GL\_SRC\_ALPHA</span></span>             | <span data-ttu-id="65943-170">(*Un*?</span><span class="sxs-lookup"><span data-stu-id="65943-170">(*A*?</span></span><span data-ttu-id="65943-171"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="65943-171"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="65943-172"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="65943-172"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="65943-173"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="65943-173"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="65943-174"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-174"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="65943-175">GL \_ un \_ moins de \_ src \_ alpha</span><span class="sxs-lookup"><span data-stu-id="65943-175">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> | <span data-ttu-id="65943-176">(1, 1, 1, 1)-(*A*?</span><span class="sxs-lookup"><span data-stu-id="65943-176">(1,1,1,1) - (*A*?</span></span><span data-ttu-id="65943-177"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="65943-177"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="65943-178"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="65943-178"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="65943-179"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="65943-179"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="65943-180"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-180"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="65943-181">de l' \_ heure d’été alpha du GL \_</span><span class="sxs-lookup"><span data-stu-id="65943-181">GL\_DST\_ALPHA</span></span>             | <span data-ttu-id="65943-182">(*A*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub></sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub></sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-182">(*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="65943-183">GL \_ 1 \_ moins \_ heure d’été \_ alpha</span><span class="sxs-lookup"><span data-stu-id="65943-183">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> | <span data-ttu-id="65943-184">(1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub></sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>k  /  <sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-184">(1,1,1,1) - (*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="65943-185">\_ \_ saturation alpha de la source GL \_</span><span class="sxs-lookup"><span data-stu-id="65943-185">GL\_SRC\_ALPHA\_SATURATE</span></span>   | <span data-ttu-id="65943-186">(i, i,*i,* 1)</span><span class="sxs-lookup"><span data-stu-id="65943-186">(*i,i,i,* 1)</span></span>                                                                                                                                                 |



 

<span data-ttu-id="65943-187">Dans le tableau,</span><span class="sxs-lookup"><span data-stu-id="65943-187">In the table,</span></span>

<span data-ttu-id="65943-188">*i* = min (*A*?</span><span class="sxs-lookup"><span data-stu-id="65943-188">*i* = min (*A*?</span></span> <span data-ttu-id="65943-189">, *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="65943-189">, *k*<sub>A</sub>  - *A*<sub>d</sub> ) / *k*<sub>A</sub></span></span>

<span data-ttu-id="65943-190">Pour déterminer les valeurs RVBA lissées d’un pixel lors du dessin en mode RVBA, le système utilise les équations suivantes :</span><span class="sxs-lookup"><span data-stu-id="65943-190">To determine the blended RGBA values of a pixel when drawing in RGBA mode, the system uses the following equations:</span></span>

<span data-ttu-id="65943-191">*R* (*d*) = min ( *k*<sub>r</sub> , *r*? *r r*<sub>r d</sub>  +  *r*<sub></sub> <sub></sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-191">*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub> + *R*<sub>d</sub> *d*<sub>R</sub> )</span></span>

<span data-ttu-id="65943-192">*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  *g d*<sub></sub> <sub>g</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-192">*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub> + *G*<sub>d</sub> *d*<sub>G</sub>  )</span></span>

<span data-ttu-id="65943-193">*B* (*d*) = min ( *k*<sub>b</sub> *, b*? *s*<sub>b</sub>  +  *b*<sub>d</sub> <sub>b</sub> )</span><span class="sxs-lookup"><span data-stu-id="65943-193">*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub> + *B*<sub>d</sub> *d*<sub>B</sub>  )</span></span>

<span data-ttu-id="65943-194">*A* (*d*) = min ( *k*<sub>a</sub> , *a*? *s*<sub>a a</sub>  +  <sub>d</sub> <sub></sub> a)</span><span class="sxs-lookup"><span data-stu-id="65943-194">*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub> + *A*<sub>d</sub> *d*<sub>A</sub>  )</span></span>

<span data-ttu-id="65943-195">En dépit de la précision apparente des équations ci-dessus, la fusion de l’arithmétique n’est pas exactement spécifiée, car la fusion opère avec des valeurs de couleur d’entier impréciss.</span><span class="sxs-lookup"><span data-stu-id="65943-195">Despite the apparent precision of the above equations, blending arithmetic is not exactly specified, because blending operates with imprecise integer color values.</span></span> <span data-ttu-id="65943-196">Toutefois, un facteur de fusion qui doit être égal à un est garanti ne pas modifier son multiplicande, et un facteur de fusion égal à zéro réduit ses multiplicande à zéro.</span><span class="sxs-lookup"><span data-stu-id="65943-196">However, a blend factor that should be equal to one is guaranteed not to modify its multiplicand, and a blend factor equal to zero reduces its multiplicand to zero.</span></span> <span data-ttu-id="65943-197">Ainsi, par exemple, quand *sfactor* est GL \_ src \_ alpha, *dfactor* est GL \_ un \_ moins \_ src \_ alpha et *a*? est égal à *k*<sub>a</sub>, les équations réduisent le remplacement simple :</span><span class="sxs-lookup"><span data-stu-id="65943-197">Thus, for example, when *sfactor* is GL\_SRC\_ALPHA, *dfactor* is GL\_ONE\_MINUS\_SRC\_ALPHA, and *A*? is equal to *k*<sub>A</sub>, the equations reduce to simple replacement:</span></span>

<span data-ttu-id="65943-198">*R*<sub>d</sub>  =  ?</span><span class="sxs-lookup"><span data-stu-id="65943-198">*R*<sub>d</sub> = *R*?</span></span>

<span data-ttu-id="65943-199">*G*<sub>d</sub>  =  *g*?</span><span class="sxs-lookup"><span data-stu-id="65943-199">*G*<sub>d</sub> = *G*?</span></span>

<span data-ttu-id="65943-200">B<sub>d</sub>  =  ?</span><span class="sxs-lookup"><span data-stu-id="65943-200">B <sub>d</sub> = *B*?</span></span>

<span data-ttu-id="65943-201">*A*<sub></sub>  =  ?</span><span class="sxs-lookup"><span data-stu-id="65943-201">*A*<sub>d</sub> = *A*?</span></span>

## <a name="examples"></a><span data-ttu-id="65943-202">Exemples</span><span class="sxs-lookup"><span data-stu-id="65943-202">Examples</span></span>

<span data-ttu-id="65943-203">La transparence est implémentée au mieux à l’aide de **glBlendFunc**(GL \_ src \_ alpha, GL \_ un \_ moins \_ src \_ alpha) avec des primitives triées du plus éloigné au plus proche.</span><span class="sxs-lookup"><span data-stu-id="65943-203">Transparency is best implemented using **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) with primitives sorted from farthest to nearest.</span></span> <span data-ttu-id="65943-204">Notez que ce calcul de transparence ne nécessite pas la présence d’alpha bitplanes dans le trame.</span><span class="sxs-lookup"><span data-stu-id="65943-204">Note that this transparency calculation does not require the presence of alpha bitplanes in the framebuffer.</span></span>

<span data-ttu-id="65943-205">Vous pouvez également utiliser **glBlendFunc**(GL \_ src \_ alpha, GL \_ One \_ moins \_ src \_ alpha) pour le rendu des points et des lignes antialiasés dans un ordre arbitraire.</span><span class="sxs-lookup"><span data-stu-id="65943-205">You can also use **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) for rendering antialiased points and lines in arbitrary order.</span></span>

<span data-ttu-id="65943-206">Pour optimiser l’anticrénelage des polygones, utilisez **glBlendFunc**(GL \_ src \_ alpha \_ saturé, GL \_ un) avec des polygones triés du plus proche au plus éloigné.</span><span class="sxs-lookup"><span data-stu-id="65943-206">To optimize polygon antialiasing, use **glBlendFunc**(GL\_SRC\_ALPHA\_SATURATE, GL\_ONE) with polygons sorted from nearest to farthest.</span></span> <span data-ttu-id="65943-207">(Voir la comptabilité \_ \_Argument Smooth polygonal dans [**glEnable**](glenable.md) pour plus d’informations sur l’anticrénelage polygonal.) Bitplanes alpha de destination, qui doit être présent pour que cette fonction Blend fonctionne correctement, stocke la couverture accumulée.</span><span class="sxs-lookup"><span data-stu-id="65943-207">(See the GL\_POLYGON\_SMOOTH argument in [**glEnable**](glenable.md) for information on polygon antialiasing.) Destination alpha bitplanes, which must be present for this blend function to operate correctly, store the accumulated coverage.</span></span>

<span data-ttu-id="65943-208">La valeur alpha entrante (source) est une opacité de matériau, comprise entre 1,0 (*K*<sub>a</sub> ), qui représente l’opacité complète, et 0,0 (0), représentant une transparence totale.</span><span class="sxs-lookup"><span data-stu-id="65943-208">Incoming (source) alpha is a material opacity, ranging from 1.0 (*K*<sub>A</sub> ), representing complete opacity, to 0.0 (0), representing complete transparency.</span></span>

<span data-ttu-id="65943-209">Lorsque vous activez plusieurs mémoires tampons de couleur pour le dessin, chaque mémoire tampon activée est fusionnée séparément et le contenu de la mémoire tampon est utilisé pour la couleur de destination.</span><span class="sxs-lookup"><span data-stu-id="65943-209">When you enable more than one color buffer for drawing, each enabled buffer is blended separately, and the contents of the buffer is used for destination color.</span></span> <span data-ttu-id="65943-210">(Voir [**glDrawBuffer**](gldrawbuffer.md).)</span><span class="sxs-lookup"><span data-stu-id="65943-210">(See [**glDrawBuffer**](gldrawbuffer.md).)</span></span>

<span data-ttu-id="65943-211">La fusion affecte uniquement le rendu RVBA.</span><span class="sxs-lookup"><span data-stu-id="65943-211">Blending affects only RGBA rendering.</span></span> <span data-ttu-id="65943-212">Elle est ignorée par les convertisseurs d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="65943-212">It is ignored by color-index renderers.</span></span>

<span data-ttu-id="65943-213">Les fonctions suivantes récupèrent les informations relatives à **glBlendFunc**:</span><span class="sxs-lookup"><span data-stu-id="65943-213">The following functions retrieve information related to **glBlendFunc**:</span></span>

<span data-ttu-id="65943-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Blend \_ src</span><span class="sxs-lookup"><span data-stu-id="65943-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_SRC</span></span>

<span data-ttu-id="65943-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Blend \_ DST</span><span class="sxs-lookup"><span data-stu-id="65943-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_DST</span></span>

<span data-ttu-id="65943-216">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Blend</span><span class="sxs-lookup"><span data-stu-id="65943-216">[**glIsEnabled**](glisenabled.md) with argument GL\_BLEND</span></span>

## <a name="requirements"></a><span data-ttu-id="65943-217">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65943-217">Requirements</span></span>



| <span data-ttu-id="65943-218">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65943-218">Requirement</span></span> | <span data-ttu-id="65943-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="65943-219">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65943-220">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65943-220">Minimum supported client</span></span><br/> | <span data-ttu-id="65943-221">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65943-221">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65943-222">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65943-222">Minimum supported server</span></span><br/> | <span data-ttu-id="65943-223">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65943-223">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65943-224">En-tête</span><span class="sxs-lookup"><span data-stu-id="65943-224">Header</span></span><br/>                   | <dl> <span data-ttu-id="65943-225"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="65943-225"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="65943-226">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65943-226">Library</span></span><br/>                  | <dl> <span data-ttu-id="65943-227"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65943-227"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="65943-228">DLL</span><span class="sxs-lookup"><span data-stu-id="65943-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65943-229"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65943-229"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65943-230">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65943-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65943-231">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="65943-231">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="65943-232">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="65943-232">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="65943-233">**glClear**</span><span class="sxs-lookup"><span data-stu-id="65943-233">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="65943-234">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="65943-234">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="65943-235">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="65943-235">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="65943-236">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="65943-236">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="65943-237">**glGet**</span><span class="sxs-lookup"><span data-stu-id="65943-237">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="65943-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="65943-238">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="65943-239">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="65943-239">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="65943-240">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="65943-240">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





