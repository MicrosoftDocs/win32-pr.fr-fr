---
description: Initialise ou réinitialise la liste d’images système.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319142"
---
# <a name="fileiconinit-function"></a><span data-ttu-id="c9b06-103">FileIconInit fonction)</span><span class="sxs-lookup"><span data-stu-id="c9b06-103">FileIconInit function</span></span>

<span data-ttu-id="c9b06-104">Initialise ou réinitialise la liste d’images système.</span><span class="sxs-lookup"><span data-stu-id="c9b06-104">Initializes or reinitializes the system image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b06-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9b06-105">Syntax</span></span>


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a><span data-ttu-id="c9b06-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9b06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b06-107">*fRestoreCache* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9b06-107">*fRestoreCache* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b06-108">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="c9b06-108">Type: **BOOL**</span></span>

<span data-ttu-id="c9b06-109">**True** pour restaurer le cache de l’image système à partir du disque ; **False** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c9b06-109">**TRUE** to restore the system image cache from disk; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9b06-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9b06-110">Return value</span></span>

<span data-ttu-id="c9b06-111">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="c9b06-111">Type: **BOOL**</span></span>

<span data-ttu-id="c9b06-112">**True** si le cache a été actualisé avec succès, **false** en cas d’échec de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="c9b06-112">**TRUE** if the cache was successfully refreshed, **FALSE** if the initialization failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9b06-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c9b06-113">Remarks</span></span>

<span data-ttu-id="c9b06-114">Si vous utilisez des listes d’images système dans votre propre processus, vous devez appeler **FileIconInit** aux moments suivants :</span><span class="sxs-lookup"><span data-stu-id="c9b06-114">If you are using system image lists in your own process, you must call **FileIconInit** at the following times:</span></span>

-   <span data-ttu-id="c9b06-115">Au lancement.</span><span class="sxs-lookup"><span data-stu-id="c9b06-115">On launch.</span></span>
-   <span data-ttu-id="c9b06-116">En réponse à un message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) lorsque l’indicateur [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) est défini.</span><span class="sxs-lookup"><span data-stu-id="c9b06-116">In response to a [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message when the [**SPI\_SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) flag is set.</span></span>

<span data-ttu-id="c9b06-117">**FileIconInit** n’est pas inclus dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="c9b06-117">**FileIconInit** is not included in a header file.</span></span> <span data-ttu-id="c9b06-118">Vous devez l’appeler directement à partir de Shell32.dll, en utilisant l’ordinal 660.</span><span class="sxs-lookup"><span data-stu-id="c9b06-118">You must call it directly from Shell32.dll, using ordinal 660.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b06-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c9b06-119">Requirements</span></span>



| <span data-ttu-id="c9b06-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9b06-120">Requirement</span></span> | <span data-ttu-id="c9b06-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9b06-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b06-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9b06-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b06-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9b06-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c9b06-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9b06-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b06-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9b06-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c9b06-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c9b06-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9b06-127"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9b06-127"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
