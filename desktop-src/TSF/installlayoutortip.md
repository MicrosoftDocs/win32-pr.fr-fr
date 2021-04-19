---
title: InstallLayoutOrTip fonction)
description: Active les dispositions de clavier ou les services de texte spécifiés.
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- InstallLayoutOrTip fonction Text Services Framework
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510540"
---
# <a name="installlayoutortip-function"></a><span data-ttu-id="bb54a-104">InstallLayoutOrTip fonction)</span><span class="sxs-lookup"><span data-stu-id="bb54a-104">InstallLayoutOrTip function</span></span>

<span data-ttu-id="bb54a-105">Active les dispositions de clavier ou les services de texte spécifiés.</span><span class="sxs-lookup"><span data-stu-id="bb54a-105">Enables the specified keyboard layouts or text services.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb54a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb54a-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bb54a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb54a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb54a-108">*PSZ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb54a-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb54a-109">Chaîne qui représente la liste de la disposition du clavier ou la liste des profils des services de texte.</span><span class="sxs-lookup"><span data-stu-id="bb54a-109">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="bb54a-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb54a-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb54a-111">Champ de valeurs de champ qui spécifie les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="bb54a-111">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="bb54a-112">Les identificateurs suivants ne sont pas définis dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="bb54a-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="bb54a-113">Vous devez soit utiliser la valeur hexadécimale, soit \# définir les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="bb54a-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="bb54a-114">Par exemple, pour utiliser **la \_ désinstallation de ilot** , vous devez inclure `#define ILOT_UNINSTALL 0x00000001` dans votre code.</span><span class="sxs-lookup"><span data-stu-id="bb54a-114">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="bb54a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb54a-115">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="bb54a-116">Signification</span><span class="sxs-lookup"><span data-stu-id="bb54a-116">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="bb54a-117"><dt>**Ilot \_ Désinstaller**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-117"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="bb54a-118">Identique à **ilot \_ désactivé**.</span><span class="sxs-lookup"><span data-stu-id="bb54a-118">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="bb54a-119"><dt>**Ilot \_ DEFPROFILE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-119"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="bb54a-120">Définit la disposition ou le Conseil spécifié en tant qu’élément par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb54a-120">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <span data-ttu-id="bb54a-121"><dt>**Ilot \_ DEFUSER4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-121"><dt>**ILOT\_DEFUSER4**</dt> <dt>0x00000004</dt></span></span> </dl>                                              | <span data-ttu-id="bb54a-122">Modifie le paramètre de. Valeurs.</span><span class="sxs-lookup"><span data-stu-id="bb54a-122">Changes the setting of .Default.</span></span><br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <span data-ttu-id="bb54a-123"><dt>**Ilot \_ SYSLOCALE**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-123"><dt>**ILOT\_SYSLOCALE**</dt> <dt>0x00000008</dt></span></span> </dl>                                           | <span data-ttu-id="bb54a-124">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="bb54a-124">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <span data-ttu-id="bb54a-125"><dt>**Ilot \_ NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-125"><dt>**ILOT\_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="bb54a-126">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="bb54a-126">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="bb54a-127"><dt>**Ilot \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-127"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="bb54a-128">Le paramètre est enregistré, mais n’est pas appliqué à la session active.</span><span class="sxs-lookup"><span data-stu-id="bb54a-128">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="bb54a-129"><dt>**Ilot \_ CLEANINSTALL**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-129"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="bb54a-130">Désactive toutes les dispositions de clavier et les services de texte actuels.</span><span class="sxs-lookup"><span data-stu-id="bb54a-130">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="bb54a-131"><dt>**Ilot \_ Désactivation**</dt> de <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-131"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="bb54a-132">Désactive la disposition de clavier et le service de texte spécifiés.</span><span class="sxs-lookup"><span data-stu-id="bb54a-132">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb54a-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb54a-133">Return value</span></span>



| <span data-ttu-id="bb54a-134">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bb54a-134">Return code</span></span>                                                                          | <span data-ttu-id="bb54a-135">Description</span><span class="sxs-lookup"><span data-stu-id="bb54a-135">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="bb54a-136"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-136"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="bb54a-137">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="bb54a-137">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="bb54a-138"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-138"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="bb54a-139">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="bb54a-139">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb54a-140">Notes</span><span class="sxs-lookup"><span data-stu-id="bb54a-140">Remarks</span></span>

<span data-ttu-id="bb54a-141">Le format de chaîne de la liste de présentation est le suivant :</span><span class="sxs-lookup"><span data-stu-id="bb54a-141">The string format of the layout list is:</span></span>

<span data-ttu-id="bb54a-142"><LangID 1> : <KLID 1> ; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="bb54a-142"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="bb54a-143">Le format de chaîne de la liste des profils de service de texte est le suivant :</span><span class="sxs-lookup"><span data-stu-id="bb54a-143">The string format of the text service profile list is:</span></span>

<span data-ttu-id="bb54a-144"><LangID 1> : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="bb54a-144"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="bb54a-145">Voici un exemple de valeur pour le paramètre *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="bb54a-145">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="bb54a-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="bb54a-146">Examples</span></span>

<span data-ttu-id="bb54a-147">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="bb54a-147">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="bb54a-148">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="bb54a-148">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="bb54a-149">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="bb54a-149">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="bb54a-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb54a-150">Requirements</span></span>



| <span data-ttu-id="bb54a-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb54a-151">Requirement</span></span> | <span data-ttu-id="bb54a-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb54a-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb54a-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb54a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="bb54a-154">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb54a-154">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bb54a-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb54a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="bb54a-156">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb54a-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bb54a-157">DLL</span><span class="sxs-lookup"><span data-stu-id="bb54a-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb54a-158"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb54a-158"><dt>Input.dll</dt></span></span> </dl> |



 

