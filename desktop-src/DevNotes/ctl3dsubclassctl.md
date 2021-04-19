---
description: Sous-classe un contrôle individuel, sauf si le contrôle s’affiche dans une boîte de dialogue.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545611"
---
# <a name="ctl3dsubclassctl-function"></a><span data-ttu-id="88f4e-103">Ctl3dSubclassCtl fonction)</span><span class="sxs-lookup"><span data-stu-id="88f4e-103">Ctl3dSubclassCtl function</span></span>

<span data-ttu-id="88f4e-104">Sous-classe un contrôle individuel, sauf si le contrôle s’affiche dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88f4e-104">Subclasses an individual control unless the control appears in a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f4e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88f4e-105">Syntax</span></span>


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="88f4e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88f4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88f4e-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="88f4e-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="88f4e-108">Handle de la fenêtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="88f4e-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88f4e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88f4e-109">Return value</span></span>

<span data-ttu-id="88f4e-110">Retourne la **valeur true** si le contrôle est sous-classé avec succès ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="88f4e-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="88f4e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="88f4e-111">Remarks</span></span>

<span data-ttu-id="88f4e-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="88f4e-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="88f4e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88f4e-113">Requirements</span></span>



| <span data-ttu-id="88f4e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88f4e-114">Requirement</span></span> | <span data-ttu-id="88f4e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="88f4e-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88f4e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="88f4e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="88f4e-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88f4e-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f4e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88f4e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f4e-119">**Ctl3dUnsubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="88f4e-119">**Ctl3dUnsubclassCtl**</span></span>](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
