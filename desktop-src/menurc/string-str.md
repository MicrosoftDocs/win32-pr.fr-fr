---
title: Structure de chaîne
description: Représente l’Organisation des données dans une ressource de version de fichier. Elle contient une chaîne qui décrit un aspect spécifique d’un fichier, par exemple, la version d’un fichier, ses mentions de droits d’auteur ou ses marques.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menus de structure de chaîne et autres ressources
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509702"
---
# <a name="string-structure"></a><span data-ttu-id="87c39-105">Structure de chaîne</span><span class="sxs-lookup"><span data-stu-id="87c39-105">String structure</span></span>

<span data-ttu-id="87c39-106">Représente l’Organisation des données dans une ressource de version de fichier.</span><span class="sxs-lookup"><span data-stu-id="87c39-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="87c39-107">Elle contient une chaîne qui décrit un aspect spécifique d’un fichier, par exemple, la version d’un fichier, ses mentions de droits d’auteur ou ses marques.</span><span class="sxs-lookup"><span data-stu-id="87c39-107">It contains a string that describes a specific aspect of a file, for example, a file's version, its copyright notices, or its trademarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c39-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87c39-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a><span data-ttu-id="87c39-109">Membres</span><span class="sxs-lookup"><span data-stu-id="87c39-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="87c39-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="87c39-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="87c39-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="87c39-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="87c39-112">Longueur, en octets, de cette structure de **chaîne** .</span><span class="sxs-lookup"><span data-stu-id="87c39-112">The length, in bytes, of this **String** structure.</span></span>

</dd> <dt>

<span data-ttu-id="87c39-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="87c39-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="87c39-114">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="87c39-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="87c39-115">Taille, en termes, du membre de **valeur** .</span><span class="sxs-lookup"><span data-stu-id="87c39-115">The size, in words, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="87c39-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="87c39-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="87c39-117">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="87c39-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="87c39-118">Type de données de la ressource de version.</span><span class="sxs-lookup"><span data-stu-id="87c39-118">The type of data in the version resource.</span></span> <span data-ttu-id="87c39-119">Ce membre est 1 si la ressource de version contient des données texte et 0 si la ressource de version contient des données binaires.</span><span class="sxs-lookup"><span data-stu-id="87c39-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="87c39-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="87c39-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="87c39-121">Type : **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="87c39-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="87c39-122">Chaîne Unicode arbitraire.</span><span class="sxs-lookup"><span data-stu-id="87c39-122">An arbitrary Unicode string.</span></span> <span data-ttu-id="87c39-123">Le membre **szKey** peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="87c39-123">The **szKey** member can be one or more of the following values.</span></span> <span data-ttu-id="87c39-124">Ces valeurs sont uniquement des indications.</span><span class="sxs-lookup"><span data-stu-id="87c39-124">These values are guidelines only.</span></span>

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span data-ttu-id="87c39-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Inclus**</span><span class="sxs-lookup"><span data-stu-id="87c39-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comments**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-126">Le membre de **valeur** contient toutes les informations supplémentaires qui doivent être affichées à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="87c39-126">The **Value** member contains any additional information that should be displayed for diagnostic purposes.</span></span> <span data-ttu-id="87c39-127">Cette chaîne peut être une longueur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="87c39-127">This string can be an arbitrary length.</span></span>

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span data-ttu-id="87c39-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Prennent**</span><span class="sxs-lookup"><span data-stu-id="87c39-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-129">Le membre de **valeur** identifie la société qui a produit le fichier.</span><span class="sxs-lookup"><span data-stu-id="87c39-129">The **Value** member identifies the company that produced the file.</span></span> <span data-ttu-id="87c39-130">Par exemple, « Microsoft Corporation » ou « Standard Microsystems Corporation, Inc. »</span><span class="sxs-lookup"><span data-stu-id="87c39-130">For example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span>

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span data-ttu-id="87c39-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="87c39-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-132">Le membre de **valeur** décrit le fichier de façon à ce qu’il puisse être présenté aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="87c39-132">The **Value** member describes the file in such a way that it can be presented to users.</span></span> <span data-ttu-id="87c39-133">Cette chaîne peut être présentée dans une zone de liste lorsque l’utilisateur choisit les fichiers à installer.</span><span class="sxs-lookup"><span data-stu-id="87c39-133">This string may be presented in a list box when the user is choosing files to install.</span></span> <span data-ttu-id="87c39-134">Par exemple, « pilote de clavier pour les claviers de style AT » ou « Microsoft Word pour Windows ».</span><span class="sxs-lookup"><span data-stu-id="87c39-134">For example, "Keyboard driver for AT-style keyboards" or "Microsoft Word for Windows".</span></span>

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span data-ttu-id="87c39-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="87c39-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-136">Le membre de **valeur** identifie la version de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="87c39-136">The **Value** member identifies the version of this file.</span></span> <span data-ttu-id="87c39-137">Par exemple, la **valeur** peut être « 3.00 a » ou « 5,00. RC2 ».</span><span class="sxs-lookup"><span data-stu-id="87c39-137">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span data-ttu-id="87c39-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span><span class="sxs-lookup"><span data-stu-id="87c39-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-139">Le membre de **valeur** identifie le nom interne du fichier, s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="87c39-139">The **Value** member identifies the file's internal name, if one exists.</span></span> <span data-ttu-id="87c39-140">Par exemple, cette chaîne peut contenir le nom du module pour une DLL, un nom de périphérique virtuel pour un appareil virtuel Windows ou un nom de périphérique pour un pilote de périphérique MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="87c39-140">For example, this string could contain the module name for a DLL, a virtual device name for a Windows virtual device, or a device name for a MS-DOS device driver.</span></span>

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span data-ttu-id="87c39-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="87c39-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-142">Le membre **value** décrit toutes les mentions de droits d’auteur, marques déposées et marques déposées qui s’appliquent au fichier.</span><span class="sxs-lookup"><span data-stu-id="87c39-142">The **Value** member describes all copyright notices, trademarks, and registered trademarks that apply to the file.</span></span> <span data-ttu-id="87c39-143">Cela doit inclure le texte intégral de la totalité des mentions, symboles légaux, dates de copyright, numéros de marques, etc.</span><span class="sxs-lookup"><span data-stu-id="87c39-143">This should include the full text of all notices, legal symbols, copyright dates, trademark numbers, and so on.</span></span> <span data-ttu-id="87c39-144">En anglais, cette chaîne doit être au format « Copyright Microsoft Corp. 1990 1994 ».</span><span class="sxs-lookup"><span data-stu-id="87c39-144">In English, this string should be in the format "Copyright Microsoft Corp. 1990  1994".</span></span>

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span data-ttu-id="87c39-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="87c39-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-146">Le membre **value** décrit toutes les marques et les marques déposées qui s’appliquent au fichier.</span><span class="sxs-lookup"><span data-stu-id="87c39-146">The **Value** member describes all trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="87c39-147">Cela doit inclure le texte intégral de la totalité des mentions, symboles légaux, numéros de marques, etc.</span><span class="sxs-lookup"><span data-stu-id="87c39-147">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="87c39-148">En français, cette chaîne doit avoir le format « Windows est une marque de Microsoft Corporation ».</span><span class="sxs-lookup"><span data-stu-id="87c39-148">In English, this string should be in the format "Windows is a trademark of Microsoft Corporation".</span></span>

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span data-ttu-id="87c39-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="87c39-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-150">Le membre de **valeur** identifie le nom d’origine du fichier, à l’exclusion du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="87c39-150">The **Value** member identifies the original name of the file, not including a path.</span></span> <span data-ttu-id="87c39-151">Cela permet à une application de déterminer si un fichier a été renommé par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="87c39-151">This enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="87c39-152">Ce nom peut ne pas être au format MS-DOS 8,3 Si le fichier est spécifique à un système de fichiers non FAT.</span><span class="sxs-lookup"><span data-stu-id="87c39-152">This name may not be MS-DOS 8.3-format if the file is specific to a non-FAT file system.</span></span>

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span data-ttu-id="87c39-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="87c39-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-154">Le membre de **valeur** décrit par qui, où et pourquoi cette version privée du fichier a été générée.</span><span class="sxs-lookup"><span data-stu-id="87c39-154">The **Value** member describes by whom, where, and why this private version of the file was built.</span></span> <span data-ttu-id="87c39-155">Cette chaîne doit être présente uniquement si l’indicateur **vs \_ FF \_ PRIVATEBUILD** est défini dans le membre **dwFileFlags** de la structure [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="87c39-155">This string should only be present if the **VS\_FF\_PRIVATEBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="87c39-156">Par exemple, la **valeur** peut être « générée par Oscar sur \\ OSCAR2 ».</span><span class="sxs-lookup"><span data-stu-id="87c39-156">For example, **Value** could be "Built by OSCAR on \\OSCAR2".</span></span>

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span data-ttu-id="87c39-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span><span class="sxs-lookup"><span data-stu-id="87c39-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-158">Le membre de **valeur** identifie le nom du produit avec lequel ce fichier est distribué.</span><span class="sxs-lookup"><span data-stu-id="87c39-158">The **Value** member identifies the name of the product with which this file is distributed.</span></span> <span data-ttu-id="87c39-159">Par exemple, cette chaîne peut être « Microsoft Windows ».</span><span class="sxs-lookup"><span data-stu-id="87c39-159">For example, this string could be "Microsoft Windows".</span></span>

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span data-ttu-id="87c39-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="87c39-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-161">Le membre de **valeur** identifie la version du produit avec lequel ce fichier est distribué.</span><span class="sxs-lookup"><span data-stu-id="87c39-161">The **Value** member identifies the version of the product with which this file is distributed.</span></span> <span data-ttu-id="87c39-162">Par exemple, la **valeur** peut être « 3.00 a » ou « 5,00. RC2 ».</span><span class="sxs-lookup"><span data-stu-id="87c39-162">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span data-ttu-id="87c39-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="87c39-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span></span>


</dt> <dd>

<span data-ttu-id="87c39-164">Le membre **value** décrit la différence entre cette version du fichier et la version normale.</span><span class="sxs-lookup"><span data-stu-id="87c39-164">The **Value** member describes how this version of the file differs from the normal version.</span></span> <span data-ttu-id="87c39-165">Cette entrée doit être présente uniquement si l’indicateur **vs \_ FF \_ SPECIALBUILD** est défini dans le membre **dwFileFlags** de la structure [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="87c39-165">This entry should only be present if the **VS\_FF\_SPECIALBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="87c39-166">Par exemple, la **valeur** peut être « build privée pour les problèmes de souris de résolution Olivetti sur les ordinateurs M250 et M250E ».</span><span class="sxs-lookup"><span data-stu-id="87c39-166">For example, **Value** could be "Private build for Olivetti solving mouse problems on M250 and M250E computers".</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="87c39-167">**Remplissage**</span><span class="sxs-lookup"><span data-stu-id="87c39-167">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="87c39-168">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="87c39-168">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="87c39-169">Autant de mots zéro que nécessaire pour aligner le membre **value** sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="87c39-169">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="87c39-170">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="87c39-170">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="87c39-171">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="87c39-171">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="87c39-172">Chaîne se terminant par zéro.</span><span class="sxs-lookup"><span data-stu-id="87c39-172">A zero-terminated string.</span></span> <span data-ttu-id="87c39-173">Pour plus d’informations, consultez la description du membre **szKey** .</span><span class="sxs-lookup"><span data-stu-id="87c39-173">See the **szKey** member description for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87c39-174">Notes</span><span class="sxs-lookup"><span data-stu-id="87c39-174">Remarks</span></span>

<span data-ttu-id="87c39-175">Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="87c39-175">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="87c39-176">Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="87c39-176">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="87c39-177">Une structure de **chaîne** peut avoir la valeur **szKey** , par exemple, « CompanyName » et la **valeur** « Microsoft Corporation ».</span><span class="sxs-lookup"><span data-stu-id="87c39-177">A **String** structure may have an **szKey** value of, for example, "CompanyName" and a **Value** of "Microsoft Corporation".</span></span> <span data-ttu-id="87c39-178">Une autre structure de **chaîne** avec la même valeur **szKey** peut contenir la **valeur** « Microsoft GmbH ».</span><span class="sxs-lookup"><span data-stu-id="87c39-178">Another **String** structure with the same **szKey** value could contain a **Value** of "Microsoft GmbH".</span></span> <span data-ttu-id="87c39-179">Cela peut se produire si la deuxième structure de **chaîne** était associée à une structure [**STRINGTABLE**](stringtable.md) dont la valeur **SzKey** est 040704b0 c’est-à-dire, allemande/Unicode.</span><span class="sxs-lookup"><span data-stu-id="87c39-179">This might occur if the second **String** structure were associated with a [**StringTable**](stringtable.md) structure whose **szKey** value is 040704b0   that is, German/Unicode.</span></span>

## <a name="requirements"></a><span data-ttu-id="87c39-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87c39-180">Requirements</span></span>



| <span data-ttu-id="87c39-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87c39-181">Requirement</span></span> | <span data-ttu-id="87c39-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="87c39-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="87c39-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c39-183">Minimum supported client</span></span><br/> | <span data-ttu-id="87c39-184">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87c39-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="87c39-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c39-185">Minimum supported server</span></span><br/> | <span data-ttu-id="87c39-186">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87c39-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="87c39-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87c39-187">See also</span></span>

<dl> <dt>

<span data-ttu-id="87c39-188">**Référence**</span><span class="sxs-lookup"><span data-stu-id="87c39-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="87c39-189">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="87c39-189">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="87c39-190">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="87c39-190">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[<span data-ttu-id="87c39-191">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="87c39-191">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="87c39-192">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="87c39-192">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="87c39-193">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="87c39-193">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="87c39-194">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="87c39-194">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





