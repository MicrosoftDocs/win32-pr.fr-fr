---
title: SetDefaultLayoutOrTipUserReg fonction)
description: Définit la disposition de clavier spécifiée ou un service de texte comme élément d’entrée par défaut du registre de l’utilisateur.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- SetDefaultLayoutOrTipUserReg fonction Text Services Framework
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103017"
---
# <a name="setdefaultlayoutortipuserreg-function"></a><span data-ttu-id="d371c-104">SetDefaultLayoutOrTipUserReg fonction)</span><span class="sxs-lookup"><span data-stu-id="d371c-104">SetDefaultLayoutOrTipUserReg function</span></span>

<span data-ttu-id="d371c-105">Définit la disposition de clavier spécifiée ou un service de texte comme élément d’entrée par défaut du registre de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d371c-105">Sets the specified keyboard layout or a text service as a default input item of the user registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="d371c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d371c-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d371c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d371c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d371c-108">*pszUserReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d371c-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d371c-109">Chemin d’accès au registre de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d371c-109">The registry path of the user.</span></span> <span data-ttu-id="d371c-110">Si ce paramètre a la **valeur null**, HKEY \_ Current \_ User est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d371c-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="d371c-111">*pszSystemReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d371c-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d371c-112">Chemin d’accès au registre du système.</span><span class="sxs-lookup"><span data-stu-id="d371c-112">The registry path of the system.</span></span> <span data-ttu-id="d371c-113">Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ System est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d371c-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="d371c-114">*pszSoftwareReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d371c-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d371c-115">Chemin d’accès du Registre du logiciel.</span><span class="sxs-lookup"><span data-stu-id="d371c-115">The registry path of the software.</span></span> <span data-ttu-id="d371c-116">Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ Software est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d371c-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="d371c-117">*PSZ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d371c-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d371c-118">Chaîne qui représente la liste de la disposition du clavier ou la liste des profils des services de texte.</span><span class="sxs-lookup"><span data-stu-id="d371c-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="d371c-119">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d371c-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d371c-120">Champ de valeurs de champ qui spécifie les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="d371c-120">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="d371c-121">Les identificateurs suivants ne sont pas définis dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="d371c-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="d371c-122">Vous devez soit utiliser la valeur hexadécimale, soit \# définir les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="d371c-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="d371c-123">Par exemple, pour utiliser SDLOT \_ NOAPPLYTOCURRENTSESSION, vous devez inclure \# define SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 dans votre code.</span><span class="sxs-lookup"><span data-stu-id="d371c-123">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="d371c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d371c-124">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="d371c-125">Signification</span><span class="sxs-lookup"><span data-stu-id="d371c-125">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="d371c-126"><dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d371c-126"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="d371c-127">Stocke le paramètre dans le registre, mais ne met pas à jour le paramètre de clavier du runtime de la session active.</span><span class="sxs-lookup"><span data-stu-id="d371c-127">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="d371c-128">Si l’autre chemin d’accès au registre est défini dans **SetDefaultLayoutOrTipUserReg**, cet indicateur doit être défini.</span><span class="sxs-lookup"><span data-stu-id="d371c-128">If the alternative registry path is set in **SetDefaultLayoutOrTipUserReg**, this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="d371c-129"><dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d371c-129"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="d371c-130">Applique le paramètre immédiatement sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="d371c-130">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d371c-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d371c-131">Return value</span></span>



| <span data-ttu-id="d371c-132">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d371c-132">Return code</span></span>                                                                          | <span data-ttu-id="d371c-133">Description</span><span class="sxs-lookup"><span data-stu-id="d371c-133">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d371c-134"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="d371c-134"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="d371c-135">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="d371c-135">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="d371c-136"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="d371c-136"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="d371c-137">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="d371c-137">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d371c-138">Notes</span><span class="sxs-lookup"><span data-stu-id="d371c-138">Remarks</span></span>

<span data-ttu-id="d371c-139">Le format de chaîne de la liste de présentation est le suivant :</span><span class="sxs-lookup"><span data-stu-id="d371c-139">The string format of the layout list is:</span></span>

<span data-ttu-id="d371c-140"><LangID 1> : <KLID 1> ; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="d371c-140"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="d371c-141">Le format de chaîne de la liste des profils de service de texte est le suivant :</span><span class="sxs-lookup"><span data-stu-id="d371c-141">The string format of the text service profile list is:</span></span>

<span data-ttu-id="d371c-142"><LangID 1> : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="d371c-142"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="d371c-143">Voici un exemple de valeur pour le paramètre *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="d371c-143">The following is an example of a value for the *psz* parameter:</span></span>


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="d371c-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="d371c-144">Examples</span></span>

<span data-ttu-id="d371c-145">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="d371c-145">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="d371c-146">L’exemple suivant montre comment obtenir un pointeur vers cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d371c-146">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="d371c-147">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="d371c-147">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="d371c-148">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="d371c-148">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="d371c-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d371c-149">Requirements</span></span>



| <span data-ttu-id="d371c-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d371c-150">Requirement</span></span> | <span data-ttu-id="d371c-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="d371c-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d371c-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d371c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d371c-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d371c-153">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d371c-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d371c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d371c-155">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d371c-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d371c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="d371c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d371c-157"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d371c-157"><dt>Input.dll</dt></span></span> </dl> |



 

