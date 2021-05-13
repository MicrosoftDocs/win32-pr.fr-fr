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
ms.openlocfilehash: 46df03208ecc468aac366fb0b4cfb33e1a68157e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841680"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="facb0-103">CanShareFolderW fonction)</span><span class="sxs-lookup"><span data-stu-id="facb0-103">CanShareFolderW function</span></span>

<span data-ttu-id="facb0-104">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="facb0-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="facb0-105">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="facb0-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="facb0-106">Utilisé pour déterminer s’il faut afficher l’option **partager ce dossier** dans l’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="facb0-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="facb0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="facb0-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="facb0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="facb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="facb0-109">*pszPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="facb0-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facb0-110">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="facb0-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="facb0-111">Pointeur vers une chaîne qui spécifie le chemin d’accès du dossier à tester.</span><span class="sxs-lookup"><span data-stu-id="facb0-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="facb0-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="facb0-112">Return value</span></span>

<span data-ttu-id="facb0-113">Type : **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="facb0-113">Type: **STDAPI**</span></span>

<span data-ttu-id="facb0-114">Les valeurs de retour sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="facb0-114">Return values include the following.</span></span>



| <span data-ttu-id="facb0-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="facb0-115">Return code/value</span></span>                                                                        | <span data-ttu-id="facb0-116">Description</span><span class="sxs-lookup"><span data-stu-id="facb0-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="facb0-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="facb0-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="facb0-118">Le chemin d’accès pointé par *pszPath* spécifie un dossier qui peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="facb0-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="facb0-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="facb0-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="facb0-120">Le chemin d’accès pointé par *pszPath* spécifie un dossier qui ne peut pas être partagé.</span><span class="sxs-lookup"><span data-stu-id="facb0-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="facb0-121"><dt>Erreur HRESULT</dt></span><span class="sxs-lookup"><span data-stu-id="facb0-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="facb0-122">Une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="facb0-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="facb0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="facb0-123">Remarks</span></span>

<span data-ttu-id="facb0-124">Cette fonction n’a pas de fichier. lib associé.</span><span class="sxs-lookup"><span data-stu-id="facb0-124">This function has no associated .lib file.</span></span> <span data-ttu-id="facb0-125">Vous devez utiliser [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="facb0-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="facb0-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="facb0-126">Requirements</span></span>



| <span data-ttu-id="facb0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="facb0-127">Requirement</span></span> | <span data-ttu-id="facb0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="facb0-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="facb0-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="facb0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="facb0-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="facb0-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="facb0-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="facb0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="facb0-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="facb0-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="facb0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="facb0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="facb0-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="facb0-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="facb0-135">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="facb0-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="facb0-136">**CanShareFolderW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="facb0-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="facb0-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="facb0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="facb0-138">**ShowShareFolderUI**</span><span class="sxs-lookup"><span data-stu-id="facb0-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
