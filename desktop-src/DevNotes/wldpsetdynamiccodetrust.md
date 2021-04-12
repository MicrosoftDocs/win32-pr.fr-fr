---
description: Définit une liste de révocation de code dynamique de la liste de révocation de certificats .NET sur disque pour .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: WldpSetDynamicCodeTrust, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393023"
---
# <a name="wldpsetdynamiccodetrust-function"></a><span data-ttu-id="8ccea-103">WldpSetDynamicCodeTrust fonction)</span><span class="sxs-lookup"><span data-stu-id="8ccea-103">WldpSetDynamicCodeTrust function</span></span>

<span data-ttu-id="8ccea-104">Définit une liste de révocation de code dynamique de la liste de révocation de certificats .NET sur disque pour .NET.</span><span class="sxs-lookup"><span data-stu-id="8ccea-104">Sets an on-disk .NET CRL Dynamic Code trustable for .NET.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ccea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ccea-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a><span data-ttu-id="8ccea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ccea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ccea-107">*FileHandle*</span><span class="sxs-lookup"><span data-stu-id="8ccea-107">*FileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="8ccea-108">Handle vers un fichier de code dynamique sur disque.</span><span class="sxs-lookup"><span data-stu-id="8ccea-108">Handle to a on-disk dynamic code file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ccea-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ccea-109">Return value</span></span>

<span data-ttu-id="8ccea-110">Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8ccea-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ccea-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ccea-111">Requirements</span></span>



| <span data-ttu-id="8ccea-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ccea-112">Requirement</span></span> | <span data-ttu-id="8ccea-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ccea-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ccea-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ccea-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8ccea-115">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ccea-115">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8ccea-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ccea-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8ccea-117">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ccea-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8ccea-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ccea-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ccea-119"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ccea-119"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ccea-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8ccea-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ccea-121"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ccea-121"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




