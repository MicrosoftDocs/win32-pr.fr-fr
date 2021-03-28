---
description: Utilisé pour déterminer s’il faut afficher l’option partager ce dossier dans l’affichage Web.
title: CanShareFolderW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525402"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="98a1c-103">CanShareFolderW fonction)</span><span class="sxs-lookup"><span data-stu-id="98a1c-103">CanShareFolderW function</span></span>

<span data-ttu-id="98a1c-104">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="98a1c-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="98a1c-105">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="98a1c-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="98a1c-106">Utilisé pour déterminer s’il faut afficher l’option **partager ce dossier** dans l’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="98a1c-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="98a1c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98a1c-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="98a1c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98a1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98a1c-109">*pszPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98a1c-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98a1c-110">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="98a1c-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="98a1c-111">Pointeur vers une chaîne qui spécifie le chemin d’accès du dossier à tester.</span><span class="sxs-lookup"><span data-stu-id="98a1c-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98a1c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98a1c-112">Return value</span></span>

<span data-ttu-id="98a1c-113">Type : **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="98a1c-113">Type: **STDAPI**</span></span>

<span data-ttu-id="98a1c-114">Les valeurs de retour sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="98a1c-114">Return values include the following.</span></span>



| <span data-ttu-id="98a1c-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="98a1c-115">Return code/value</span></span>                                                                        | <span data-ttu-id="98a1c-116">Description</span><span class="sxs-lookup"><span data-stu-id="98a1c-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98a1c-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98a1c-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="98a1c-118">Le chemin d’accès pointé par *pszPath* spécifie un dossier qui peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="98a1c-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="98a1c-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="98a1c-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="98a1c-120">Le chemin d’accès pointé par *pszPath* spécifie un dossier qui ne peut pas être partagé.</span><span class="sxs-lookup"><span data-stu-id="98a1c-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="98a1c-121"><dt>Erreur HRESULT</dt></span><span class="sxs-lookup"><span data-stu-id="98a1c-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="98a1c-122">Une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="98a1c-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="98a1c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="98a1c-123">Remarks</span></span>

<span data-ttu-id="98a1c-124">Cette fonction n’a pas de fichier. lib associé.</span><span class="sxs-lookup"><span data-stu-id="98a1c-124">This function has no associated .lib file.</span></span> <span data-ttu-id="98a1c-125">Vous devez utiliser [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="98a1c-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="98a1c-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="98a1c-126">Requirements</span></span>



| <span data-ttu-id="98a1c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98a1c-127">Requirement</span></span> | <span data-ttu-id="98a1c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="98a1c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98a1c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98a1c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="98a1c-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98a1c-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="98a1c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98a1c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="98a1c-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98a1c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="98a1c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="98a1c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98a1c-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98a1c-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="98a1c-135">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="98a1c-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="98a1c-136">**CanShareFolderW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="98a1c-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="98a1c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98a1c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a1c-138">**ShowShareFolderUI**</span><span class="sxs-lookup"><span data-stu-id="98a1c-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
