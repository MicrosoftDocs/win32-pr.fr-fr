---
title: fonction glCopyTexImage1D (GL. h)
description: La fonction glCopyTexImage1D copie les pixels du trame dans une image de texture unidimensionnelle.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- glCopyTexImage1D fonction OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510335"
---
# <a name="glcopyteximage1d-function"></a><span data-ttu-id="c06b8-104">glCopyTexImage1D fonction)</span><span class="sxs-lookup"><span data-stu-id="c06b8-104">glCopyTexImage1D function</span></span>

<span data-ttu-id="c06b8-105">La fonction **glCopyTexImage1D** copie les pixels du trame dans une image de texture unidimensionnelle.</span><span class="sxs-lookup"><span data-stu-id="c06b8-105">The **glCopyTexImage1D** function copies pixels from the framebuffer into a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="c06b8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c06b8-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="c06b8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c06b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06b8-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="c06b8-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b8-109">Cible pour laquelle les données de l’image seront modifiées.</span><span class="sxs-lookup"><span data-stu-id="c06b8-109">The target for which the image data will be changed.</span></span> <span data-ttu-id="c06b8-110">Doit avoir la texture GL \_ valeur \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="c06b8-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="c06b8-111">*level*</span><span class="sxs-lookup"><span data-stu-id="c06b8-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b8-112">Numéro de niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="c06b8-112">The level-of-detail number.</span></span> <span data-ttu-id="c06b8-113">Le niveau 0 est l’image de base.</span><span class="sxs-lookup"><span data-stu-id="c06b8-113">Level 0 is the base image.</span></span> <span data-ttu-id="c06b8-114">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="c06b8-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="c06b8-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="c06b8-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b8-116">Format interne et résolution des données de texture.</span><span class="sxs-lookup"><span data-stu-id="c06b8-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="c06b8-117">Ce paramètre doit être l’une des valeurs symboliques suivantes.</span><span class="sxs-lookup"><span data-stu-id="c06b8-117">This parameter must be one of the following symbolic values.</span></span>



| <span data-ttu-id="c06b8-118">Constante</span><span class="sxs-lookup"><span data-stu-id="c06b8-118">Constant</span></span>                 | <span data-ttu-id="c06b8-119">Bits R</span><span class="sxs-lookup"><span data-stu-id="c06b8-119">R Bits</span></span> | <span data-ttu-id="c06b8-120">Bits G</span><span class="sxs-lookup"><span data-stu-id="c06b8-120">G Bits</span></span> | <span data-ttu-id="c06b8-121">Bits B</span><span class="sxs-lookup"><span data-stu-id="c06b8-121">B Bits</span></span> | <span data-ttu-id="c06b8-122">Un bits</span><span class="sxs-lookup"><span data-stu-id="c06b8-122">A Bits</span></span> | <span data-ttu-id="c06b8-123">L bits</span><span class="sxs-lookup"><span data-stu-id="c06b8-123">L Bits</span></span> | <span data-ttu-id="c06b8-124">I bits</span><span class="sxs-lookup"><span data-stu-id="c06b8-124">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="c06b8-125">GL \_ alpha</span><span class="sxs-lookup"><span data-stu-id="c06b8-125">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="c06b8-126">\_Alpha4 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-126">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="c06b8-127">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-127">4</span></span>      |        |        |
| <span data-ttu-id="c06b8-128">\_ALPHA8 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-128">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="c06b8-129">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-129">8</span></span>      |        |        |
| <span data-ttu-id="c06b8-130">\_ALPHA12 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-130">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="c06b8-131">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-131">12</span></span>     |        |        |
| <span data-ttu-id="c06b8-132">\_ALPHA16 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-132">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="c06b8-133">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-133">16</span></span>     |        |        |
| <span data-ttu-id="c06b8-134">LUMINANCE du GL \_</span><span class="sxs-lookup"><span data-stu-id="c06b8-134">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="c06b8-135">\_LUMINANCE4 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-135">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="c06b8-136">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-136">4</span></span>      |        |
| <span data-ttu-id="c06b8-137">\_LUMINANCE8 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-137">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="c06b8-138">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-138">8</span></span>      |        |
| <span data-ttu-id="c06b8-139">\_LUMINANCE12 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-139">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="c06b8-140">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-140">12</span></span>     |        |
| <span data-ttu-id="c06b8-141">\_LUMINANCE16 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-141">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="c06b8-142">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-142">16</span></span>     |        |
| <span data-ttu-id="c06b8-143">\_luminance \_ alpha du GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-143">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="c06b8-144">GL \_ LUMINANCE4 \_ alpha4</span><span class="sxs-lookup"><span data-stu-id="c06b8-144">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="c06b8-145">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-145">4</span></span>      | <span data-ttu-id="c06b8-146">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-146">4</span></span>      |        |
| <span data-ttu-id="c06b8-147">GL \_ LUMINANCE6 \_ alpha2</span><span class="sxs-lookup"><span data-stu-id="c06b8-147">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="c06b8-148">2</span><span class="sxs-lookup"><span data-stu-id="c06b8-148">2</span></span>      | <span data-ttu-id="c06b8-149">6</span><span class="sxs-lookup"><span data-stu-id="c06b8-149">6</span></span>      |        |
| <span data-ttu-id="c06b8-150">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="c06b8-150">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="c06b8-151">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-151">8</span></span>      | <span data-ttu-id="c06b8-152">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-152">8</span></span>      |        |
| <span data-ttu-id="c06b8-153">GL \_ LUMINANCE12 \_ alpha4</span><span class="sxs-lookup"><span data-stu-id="c06b8-153">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="c06b8-154">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-154">4</span></span>      | <span data-ttu-id="c06b8-155">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-155">12</span></span>     |        |
| <span data-ttu-id="c06b8-156">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="c06b8-156">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="c06b8-157">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-157">12</span></span>     | <span data-ttu-id="c06b8-158">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-158">12</span></span>     |        |
| <span data-ttu-id="c06b8-159">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="c06b8-159">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="c06b8-160">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-160">16</span></span>     | <span data-ttu-id="c06b8-161">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-161">16</span></span>     |        |
| <span data-ttu-id="c06b8-162">intensité du GL \_</span><span class="sxs-lookup"><span data-stu-id="c06b8-162">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="c06b8-163">\_INTENSITY4 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-163">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="c06b8-164">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-164">4</span></span>      |
| <span data-ttu-id="c06b8-165">\_INTENSITY8 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-165">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="c06b8-166">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-166">8</span></span>      |
| <span data-ttu-id="c06b8-167">\_INTENSITY12 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-167">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="c06b8-168">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-168">12</span></span>     |
| <span data-ttu-id="c06b8-169">\_INTENSITY16 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-169">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="c06b8-170">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-170">16</span></span>     |
| <span data-ttu-id="c06b8-171">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-171">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="c06b8-172">GL \_ R3 \_ G3 \_ a2</span><span class="sxs-lookup"><span data-stu-id="c06b8-172">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="c06b8-173">3</span><span class="sxs-lookup"><span data-stu-id="c06b8-173">3</span></span>      | <span data-ttu-id="c06b8-174">3</span><span class="sxs-lookup"><span data-stu-id="c06b8-174">3</span></span>      | <span data-ttu-id="c06b8-175">2</span><span class="sxs-lookup"><span data-stu-id="c06b8-175">2</span></span>      |        |        |        |
| <span data-ttu-id="c06b8-176">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-176">GL\_RGB4</span></span>                 | <span data-ttu-id="c06b8-177">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-177">4</span></span>      | <span data-ttu-id="c06b8-178">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-178">4</span></span>      | <span data-ttu-id="c06b8-179">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-179">4</span></span>      |        |        |        |
| <span data-ttu-id="c06b8-180">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-180">GL\_RGB5</span></span>                 | <span data-ttu-id="c06b8-181">5</span><span class="sxs-lookup"><span data-stu-id="c06b8-181">5</span></span>      | <span data-ttu-id="c06b8-182">5</span><span class="sxs-lookup"><span data-stu-id="c06b8-182">5</span></span>      | <span data-ttu-id="c06b8-183">5</span><span class="sxs-lookup"><span data-stu-id="c06b8-183">5</span></span>      |        |        |        |
| <span data-ttu-id="c06b8-184">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-184">GL\_RGB8</span></span>                 | <span data-ttu-id="c06b8-185">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-185">8</span></span>      | <span data-ttu-id="c06b8-186">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-186">8</span></span>      | <span data-ttu-id="c06b8-187">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-187">8</span></span>      |        |        |        |
| <span data-ttu-id="c06b8-188">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-188">GL\_RGB10</span></span>                | <span data-ttu-id="c06b8-189">10</span><span class="sxs-lookup"><span data-stu-id="c06b8-189">10</span></span>     | <span data-ttu-id="c06b8-190">10</span><span class="sxs-lookup"><span data-stu-id="c06b8-190">10</span></span>     | <span data-ttu-id="c06b8-191">10</span><span class="sxs-lookup"><span data-stu-id="c06b8-191">10</span></span>     |        |        |        |
| <span data-ttu-id="c06b8-192">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-192">GL\_RGB12</span></span>                | <span data-ttu-id="c06b8-193">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-193">12</span></span>     | <span data-ttu-id="c06b8-194">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-194">12</span></span>     | <span data-ttu-id="c06b8-195">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-195">12</span></span>     |        |        |        |
| <span data-ttu-id="c06b8-196">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-196">GL\_RGB16</span></span>                | <span data-ttu-id="c06b8-197">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-197">16</span></span>     | <span data-ttu-id="c06b8-198">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-198">16</span></span>     | <span data-ttu-id="c06b8-199">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-199">16</span></span>     |        |        |        |
| <span data-ttu-id="c06b8-200">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="c06b8-200">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="c06b8-201">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-201">GL\_RGBA2</span></span>                | <span data-ttu-id="c06b8-202">2</span><span class="sxs-lookup"><span data-stu-id="c06b8-202">2</span></span>      | <span data-ttu-id="c06b8-203">2</span><span class="sxs-lookup"><span data-stu-id="c06b8-203">2</span></span>      | <span data-ttu-id="c06b8-204">2</span><span class="sxs-lookup"><span data-stu-id="c06b8-204">2</span></span>      | <span data-ttu-id="c06b8-205">2</span><span class="sxs-lookup"><span data-stu-id="c06b8-205">2</span></span>      |        |        |
| <span data-ttu-id="c06b8-206">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-206">GL\_RGBA4</span></span>                | <span data-ttu-id="c06b8-207">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-207">4</span></span>      | <span data-ttu-id="c06b8-208">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-208">4</span></span>      | <span data-ttu-id="c06b8-209">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-209">4</span></span>      | <span data-ttu-id="c06b8-210">4</span><span class="sxs-lookup"><span data-stu-id="c06b8-210">4</span></span>      |        |        |
| <span data-ttu-id="c06b8-211">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="c06b8-211">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="c06b8-212">5</span><span class="sxs-lookup"><span data-stu-id="c06b8-212">5</span></span>      | <span data-ttu-id="c06b8-213">5</span><span class="sxs-lookup"><span data-stu-id="c06b8-213">5</span></span>      | <span data-ttu-id="c06b8-214">5</span><span class="sxs-lookup"><span data-stu-id="c06b8-214">5</span></span>      | <span data-ttu-id="c06b8-215">1</span><span class="sxs-lookup"><span data-stu-id="c06b8-215">1</span></span>      |        |        |
| <span data-ttu-id="c06b8-216">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-216">GL\_RGBA8</span></span>                | <span data-ttu-id="c06b8-217">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-217">8</span></span>      | <span data-ttu-id="c06b8-218">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-218">8</span></span>      | <span data-ttu-id="c06b8-219">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-219">8</span></span>      | <span data-ttu-id="c06b8-220">8</span><span class="sxs-lookup"><span data-stu-id="c06b8-220">8</span></span>      |        |        |
| <span data-ttu-id="c06b8-221">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="c06b8-221">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="c06b8-222">10</span><span class="sxs-lookup"><span data-stu-id="c06b8-222">10</span></span>     | <span data-ttu-id="c06b8-223">10</span><span class="sxs-lookup"><span data-stu-id="c06b8-223">10</span></span>     | <span data-ttu-id="c06b8-224">10</span><span class="sxs-lookup"><span data-stu-id="c06b8-224">10</span></span>     | <span data-ttu-id="c06b8-225">2</span><span class="sxs-lookup"><span data-stu-id="c06b8-225">2</span></span>      |        |        |
| <span data-ttu-id="c06b8-226">\_RGBA12 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-226">GL\_RGBA12</span></span>               | <span data-ttu-id="c06b8-227">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-227">12</span></span>     | <span data-ttu-id="c06b8-228">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-228">12</span></span>     | <span data-ttu-id="c06b8-229">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-229">12</span></span>     | <span data-ttu-id="c06b8-230">12</span><span class="sxs-lookup"><span data-stu-id="c06b8-230">12</span></span>     |        |        |
| <span data-ttu-id="c06b8-231">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="c06b8-231">GL\_RGBA16</span></span>               | <span data-ttu-id="c06b8-232">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-232">16</span></span>     | <span data-ttu-id="c06b8-233">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-233">16</span></span>     | <span data-ttu-id="c06b8-234">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-234">16</span></span>     | <span data-ttu-id="c06b8-235">16</span><span class="sxs-lookup"><span data-stu-id="c06b8-235">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="c06b8-236">*x*</span><span class="sxs-lookup"><span data-stu-id="c06b8-236">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b8-237">Coordonnée du plan x de la fenêtre du coin inférieur gauche de la ligne de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="c06b8-237">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="c06b8-238">*y*</span><span class="sxs-lookup"><span data-stu-id="c06b8-238">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b8-239">Coordonnée du plan y de la fenêtre du coin inférieur gauche de la ligne de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="c06b8-239">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="c06b8-240">*width*</span><span class="sxs-lookup"><span data-stu-id="c06b8-240">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b8-241">Largeur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="c06b8-241">The width of the texture image.</span></span> <span data-ttu-id="c06b8-242">Doit être égal à zéro ou 2n + 2 (*bordure*) pour un nombre entier *n*.</span><span class="sxs-lookup"><span data-stu-id="c06b8-242">Must be zero or 2n + 2(*border*) for some integer *n*.</span></span> <span data-ttu-id="c06b8-243">La hauteur de l’image de texture est 1.</span><span class="sxs-lookup"><span data-stu-id="c06b8-243">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="c06b8-244">*2S*</span><span class="sxs-lookup"><span data-stu-id="c06b8-244">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b8-245">Largeur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="c06b8-245">The width of the border.</span></span> <span data-ttu-id="c06b8-246">Doit être égal à zéro ou égal à 1.</span><span class="sxs-lookup"><span data-stu-id="c06b8-246">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c06b8-247">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c06b8-247">Return value</span></span>

<span data-ttu-id="c06b8-248">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c06b8-248">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c06b8-249">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c06b8-249">Error codes</span></span>

<span data-ttu-id="c06b8-250">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c06b8-250">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c06b8-251">Nom</span><span class="sxs-lookup"><span data-stu-id="c06b8-251">Name</span></span>                                                                                                  | <span data-ttu-id="c06b8-252">Signification</span><span class="sxs-lookup"><span data-stu-id="c06b8-252">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c06b8-253"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c06b8-253"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c06b8-254">la *cible* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="c06b8-254">*target* was not an accepted value.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="c06b8-255"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c06b8-255"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c06b8-256">le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* est la valeur retournée de la \_ taille de texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c06b8-256">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                           |
| <dl> <span data-ttu-id="c06b8-257"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c06b8-257"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c06b8-258">la *bordure* n’était pas égale à zéro ou 1.</span><span class="sxs-lookup"><span data-stu-id="c06b8-258">*border* was not zero or 1.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="c06b8-259"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c06b8-259"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c06b8-260">la *largeur* était inférieure à zéro, supérieure à 2 + \_ taille maximale de la texture GL \_ \_ , ou la *largeur* ne peut pas être représentée sous la forme 2n + (*Border*) pour un nombre entier *n*.</span><span class="sxs-lookup"><span data-stu-id="c06b8-260">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n +(*border*) for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="c06b8-261"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c06b8-261"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c06b8-262">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c06b8-262">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="c06b8-263">Notes</span><span class="sxs-lookup"><span data-stu-id="c06b8-263">Remarks</span></span>

<span data-ttu-id="c06b8-264">La fonction **glCopyTexImage1D** définit une image de texture unidimensionnelle à l’aide de pixels du trame actuel, plutôt qu’à partir de la mémoire principale comme c’est le cas pour [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="c06b8-264">The **glCopyTexImage1D** function defines a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage1D**](glteximage1d.md).</span></span>

<span data-ttu-id="c06b8-265">À l’aide du niveau de mipmap spécifié avec *Level*, les tableaux de texture sont définis sous la forme d’une ligne de pixels alignée avec l’angle inférieur gauche de la fenêtre aux coordonnées spécifiées par *x* et *y*, avec une longueur égale à la *largeur* + 2 \* .</span><span class="sxs-lookup"><span data-stu-id="c06b8-265">Using the mipmap level specified with *level*, texture arrays are defined as a pixel row aligned with the lower-left corner of the window at the coordinates specified by *x* and *y*, with a length equal to *width* + 2 \* *border*.</span></span> <span data-ttu-id="c06b8-266">Le format interne du tableau de texture est spécifié avec le paramètre *internalFormat* .</span><span class="sxs-lookup"><span data-stu-id="c06b8-266">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="c06b8-267">La fonction **glCopyTexImage1D** traite les pixels d’une ligne de la même façon que [**glCopyPixels**](glcopypixels.md), sauf qu’avant la conversion finale des pixels, toutes les valeurs de composant de pixel sont ancrées à la plage \[ 0, 1 \] et converties au format interne de la texture pour le stockage dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="c06b8-267">The **glCopyTexImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="c06b8-268">L’ordonnancement des pixels est déterminé par des coordonnées *x* inférieures correspondant à des coordonnées de texture inférieures.</span><span class="sxs-lookup"><span data-stu-id="c06b8-268">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="c06b8-269">Si l’un des pixels dans une ligne spécifiée du trame actuel est en dehors de la fenêtre associée au contexte de rendu actuel, ses valeurs ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="c06b8-269">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="c06b8-270">Vous ne pouvez pas inclure d’appels à **glCopyTexImage1D** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c06b8-270">You cannot include calls to **glCopyTexImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="c06b8-271">La fonction **glCopyTexImage1D** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c06b8-271">The **glCopyTexImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="c06b8-272">La texturation n’a aucun effet dans le mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="c06b8-272">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="c06b8-273">Les fonctions [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement de la même façon qu’elles affectent [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="c06b8-273">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="c06b8-274">La fonction suivante récupère des informations relatives à **glCopyTexImage1D**:</span><span class="sxs-lookup"><span data-stu-id="c06b8-274">The following function retrieves information related to **glCopyTexImage1D**:</span></span>

<span data-ttu-id="c06b8-275">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="c06b8-275">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="c06b8-276">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c06b8-276">Requirements</span></span>



| <span data-ttu-id="c06b8-277">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c06b8-277">Requirement</span></span> | <span data-ttu-id="c06b8-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="c06b8-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c06b8-279">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c06b8-279">Minimum supported client</span></span><br/> | <span data-ttu-id="c06b8-280">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c06b8-280">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c06b8-281">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c06b8-281">Minimum supported server</span></span><br/> | <span data-ttu-id="c06b8-282">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c06b8-282">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c06b8-283">En-tête</span><span class="sxs-lookup"><span data-stu-id="c06b8-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="c06b8-284"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c06b8-284"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c06b8-285">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c06b8-285">Library</span></span><br/>                  | <dl> <span data-ttu-id="c06b8-286"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c06b8-286"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c06b8-287">DLL</span><span class="sxs-lookup"><span data-stu-id="c06b8-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c06b8-288"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c06b8-288"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c06b8-289">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c06b8-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06b8-290">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="c06b8-290">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="c06b8-291">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="c06b8-291">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="c06b8-292">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="c06b8-292">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="c06b8-293">**glFog**</span><span class="sxs-lookup"><span data-stu-id="c06b8-293">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="c06b8-294">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="c06b8-294">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="c06b8-295">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="c06b8-295">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="c06b8-296">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="c06b8-296">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="c06b8-297">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="c06b8-297">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="c06b8-298">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="c06b8-298">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="c06b8-299">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="c06b8-299">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="c06b8-300">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="c06b8-300">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





