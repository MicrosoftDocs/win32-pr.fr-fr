---
title: EnumEnabledLayoutOrTip fonction)
description: Énumère toutes les dispositions de clavier activées ou les services de texte du paramètre utilisateur spécifié.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- EnumEnabledLayoutOrTip fonction Text Services Framework
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510138"
---
# <a name="enumenabledlayoutortip-function"></a><span data-ttu-id="b0899-104">EnumEnabledLayoutOrTip fonction)</span><span class="sxs-lookup"><span data-stu-id="b0899-104">EnumEnabledLayoutOrTip function</span></span>

<span data-ttu-id="b0899-105">Énumère toutes les dispositions de clavier activées ou les services de texte du paramètre utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="b0899-105">Enumerates all enabled keyboard layouts or text services of the specified user setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0899-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0899-106">Syntax</span></span>


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a><span data-ttu-id="b0899-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0899-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0899-108">*pszUserReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b0899-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0899-109">Chemin d’accès au registre de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0899-109">The registry path of the user.</span></span> <span data-ttu-id="b0899-110">Si ce paramètre a la **valeur null**, HKEY \_ Current \_ User est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b0899-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="b0899-111">*pszSystemReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b0899-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0899-112">Chemin d’accès au registre du système.</span><span class="sxs-lookup"><span data-stu-id="b0899-112">The registry path of the system.</span></span> <span data-ttu-id="b0899-113">Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ System est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b0899-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="b0899-114">*pszSoftwareReg* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b0899-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0899-115">Chemin d’accès du Registre du logiciel.</span><span class="sxs-lookup"><span data-stu-id="b0899-115">The registry path of the software.</span></span> <span data-ttu-id="b0899-116">Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ Software est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b0899-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="b0899-117">*pLayoutOrTipProfile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0899-117">*pLayoutOrTipProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0899-118">Pointeur vers la mémoire tampon qui reçoit le tableau LAYOUTORTIPPROFILE.</span><span class="sxs-lookup"><span data-stu-id="b0899-118">Pointer to the buffer that receives the LAYOUTORTIPPROFILE array.</span></span>

</dd> <dt>

<span data-ttu-id="b0899-119">*uBufLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0899-119">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0899-120">Longueur de la mémoire tampon vers laquelle pointe *pLayoutOrTipProfile*.</span><span class="sxs-lookup"><span data-stu-id="b0899-120">The length of the buffer pointed to by *pLayoutOrTipProfile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0899-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0899-121">Return value</span></span>

<span data-ttu-id="b0899-122">Si *pLayoutOrTipProfile* a la **valeur null**, le nombre d’éléments de clavier activés dans le paramètre utilisateur ; dans le cas contraire, il s’agit du nombre d’éléments de clavier copiés dans *pLayoutOrTipProfile*.</span><span class="sxs-lookup"><span data-stu-id="b0899-122">If *pLayoutOrTipProfile* is **NULL**, the number of keyboard items that are enabled in the user setting; otherwise, the number of keyboard items that are copied into *pLayoutOrTipProfile*.</span></span>

<span data-ttu-id="b0899-123">Pour les langages de l’éditeur de méthode d’entrée (IME), tous les IME sont retournés, même si un seul IME est activé.</span><span class="sxs-lookup"><span data-stu-id="b0899-123">For Input Method Editor (IME) languages, all IMEs are returned, even when only one IME is enabled.</span></span> <span data-ttu-id="b0899-124">Par exemple, si CHT New Quick IME est activé pour un utilisateur, la fonction **EnumEnabledLayoutOrTip** retourne les 5 IME cht.</span><span class="sxs-lookup"><span data-stu-id="b0899-124">For example, if a user has the CHT New Quick IME enabled, the **EnumEnabledLayoutOrTip** function returns all 5 CHT IMEs.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0899-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b0899-125">Remarks</span></span>

<span data-ttu-id="b0899-126">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="b0899-126">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="b0899-127">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="b0899-127">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="b0899-128">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="b0899-128">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="b0899-129">La définition de LAYOUTORTIPPROFILE est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b0899-129">The definition of LAYOUTORTIPPROFILE is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a><span data-ttu-id="b0899-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0899-130">Requirements</span></span>



| <span data-ttu-id="b0899-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0899-131">Requirement</span></span> | <span data-ttu-id="b0899-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0899-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b0899-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0899-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b0899-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0899-134">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b0899-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0899-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b0899-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0899-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b0899-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b0899-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0899-138"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0899-138"><dt>Input.dll</dt></span></span> </dl> |



 

