---
description: Charge le fichier de ressources AppHelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393076"
---
# <a name="sdbopenapphelpresourcefile-function"></a><span data-ttu-id="539c6-103">SdbOpenApphelpResourceFile fonction)</span><span class="sxs-lookup"><span data-stu-id="539c6-103">SdbOpenApphelpResourceFile function</span></span>

<span data-ttu-id="539c6-104">Charge le fichier de ressources AppHelp.</span><span class="sxs-lookup"><span data-stu-id="539c6-104">Loads the Apphelp resource file.</span></span>

## <a name="syntax"></a><span data-ttu-id="539c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="539c6-105">Syntax</span></span>


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a><span data-ttu-id="539c6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="539c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="539c6-107">*pwszACResourceFile* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="539c6-107">*pwszACResourceFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="539c6-108">Chemin d’accès au fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="539c6-108">The path to the resource file.</span></span> <span data-ttu-id="539c6-109">Si ce paramètre a la **valeur null**, la dll de ressource locale est ouverte.</span><span class="sxs-lookup"><span data-stu-id="539c6-109">If this parameter is **NULL**, the local resource DLL is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="539c6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="539c6-110">Return value</span></span>

<span data-ttu-id="539c6-111">La fonction retourne un handle au fichier de ressources ouvert.</span><span class="sxs-lookup"><span data-stu-id="539c6-111">The function returns a handle to the opened resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="539c6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="539c6-112">Requirements</span></span>



| <span data-ttu-id="539c6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="539c6-113">Requirement</span></span> | <span data-ttu-id="539c6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="539c6-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="539c6-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="539c6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="539c6-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="539c6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="539c6-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="539c6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="539c6-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="539c6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="539c6-119">DLL</span><span class="sxs-lookup"><span data-stu-id="539c6-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="539c6-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="539c6-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




