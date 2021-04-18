---
title: QueryLayoutOrTipStringUserReg fonction)
description: Interroge la chaîne spécifiée qui représente le format d’une liste de dispositions de clavier ou d’une liste de profils de services de texte du chemin d’accès au registre spécifié.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- QueryLayoutOrTipStringUserReg fonction Text Services Framework
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511961"
---
# <a name="querylayoutortipstringuserreg-function"></a><span data-ttu-id="0244f-104">QueryLayoutOrTipStringUserReg fonction)</span><span class="sxs-lookup"><span data-stu-id="0244f-104">QueryLayoutOrTipStringUserReg function</span></span>

<span data-ttu-id="0244f-105">Interroge la chaîne spécifiée qui représente le format d’une liste de dispositions de clavier ou d’une liste de profils de services de texte du chemin d’accès au registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="0244f-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list of the specified registry path.</span></span>

## <a name="syntax"></a><span data-ttu-id="0244f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0244f-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0244f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0244f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0244f-108">*pszUserReg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0244f-108">*pszUserReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0244f-109">Chemin d’accès au registre de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0244f-109">The registry path of the user.</span></span> <span data-ttu-id="0244f-110">Si ce paramètre a la **valeur null**, HKEY \_ Current \_ User est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0244f-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="0244f-111">*pszSystemReg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0244f-111">*pszSystemReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0244f-112">Chemin d’accès au registre du système.</span><span class="sxs-lookup"><span data-stu-id="0244f-112">The registry path of the system.</span></span> <span data-ttu-id="0244f-113">Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ System est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0244f-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="0244f-114">*pszSoftwareReg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0244f-114">*pszSoftwareReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0244f-115">Chemin d’accès du Registre du logiciel.</span><span class="sxs-lookup"><span data-stu-id="0244f-115">The registry path of the software.</span></span> <span data-ttu-id="0244f-116">Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ Software est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0244f-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="0244f-117">*PSZ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0244f-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0244f-118">Chaîne qui représente une liste de dispositions de clavier ou une liste de profils de services de texte.</span><span class="sxs-lookup"><span data-stu-id="0244f-118">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="0244f-119">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0244f-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0244f-120">Doit être 0.</span><span class="sxs-lookup"><span data-stu-id="0244f-120">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0244f-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0244f-121">Return value</span></span>

<span data-ttu-id="0244f-122">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0244f-122">This function can return one of these values.</span></span>



| <span data-ttu-id="0244f-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0244f-123">Return code</span></span>                                                                                  | <span data-ttu-id="0244f-124">Description</span><span class="sxs-lookup"><span data-stu-id="0244f-124">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0244f-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0244f-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0244f-126">Toutes les dispositions ou tous les profils définis dans **PSZ** sont valides.</span><span class="sxs-lookup"><span data-stu-id="0244f-126">All layouts or profiles defined in **psz** are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="0244f-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0244f-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0244f-128">Une ou plusieurs des dispositions ou des profils définis dans **PSZ** ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0244f-128">One or more of the layouts or profiles defined in **psz** are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0244f-129">Notes</span><span class="sxs-lookup"><span data-stu-id="0244f-129">Remarks</span></span>

<span data-ttu-id="0244f-130">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="0244f-130">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="0244f-131">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="0244f-131">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="0244f-132">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="0244f-132">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="0244f-133">Le format de chaîne de la liste de présentation est le suivant :</span><span class="sxs-lookup"><span data-stu-id="0244f-133">The string format of the layout list is:</span></span>

<span data-ttu-id="0244f-134"><LangID 1> : <KLID 1> ; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="0244f-134"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="0244f-135">Le format de chaîne de la liste des profils de service de texte est le suivant :</span><span class="sxs-lookup"><span data-stu-id="0244f-135">The string format of the text service profile list is:</span></span>

<span data-ttu-id="0244f-136"><LangID 1> : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="0244f-136"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="0244f-137">Voici un exemple de valeur pour le paramètre *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="0244f-137">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="0244f-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0244f-138">Requirements</span></span>



| <span data-ttu-id="0244f-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0244f-139">Requirement</span></span> | <span data-ttu-id="0244f-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="0244f-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0244f-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0244f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0244f-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0244f-142">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0244f-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0244f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0244f-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0244f-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0244f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0244f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0244f-146"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0244f-146"><dt>Input.dll</dt></span></span> </dl> |



 

