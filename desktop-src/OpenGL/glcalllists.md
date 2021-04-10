---
title: fonction glCallLists (GL. h)
description: La fonction glCallLists exécute une liste de listes d’affichage.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glCallLists fonction OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942266"
---
# <a name="glcalllists-function"></a><span data-ttu-id="4086b-104">glCallLists fonction)</span><span class="sxs-lookup"><span data-stu-id="4086b-104">glCallLists function</span></span>

<span data-ttu-id="4086b-105">La fonction **glCallLists** exécute une liste de listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4086b-105">The **glCallLists** function executes a list of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="4086b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4086b-106">Syntax</span></span>


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a><span data-ttu-id="4086b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4086b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4086b-108">*n*</span><span class="sxs-lookup"><span data-stu-id="4086b-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="4086b-109">Nombre de listes d’affichage à exécuter.</span><span class="sxs-lookup"><span data-stu-id="4086b-109">The number of display lists to be executed.</span></span>

</dd> <dt>

<span data-ttu-id="4086b-110">*type*</span><span class="sxs-lookup"><span data-stu-id="4086b-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="4086b-111">Type des valeurs dans les *listes*.</span><span class="sxs-lookup"><span data-stu-id="4086b-111">The type of values in *lists*.</span></span> <span data-ttu-id="4086b-112">Les constantes symboliques suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="4086b-112">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="4086b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4086b-113">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="4086b-114">Signification</span><span class="sxs-lookup"><span data-stu-id="4086b-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="4086b-115"><dt>**\_octet GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-115"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="4086b-116">Le paramètre *Lists* est traité comme un tableau d’octets signés, chacun compris entre-128 et 127.</span><span class="sxs-lookup"><span data-stu-id="4086b-116">The *lists* parameter is treated as an array of signed bytes, each in the range -128 through 127.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="4086b-117"><dt>**\_octet non signé GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-117"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="4086b-118">Le paramètre *Lists* est traité comme un tableau d’octets non signés, chacun compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="4086b-118">The *lists* parameter is treated as an array of unsigned bytes, each in the range 0 through 255.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="4086b-119"><dt>**\_abrégé GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-119"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="4086b-120">Le paramètre *Lists* est traité comme un tableau d’entiers de 2 octets signés, chacun dans la plage comprise entre-32768 et 32767.</span><span class="sxs-lookup"><span data-stu-id="4086b-120">The *lists* parameter is treated as an array of signed 2-byte integers, each in the range -32768 through 32767.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="4086b-121"><dt>**NON signé dans le GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-121"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="4086b-122">Le paramètre *Lists* est traité comme un tableau d’entiers de 2 octets non signés, chacun compris entre 0 et 65535.</span><span class="sxs-lookup"><span data-stu-id="4086b-122">The *lists* parameter is treated as an array of unsigned 2-byte integers, each in the range 0 through 65535.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="4086b-123"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-123"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="4086b-124">Le paramètre *Lists* est traité comme un tableau d’entiers signés sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="4086b-124">The *lists* parameter is treated as an array of signed 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="4086b-125"><dt>**\_entier non signé GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-125"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="4086b-126">Le paramètre *Lists* est traité comme un tableau d’entiers non signés sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="4086b-126">The *lists* parameter is treated as an array of unsigned 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="4086b-127"><dt>**valeur \_ float du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-127"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="4086b-128">Le paramètre *Lists* est traité comme un tableau de valeurs à virgule flottante de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="4086b-128">The *lists* parameter is treated as an array of 4-byte, floating-point values.</span></span><br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <span data-ttu-id="4086b-129"><dt>**GL \_ 2 \_ octets**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-129"><dt>**GL\_2\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="4086b-130">Le paramètre *Lists* est traité comme un tableau d’octets non signés.</span><span class="sxs-lookup"><span data-stu-id="4086b-130">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="4086b-131">Chaque paire d’octets spécifie un nom de liste d’affichage unique.</span><span class="sxs-lookup"><span data-stu-id="4086b-131">Each pair of bytes specifies a single display-list name.</span></span> <span data-ttu-id="4086b-132">La valeur de la paire est calculée comme 256 fois la valeur non signée du premier octet plus la valeur non signée du deuxième octet.</span><span class="sxs-lookup"><span data-stu-id="4086b-132">The value of the pair is computed as 256 times the unsigned value of the first byte plus the unsigned value of the second byte.</span></span><br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <span data-ttu-id="4086b-133"><dt>**GL \_ 3 \_ octets**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-133"><dt>**GL\_3\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="4086b-134">Le paramètre *Lists* est traité comme un tableau d’octets non signés.</span><span class="sxs-lookup"><span data-stu-id="4086b-134">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="4086b-135">Chaque triplet d’octets spécifie un nom de liste d’affichage unique.</span><span class="sxs-lookup"><span data-stu-id="4086b-135">Each triplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="4086b-136">La valeur de l’triplet est calculée comme 65536 fois la valeur non signée du premier octet, plus 256 fois la valeur non signée du deuxième octet, plus la valeur non signée du troisième octet.</span><span class="sxs-lookup"><span data-stu-id="4086b-136">The value of the triplet is computed as 65536 times the unsigned value of the first byte, plus 256 times the unsigned value of the second byte, plus the unsigned value of the third byte.</span></span><br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <span data-ttu-id="4086b-137"><dt>**GL \_ 4 \_ octets**</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-137"><dt>**GL\_4\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="4086b-138">Le paramètre *Lists* est traité comme un tableau d’octets non signés.</span><span class="sxs-lookup"><span data-stu-id="4086b-138">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="4086b-139">Chaque quadruplet d’octets spécifie un nom de liste d’affichage unique.</span><span class="sxs-lookup"><span data-stu-id="4086b-139">Each quadruplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="4086b-140">La valeur de l’quadruplet est calculée comme 16777216 fois la valeur non signée du premier octet, plus 65536 fois la valeur non signée du deuxième octet, plus 256 fois la valeur non signée du troisième octet, plus la valeur non signée du quatrième octet, et la valeur non signée.</span><span class="sxs-lookup"><span data-stu-id="4086b-140">The value of the quadruplet is computed as 16777216 times the unsigned value of the first byte, plus 65536 times the unsigned value of the second byte, plus 256 times the unsigned value of the third byte, plus the unsigned value of the fourth byte.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4086b-141">*suivant*</span><span class="sxs-lookup"><span data-stu-id="4086b-141">*lists*</span></span> 
</dt> <dd>

<span data-ttu-id="4086b-142">Adresse d’un tableau d’offsets de nom dans la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4086b-142">The address of an array of name offsets in the display list.</span></span> <span data-ttu-id="4086b-143">Le type de pointeur est void, car les offsets peuvent être bytes, Short, ints ou Floats, en fonction de la valeur de *type*.</span><span class="sxs-lookup"><span data-stu-id="4086b-143">The pointer type is void because the offsets can be bytes, shorts, ints, or floats, depending on the value of *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4086b-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4086b-144">Return value</span></span>

<span data-ttu-id="4086b-145">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4086b-145">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4086b-146">Notes</span><span class="sxs-lookup"><span data-stu-id="4086b-146">Remarks</span></span>

<span data-ttu-id="4086b-147">La fonction **glCallLists** provoque l’exécution de chaque liste d’affichage dans la liste des noms passés comme *listes* .</span><span class="sxs-lookup"><span data-stu-id="4086b-147">The **glCallLists** function causes each display list in the list of names passed as *lists* to be executed.</span></span> <span data-ttu-id="4086b-148">Par conséquent, les fonctions enregistrées dans chaque liste d’affichage sont exécutées dans l’ordre, exactement comme si elles étaient appelées sans utiliser de liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4086b-148">As a result, the functions saved in each display list are executed in order, just as if they were called without using a display list.</span></span> <span data-ttu-id="4086b-149">Les noms des listes d’affichage qui n’ont pas été définies sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="4086b-149">Names of display lists that have not been defined are ignored.</span></span>

<span data-ttu-id="4086b-150">La fonction **glCallLists** fournit un moyen efficace d’exécuter des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4086b-150">The **glCallLists** function provides an efficient means for executing display lists.</span></span> <span data-ttu-id="4086b-151">Le paramètre *n* spécifie le nombre de listes avec divers formats de noms (spécifiés par le paramètre de *type* ) **glCallLists** exécute.</span><span class="sxs-lookup"><span data-stu-id="4086b-151">The *n* parameter specifies the number of lists with various name formats (specified by the *type* parameter) **glCallLists** executes.</span></span>

<span data-ttu-id="4086b-152">La liste des noms de liste d’affichage ne se termine pas par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="4086b-152">The list of display list names is not null-terminated.</span></span> <span data-ttu-id="4086b-153">Au lieu de cela, *n* spécifie le nombre de noms à prendre dans les *listes*.</span><span class="sxs-lookup"><span data-stu-id="4086b-153">Rather, *n* specifies how many names are to be taken from *lists*.</span></span>

<span data-ttu-id="4086b-154">La fonction [**glListBase**](gllistbase.md) rend un niveau d’indirection supplémentaire disponible.</span><span class="sxs-lookup"><span data-stu-id="4086b-154">The [**glListBase**](gllistbase.md) function makes an additional level of indirection available.</span></span> <span data-ttu-id="4086b-155">La fonction **glListBase** spécifie un décalage non signé qui est ajouté à chaque nom de liste d’affichage spécifié dans les *listes* avant l’exécution de cette liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4086b-155">The **glListBase** function specifies an unsigned offset that is added to each display list name specified in *lists* before that display list is executed.</span></span>

<span data-ttu-id="4086b-156">La fonction **glCallLists** peut apparaître à l’intérieur d’une liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4086b-156">The **glCallLists** function can appear inside a display list.</span></span> <span data-ttu-id="4086b-157">Pour éviter la possibilité d’une récurrence infinie résultant de l’appel d’une liste d’affichage, une limite est placée sur le niveau d’imbrication des listes d’affichage au cours de l’exécution de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4086b-157">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display list execution.</span></span> <span data-ttu-id="4086b-158">Cette limite doit être au moins de 64, et dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="4086b-158">This limit must be at least 64, and it depends on the implementation.</span></span>

<span data-ttu-id="4086b-159">L’État OpenGL n’est pas enregistré et restauré à travers un appel à **glCallLists**.</span><span class="sxs-lookup"><span data-stu-id="4086b-159">The OpenGL state is not saved and restored across a call to **glCallLists**.</span></span> <span data-ttu-id="4086b-160">Ainsi, les modifications apportées à l’État OpenGL pendant l’exécution des listes d’affichage sont conservées une fois l’exécution terminée.</span><span class="sxs-lookup"><span data-stu-id="4086b-160">Thus, changes made to the OpenGL state during the execution of the display lists remain after execution is completed.</span></span> <span data-ttu-id="4086b-161">Utilisez [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)et [**glPopMatrix**](glpopmatrix.md) pour conserver l’État OpenGL sur les appels **glCallLists** .</span><span class="sxs-lookup"><span data-stu-id="4086b-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md) to preserve the OpenGL state across **glCallLists** calls.</span></span>

<span data-ttu-id="4086b-162">Vous pouvez exécuter des listes d’affichage entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md), à condition que la liste d’affichage comprenne uniquement les fonctions autorisées dans cet intervalle.</span><span class="sxs-lookup"><span data-stu-id="4086b-162">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="4086b-163">Les fonctions suivantes récupèrent les informations relatives à la fonction **glCallLists** :</span><span class="sxs-lookup"><span data-stu-id="4086b-163">The following functions retrieve information related to the **glCallLists** function:</span></span>

<span data-ttu-id="4086b-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ List \_ base</span><span class="sxs-lookup"><span data-stu-id="4086b-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIST\_BASE</span></span>

<span data-ttu-id="4086b-165">**glGet** with argument GL \_ Max \_ List \_ imbrication</span><span class="sxs-lookup"><span data-stu-id="4086b-165">**glGet** with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="4086b-166">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="4086b-166">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="4086b-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4086b-167">Requirements</span></span>



| <span data-ttu-id="4086b-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4086b-168">Requirement</span></span> | <span data-ttu-id="4086b-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="4086b-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4086b-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4086b-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4086b-171">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4086b-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4086b-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4086b-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4086b-173">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4086b-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4086b-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="4086b-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="4086b-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4086b-176">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4086b-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="4086b-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4086b-178">DLL</span><span class="sxs-lookup"><span data-stu-id="4086b-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4086b-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4086b-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4086b-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4086b-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4086b-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4086b-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4086b-182">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="4086b-182">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="4086b-183">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="4086b-183">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="4086b-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4086b-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4086b-185">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="4086b-185">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="4086b-186">**glGet**</span><span class="sxs-lookup"><span data-stu-id="4086b-186">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4086b-187">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="4086b-187">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="4086b-188">**glListBase**</span><span class="sxs-lookup"><span data-stu-id="4086b-188">**glListBase**</span></span>](gllistbase.md)
</dt> <dt>

[<span data-ttu-id="4086b-189">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="4086b-189">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="4086b-190">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="4086b-190">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="4086b-191">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="4086b-191">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="4086b-192">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="4086b-192">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="4086b-193">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="4086b-193">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





