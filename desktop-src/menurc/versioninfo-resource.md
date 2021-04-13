---
title: Ressource VERSIONINFO
description: Définit une ressource d’informations sur la version. La ressource contient des informations sur le fichier en tant que son numéro de version, son système d’exploitation prévu et son nom de fichier d’origine. La ressource est destinée à être utilisée avec les fonctions d’informations de version.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menus de la ressource VERSIONINFO et autres ressources
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "104316716"
---
# <a name="versioninfo-resource"></a><span data-ttu-id="64a4d-106">Ressource VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="64a4d-106">VERSIONINFO resource</span></span>

<span data-ttu-id="64a4d-107">Définit une ressource d’informations sur la version.</span><span class="sxs-lookup"><span data-stu-id="64a4d-107">Defines a version-information resource.</span></span> <span data-ttu-id="64a4d-108">La ressource contient des informations sur le fichier en tant que son numéro de version, son système d’exploitation prévu et son nom de fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="64a4d-108">The resource contains such information about the file as its version number, its intended operating system, and its original filename.</span></span> <span data-ttu-id="64a4d-109">La ressource est destinée à être utilisée avec les fonctions d' [informations de version](./version-information.md) .</span><span class="sxs-lookup"><span data-stu-id="64a4d-109">The resource is intended to be used with the [Version Information](./version-information.md) functions.</span></span>

<span data-ttu-id="64a4d-110">Il existe deux façons de mettre en forme une instruction **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="64a4d-110">There are two ways to format a **VERSIONINFO** statement:</span></span>

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

<span data-ttu-id="64a4d-111">\- ou -</span><span class="sxs-lookup"><span data-stu-id="64a4d-111">\- or -</span></span>

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="64a4d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64a4d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64a4d-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span><span class="sxs-lookup"><span data-stu-id="64a4d-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-114">Identificateur de ressource des informations de version.</span><span class="sxs-lookup"><span data-stu-id="64a4d-114">Version-information resource identifier.</span></span> <span data-ttu-id="64a4d-115">Cette valeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="64a4d-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="64a4d-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*informations fixes*</span><span class="sxs-lookup"><span data-stu-id="64a4d-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-117">Les informations de version, telles que la version du fichier et le système d’exploitation prévu.</span><span class="sxs-lookup"><span data-stu-id="64a4d-117">Version information, such as the file version and the intended operating system.</span></span> <span data-ttu-id="64a4d-118">Ce paramètre est constitué des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-118">This parameter consists of the following statements.</span></span>



| <span data-ttu-id="64a4d-119">.</span><span class="sxs-lookup"><span data-stu-id="64a4d-119">Statement</span></span>                         | <span data-ttu-id="64a4d-120">Description</span><span class="sxs-lookup"><span data-stu-id="64a4d-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64a4d-121"> *Version* de FileVersion</span><span class="sxs-lookup"><span data-stu-id="64a4d-121">**FILEVERSION** *version*</span></span>         | <span data-ttu-id="64a4d-122">Numéro de version binaire du fichier.</span><span class="sxs-lookup"><span data-stu-id="64a4d-122">Binary version number for the file.</span></span> <span data-ttu-id="64a4d-123">La *version* se compose d’entiers 2 32 bits, définis par des entiers 4 16 bits.</span><span class="sxs-lookup"><span data-stu-id="64a4d-123">The *version* consists of two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="64a4d-124">Par exemple, « FILEVERSION 3, 10, 0, 61 » est traduit en deux mots doubles : 0x0003000a et 0x0000003d, dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="64a4d-124">For example, "FILEVERSION 3,10,0,61" is translated into two doublewords: 0x0003000a and 0x0000003d, in that order.</span></span> <span data-ttu-id="64a4d-125">Par conséquent, si la *version* est définie par les valeurs **DWORD** *DW1* et *DW2*, elles doivent apparaître dans l’instruction **FileVersion** comme suit : `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` .</span><span class="sxs-lookup"><span data-stu-id="64a4d-125">Therefore, if *version* is defined by the **DWORD** values *dw1* and *dw2*, they need to appear in the **FILEVERSION** statement as follows: `HIWORD(dw1)`, `LOWORD(dw1)`, `HIWORD(dw2)`, `LOWORD(dw2)`.</span></span> |
| <span data-ttu-id="64a4d-126"> *Version* de PRODUCTVERSION</span><span class="sxs-lookup"><span data-stu-id="64a4d-126">**PRODUCTVERSION** *version*</span></span>      | <span data-ttu-id="64a4d-127">Numéro de version binaire du produit avec lequel le fichier est distribué.</span><span class="sxs-lookup"><span data-stu-id="64a4d-127">Binary version number for the product with which the file is distributed.</span></span> <span data-ttu-id="64a4d-128">Le paramètre de *version* est un entier 2 32 bits, défini par des entiers 4 16 bits.</span><span class="sxs-lookup"><span data-stu-id="64a4d-128">The *version* parameter is two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="64a4d-129">Pour plus d’informations sur la *version*, consultez la description de **FileVersion** .</span><span class="sxs-lookup"><span data-stu-id="64a4d-129">For more information about *version*, see the **FILEVERSION** description.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="64a4d-130">**FILEFLAGSMASK** *FILEFLAGSMASK*</span><span class="sxs-lookup"><span data-stu-id="64a4d-130">**FILEFLAGSMASK** *fileflagsmask*</span></span> | <span data-ttu-id="64a4d-131">Indique les bits de l’instruction **FileFlags** qui sont valides.</span><span class="sxs-lookup"><span data-stu-id="64a4d-131">Indicates which bits in the **FILEFLAGS** statement are valid.</span></span> <span data-ttu-id="64a4d-132">Pour Windows 16 bits, cette valeur est 0x3F.</span><span class="sxs-lookup"><span data-stu-id="64a4d-132">For 16-bit Windows, this value is 0x3f.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="64a4d-133">**FileFlags FileFlags** </span><span class="sxs-lookup"><span data-stu-id="64a4d-133">**FILEFLAGS** *fileflags*</span></span>         | <span data-ttu-id="64a4d-134">Attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="64a4d-134">Attributes of the file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="64a4d-135">**Fichieros** </span><span class="sxs-lookup"><span data-stu-id="64a4d-135">**FILEOS** *fileos*</span></span>               | <span data-ttu-id="64a4d-136">Système d’exploitation pour lequel ce fichier a été conçu.</span><span class="sxs-lookup"><span data-stu-id="64a4d-136">Operating system for which this file was designed.</span></span> <span data-ttu-id="64a4d-137">Le paramètre *fileos* peut être l’une des valeurs de système d’exploitation spécifiées dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-137">The *fileos* parameter can be one of the operating system values given in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="64a4d-138">**Filetype type_fichier** </span><span class="sxs-lookup"><span data-stu-id="64a4d-138">**FILETYPE** *filetype*</span></span>           | <span data-ttu-id="64a4d-139">Type général de fichier.</span><span class="sxs-lookup"><span data-stu-id="64a4d-139">General type of file.</span></span> <span data-ttu-id="64a4d-140">Le paramètre *filetype* peut être l’une des valeurs de type de fichier listées dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-140">The *filetype* parameter can be one of the file type values listed in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="64a4d-141"> *Sous-type* FILESUBTYPE</span><span class="sxs-lookup"><span data-stu-id="64a4d-141">**FILESUBTYPE** *subtype*</span></span>         | <span data-ttu-id="64a4d-142">Fonction du fichier.</span><span class="sxs-lookup"><span data-stu-id="64a4d-142">Function of the file.</span></span> <span data-ttu-id="64a4d-143">Le paramètre *SubType* est égal à zéro, sauf si le paramètre *filetype* de l’instruction **FILETYPE** est VFT \_ DRV, VFT \_ font ou VFT \_ vxd.</span><span class="sxs-lookup"><span data-stu-id="64a4d-143">The *subtype* parameter is zero unless the *filetype* parameter in the **FILETYPE** statement is VFT\_DRV, VFT\_FONT, or VFT\_VXD.</span></span> <span data-ttu-id="64a4d-144">Pour obtenir la liste des valeurs de sous-type de fichier, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-144">For a list of file subtype values, see the Remarks section.</span></span>                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="64a4d-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*bloc-instruction*</span><span class="sxs-lookup"><span data-stu-id="64a4d-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-146">Spécifie un ou plusieurs blocs d’informations sur la version.</span><span class="sxs-lookup"><span data-stu-id="64a4d-146">Specifies one or more version-information blocks.</span></span> <span data-ttu-id="64a4d-147">Un bloc peut contenir des informations de chaîne ou des informations sur les variables.</span><span class="sxs-lookup"><span data-stu-id="64a4d-147">A block can contain string information or variable information.</span></span> <span data-ttu-id="64a4d-148">Pour plus d’informations, consultez bloc [**StringFileInfo**](stringfileinfo-block.md) ou [**bloc VarFileInfo**](varfileinfo-block.md).</span><span class="sxs-lookup"><span data-stu-id="64a4d-148">For more information, see [**StringFileInfo Block**](stringfileinfo-block.md) or [**VarFileInfo Block**](varfileinfo-block.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64a4d-149">Notes</span><span class="sxs-lookup"><span data-stu-id="64a4d-149">Remarks</span></span>

<span data-ttu-id="64a4d-150">Pour utiliser les constantes spécifiées avec l’instruction **VERSIONINFO** , vous devez inclure le fichier d’en-tête winver. h ou Windows. h dans le fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="64a4d-150">To use the constants specified with the **VERSIONINFO** statement, you must include the Winver.h or Windows.h header file in the resource-definition file.</span></span>

<span data-ttu-id="64a4d-151">La liste suivante décrit les paramètres utilisés dans l’instruction **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="64a4d-151">The following list describes the parameters used in the **VERSIONINFO** statement:</span></span>

<dl> <dt>

<span data-ttu-id="64a4d-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*FILEFLAGS*</span><span class="sxs-lookup"><span data-stu-id="64a4d-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-153">Combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-153">A combination of the following values.</span></span>



| <span data-ttu-id="64a4d-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a4d-154">Value</span></span>                      | <span data-ttu-id="64a4d-155">Description</span><span class="sxs-lookup"><span data-stu-id="64a4d-155">Description</span></span>                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64a4d-156">**débogage VS \_ FF \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-156">**VS\_FF\_DEBUG**</span></span>          | <span data-ttu-id="64a4d-157">Le fichier contient des informations de débogage ou est compilé avec les fonctionnalités de débogage activées.</span><span class="sxs-lookup"><span data-stu-id="64a4d-157">File contains debugging information or is compiled with debugging features enabled.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="64a4d-158">**VS \_ FF \_ corrigé**</span><span class="sxs-lookup"><span data-stu-id="64a4d-158">**VS\_FF\_PATCHED**</span></span>        | <span data-ttu-id="64a4d-159">Le fichier a été modifié et n’est pas identique au fichier d’envoi d’origine portant le même numéro de version.</span><span class="sxs-lookup"><span data-stu-id="64a4d-159">File has been modified and is not identical to the original shipping file of the same version number.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="64a4d-160">**\_ \_ version préliminaire de vs FF**</span><span class="sxs-lookup"><span data-stu-id="64a4d-160">**VS\_FF\_PRERELEASE**</span></span>     | <span data-ttu-id="64a4d-161">Le fichier est une version de développement, et non un produit commercialisé.</span><span class="sxs-lookup"><span data-stu-id="64a4d-161">File is a development version, not a commercially released product.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="64a4d-162">**VS \_ FF \_ PRIVATEBUILD**</span><span class="sxs-lookup"><span data-stu-id="64a4d-162">**VS\_FF\_PRIVATEBUILD**</span></span>   | <span data-ttu-id="64a4d-163">Le fichier n’a pas été créé à l’aide de procédures de version standard.</span><span class="sxs-lookup"><span data-stu-id="64a4d-163">File was not built using standard release procedures.</span></span> <span data-ttu-id="64a4d-164">Si cette valeur est donnée, le [**bloc StringFileInfo**](stringfileinfo-block.md) doit contenir une chaîne **PrivateBuild** .</span><span class="sxs-lookup"><span data-stu-id="64a4d-164">If this value is given, the [**StringFileInfo block**](stringfileinfo-block.md) must contain a **PrivateBuild** string.</span></span>                                                                                              |
| <span data-ttu-id="64a4d-165">**VS \_ FF \_ SPECIALBUILD**</span><span class="sxs-lookup"><span data-stu-id="64a4d-165">**VS\_FF\_SPECIALBUILD**</span></span>   | <span data-ttu-id="64a4d-166">Le fichier a été généré par la société d’origine à l’aide de procédures de version standard, mais il s’agit d’une variante du fichier standard du même numéro de version.</span><span class="sxs-lookup"><span data-stu-id="64a4d-166">File was built by the original company using standard release procedures but is a variation of the standard file of the same version number.</span></span> <span data-ttu-id="64a4d-167">Si cette valeur est donnée, le bloc de [bloc **StringFileInfo**](stringfileinfo-block.md) doit contenir une chaîne **SpecialBuild** .</span><span class="sxs-lookup"><span data-stu-id="64a4d-167">If this value is given, the [**StringFileInfo** block](stringfileinfo-block.md) block must contain a **SpecialBuild** string.</span></span> |
| <span data-ttu-id="64a4d-168">**VS \_ FFI \_ FILEFLAGSMASK**</span><span class="sxs-lookup"><span data-stu-id="64a4d-168">**VS\_FFI\_FILEFLAGSMASK**</span></span> | <span data-ttu-id="64a4d-169">Combinaison de toutes les valeurs précédentes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-169">A combination of all the preceding values.</span></span>                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="64a4d-170"><span id="fileos"></span><span id="FILEOS"></span>*fichieros*</span><span class="sxs-lookup"><span data-stu-id="64a4d-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-171">Une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-171">One of the following values.</span></span>



| <span data-ttu-id="64a4d-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a4d-172">Value</span></span>                   | <span data-ttu-id="64a4d-173">Description</span><span class="sxs-lookup"><span data-stu-id="64a4d-173">Description</span></span>                                                      |
|-------------------------|------------------------------------------------------------------|
| <span data-ttu-id="64a4d-174">**VOS \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="64a4d-174">**VOS\_UNKNOWN**</span></span>        | <span data-ttu-id="64a4d-175">Le système d’exploitation pour lequel le fichier a été conçu est inconnu.</span><span class="sxs-lookup"><span data-stu-id="64a4d-175">The operating system for which the file was designed is unknown.</span></span> |
| <span data-ttu-id="64a4d-176">**VOS \_ dos**</span><span class="sxs-lookup"><span data-stu-id="64a4d-176">**VOS\_DOS**</span></span>            | <span data-ttu-id="64a4d-177">Le fichier a été conçu pour MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="64a4d-177">File was designed for MS-DOS.</span></span>                                    |
| <span data-ttu-id="64a4d-178">**VOS \_ NT**</span><span class="sxs-lookup"><span data-stu-id="64a4d-178">**VOS\_NT**</span></span>             | <span data-ttu-id="64a4d-179">Le fichier a été conçu pour Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="64a4d-179">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="64a4d-180">**VOS \_ \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="64a4d-180">**VOS\_\_WINDOWS16**</span></span>    | <span data-ttu-id="64a4d-181">Le fichier a été conçu pour Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="64a4d-181">File was designed for 16-bit Windows.</span></span>                            |
| <span data-ttu-id="64a4d-182">**VOS \_ \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="64a4d-182">**VOS\_\_WINDOWS32**</span></span>    | <span data-ttu-id="64a4d-183">Le fichier a été conçu pour Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="64a4d-183">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="64a4d-184">**VOS \_ dos \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="64a4d-184">**VOS\_DOS\_WINDOWS16**</span></span> | <span data-ttu-id="64a4d-185">Le fichier a été conçu pour Windows 16 bits s’exécutant avec MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="64a4d-185">File was designed for 16-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="64a4d-186">**VOS \_ dos \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="64a4d-186">**VOS\_DOS\_WINDOWS32**</span></span> | <span data-ttu-id="64a4d-187">Le fichier a été conçu pour Windows 32 bits s’exécutant avec MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="64a4d-187">File was designed for 32-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="64a4d-188">**VOS \_ NT \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="64a4d-188">**VOS\_NT\_WINDOWS32**</span></span>  | <span data-ttu-id="64a4d-189">Le fichier a été conçu pour Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="64a4d-189">File was designed for 32-bit Windows.</span></span>                            |



 

<span data-ttu-id="64a4d-190">Les valeurs 0x00002L, 0x00003L, 0x20000L et 0x30000L sont réservées.</span><span class="sxs-lookup"><span data-stu-id="64a4d-190">The values 0x00002L, 0x00003L, 0x20000L and 0x30000L are reserved.</span></span>

</dd> <dt>

<span data-ttu-id="64a4d-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span><span class="sxs-lookup"><span data-stu-id="64a4d-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-192">Une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-192">One of the following values.</span></span>



| <span data-ttu-id="64a4d-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a4d-193">Value</span></span>                | <span data-ttu-id="64a4d-194">Description</span><span class="sxs-lookup"><span data-stu-id="64a4d-194">Description</span></span>                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64a4d-195">**VFT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="64a4d-195">**VFT\_UNKNOWN**</span></span>     | <span data-ttu-id="64a4d-196">Le type de fichier est inconnu.</span><span class="sxs-lookup"><span data-stu-id="64a4d-196">File type is unknown.</span></span>                                                                                                       |
| <span data-ttu-id="64a4d-197">**\_application VFT**</span><span class="sxs-lookup"><span data-stu-id="64a4d-197">**VFT\_APP**</span></span>         | <span data-ttu-id="64a4d-198">Le fichier contient une application.</span><span class="sxs-lookup"><span data-stu-id="64a4d-198">File contains an application.</span></span>                                                                                               |
| <span data-ttu-id="64a4d-199">**\_dll VFT**</span><span class="sxs-lookup"><span data-stu-id="64a4d-199">**VFT\_DLL**</span></span>         | <span data-ttu-id="64a4d-200">Le fichier contient une bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="64a4d-200">File contains a dynamic-link library (DLL).</span></span>                                                                                 |
| <span data-ttu-id="64a4d-201">**VFT \_ DRV**</span><span class="sxs-lookup"><span data-stu-id="64a4d-201">**VFT\_DRV**</span></span>         | <span data-ttu-id="64a4d-202">Le fichier contient un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="64a4d-202">File contains a device driver.</span></span> <span data-ttu-id="64a4d-203">Si *filetype* est **VFT \_ DRV**, *SubType* contient une description plus spécifique du pilote.</span><span class="sxs-lookup"><span data-stu-id="64a4d-203">If *filetype* is **VFT\_DRV**, *subtype* contains a more specific description of the driver.</span></span> |
| <span data-ttu-id="64a4d-204">**\_police VFT**</span><span class="sxs-lookup"><span data-stu-id="64a4d-204">**VFT\_FONT**</span></span>        | <span data-ttu-id="64a4d-205">Le fichier contient une police.</span><span class="sxs-lookup"><span data-stu-id="64a4d-205">File contains a font.</span></span> <span data-ttu-id="64a4d-206">Si *filetype* est \_ la police VFT *, SubType* contient une description plus spécifique de la police.</span><span class="sxs-lookup"><span data-stu-id="64a4d-206">If *filetype* is VFT\_FONT, *subtype* contains a more specific description of the font.</span></span>               |
| <span data-ttu-id="64a4d-207">**VFT \_ vxd**</span><span class="sxs-lookup"><span data-stu-id="64a4d-207">**VFT\_VXD**</span></span>         | <span data-ttu-id="64a4d-208">Le fichier contient un appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="64a4d-208">File contains a virtual device.</span></span>                                                                                             |
| <span data-ttu-id="64a4d-209">**VFT \_ static \_ lib**</span><span class="sxs-lookup"><span data-stu-id="64a4d-209">**VFT\_STATIC\_LIB**</span></span> | <span data-ttu-id="64a4d-210">Le fichier contient une bibliothèque de liens statiques.</span><span class="sxs-lookup"><span data-stu-id="64a4d-210">File contains a static-link library.</span></span>                                                                                        |



 

<span data-ttu-id="64a4d-211">Toutes les autres valeurs sont réservées à une utilisation par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64a4d-211">All other values are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="64a4d-212"><span id="subtype"></span><span id="SUBTYPE"></span>*sous-type*</span><span class="sxs-lookup"><span data-stu-id="64a4d-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtype*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-213">Informations supplémentaires sur le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="64a4d-213">Additional information about the file type.</span></span>

<span data-ttu-id="64a4d-214">Si *filetype* spécifie **VFT \_ DRV**, ce paramètre peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-214">If *filetype* specifies **VFT\_DRV**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="64a4d-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a4d-215">Value</span></span>                             | <span data-ttu-id="64a4d-216">Description</span><span class="sxs-lookup"><span data-stu-id="64a4d-216">Description</span></span>                               |
|-----------------------------------|-------------------------------------------|
| <span data-ttu-id="64a4d-217">**VFT2 \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="64a4d-217">**VFT2\_UNKNOWN**</span></span>                 | <span data-ttu-id="64a4d-218">Le type de pilote est inconnu.</span><span class="sxs-lookup"><span data-stu-id="64a4d-218">Driver type is unknown.</span></span>                   |
| <span data-ttu-id="64a4d-219">**VFT2 \_ DRV \_ comm**</span><span class="sxs-lookup"><span data-stu-id="64a4d-219">**VFT2\_DRV\_COMM**</span></span>               | <span data-ttu-id="64a4d-220">Le fichier contient un pilote de communication.</span><span class="sxs-lookup"><span data-stu-id="64a4d-220">File contains a communications driver.</span></span>    |
| <span data-ttu-id="64a4d-221">**\_Imprimante VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-221">**VFT2\_DRV\_PRINTER**</span></span>            | <span data-ttu-id="64a4d-222">Le fichier contient un pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="64a4d-222">File contains a printer driver.</span></span>           |
| <span data-ttu-id="64a4d-223">**\_Clavier VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-223">**VFT2\_DRV\_KEYBOARD**</span></span>           | <span data-ttu-id="64a4d-224">Le fichier contient un pilote de clavier.</span><span class="sxs-lookup"><span data-stu-id="64a4d-224">File contains a keyboard driver.</span></span>          |
| <span data-ttu-id="64a4d-225">**\_Langage VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-225">**VFT2\_DRV\_LANGUAGE**</span></span>           | <span data-ttu-id="64a4d-226">Le fichier contient un pilote de langage.</span><span class="sxs-lookup"><span data-stu-id="64a4d-226">File contains a language driver.</span></span>          |
| <span data-ttu-id="64a4d-227">**\_Affichage du DRV VFT2 \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-227">**VFT2\_DRV\_DISPLAY**</span></span>            | <span data-ttu-id="64a4d-228">Le fichier contient un pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="64a4d-228">File contains a display driver.</span></span>           |
| <span data-ttu-id="64a4d-229">**\_Souris VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-229">**VFT2\_DRV\_MOUSE**</span></span>              | <span data-ttu-id="64a4d-230">Le fichier contient un pilote de souris.</span><span class="sxs-lookup"><span data-stu-id="64a4d-230">File contains a mouse driver.</span></span>             |
| <span data-ttu-id="64a4d-231">**\_Réseau VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-231">**VFT2\_DRV\_NETWORK**</span></span>            | <span data-ttu-id="64a4d-232">Le fichier contient un pilote réseau.</span><span class="sxs-lookup"><span data-stu-id="64a4d-232">File contains a network driver.</span></span>           |
| <span data-ttu-id="64a4d-233">**\_Système VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-233">**VFT2\_DRV\_SYSTEM**</span></span>             | <span data-ttu-id="64a4d-234">Le fichier contient un pilote système.</span><span class="sxs-lookup"><span data-stu-id="64a4d-234">File contains a system driver.</span></span>            |
| <span data-ttu-id="64a4d-235">**VFT2 \_ DRV \_ installable**</span><span class="sxs-lookup"><span data-stu-id="64a4d-235">**VFT2\_DRV\_INSTALLABLE**</span></span>        | <span data-ttu-id="64a4d-236">Le fichier contient un pilote installable.</span><span class="sxs-lookup"><span data-stu-id="64a4d-236">File contains an installable driver.</span></span>      |
| <span data-ttu-id="64a4d-237">**VFT2 \_ DRV \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-237">**VFT2\_DRV\_SOUND**</span></span>              | <span data-ttu-id="64a4d-238">Le fichier contient un pilote audio.</span><span class="sxs-lookup"><span data-stu-id="64a4d-238">File contains a sound driver.</span></span>             |
| <span data-ttu-id="64a4d-239">**Imprimante avec version de VFT2 \_ DRV \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-239">**VFT2\_DRV\_VERSIONED\_PRINTER**</span></span> | <span data-ttu-id="64a4d-240">Le fichier contient un pilote d’imprimante avec version.</span><span class="sxs-lookup"><span data-stu-id="64a4d-240">File contains a versioned printer driver.</span></span> |



 

<span data-ttu-id="64a4d-241">Si *filetype* spécifie la **\_ police VFT**, ce paramètre peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64a4d-241">If *filetype* specifies **VFT\_FONT**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="64a4d-242">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a4d-242">Value</span></span>                    | <span data-ttu-id="64a4d-243">Description</span><span class="sxs-lookup"><span data-stu-id="64a4d-243">Description</span></span>                    |
|--------------------------|--------------------------------|
| <span data-ttu-id="64a4d-244">**VFT2 \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="64a4d-244">**VFT2\_UNKNOWN**</span></span>        | <span data-ttu-id="64a4d-245">Le type de police est inconnu.</span><span class="sxs-lookup"><span data-stu-id="64a4d-245">Font type is unknown.</span></span>          |
| <span data-ttu-id="64a4d-246">**VFT2 de \_ police \_ Raster**</span><span class="sxs-lookup"><span data-stu-id="64a4d-246">**VFT2\_FONT\_RASTER**</span></span>   | <span data-ttu-id="64a4d-247">Le fichier contient une police raster.</span><span class="sxs-lookup"><span data-stu-id="64a4d-247">File contains a raster font.</span></span>   |
| <span data-ttu-id="64a4d-248">**\_Vecteur de police VFT2 \_**</span><span class="sxs-lookup"><span data-stu-id="64a4d-248">**VFT2\_FONT\_VECTOR**</span></span>   | <span data-ttu-id="64a4d-249">Le fichier contient une police vectorielle.</span><span class="sxs-lookup"><span data-stu-id="64a4d-249">File contains a vector font.</span></span>   |
| <span data-ttu-id="64a4d-250">**VFT2 \_ police \_ TrueType**</span><span class="sxs-lookup"><span data-stu-id="64a4d-250">**VFT2\_FONT\_TRUETYPE**</span></span> | <span data-ttu-id="64a4d-251">Le fichier contient une police TrueType.</span><span class="sxs-lookup"><span data-stu-id="64a4d-251">File contains a TrueType font.</span></span> |



 

<span data-ttu-id="64a4d-252">Si *filetype* spécifie VFT \_ vxd, ce paramètre doit être l’identificateur de l’appareil virtuel inclus dans le bloc de contrôle de l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="64a4d-252">If *filetype* specifies VFT\_VXD, this parameter must be the virtual-device identifier included in the virtual-device control block.</span></span>

<span data-ttu-id="64a4d-253">Toutes les valeurs de *sous-type* non répertoriées ici sont réservées à une utilisation par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64a4d-253">All *subtype* values not listed here are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="64a4d-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="64a4d-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-255">L’un des codes de langue suivants.</span><span class="sxs-lookup"><span data-stu-id="64a4d-255">One of the following language codes.</span></span>



| <span data-ttu-id="64a4d-256">Code</span><span class="sxs-lookup"><span data-stu-id="64a4d-256">Code</span></span>   | <span data-ttu-id="64a4d-257">Langage</span><span class="sxs-lookup"><span data-stu-id="64a4d-257">Language</span></span>            | <span data-ttu-id="64a4d-258">Code</span><span class="sxs-lookup"><span data-stu-id="64a4d-258">Code</span></span>   | <span data-ttu-id="64a4d-259">Langage</span><span class="sxs-lookup"><span data-stu-id="64a4d-259">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="64a4d-260">0x0401</span><span class="sxs-lookup"><span data-stu-id="64a4d-260">0x0401</span></span> | <span data-ttu-id="64a4d-261">Arabe</span><span class="sxs-lookup"><span data-stu-id="64a4d-261">Arabic</span></span>              | <span data-ttu-id="64a4d-262">0x0415</span><span class="sxs-lookup"><span data-stu-id="64a4d-262">0x0415</span></span> | <span data-ttu-id="64a4d-263">Polonais</span><span class="sxs-lookup"><span data-stu-id="64a4d-263">Polish</span></span>                    |
| <span data-ttu-id="64a4d-264">0x0402</span><span class="sxs-lookup"><span data-stu-id="64a4d-264">0x0402</span></span> | <span data-ttu-id="64a4d-265">Bulgare</span><span class="sxs-lookup"><span data-stu-id="64a4d-265">Bulgarian</span></span>           | <span data-ttu-id="64a4d-266">0x0416</span><span class="sxs-lookup"><span data-stu-id="64a4d-266">0x0416</span></span> | <span data-ttu-id="64a4d-267">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="64a4d-267">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="64a4d-268">0x0403</span><span class="sxs-lookup"><span data-stu-id="64a4d-268">0x0403</span></span> | <span data-ttu-id="64a4d-269">Catalan</span><span class="sxs-lookup"><span data-stu-id="64a4d-269">Catalan</span></span>             | <span data-ttu-id="64a4d-270">0x0417</span><span class="sxs-lookup"><span data-stu-id="64a4d-270">0x0417</span></span> | <span data-ttu-id="64a4d-271">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="64a4d-271">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="64a4d-272">0x0404</span><span class="sxs-lookup"><span data-stu-id="64a4d-272">0x0404</span></span> | <span data-ttu-id="64a4d-273">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="64a4d-273">Traditional Chinese</span></span> | <span data-ttu-id="64a4d-274">0x0418</span><span class="sxs-lookup"><span data-stu-id="64a4d-274">0x0418</span></span> | <span data-ttu-id="64a4d-275">Roumain</span><span class="sxs-lookup"><span data-stu-id="64a4d-275">Romanian</span></span>                  |
| <span data-ttu-id="64a4d-276">0x0405</span><span class="sxs-lookup"><span data-stu-id="64a4d-276">0x0405</span></span> | <span data-ttu-id="64a4d-277">Tchèque</span><span class="sxs-lookup"><span data-stu-id="64a4d-277">Czech</span></span>               | <span data-ttu-id="64a4d-278">0x0419</span><span class="sxs-lookup"><span data-stu-id="64a4d-278">0x0419</span></span> | <span data-ttu-id="64a4d-279">Russe</span><span class="sxs-lookup"><span data-stu-id="64a4d-279">Russian</span></span>                   |
| <span data-ttu-id="64a4d-280">0x0406</span><span class="sxs-lookup"><span data-stu-id="64a4d-280">0x0406</span></span> | <span data-ttu-id="64a4d-281">Danois</span><span class="sxs-lookup"><span data-stu-id="64a4d-281">Danish</span></span>              | <span data-ttu-id="64a4d-282">0x041A</span><span class="sxs-lookup"><span data-stu-id="64a4d-282">0x041A</span></span> | <span data-ttu-id="64a4d-283">Croato-Serbian (latin)</span><span class="sxs-lookup"><span data-stu-id="64a4d-283">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="64a4d-284">0x0407</span><span class="sxs-lookup"><span data-stu-id="64a4d-284">0x0407</span></span> | <span data-ttu-id="64a4d-285">Allemand</span><span class="sxs-lookup"><span data-stu-id="64a4d-285">German</span></span>              | <span data-ttu-id="64a4d-286">0x041B</span><span class="sxs-lookup"><span data-stu-id="64a4d-286">0x041B</span></span> | <span data-ttu-id="64a4d-287">Slovaque</span><span class="sxs-lookup"><span data-stu-id="64a4d-287">Slovak</span></span>                    |
| <span data-ttu-id="64a4d-288">0x0408</span><span class="sxs-lookup"><span data-stu-id="64a4d-288">0x0408</span></span> | <span data-ttu-id="64a4d-289">Grec</span><span class="sxs-lookup"><span data-stu-id="64a4d-289">Greek</span></span>               | <span data-ttu-id="64a4d-290">0x041C</span><span class="sxs-lookup"><span data-stu-id="64a4d-290">0x041C</span></span> | <span data-ttu-id="64a4d-291">Albanais</span><span class="sxs-lookup"><span data-stu-id="64a4d-291">Albanian</span></span>                  |
| <span data-ttu-id="64a4d-292">0x0409</span><span class="sxs-lookup"><span data-stu-id="64a4d-292">0x0409</span></span> | <span data-ttu-id="64a4d-293">Anglais (États-Unis)</span><span class="sxs-lookup"><span data-stu-id="64a4d-293">U.S. English</span></span>        | <span data-ttu-id="64a4d-294">0x041D</span><span class="sxs-lookup"><span data-stu-id="64a4d-294">0x041D</span></span> | <span data-ttu-id="64a4d-295">Suédois</span><span class="sxs-lookup"><span data-stu-id="64a4d-295">Swedish</span></span>                   |
| <span data-ttu-id="64a4d-296">0x040A</span><span class="sxs-lookup"><span data-stu-id="64a4d-296">0x040A</span></span> | <span data-ttu-id="64a4d-297">Espagnol castillan</span><span class="sxs-lookup"><span data-stu-id="64a4d-297">Castilian Spanish</span></span>   | <span data-ttu-id="64a4d-298">0x041E</span><span class="sxs-lookup"><span data-stu-id="64a4d-298">0x041E</span></span> | <span data-ttu-id="64a4d-299">Thaï</span><span class="sxs-lookup"><span data-stu-id="64a4d-299">Thai</span></span>                      |
| <span data-ttu-id="64a4d-300">0x040B</span><span class="sxs-lookup"><span data-stu-id="64a4d-300">0x040B</span></span> | <span data-ttu-id="64a4d-301">Finnois</span><span class="sxs-lookup"><span data-stu-id="64a4d-301">Finnish</span></span>             | <span data-ttu-id="64a4d-302">0x041F</span><span class="sxs-lookup"><span data-stu-id="64a4d-302">0x041F</span></span> | <span data-ttu-id="64a4d-303">Turc</span><span class="sxs-lookup"><span data-stu-id="64a4d-303">Turkish</span></span>                   |
| <span data-ttu-id="64a4d-304">0x040C</span><span class="sxs-lookup"><span data-stu-id="64a4d-304">0x040C</span></span> | <span data-ttu-id="64a4d-305">Français</span><span class="sxs-lookup"><span data-stu-id="64a4d-305">French</span></span>              | <span data-ttu-id="64a4d-306">0x0420</span><span class="sxs-lookup"><span data-stu-id="64a4d-306">0x0420</span></span> | <span data-ttu-id="64a4d-307">Ourdou</span><span class="sxs-lookup"><span data-stu-id="64a4d-307">Urdu</span></span>                      |
| <span data-ttu-id="64a4d-308">0x040D</span><span class="sxs-lookup"><span data-stu-id="64a4d-308">0x040D</span></span> | <span data-ttu-id="64a4d-309">Hébreu</span><span class="sxs-lookup"><span data-stu-id="64a4d-309">Hebrew</span></span>              | <span data-ttu-id="64a4d-310">0x0421</span><span class="sxs-lookup"><span data-stu-id="64a4d-310">0x0421</span></span> | <span data-ttu-id="64a4d-311">Bahasa</span><span class="sxs-lookup"><span data-stu-id="64a4d-311">Bahasa</span></span>                    |
| <span data-ttu-id="64a4d-312">0x040E</span><span class="sxs-lookup"><span data-stu-id="64a4d-312">0x040E</span></span> | <span data-ttu-id="64a4d-313">Hongrois</span><span class="sxs-lookup"><span data-stu-id="64a4d-313">Hungarian</span></span>           | <span data-ttu-id="64a4d-314">0x0804</span><span class="sxs-lookup"><span data-stu-id="64a4d-314">0x0804</span></span> | <span data-ttu-id="64a4d-315">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="64a4d-315">Simplified Chinese</span></span>        |
| <span data-ttu-id="64a4d-316">0x040F</span><span class="sxs-lookup"><span data-stu-id="64a4d-316">0x040F</span></span> | <span data-ttu-id="64a4d-317">Islandais</span><span class="sxs-lookup"><span data-stu-id="64a4d-317">Icelandic</span></span>           | <span data-ttu-id="64a4d-318">0x0807</span><span class="sxs-lookup"><span data-stu-id="64a4d-318">0x0807</span></span> | <span data-ttu-id="64a4d-319">Allemand Suisse</span><span class="sxs-lookup"><span data-stu-id="64a4d-319">Swiss German</span></span>              |
| <span data-ttu-id="64a4d-320">0x0410</span><span class="sxs-lookup"><span data-stu-id="64a4d-320">0x0410</span></span> | <span data-ttu-id="64a4d-321">Italien</span><span class="sxs-lookup"><span data-stu-id="64a4d-321">Italian</span></span>             | <span data-ttu-id="64a4d-322">0x0809</span><span class="sxs-lookup"><span data-stu-id="64a4d-322">0x0809</span></span> | <span data-ttu-id="64a4d-323">au Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="64a4d-323">U.K.</span></span> <span data-ttu-id="64a4d-324">Anglais</span><span class="sxs-lookup"><span data-stu-id="64a4d-324">English</span></span>              |
| <span data-ttu-id="64a4d-325">0x0411</span><span class="sxs-lookup"><span data-stu-id="64a4d-325">0x0411</span></span> | <span data-ttu-id="64a4d-326">Japonais</span><span class="sxs-lookup"><span data-stu-id="64a4d-326">Japanese</span></span>            | <span data-ttu-id="64a4d-327">0x080A</span><span class="sxs-lookup"><span data-stu-id="64a4d-327">0x080A</span></span> | <span data-ttu-id="64a4d-328">Espagnol (Mexique)</span><span class="sxs-lookup"><span data-stu-id="64a4d-328">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="64a4d-329">0x0412</span><span class="sxs-lookup"><span data-stu-id="64a4d-329">0x0412</span></span> | <span data-ttu-id="64a4d-330">Coréen</span><span class="sxs-lookup"><span data-stu-id="64a4d-330">Korean</span></span>              | <span data-ttu-id="64a4d-331">0x080C</span><span class="sxs-lookup"><span data-stu-id="64a4d-331">0x080C</span></span> | <span data-ttu-id="64a4d-332">Français belge</span><span class="sxs-lookup"><span data-stu-id="64a4d-332">Belgian French</span></span>            |
| <span data-ttu-id="64a4d-333">0x0413</span><span class="sxs-lookup"><span data-stu-id="64a4d-333">0x0413</span></span> | <span data-ttu-id="64a4d-334">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="64a4d-334">Dutch</span></span>               | <span data-ttu-id="64a4d-335">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="64a4d-335">0x0C0C</span></span> | <span data-ttu-id="64a4d-336">Français (Canada)</span><span class="sxs-lookup"><span data-stu-id="64a4d-336">Canadian French</span></span>           |
| <span data-ttu-id="64a4d-337">0x0414</span><span class="sxs-lookup"><span data-stu-id="64a4d-337">0x0414</span></span> | <span data-ttu-id="64a4d-338">Norvégien?</span><span class="sxs-lookup"><span data-stu-id="64a4d-338">Norwegian ?</span></span> <span data-ttu-id="64a4d-339">Bokmal</span><span class="sxs-lookup"><span data-stu-id="64a4d-339">Bokmal</span></span>  | <span data-ttu-id="64a4d-340">0x100C</span><span class="sxs-lookup"><span data-stu-id="64a4d-340">0x100C</span></span> | <span data-ttu-id="64a4d-341">Français Suisse</span><span class="sxs-lookup"><span data-stu-id="64a4d-341">Swiss French</span></span>              |
| <span data-ttu-id="64a4d-342">0x0810</span><span class="sxs-lookup"><span data-stu-id="64a4d-342">0x0810</span></span> | <span data-ttu-id="64a4d-343">Italien Suisse</span><span class="sxs-lookup"><span data-stu-id="64a4d-343">Swiss Italian</span></span>       | <span data-ttu-id="64a4d-344">0x0816</span><span class="sxs-lookup"><span data-stu-id="64a4d-344">0x0816</span></span> | <span data-ttu-id="64a4d-345">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="64a4d-345">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="64a4d-346">0x0813</span><span class="sxs-lookup"><span data-stu-id="64a4d-346">0x0813</span></span> | <span data-ttu-id="64a4d-347">Néerlandais (Belgique)</span><span class="sxs-lookup"><span data-stu-id="64a4d-347">Belgian Dutch</span></span>       | <span data-ttu-id="64a4d-348">0x081A</span><span class="sxs-lookup"><span data-stu-id="64a4d-348">0x081A</span></span> | <span data-ttu-id="64a4d-349">Serbo-Croatian (cyrillique)</span><span class="sxs-lookup"><span data-stu-id="64a4d-349">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="64a4d-350">0x0814</span><span class="sxs-lookup"><span data-stu-id="64a4d-350">0x0814</span></span> | <span data-ttu-id="64a4d-351">Norvégien?</span><span class="sxs-lookup"><span data-stu-id="64a4d-351">Norwegian ?</span></span> <span data-ttu-id="64a4d-352">Nynorsk</span><span class="sxs-lookup"><span data-stu-id="64a4d-352">Nynorsk</span></span> |        |                           |



 

</dd> <dt>

<span data-ttu-id="64a4d-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="64a4d-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-354">Un des identificateurs de jeu de caractères suivants.</span><span class="sxs-lookup"><span data-stu-id="64a4d-354">One of the following character-set identifiers.</span></span>



| <span data-ttu-id="64a4d-355">Decimal</span><span class="sxs-lookup"><span data-stu-id="64a4d-355">Decimal</span></span> | <span data-ttu-id="64a4d-356">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="64a4d-356">Hexadecimal</span></span> | <span data-ttu-id="64a4d-357">Jeu de caractères</span><span class="sxs-lookup"><span data-stu-id="64a4d-357">Character Set</span></span>              |
|---------|-------------|----------------------------|
| <span data-ttu-id="64a4d-358">0</span><span class="sxs-lookup"><span data-stu-id="64a4d-358">0</span></span>       | <span data-ttu-id="64a4d-359">0000</span><span class="sxs-lookup"><span data-stu-id="64a4d-359">0000</span></span>        | <span data-ttu-id="64a4d-360">ASCII 7 bits</span><span class="sxs-lookup"><span data-stu-id="64a4d-360">7-bit ASCII</span></span>                |
| <span data-ttu-id="64a4d-361">932</span><span class="sxs-lookup"><span data-stu-id="64a4d-361">932</span></span>     | <span data-ttu-id="64a4d-362">03A4</span><span class="sxs-lookup"><span data-stu-id="64a4d-362">03A4</span></span>        | <span data-ttu-id="64a4d-363">Le Japon (Maj ?</span><span class="sxs-lookup"><span data-stu-id="64a4d-363">Japan (Shift ?</span></span> <span data-ttu-id="64a4d-364">JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="64a4d-364">JIS X-0208)</span></span> |
| <span data-ttu-id="64a4d-365">949</span><span class="sxs-lookup"><span data-stu-id="64a4d-365">949</span></span>     | <span data-ttu-id="64a4d-366">03B5</span><span class="sxs-lookup"><span data-stu-id="64a4d-366">03B5</span></span>        | <span data-ttu-id="64a4d-367">Corée (Maj ?</span><span class="sxs-lookup"><span data-stu-id="64a4d-367">Korea (Shift ?</span></span> <span data-ttu-id="64a4d-368">KSC 5601)</span><span class="sxs-lookup"><span data-stu-id="64a4d-368">KSC 5601)</span></span>   |
| <span data-ttu-id="64a4d-369">950</span><span class="sxs-lookup"><span data-stu-id="64a4d-369">950</span></span>     | <span data-ttu-id="64a4d-370">03B6</span><span class="sxs-lookup"><span data-stu-id="64a4d-370">03B6</span></span>        | <span data-ttu-id="64a4d-371">Taïwan (Big5)</span><span class="sxs-lookup"><span data-stu-id="64a4d-371">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="64a4d-372">1200</span><span class="sxs-lookup"><span data-stu-id="64a4d-372">1200</span></span>    | <span data-ttu-id="64a4d-373">04B0</span><span class="sxs-lookup"><span data-stu-id="64a4d-373">04B0</span></span>        | <span data-ttu-id="64a4d-374">Unicode</span><span class="sxs-lookup"><span data-stu-id="64a4d-374">Unicode</span></span>                    |
| <span data-ttu-id="64a4d-375">1250</span><span class="sxs-lookup"><span data-stu-id="64a4d-375">1250</span></span>    | <span data-ttu-id="64a4d-376">04E2</span><span class="sxs-lookup"><span data-stu-id="64a4d-376">04E2</span></span>        | <span data-ttu-id="64a4d-377">Latin-2 (Europe de l’est)</span><span class="sxs-lookup"><span data-stu-id="64a4d-377">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="64a4d-378">1251</span><span class="sxs-lookup"><span data-stu-id="64a4d-378">1251</span></span>    | <span data-ttu-id="64a4d-379">04E3</span><span class="sxs-lookup"><span data-stu-id="64a4d-379">04E3</span></span>        | <span data-ttu-id="64a4d-380">Cyrillique</span><span class="sxs-lookup"><span data-stu-id="64a4d-380">Cyrillic</span></span>                   |
| <span data-ttu-id="64a4d-381">1252</span><span class="sxs-lookup"><span data-stu-id="64a4d-381">1252</span></span>    | <span data-ttu-id="64a4d-382">04E4</span><span class="sxs-lookup"><span data-stu-id="64a4d-382">04E4</span></span>        | <span data-ttu-id="64a4d-383">Multilingue</span><span class="sxs-lookup"><span data-stu-id="64a4d-383">Multilingual</span></span>               |
| <span data-ttu-id="64a4d-384">1253</span><span class="sxs-lookup"><span data-stu-id="64a4d-384">1253</span></span>    | <span data-ttu-id="64a4d-385">04E5</span><span class="sxs-lookup"><span data-stu-id="64a4d-385">04E5</span></span>        | <span data-ttu-id="64a4d-386">Grec</span><span class="sxs-lookup"><span data-stu-id="64a4d-386">Greek</span></span>                      |
| <span data-ttu-id="64a4d-387">1254</span><span class="sxs-lookup"><span data-stu-id="64a4d-387">1254</span></span>    | <span data-ttu-id="64a4d-388">04E6</span><span class="sxs-lookup"><span data-stu-id="64a4d-388">04E6</span></span>        | <span data-ttu-id="64a4d-389">Turc</span><span class="sxs-lookup"><span data-stu-id="64a4d-389">Turkish</span></span>                    |
| <span data-ttu-id="64a4d-390">1 255</span><span class="sxs-lookup"><span data-stu-id="64a4d-390">1255</span></span>    | <span data-ttu-id="64a4d-391">04E7</span><span class="sxs-lookup"><span data-stu-id="64a4d-391">04E7</span></span>        | <span data-ttu-id="64a4d-392">Hébreu</span><span class="sxs-lookup"><span data-stu-id="64a4d-392">Hebrew</span></span>                     |
| <span data-ttu-id="64a4d-393">1256</span><span class="sxs-lookup"><span data-stu-id="64a4d-393">1256</span></span>    | <span data-ttu-id="64a4d-394">04E8</span><span class="sxs-lookup"><span data-stu-id="64a4d-394">04E8</span></span>        | <span data-ttu-id="64a4d-395">Arabe</span><span class="sxs-lookup"><span data-stu-id="64a4d-395">Arabic</span></span>                     |



 

</dd> <dt>

<span data-ttu-id="64a4d-396"><span id="string-name"></span><span id="STRING-NAME"></span>*nom de chaîne*</span><span class="sxs-lookup"><span data-stu-id="64a4d-396"><span id="string-name"></span><span id="STRING-NAME"></span>*string-name*</span></span>
</dt> <dd>

<span data-ttu-id="64a4d-397">L’un des noms prédéfinis suivants.</span><span class="sxs-lookup"><span data-stu-id="64a4d-397">One of the following predefined names.</span></span>



| <span data-ttu-id="64a4d-398">Nom</span><span class="sxs-lookup"><span data-stu-id="64a4d-398">Name</span></span>                 | <span data-ttu-id="64a4d-399">Description</span><span class="sxs-lookup"><span data-stu-id="64a4d-399">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64a4d-400">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="64a4d-400">**Comments**</span></span>         | <span data-ttu-id="64a4d-401">Informations supplémentaires à afficher à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="64a4d-401">Additional information that should be displayed for diagnostic purposes.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="64a4d-402">**Prennent**</span><span class="sxs-lookup"><span data-stu-id="64a4d-402">**CompanyName**</span></span>      | <span data-ttu-id="64a4d-403">Société qui a produit le fichier ? par exemple, « Microsoft Corporation » ou « Standard Microsystems Corporation, Inc. »</span><span class="sxs-lookup"><span data-stu-id="64a4d-403">Company that produced the file?for example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span> <span data-ttu-id="64a4d-404">Cette chaîne est requise.</span><span class="sxs-lookup"><span data-stu-id="64a4d-404">This string is required.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="64a4d-405">**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="64a4d-405">**FileDescription**</span></span>  | <span data-ttu-id="64a4d-406">Description du fichier à présenter aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="64a4d-406">File description to be presented to users.</span></span> <span data-ttu-id="64a4d-407">Cette chaîne peut être affichée dans une zone de liste lorsque l’utilisateur choisit les fichiers à installer ? par exemple, « pilote de clavier pour AT-Style claviers ».</span><span class="sxs-lookup"><span data-stu-id="64a4d-407">This string may be displayed in a list box when the user is choosing files to install?for example, "Keyboard Driver for AT-Style Keyboards".</span></span> <span data-ttu-id="64a4d-408">Cette chaîne est requise.</span><span class="sxs-lookup"><span data-stu-id="64a4d-408">This string is required.</span></span>                                                                                            |
| <span data-ttu-id="64a4d-409">**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="64a4d-409">**FileVersion**</span></span>      | <span data-ttu-id="64a4d-410">Numéro de version du fichier, par exemple « 3,10 » ou « 5,00. RC2 ».</span><span class="sxs-lookup"><span data-stu-id="64a4d-410">Version number of the file?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="64a4d-411">Cette chaîne est requise.</span><span class="sxs-lookup"><span data-stu-id="64a4d-411">This string is required.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="64a4d-412">**InternalName**</span><span class="sxs-lookup"><span data-stu-id="64a4d-412">**InternalName**</span></span>     | <span data-ttu-id="64a4d-413">Nom interne du fichier, s’il en existe un, par exemple, un nom de module s’il s’agit d’une bibliothèque de liens dynamiques.</span><span class="sxs-lookup"><span data-stu-id="64a4d-413">Internal name of the file, if one exists?for example, a module name if the file is a dynamic-link library.</span></span> <span data-ttu-id="64a4d-414">Si le fichier n’a pas de nom interne, cette chaîne doit être le nom de fichier d’origine, sans extension.</span><span class="sxs-lookup"><span data-stu-id="64a4d-414">If the file has no internal name, this string should be the original filename, without extension.</span></span> <span data-ttu-id="64a4d-415">Cette chaîne est requise.</span><span class="sxs-lookup"><span data-stu-id="64a4d-415">This string is required.</span></span>                                                                       |
| <span data-ttu-id="64a4d-416">**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="64a4d-416">**LegalCopyright**</span></span>   | <span data-ttu-id="64a4d-417">Mentions de droits d’auteur s’appliquant au fichier.</span><span class="sxs-lookup"><span data-stu-id="64a4d-417">Copyright notices that apply to the file.</span></span> <span data-ttu-id="64a4d-418">Cela doit inclure le texte intégral de toutes les mentions, symboles légaux, dates de copyright, etc.</span><span class="sxs-lookup"><span data-stu-id="64a4d-418">This should include the full text of all notices, legal symbols, copyright dates, and so on.</span></span> <span data-ttu-id="64a4d-419">Cette chaîne est facultative.</span><span class="sxs-lookup"><span data-stu-id="64a4d-419">This string is optional.</span></span>                                                                                                                                             |
| <span data-ttu-id="64a4d-420">**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="64a4d-420">**LegalTrademarks**</span></span>  | <span data-ttu-id="64a4d-421">Marques et marques déposées qui s’appliquent au fichier.</span><span class="sxs-lookup"><span data-stu-id="64a4d-421">Trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="64a4d-422">Cela doit inclure le texte intégral de la totalité des mentions, symboles légaux, numéros de marques, etc.</span><span class="sxs-lookup"><span data-stu-id="64a4d-422">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="64a4d-423">Cette chaîne est facultative.</span><span class="sxs-lookup"><span data-stu-id="64a4d-423">This string is optional.</span></span>                                                                                                                        |
| <span data-ttu-id="64a4d-424">**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="64a4d-424">**OriginalFilename**</span></span> | <span data-ttu-id="64a4d-425">Nom d’origine du fichier, à l’exclusion du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="64a4d-425">Original name of the file, not including a path.</span></span> <span data-ttu-id="64a4d-426">Ces informations permettent à une application de déterminer si un fichier a été renommé par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="64a4d-426">This information enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="64a4d-427">Le format du nom dépend du système de fichiers pour lequel le fichier a été créé.</span><span class="sxs-lookup"><span data-stu-id="64a4d-427">The format of the name depends on the file system for which the file was created.</span></span> <span data-ttu-id="64a4d-428">Cette chaîne est requise.</span><span class="sxs-lookup"><span data-stu-id="64a4d-428">This string is required.</span></span>                                                 |
| <span data-ttu-id="64a4d-429">**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="64a4d-429">**PrivateBuild**</span></span>     | <span data-ttu-id="64a4d-430">Informations sur une version privée du fichier, par exemple, « créé par TESTER1 sur \\ Testbed ».</span><span class="sxs-lookup"><span data-stu-id="64a4d-430">Information about a private version of the file?for example, "Built by TESTER1 on \\TESTBED".</span></span> <span data-ttu-id="64a4d-431">Cette chaîne doit être présente uniquement si **vs \_ FF \_ PRIVATEBUILD** est spécifié dans le paramètre *FileFlags* du bloc racine.</span><span class="sxs-lookup"><span data-stu-id="64a4d-431">This string should be present only if **VS\_FF\_PRIVATEBUILD** is specified in the *fileflags* parameter of the root block.</span></span>                                                                                   |
| <span data-ttu-id="64a4d-432">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="64a4d-432">**ProductName**</span></span>      | <span data-ttu-id="64a4d-433">Nom du produit avec lequel le fichier est distribué.</span><span class="sxs-lookup"><span data-stu-id="64a4d-433">Name of the product with which the file is distributed.</span></span> <span data-ttu-id="64a4d-434">Cette chaîne est requise.</span><span class="sxs-lookup"><span data-stu-id="64a4d-434">This string is required.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="64a4d-435">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="64a4d-435">**ProductVersion**</span></span>   | <span data-ttu-id="64a4d-436">Version du produit avec lequel le fichier est distribué, par exemple « 3,10 » ou « 5,00. RC2 ».</span><span class="sxs-lookup"><span data-stu-id="64a4d-436">Version of the product with which the file is distributed?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="64a4d-437">Cette chaîne est requise.</span><span class="sxs-lookup"><span data-stu-id="64a4d-437">This string is required.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="64a4d-438">**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="64a4d-438">**SpecialBuild**</span></span>     | <span data-ttu-id="64a4d-439">Texte qui indique la différence entre cette version du fichier et la version standard, par exemple « build privée pour TESTER1 résolution des problèmes de souris sur les ordinateurs M250 et M250E ».</span><span class="sxs-lookup"><span data-stu-id="64a4d-439">Text that indicates how this version of the file differs from the standard version?for example, "Private build for TESTER1 solving mouse problems on M250 and M250E computers".</span></span> <span data-ttu-id="64a4d-440">Cette chaîne doit être présente uniquement si **vs \_ FF \_ SPECIALBUILD** est spécifié dans le paramètre *FileFlags* du bloc racine.</span><span class="sxs-lookup"><span data-stu-id="64a4d-440">This string should be present only if **VS\_FF\_SPECIALBUILD** is specified in the *fileflags* parameter of the root block.</span></span> |



 

</dd> </dl>

<span data-ttu-id="64a4d-441">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="64a4d-441">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="64a4d-442">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="64a4d-442">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="64a4d-443">Exemples</span><span class="sxs-lookup"><span data-stu-id="64a4d-443">Examples</span></span>

<span data-ttu-id="64a4d-444">L’exemple suivant définit une ressource **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="64a4d-444">The following example defines a **VERSIONINFO** resource:</span></span>

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a><span data-ttu-id="64a4d-445">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64a4d-445">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a4d-446">Utilisation des informations de version</span><span class="sxs-lookup"><span data-stu-id="64a4d-446">Using Version Information</span></span>](./using-version-information.md)
</dt> <dt>

[<span data-ttu-id="64a4d-447">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="64a4d-447">Version Information</span></span>](./version-information.md)
</dt> </dl>

 

 