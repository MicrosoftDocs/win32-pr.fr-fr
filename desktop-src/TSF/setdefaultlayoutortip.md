---
title: SetDefaultLayoutOrTip fonction)
description: Définit la disposition de clavier spécifiée ou un service de texte comme élément d’entrée par défaut de l’utilisateur actuel.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- SetDefaultLayoutOrTip fonction Text Services Framework
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103193"
---
# <a name="setdefaultlayoutortip-function"></a><span data-ttu-id="f14b2-104">SetDefaultLayoutOrTip fonction)</span><span class="sxs-lookup"><span data-stu-id="f14b2-104">SetDefaultLayoutOrTip function</span></span>

<span data-ttu-id="f14b2-105">Définit la disposition de clavier spécifiée ou un service de texte comme élément d’entrée par défaut de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="f14b2-105">Sets the specified keyboard layout or a text service as the default input item of the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="f14b2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f14b2-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f14b2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f14b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f14b2-108">*PSZ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f14b2-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f14b2-109">Chaîne qui représente une liste de dispositions de clavier ou une liste de profils de services de texte.</span><span class="sxs-lookup"><span data-stu-id="f14b2-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="f14b2-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f14b2-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f14b2-111">Champ de valeurs de champ qui spécifie les indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="f14b2-111">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="f14b2-112">Les identificateurs suivants ne sont pas définis dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="f14b2-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="f14b2-113">Vous devez soit utiliser la valeur hexadécimale, soit \# définir les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="f14b2-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="f14b2-114">Par exemple, pour utiliser SDLOT \_ NOAPPLYTOCURRENTSESSION, vous devez inclure \# define SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 dans votre code.</span><span class="sxs-lookup"><span data-stu-id="f14b2-114">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="f14b2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f14b2-115">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="f14b2-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f14b2-116">Meaning</span></span>                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="f14b2-117"><dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f14b2-117"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="f14b2-118">Stocke le paramètre dans le registre, mais ne met pas à jour le paramètre de clavier du runtime de la session active.</span><span class="sxs-lookup"><span data-stu-id="f14b2-118">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="f14b2-119">Si l’autre chemin d’accès au registre est défini dans [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), cet indicateur doit être défini.</span><span class="sxs-lookup"><span data-stu-id="f14b2-119">If the alternative registry path is set in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="f14b2-120"><dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f14b2-120"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="f14b2-121">Applique le paramètre immédiatement sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="f14b2-121">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f14b2-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f14b2-122">Return value</span></span>



| <span data-ttu-id="f14b2-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f14b2-123">Return code</span></span>                                                                          | <span data-ttu-id="f14b2-124">Description</span><span class="sxs-lookup"><span data-stu-id="f14b2-124">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="f14b2-125"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="f14b2-125"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="f14b2-126">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="f14b2-126">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="f14b2-127"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="f14b2-127"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="f14b2-128">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="f14b2-128">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f14b2-129">Notes</span><span class="sxs-lookup"><span data-stu-id="f14b2-129">Remarks</span></span>

<span data-ttu-id="f14b2-130">Le format de chaîne de la liste de présentation est le suivant :</span><span class="sxs-lookup"><span data-stu-id="f14b2-130">The string format of the layout list is:</span></span>

<span data-ttu-id="f14b2-131"><LangID 1> : <KLID 1> ; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="f14b2-131"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="f14b2-132">Le format de chaîne de la liste des profils de service de texte est le suivant :</span><span class="sxs-lookup"><span data-stu-id="f14b2-132">The string format of the text service profile list is:</span></span>

<span data-ttu-id="f14b2-133"><LangID 1> : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="f14b2-133"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="f14b2-134">Voici un exemple de valeur pour le paramètre *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="f14b2-134">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="f14b2-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="f14b2-135">Examples</span></span>

<span data-ttu-id="f14b2-136">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="f14b2-136">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="f14b2-137">L’exemple suivant montre comment obtenir un pointeur vers cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f14b2-137">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="f14b2-138">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="f14b2-138">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="f14b2-139">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="f14b2-139">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="f14b2-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f14b2-140">Requirements</span></span>



| <span data-ttu-id="f14b2-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f14b2-141">Requirement</span></span> | <span data-ttu-id="f14b2-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f14b2-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f14b2-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14b2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f14b2-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f14b2-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f14b2-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14b2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f14b2-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f14b2-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f14b2-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f14b2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f14b2-148"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f14b2-148"><dt>Input.dll</dt></span></span> </dl> |



 

