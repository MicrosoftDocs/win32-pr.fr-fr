---
description: Désactive le sous-classement pour le contrôle spécifié.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Ctl3dUnsubclassCtl fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540029"
---
# <a name="ctl3dunsubclassctl-function"></a><span data-ttu-id="0a59a-103">Ctl3dUnsubclassCtl fonction)</span><span class="sxs-lookup"><span data-stu-id="0a59a-103">Ctl3dUnsubclassCtl function</span></span>

<span data-ttu-id="0a59a-104">Désactive le sous-classement pour le contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a59a-104">Turns off subclassing for the specified control.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a59a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a59a-105">Syntax</span></span>


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="0a59a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a59a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a59a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="0a59a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0a59a-108">Handle de la fenêtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0a59a-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a59a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a59a-109">Return value</span></span>

<span data-ttu-id="0a59a-110">Retourne la **valeur true** si le contrôle est sous-classé avec succès ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="0a59a-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a59a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0a59a-111">Remarks</span></span>

<span data-ttu-id="0a59a-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0a59a-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a59a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a59a-113">Requirements</span></span>



| <span data-ttu-id="0a59a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a59a-114">Requirement</span></span> | <span data-ttu-id="0a59a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a59a-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a59a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0a59a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0a59a-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a59a-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a59a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a59a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a59a-119">**Ctl3dSubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="0a59a-119">**Ctl3dSubclassCtl**</span></span>](ctl3dsubclassctl.md)
</dt> </dl>

 

 
