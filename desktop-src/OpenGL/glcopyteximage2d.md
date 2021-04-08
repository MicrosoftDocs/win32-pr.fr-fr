---
title: fonction glCopyTexImage2D (GL. h)
description: La fonction glCopyTexImage2D copie les pixels du trame dans une image de texture à deux dimensions.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- glCopyTexImage2D fonction OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843745"
---
# <a name="glcopyteximage2d-function"></a><span data-ttu-id="1a2b6-104">glCopyTexImage2D fonction)</span><span class="sxs-lookup"><span data-stu-id="1a2b6-104">glCopyTexImage2D function</span></span>

<span data-ttu-id="1a2b6-105">La fonction **glCopyTexImage2D** copie les pixels du trame dans une image de texture à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-105">The **glCopyTexImage2D** function copies pixels from the framebuffer into a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a2b6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a2b6-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="1a2b6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a2b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a2b6-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="1a2b6-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="1a2b6-109">Cible dans laquelle les données de l’image seront modifiées.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="1a2b6-110">Doit avoir la texture GL de valeur \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="1a2b6-111">*level*</span><span class="sxs-lookup"><span data-stu-id="1a2b6-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="1a2b6-112">Numéro de niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-112">The level-of-detail number.</span></span> <span data-ttu-id="1a2b6-113">Le niveau 0 est l’image de base.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-113">Level 0 is the base image.</span></span> <span data-ttu-id="1a2b6-114">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="1a2b6-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="1a2b6-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="1a2b6-116">Format interne et résolution des données de texture.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="1a2b6-117">Les valeurs 1, 2, 3 et 4 ne sont pas acceptées pour *internalFormat*.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-117">The values 1, 2, 3, and 4 are not accepted for *internalFormat*.</span></span> <span data-ttu-id="1a2b6-118">Le paramètre peut prendre l’une des valeurs symboliques suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-118">The parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="1a2b6-119">Constante</span><span class="sxs-lookup"><span data-stu-id="1a2b6-119">Constant</span></span>                 | <span data-ttu-id="1a2b6-120">Bits R</span><span class="sxs-lookup"><span data-stu-id="1a2b6-120">R Bits</span></span> | <span data-ttu-id="1a2b6-121">Bits G</span><span class="sxs-lookup"><span data-stu-id="1a2b6-121">G Bits</span></span> | <span data-ttu-id="1a2b6-122">Bits B</span><span class="sxs-lookup"><span data-stu-id="1a2b6-122">B Bits</span></span> | <span data-ttu-id="1a2b6-123">Un bits</span><span class="sxs-lookup"><span data-stu-id="1a2b6-123">A Bits</span></span> | <span data-ttu-id="1a2b6-124">L bits</span><span class="sxs-lookup"><span data-stu-id="1a2b6-124">L Bits</span></span> | <span data-ttu-id="1a2b6-125">I bits</span><span class="sxs-lookup"><span data-stu-id="1a2b6-125">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="1a2b6-126">GL \_ alpha</span><span class="sxs-lookup"><span data-stu-id="1a2b6-126">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="1a2b6-127">\_Alpha4 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-127">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="1a2b6-128">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-128">4</span></span>      |        |        |
| <span data-ttu-id="1a2b6-129">\_ALPHA8 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-129">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="1a2b6-130">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-130">8</span></span>      |        |        |
| <span data-ttu-id="1a2b6-131">\_ALPHA12 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-131">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="1a2b6-132">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-132">12</span></span>     |        |        |
| <span data-ttu-id="1a2b6-133">\_ALPHA16 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-133">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="1a2b6-134">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-134">16</span></span>     |        |        |
| <span data-ttu-id="1a2b6-135">LUMINANCE du GL \_</span><span class="sxs-lookup"><span data-stu-id="1a2b6-135">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="1a2b6-136">\_LUMINANCE4 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-136">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="1a2b6-137">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-137">4</span></span>      |        |
| <span data-ttu-id="1a2b6-138">\_LUMINANCE8 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-138">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="1a2b6-139">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-139">8</span></span>      |        |
| <span data-ttu-id="1a2b6-140">\_LUMINANCE12 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-140">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="1a2b6-141">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-141">12</span></span>     |        |
| <span data-ttu-id="1a2b6-142">\_LUMINANCE16 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-142">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="1a2b6-143">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-143">16</span></span>     |        |
| <span data-ttu-id="1a2b6-144">\_luminance \_ alpha du GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-144">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="1a2b6-145">GL \_ LUMINANCE4 \_ alpha4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-145">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="1a2b6-146">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-146">4</span></span>      | <span data-ttu-id="1a2b6-147">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-147">4</span></span>      |        |
| <span data-ttu-id="1a2b6-148">GL \_ LUMINANCE6 \_ alpha2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-148">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="1a2b6-149">2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-149">2</span></span>      | <span data-ttu-id="1a2b6-150">6</span><span class="sxs-lookup"><span data-stu-id="1a2b6-150">6</span></span>      |        |
| <span data-ttu-id="1a2b6-151">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-151">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="1a2b6-152">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-152">8</span></span>      | <span data-ttu-id="1a2b6-153">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-153">8</span></span>      |        |
| <span data-ttu-id="1a2b6-154">GL \_ LUMINANCE12 \_ alpha4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-154">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="1a2b6-155">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-155">4</span></span>      | <span data-ttu-id="1a2b6-156">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-156">12</span></span>     |        |
| <span data-ttu-id="1a2b6-157">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-157">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="1a2b6-158">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-158">12</span></span>     | <span data-ttu-id="1a2b6-159">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-159">12</span></span>     |        |
| <span data-ttu-id="1a2b6-160">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-160">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="1a2b6-161">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-161">16</span></span>     | <span data-ttu-id="1a2b6-162">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-162">16</span></span>     |        |
| <span data-ttu-id="1a2b6-163">intensité du GL \_</span><span class="sxs-lookup"><span data-stu-id="1a2b6-163">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="1a2b6-164">\_INTENSITY4 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-164">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="1a2b6-165">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-165">4</span></span>      |
| <span data-ttu-id="1a2b6-166">\_INTENSITY8 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-166">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="1a2b6-167">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-167">8</span></span>      |
| <span data-ttu-id="1a2b6-168">\_INTENSITY12 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-168">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="1a2b6-169">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-169">12</span></span>     |
| <span data-ttu-id="1a2b6-170">\_INTENSITY16 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-170">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="1a2b6-171">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-171">16</span></span>     |
| <span data-ttu-id="1a2b6-172">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-172">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="1a2b6-173">GL \_ R3 \_ G3 \_ a2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-173">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="1a2b6-174">3</span><span class="sxs-lookup"><span data-stu-id="1a2b6-174">3</span></span>      | <span data-ttu-id="1a2b6-175">3</span><span class="sxs-lookup"><span data-stu-id="1a2b6-175">3</span></span>      | <span data-ttu-id="1a2b6-176">2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-176">2</span></span>      |        |        |        |
| <span data-ttu-id="1a2b6-177">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-177">GL\_RGB4</span></span>                 | <span data-ttu-id="1a2b6-178">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-178">4</span></span>      | <span data-ttu-id="1a2b6-179">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-179">4</span></span>      | <span data-ttu-id="1a2b6-180">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-180">4</span></span>      |        |        |        |
| <span data-ttu-id="1a2b6-181">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-181">GL\_RGB5</span></span>                 | <span data-ttu-id="1a2b6-182">5</span><span class="sxs-lookup"><span data-stu-id="1a2b6-182">5</span></span>      | <span data-ttu-id="1a2b6-183">5</span><span class="sxs-lookup"><span data-stu-id="1a2b6-183">5</span></span>      | <span data-ttu-id="1a2b6-184">5</span><span class="sxs-lookup"><span data-stu-id="1a2b6-184">5</span></span>      |        |        |        |
| <span data-ttu-id="1a2b6-185">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-185">GL\_RGB8</span></span>                 | <span data-ttu-id="1a2b6-186">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-186">8</span></span>      | <span data-ttu-id="1a2b6-187">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-187">8</span></span>      | <span data-ttu-id="1a2b6-188">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-188">8</span></span>      |        |        |        |
| <span data-ttu-id="1a2b6-189">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-189">GL\_RGB10</span></span>                | <span data-ttu-id="1a2b6-190">10</span><span class="sxs-lookup"><span data-stu-id="1a2b6-190">10</span></span>     | <span data-ttu-id="1a2b6-191">10</span><span class="sxs-lookup"><span data-stu-id="1a2b6-191">10</span></span>     | <span data-ttu-id="1a2b6-192">10</span><span class="sxs-lookup"><span data-stu-id="1a2b6-192">10</span></span>     |        |        |        |
| <span data-ttu-id="1a2b6-193">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-193">GL\_RGB12</span></span>                | <span data-ttu-id="1a2b6-194">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-194">12</span></span>     | <span data-ttu-id="1a2b6-195">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-195">12</span></span>     | <span data-ttu-id="1a2b6-196">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-196">12</span></span>     |        |        |        |
| <span data-ttu-id="1a2b6-197">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-197">GL\_RGB16</span></span>                | <span data-ttu-id="1a2b6-198">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-198">16</span></span>     | <span data-ttu-id="1a2b6-199">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-199">16</span></span>     | <span data-ttu-id="1a2b6-200">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-200">16</span></span>     |        |        |        |
| <span data-ttu-id="1a2b6-201">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="1a2b6-201">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="1a2b6-202">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-202">GL\_RGBA2</span></span>                | <span data-ttu-id="1a2b6-203">2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-203">2</span></span>      | <span data-ttu-id="1a2b6-204">2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-204">2</span></span>      | <span data-ttu-id="1a2b6-205">2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-205">2</span></span>      | <span data-ttu-id="1a2b6-206">2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-206">2</span></span>      |        |        |
| <span data-ttu-id="1a2b6-207">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-207">GL\_RGBA4</span></span>                | <span data-ttu-id="1a2b6-208">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-208">4</span></span>      | <span data-ttu-id="1a2b6-209">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-209">4</span></span>      | <span data-ttu-id="1a2b6-210">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-210">4</span></span>      | <span data-ttu-id="1a2b6-211">4</span><span class="sxs-lookup"><span data-stu-id="1a2b6-211">4</span></span>      |        |        |
| <span data-ttu-id="1a2b6-212">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="1a2b6-212">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="1a2b6-213">5</span><span class="sxs-lookup"><span data-stu-id="1a2b6-213">5</span></span>      | <span data-ttu-id="1a2b6-214">5</span><span class="sxs-lookup"><span data-stu-id="1a2b6-214">5</span></span>      | <span data-ttu-id="1a2b6-215">5</span><span class="sxs-lookup"><span data-stu-id="1a2b6-215">5</span></span>      | <span data-ttu-id="1a2b6-216">1</span><span class="sxs-lookup"><span data-stu-id="1a2b6-216">1</span></span>      |        |        |
| <span data-ttu-id="1a2b6-217">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-217">GL\_RGBA8</span></span>                | <span data-ttu-id="1a2b6-218">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-218">8</span></span>      | <span data-ttu-id="1a2b6-219">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-219">8</span></span>      | <span data-ttu-id="1a2b6-220">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-220">8</span></span>      | <span data-ttu-id="1a2b6-221">8</span><span class="sxs-lookup"><span data-stu-id="1a2b6-221">8</span></span>      |        |        |
| <span data-ttu-id="1a2b6-222">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-222">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="1a2b6-223">10</span><span class="sxs-lookup"><span data-stu-id="1a2b6-223">10</span></span>     | <span data-ttu-id="1a2b6-224">10</span><span class="sxs-lookup"><span data-stu-id="1a2b6-224">10</span></span>     | <span data-ttu-id="1a2b6-225">10</span><span class="sxs-lookup"><span data-stu-id="1a2b6-225">10</span></span>     | <span data-ttu-id="1a2b6-226">2</span><span class="sxs-lookup"><span data-stu-id="1a2b6-226">2</span></span>      |        |        |
| <span data-ttu-id="1a2b6-227">\_RGBA12 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-227">GL\_RGBA12</span></span>               | <span data-ttu-id="1a2b6-228">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-228">12</span></span>     | <span data-ttu-id="1a2b6-229">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-229">12</span></span>     | <span data-ttu-id="1a2b6-230">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-230">12</span></span>     | <span data-ttu-id="1a2b6-231">12</span><span class="sxs-lookup"><span data-stu-id="1a2b6-231">12</span></span>     |        |        |
| <span data-ttu-id="1a2b6-232">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-232">GL\_RGBA16</span></span>               | <span data-ttu-id="1a2b6-233">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-233">16</span></span>     | <span data-ttu-id="1a2b6-234">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-234">16</span></span>     | <span data-ttu-id="1a2b6-235">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-235">16</span></span>     | <span data-ttu-id="1a2b6-236">16</span><span class="sxs-lookup"><span data-stu-id="1a2b6-236">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="1a2b6-237">*x*</span><span class="sxs-lookup"><span data-stu-id="1a2b6-237">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="1a2b6-238">Coordonnée du plan x de la fenêtre du coin inférieur gauche de la zone rectangulaire de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-238">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="1a2b6-239">*y*</span><span class="sxs-lookup"><span data-stu-id="1a2b6-239">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="1a2b6-240">Coordonnée du plan y de la fenêtre du coin inférieur gauche de la zone rectangulaire de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-240">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="1a2b6-241">*width*</span><span class="sxs-lookup"><span data-stu-id="1a2b6-241">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="1a2b6-242">Largeur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-242">The width of the texture image.</span></span> <span data-ttu-id="1a2b6-243">Doit être \*  de 2 x 2 pour un entier *n*.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-243">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="1a2b6-244">*height*</span><span class="sxs-lookup"><span data-stu-id="1a2b6-244">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="1a2b6-245">Hauteur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-245">The height of the texture image.</span></span> <span data-ttu-id="1a2b6-246">Doit être \*  de 2 x 2 pour un entier *n*.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-246">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="1a2b6-247">*2S*</span><span class="sxs-lookup"><span data-stu-id="1a2b6-247">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="1a2b6-248">Largeur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-248">The width of the border.</span></span> <span data-ttu-id="1a2b6-249">Doit être égal à zéro ou égal à 1.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-249">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a2b6-250">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a2b6-250">Return value</span></span>

<span data-ttu-id="1a2b6-251">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-251">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1a2b6-252">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1a2b6-252">Error codes</span></span>

<span data-ttu-id="1a2b6-253">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1a2b6-253">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1a2b6-254">Nom</span><span class="sxs-lookup"><span data-stu-id="1a2b6-254">Name</span></span>                                                                                                  | <span data-ttu-id="1a2b6-255">Signification</span><span class="sxs-lookup"><span data-stu-id="1a2b6-255">Meaning</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a2b6-256"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b6-256"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1a2b6-257">la *cible* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-257">*target* was not an accepted value.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="1a2b6-258"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b6-258"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1a2b6-259">le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* est la valeur retournée de la \_ taille de texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1a2b6-259">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                               |
| <dl> <span data-ttu-id="1a2b6-260"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b6-260"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1a2b6-261">la *bordure* n’était pas égale à zéro ou 1.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-261">*border* was not zero or 1.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="1a2b6-262"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b6-262"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1a2b6-263">la *largeur* était inférieure à zéro, supérieure à 2 + \_ taille maximale de la texture GL \_ \_ , ou la *largeur* ne peut pas être représentée sous la forme 2n + 2 \*  pour un entier *n*.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-263">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n + 2 \* *border* for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="1a2b6-264"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b6-264"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1a2b6-265">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1a2b6-265">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="1a2b6-266">Notes</span><span class="sxs-lookup"><span data-stu-id="1a2b6-266">Remarks</span></span>

<span data-ttu-id="1a2b6-267">La fonction **glCopyTexImage2D** définit une image de texture à deux dimensions à l’aide de pixels du trame actuel, plutôt qu’à partir de la mémoire principale comme c’est le cas pour [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="1a2b6-267">The **glCopyTexImage2D** function defines a two-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage2D**](glteximage2d.md).</span></span>

<span data-ttu-id="1a2b6-268">À l’aide du niveau de mipmap spécifié avec *Level*, les tableaux de texture sont définis comme un rectangle de pixels avec l’angle inférieur gauche situé aux coordonnées *x* et *y*, largeur égale à la *largeur* + (2 \* *bordure*) et une hauteur égale à *hauteur* + (2 \* *bordure*).</span><span class="sxs-lookup"><span data-stu-id="1a2b6-268">Using the mipmap level specified with *level*, texture arrays are defined as a rectangle of pixels with the lower-left corner located at the coordinates *x* and *y*, width equal to *width* + (2 \* *border*), and a height equal to *height* + (2 \* *border*).</span></span> <span data-ttu-id="1a2b6-269">Le format interne du tableau de texture est spécifié avec le paramètre *internalFormat* .</span><span class="sxs-lookup"><span data-stu-id="1a2b6-269">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="1a2b6-270">La fonction **glCopyTexImage2D** traite les pixels d’une ligne de la même façon que [**glCopyPixels**](glcopypixels.md) , sauf qu’avant la conversion finale des pixels, toutes les valeurs de composant de pixel sont ancrées à la plage \[ 0, 1 \] et converties au format interne de la texture pour le stockage dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-270">The **glCopyTexImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="1a2b6-271">L’ordonnancement des pixels est déterminé par des coordonnées *x* et *y* inférieures correspondant à des coordonnées de texture *s* et *t* inférieures.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-271">Pixel ordering is determined with lower *x* and *y* coordinates corresponding to lower *s* and *t* texture coordinates.</span></span> <span data-ttu-id="1a2b6-272">Si l’un des pixels dans une ligne spécifiée du trame actuel est en dehors de la fenêtre associée au contexte de rendu actuel, ses valeurs ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-272">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="1a2b6-273">Vous ne pouvez pas inclure d’appels à **glCopyTexImage2D** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-273">You cannot include calls to **glCopyTexImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="1a2b6-274">La fonction **glCopyTexImage2D** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-274">The **glCopyTexImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="1a2b6-275">La texturation n’a aucun effet dans le mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="1a2b6-275">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="1a2b6-276">Les fonctions [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement de la même façon qu’elles affectent [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="1a2b6-276">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="1a2b6-277">La fonction suivante récupère des informations relatives à **glCopyTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="1a2b6-277">The following function retrieves information related to **glCopyTexImage2D**:</span></span>

<span data-ttu-id="1a2b6-278">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 2D</span><span class="sxs-lookup"><span data-stu-id="1a2b6-278">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="1a2b6-279">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a2b6-279">Requirements</span></span>



| <span data-ttu-id="1a2b6-280">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a2b6-280">Requirement</span></span> | <span data-ttu-id="1a2b6-281">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a2b6-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a2b6-282">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a2b6-282">Minimum supported client</span></span><br/> | <span data-ttu-id="1a2b6-283">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a2b6-283">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1a2b6-284">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a2b6-284">Minimum supported server</span></span><br/> | <span data-ttu-id="1a2b6-285">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a2b6-285">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a2b6-286">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a2b6-286">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a2b6-287"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b6-287"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1a2b6-288">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a2b6-288">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a2b6-289"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b6-289"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a2b6-290">DLL</span><span class="sxs-lookup"><span data-stu-id="1a2b6-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a2b6-291"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b6-291"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a2b6-292">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a2b6-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a2b6-293">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-293">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-294">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-294">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-295">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-295">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-296">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-296">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-297">**glFog**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-297">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-298">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-298">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-299">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-299">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-300">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-300">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-301">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-301">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-302">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-302">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-303">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-303">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1a2b6-304">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="1a2b6-304">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





