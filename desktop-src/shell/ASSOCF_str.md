---
description: Fournit des informations aux méthodes de l’interface IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Énumération ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211293"
---
# <a name="assocf-enumeration"></a><span data-ttu-id="4d1c4-103">Énumération ASSOCF</span><span class="sxs-lookup"><span data-stu-id="4d1c4-103">ASSOCF enumeration</span></span>

<span data-ttu-id="4d1c4-104">Fournit des informations aux méthodes de l’interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="4d1c4-104">Provides information to the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d1c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d1c4-105">Syntax</span></span>

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="4d1c4-106">C++</span><span class="sxs-lookup"><span data-stu-id="4d1c4-106">C++</span></span></th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a><span data-ttu-id="4d1c4-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="4d1c4-107">Constants</span></span>

 <span data-ttu-id="4d1c4-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF\_NONE**</span></span> 

<span data-ttu-id="4d1c4-109">Aucune des options suivantes n’est définie.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-109">None of the following options are set.</span></span>

 <span data-ttu-id="4d1c4-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ init \_ NOREMAPCLSID**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF\_INIT\_NOREMAPCLSID**</span></span> 

<span data-ttu-id="4d1c4-111">Ordonne aux méthodes de l’interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de ne pas mapper les valeurs CLSID aux valeurs ProgID.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-111">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods not to map CLSID values to ProgID values.</span></span>

 <span data-ttu-id="4d1c4-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ init \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF\_INIT\_BYEXENAME**</span></span> 

<span data-ttu-id="4d1c4-113">Identifie la valeur du paramètre *pwszAssoc* de [**IQueryAssociations :: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) comme un nom de fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-113">Identifies the value of the *pwszAssoc* parameter of [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) as an executable file name.</span></span> <span data-ttu-id="4d1c4-114">Si cet indicateur n’est pas défini, la clé racine est définie sur le ProgID associé à la clé **. exe** au lieu du ProgID du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-114">If this flag is not set, the root key will be set to the ProgID associated with the **.exe** key instead of the executable file's ProgID.</span></span>

 <span data-ttu-id="4d1c4-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ ouvrir \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF\_OPEN\_BYEXENAME**</span></span> 

<span data-ttu-id="4d1c4-116">Identique à **ASSOCF \_ init \_ BYEXENAME**.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-116">Identical to **ASSOCF\_INIT\_BYEXENAME**.</span></span>

 <span data-ttu-id="4d1c4-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ init \_ DEFAULTTOSTAR**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF\_INIT\_DEFAULTTOSTAR**</span></span> 

<span data-ttu-id="4d1c4-118">Spécifie que lorsqu’une méthode [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) ne trouve pas la valeur demandée sous la clé racine, elle doit tenter de récupérer la valeur comparable de la **\*** sous-clé.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-118">Specifies that when an [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **\*** subkey.</span></span>

 <span data-ttu-id="4d1c4-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ init \_ DEFAULTTOFOLDER**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF\_INIT\_DEFAULTTOFOLDER**</span></span> 

<span data-ttu-id="4d1c4-120">Spécifie que lorsqu’une méthode [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) ne trouve pas la valeur demandée sous la clé racine, elle doit tenter de récupérer la valeur comparable de la sous-clé de **dossier** .</span><span class="sxs-lookup"><span data-stu-id="4d1c4-120">Specifies that when a [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **Folder** subkey.</span></span>

 <span data-ttu-id="4d1c4-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF\_NOUSERSETTINGS**</span></span> 

<span data-ttu-id="4d1c4-122">Spécifie que seules les **\_ classes HKEY \_** doivent être recherchées et que **HKEY \_ Current \_ User** doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-122">Specifies that only **HKEY\_CLASSES\_ROOT** should be searched, and that **HKEY\_CURRENT\_USER** should be ignored.</span></span>

 <span data-ttu-id="4d1c4-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOTRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF\_NOTRUNCATE**</span></span> 

<span data-ttu-id="4d1c4-124">Spécifie que la chaîne de retour ne doit pas être tronquée.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-124">Specifies that the return string should not be truncated.</span></span> <span data-ttu-id="4d1c4-125">Au lieu de cela, retournez une valeur d’erreur et la taille requise pour la chaîne complète.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-125">Instead, return an error value and the required size for the complete string.</span></span>

 <span data-ttu-id="4d1c4-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF \_ vérifier**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF\_VERIFY**</span></span> 

<span data-ttu-id="4d1c4-127">Ordonne aux méthodes [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de vérifier que les données sont exactes.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-127">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to verify that data is accurate.</span></span> <span data-ttu-id="4d1c4-128">Ce paramètre permet aux méthodes **IQueryAssociations** de lire des données à partir du disque dur de l’utilisateur à des fins de vérification.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-128">This setting allows **IQueryAssociations** methods to read data from the user's hard disk for verification.</span></span> <span data-ttu-id="4d1c4-129">Par exemple, ils peuvent vérifier le nom convivial dans le registre par rapport à celui stocké dans le fichier. exe.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-129">For example, they can check the friendly name in the registry against the one stored in the .exe file.</span></span> <span data-ttu-id="4d1c4-130">La définition de cet indicateur réduit généralement l’efficacité de la méthode.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-130">Setting this flag typically reduces the efficiency of the method.</span></span>

 <span data-ttu-id="4d1c4-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF\_REMAPRUNDLL**</span></span> 

<span data-ttu-id="4d1c4-132">Fait en sorte que les méthodes [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) ignorent Rundll.exe et retournent des informations sur sa cible.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-132">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to ignore Rundll.exe and return information about its target.</span></span> <span data-ttu-id="4d1c4-133">En général, les méthodes **IQueryAssociations** retournent des informations sur le premier fichier. exe ou. dll dans une chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-133">Typically **IQueryAssociations** methods return information about the first .exe or .dll in a command string.</span></span> <span data-ttu-id="4d1c4-134">Si une commande utilise Rundll.exe, la définition de cet indicateur indique à la méthode d’ignorer Rundll.exe et de retourner des informations sur sa cible.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-134">If a command uses Rundll.exe, setting this flag tells the method to ignore Rundll.exe and return information about its target.</span></span>

 <span data-ttu-id="4d1c4-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOFIXUPS**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF\_NOFIXUPS**</span></span> 

<span data-ttu-id="4d1c4-136">Ordonne aux méthodes [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de ne pas corriger les erreurs dans le registre, telles que le nom convivial d’une fonction qui ne correspond pas à celui trouvé dans le fichier. exe.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-136">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods not to fix errors in the registry, such as the friendly name of a function not matching the one found in the .exe file.</span></span>

 <span data-ttu-id="4d1c4-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF\_IGNOREBASECLASS**</span></span> 

<span data-ttu-id="4d1c4-138">Spécifie que la valeur de BaseClass doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-138">Specifies that the BaseClass value should be ignored.</span></span>

 <span data-ttu-id="4d1c4-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ init \_ IGNOREUNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF\_INIT\_IGNOREUNKNOWN**</span></span> 

<span data-ttu-id="4d1c4-140">**Introduit dans Windows 7**.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-140">**Introduced in Windows 7**.</span></span> <span data-ttu-id="4d1c4-141">Spécifie que le ProgID « inconnu » doit être ignoré ; au lieu de cela, échoue.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-141">Specifies that the "Unknown" ProgID should be ignored; instead, fail.</span></span>

 <span data-ttu-id="4d1c4-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF \_ init \_ ( \_ ProgID fixe)**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF\_INIT\_FIXED\_PROGID**</span></span> 

<span data-ttu-id="4d1c4-143">**Introduit dans Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-143">**Introduced in Windows 8**.</span></span> <span data-ttu-id="4d1c4-144">Spécifie que le ProgID fourni doit être mappé à l’aide des valeurs par défaut du système, plutôt que les valeurs par défaut de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-144">Specifies that the supplied ProgID should be mapped using the system defaults, rather than the current user defaults.</span></span>

 <span data-ttu-id="4d1c4-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ est un \_ protocole**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF\_IS\_PROTOCOL**</span></span> 

<span data-ttu-id="4d1c4-146">**Introduit dans Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-146">**Introduced in Windows 8**.</span></span> <span data-ttu-id="4d1c4-147">Spécifie que la valeur est un protocole et doit être mappée à l’aide des valeurs par défaut de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-147">Specifies that the value is a protocol, and should be mapped using the current user defaults.</span></span>

 <span data-ttu-id="4d1c4-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ init \_ pour le \_ fichier**</span><span class="sxs-lookup"><span data-stu-id="4d1c4-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF\_INIT\_FOR\_FILE**</span></span> 

<span data-ttu-id="4d1c4-149">**Introduite dans Windows 8.1**.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-149">**Introduced in Windows 8.1**.</span></span> <span data-ttu-id="4d1c4-150">Spécifie que le ProgID correspond à une association basée sur une extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-150">Specifies that the ProgID corresponds with a file extension based association.</span></span> <span data-ttu-id="4d1c4-151">À utiliser avec **ASSOCF \_ init \_ \_ identificateur programmatique fixe**.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-151">Use together with **ASSOCF\_INIT\_FIXED\_PROGID**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d1c4-152">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4d1c4-152">Requirements</span></span>



| <span data-ttu-id="4d1c4-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d1c4-153">Requirement</span></span> | <span data-ttu-id="4d1c4-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d1c4-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1c4-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d1c4-155">Minimum supported client</span></span> | <span data-ttu-id="4d1c4-156">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d1c4-156">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span>               |
| <span data-ttu-id="4d1c4-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d1c4-157">Minimum supported server</span></span> | <span data-ttu-id="4d1c4-158">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d1c4-158">Windows 2000 Server \[desktop apps only\]</span></span>                                 |
| <span data-ttu-id="4d1c4-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d1c4-159">Header</span></span>                   |  <span data-ttu-id="4d1c4-160">Shlwapi. h</span><span class="sxs-lookup"><span data-stu-id="4d1c4-160">Shlwapi.h</span></span>  |



## <a name="see-also"></a><span data-ttu-id="4d1c4-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d1c4-161">See also</span></span>

 <span data-ttu-id="4d1c4-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span><span class="sxs-lookup"><span data-stu-id="4d1c4-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span></span> 

 

 

<span data-ttu-id="4d1c4-163">© 2017 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-163">© 2017 Microsoft.</span></span> <span data-ttu-id="4d1c4-164">Tous droits réservés.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-164">All rights reserved.</span></span>
