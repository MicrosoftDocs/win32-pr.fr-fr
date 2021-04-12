---
description: Affiche l’onglet partage de dossiers de la feuille de propriétés du dossier spécifié.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319546"
---
# <a name="showsharefolderui-function"></a><span data-ttu-id="fa8e5-103">ShowShareFolderUI fonction)</span><span class="sxs-lookup"><span data-stu-id="fa8e5-103">ShowShareFolderUI function</span></span>

<span data-ttu-id="fa8e5-104">Affiche l’onglet **partage de dossiers** de la feuille de propriétés du dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="fa8e5-104">Displays the **Folder Sharing** tab on the properties sheet for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa8e5-105">Syntax</span></span>


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="fa8e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa8e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa8e5-107">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8e5-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8e5-108">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="fa8e5-108">Type: **HWND**</span></span>

<span data-ttu-id="fa8e5-109">Handle de la fenêtre parente pour la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fa8e5-109">A handle to the parent window for the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="fa8e5-110">*pszPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8e5-110">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8e5-111">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="fa8e5-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="fa8e5-112">Pointeur vers une chaîne qui spécifie le chemin d’accès au dossier qui affiche son onglet **partage de dossiers** .</span><span class="sxs-lookup"><span data-stu-id="fa8e5-112">A pointer to a string that specifies the path to the folder that displays its **Folder Sharing** tab.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa8e5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa8e5-113">Return value</span></span>

<span data-ttu-id="fa8e5-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fa8e5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fa8e5-115">Cette fonction retourne toujours S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fa8e5-115">This function always returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa8e5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fa8e5-116">Remarks</span></span>

<span data-ttu-id="fa8e5-117">Cette fonction n’a pas de fichier. lib associé.</span><span class="sxs-lookup"><span data-stu-id="fa8e5-117">This function has no associated .lib file.</span></span> <span data-ttu-id="fa8e5-118">Vous devez utiliser [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="fa8e5-118">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa8e5-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fa8e5-119">Requirements</span></span>



| <span data-ttu-id="fa8e5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa8e5-120">Requirement</span></span> | <span data-ttu-id="fa8e5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa8e5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8e5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fa8e5-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa8e5-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fa8e5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fa8e5-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa8e5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fa8e5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fa8e5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa8e5-127"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa8e5-127"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa8e5-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fa8e5-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fa8e5-129">**ShowShareFolderUIW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="fa8e5-129">**ShowShareFolderUIW** (Unicode)</span></span><br/>                                            |



## <a name="see-also"></a><span data-ttu-id="fa8e5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa8e5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8e5-131">**CanShareFolderW**</span><span class="sxs-lookup"><span data-stu-id="fa8e5-131">**CanShareFolderW**</span></span>](cansharefolderw.md)
</dt> </dl>

 

 
