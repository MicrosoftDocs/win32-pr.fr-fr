---
title: InstallLayoutOrTipUserReg fonction)
description: Active les dispositions de clavier ou les services de texte spécifiés pour l’utilisateur spécifié.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- InstallLayoutOrTipUserReg fonction Text Services Framework
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741628"
---
# <a name="installlayoutortipuserreg-function"></a><span data-ttu-id="199d3-104">InstallLayoutOrTipUserReg fonction)</span><span class="sxs-lookup"><span data-stu-id="199d3-104">InstallLayoutOrTipUserReg function</span></span>

<span data-ttu-id="199d3-105">Active les dispositions de clavier ou les services de texte spécifiés pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="199d3-105">Enables the specified keyboard layouts or text services for the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="199d3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="199d3-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="199d3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="199d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="199d3-108">*pszUserReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="199d3-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="199d3-109">Chemin d’accès au registre de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="199d3-109">The registry path of the user.</span></span> <span data-ttu-id="199d3-110">Si ce paramètre a la **valeur null**, HKEY \_ Current \_ User est utilisé.</span><span class="sxs-lookup"><span data-stu-id="199d3-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="199d3-111">*pszSystemReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="199d3-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="199d3-112">Chemin d’accès au registre du système.</span><span class="sxs-lookup"><span data-stu-id="199d3-112">The registry path of the system.</span></span> <span data-ttu-id="199d3-113">Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ System est utilisé.</span><span class="sxs-lookup"><span data-stu-id="199d3-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="199d3-114">*pszSoftwareReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="199d3-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="199d3-115">Chemin d’accès du Registre du logiciel.</span><span class="sxs-lookup"><span data-stu-id="199d3-115">The registry path of the software.</span></span> <span data-ttu-id="199d3-116">Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ Software est utilisé.</span><span class="sxs-lookup"><span data-stu-id="199d3-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="199d3-117">*PSZ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="199d3-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="199d3-118">Chaîne qui représente la liste de la disposition du clavier ou la liste des profils des services de texte.</span><span class="sxs-lookup"><span data-stu-id="199d3-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="199d3-119">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="199d3-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="199d3-120">Champ de valeurs de champ qui spécifie les indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="199d3-120">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="199d3-121">Les identificateurs suivants ne sont pas définis dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="199d3-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="199d3-122">Vous devez soit utiliser la valeur hexadécimale, soit \# définir les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="199d3-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="199d3-123">Par exemple, pour utiliser **la \_ désinstallation de ilot** , vous devez inclure `#define ILOT_UNINSTALL 0x00000001` dans votre code.</span><span class="sxs-lookup"><span data-stu-id="199d3-123">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="199d3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="199d3-124">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="199d3-125">Signification</span><span class="sxs-lookup"><span data-stu-id="199d3-125">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="199d3-126"><dt>**Ilot \_ Désinstaller**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="199d3-126"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="199d3-127">Identique à **ilot \_ désactivé**.</span><span class="sxs-lookup"><span data-stu-id="199d3-127">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="199d3-128"><dt>**Ilot \_ DEFPROFILE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="199d3-128"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="199d3-129">Définit la disposition ou le Conseil spécifié en tant qu’élément par défaut.</span><span class="sxs-lookup"><span data-stu-id="199d3-129">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="199d3-130"><dt>**Ilot \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="199d3-130"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="199d3-131">Le paramètre est enregistré, mais n’est pas appliqué à la session active.</span><span class="sxs-lookup"><span data-stu-id="199d3-131">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="199d3-132"><dt>**Ilot \_ CLEANINSTALL**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="199d3-132"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="199d3-133">Désactive toutes les dispositions de clavier et les services de texte actuels.</span><span class="sxs-lookup"><span data-stu-id="199d3-133">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="199d3-134"><dt>**Ilot \_ Désactivation**</dt> de <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="199d3-134"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="199d3-135">Désactive la disposition de clavier et le service de texte spécifiés.</span><span class="sxs-lookup"><span data-stu-id="199d3-135">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="199d3-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="199d3-136">Return value</span></span>



| <span data-ttu-id="199d3-137">Code de retour</span><span class="sxs-lookup"><span data-stu-id="199d3-137">Return code</span></span>                                                                         | <span data-ttu-id="199d3-138">Description</span><span class="sxs-lookup"><span data-stu-id="199d3-138">Description</span></span>                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="199d3-139"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="199d3-139"><dt>**TRUE**</dt></span></span> </dl> | <span data-ttu-id="199d3-140">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="199d3-140">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="199d3-141"><dt>**FASE**</dt></span><span class="sxs-lookup"><span data-stu-id="199d3-141"><dt>**FASE**</dt></span></span> </dl> | <span data-ttu-id="199d3-142">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="199d3-142">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="199d3-143">Notes</span><span class="sxs-lookup"><span data-stu-id="199d3-143">Remarks</span></span>

<span data-ttu-id="199d3-144">Le format de chaîne de la liste de présentation est le suivant :</span><span class="sxs-lookup"><span data-stu-id="199d3-144">The string format of the layout list is:</span></span>

<span data-ttu-id="199d3-145"><LangID 1> : <KLID 1> ; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="199d3-145"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="199d3-146">Le format de chaîne de la liste des profils de service de texte est le suivant :</span><span class="sxs-lookup"><span data-stu-id="199d3-146">The string format of the text service profile list is:</span></span>

<span data-ttu-id="199d3-147"><LangID 1> : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="199d3-147"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="199d3-148">Voici un exemple de valeur pour le paramètre *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="199d3-148">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="199d3-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="199d3-149">Examples</span></span>

<span data-ttu-id="199d3-150">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="199d3-150">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="199d3-151">L’exemple suivant montre comment obtenir un pointeur vers cette fonction.</span><span class="sxs-lookup"><span data-stu-id="199d3-151">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="199d3-152">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="199d3-152">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="199d3-153">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="199d3-153">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="199d3-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="199d3-154">Requirements</span></span>



| <span data-ttu-id="199d3-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="199d3-155">Requirement</span></span> | <span data-ttu-id="199d3-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="199d3-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="199d3-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="199d3-157">Minimum supported client</span></span><br/> | <span data-ttu-id="199d3-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="199d3-158">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="199d3-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="199d3-159">Minimum supported server</span></span><br/> | <span data-ttu-id="199d3-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="199d3-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="199d3-161">DLL</span><span class="sxs-lookup"><span data-stu-id="199d3-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="199d3-162"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="199d3-162"><dt>Input.dll</dt></span></span> </dl> |



 

