---
title: SaveSystemAcctInputSettings fonction)
description: Applique la disposition de clavier utilisateur et le paramètre de service de texte à la ruche comptes système.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- SaveSystemAcctInputSettings fonction Text Services Framework
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383971"
---
# <a name="savesystemacctinputsettings-function"></a><span data-ttu-id="9610d-104">SaveSystemAcctInputSettings fonction)</span><span class="sxs-lookup"><span data-stu-id="9610d-104">SaveSystemAcctInputSettings function</span></span>

<span data-ttu-id="9610d-105">Applique la disposition de clavier utilisateur et le paramètre de service de texte à la ruche comptes système.</span><span class="sxs-lookup"><span data-stu-id="9610d-105">Applies the user keyboard layout and text service setting to the system accounts hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9610d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9610d-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="9610d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9610d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9610d-108">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9610d-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9610d-109">Fenêtre parente de la boîte de dialogue d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="9610d-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="9610d-110">La boîte de dialogue d’avertissement n’est pas toujours affichée et apparaît correctement.</span><span class="sxs-lookup"><span data-stu-id="9610d-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="9610d-111">Si ce paramètre a la **valeur null**, la boîte de dialogue d’avertissement ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="9610d-111">If this parameter is **NULL**, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="9610d-112">*hSourceRegKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9610d-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9610d-113">Clé de Registre racine du paramètre utilisateur à copier.</span><span class="sxs-lookup"><span data-stu-id="9610d-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9610d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9610d-114">Return value</span></span>



| <span data-ttu-id="9610d-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9610d-115">Return code</span></span>                                                                          | <span data-ttu-id="9610d-116">Description</span><span class="sxs-lookup"><span data-stu-id="9610d-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9610d-117"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="9610d-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="9610d-118">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="9610d-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="9610d-119"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="9610d-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="9610d-120">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="9610d-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9610d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="9610d-121">Remarks</span></span>

<span data-ttu-id="9610d-122">La ruche du compte système est HKEY \_ Users \\ . DEFAULT, HKEY \_ Users \\ s-1-5-19 et HKEY \_ Users \\ s-1-5-20.</span><span class="sxs-lookup"><span data-stu-id="9610d-122">The system account hive is HKEY\_USERS\\.DEFAULT, HKEY\_USERS\\S-1-5-19, and HKEY\_USERS\\S-1-5-20.</span></span>

## <a name="examples"></a><span data-ttu-id="9610d-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="9610d-123">Examples</span></span>

<span data-ttu-id="9610d-124">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="9610d-124">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="9610d-125">L’exemple suivant montre comment obtenir un pointeur vers cette fonction.</span><span class="sxs-lookup"><span data-stu-id="9610d-125">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="9610d-126">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9610d-126">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="9610d-127">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="9610d-127">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="9610d-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9610d-128">Requirements</span></span>



| <span data-ttu-id="9610d-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9610d-129">Requirement</span></span> | <span data-ttu-id="9610d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9610d-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9610d-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9610d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9610d-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9610d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9610d-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9610d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9610d-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9610d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9610d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9610d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9610d-136"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9610d-136"><dt>Input.dll</dt></span></span> </dl> |



 

