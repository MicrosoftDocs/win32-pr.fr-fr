---
title: SaveDefaultUserInputSettings fonction)
description: Applique la disposition de clavier utilisateur et le paramètre de service de texte à la ruche utilisateur par défaut.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- SaveDefaultUserInputSettings fonction Text Services Framework
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384235"
---
# <a name="savedefaultuserinputsettings-function"></a><span data-ttu-id="cefc4-104">SaveDefaultUserInputSettings fonction)</span><span class="sxs-lookup"><span data-stu-id="cefc4-104">SaveDefaultUserInputSettings function</span></span>

<span data-ttu-id="cefc4-105">Applique la disposition de clavier utilisateur et le paramètre de service de texte à la ruche utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="cefc4-105">Applies the user keyboard layout and text service setting to the default user hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="cefc4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cefc4-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="cefc4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cefc4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cefc4-108">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cefc4-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cefc4-109">Fenêtre parente de la boîte de dialogue d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="cefc4-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="cefc4-110">La boîte de dialogue d’avertissement n’est pas toujours affichée et apparaît correctement.</span><span class="sxs-lookup"><span data-stu-id="cefc4-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="cefc4-111">Si ce paramètre a la valeur NULL, la boîte de dialogue d’avertissement ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="cefc4-111">If this parameter is NULL, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="cefc4-112">*hSourceRegKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cefc4-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cefc4-113">Clé de Registre racine du paramètre utilisateur à copier.</span><span class="sxs-lookup"><span data-stu-id="cefc4-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cefc4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cefc4-114">Return value</span></span>



| <span data-ttu-id="cefc4-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cefc4-115">Return code</span></span>                                                                          | <span data-ttu-id="cefc4-116">Description</span><span class="sxs-lookup"><span data-stu-id="cefc4-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="cefc4-117"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="cefc4-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="cefc4-118">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="cefc4-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="cefc4-119"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="cefc4-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="cefc4-120">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="cefc4-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="cefc4-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="cefc4-121">Examples</span></span>

<span data-ttu-id="cefc4-122">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="cefc4-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="cefc4-123">L’exemple suivant montre comment obtenir un pointeur vers cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cefc4-123">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="cefc4-124">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="cefc4-124">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="cefc4-125">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="cefc4-125">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="cefc4-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cefc4-126">Requirements</span></span>



| <span data-ttu-id="cefc4-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cefc4-127">Requirement</span></span> | <span data-ttu-id="cefc4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="cefc4-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cefc4-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cefc4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cefc4-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cefc4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cefc4-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cefc4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cefc4-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cefc4-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cefc4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cefc4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cefc4-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cefc4-134"><dt>Input.dll</dt></span></span> </dl> |



 

