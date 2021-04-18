---
title: IMsRdpClientShell2 propriété SecuredSettingsEnabled
description: Récupère une valeur qui indique si la page Web active se trouve dans une zone de sécurité d’URL Internet Explorer approuvée.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClientShell2
- Services Bureau à distance de l’interface IMsRdpClientShell2, propriété SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106529083"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a><span data-ttu-id="fecca-106">IMsRdpClientShell2 :: SecuredSettingsEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="fecca-106">IMsRdpClientShell2::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="fecca-107">Récupère une valeur qui indique si la page Web active se trouve dans une zone de sécurité d’URL Internet Explorer approuvée.</span><span class="sxs-lookup"><span data-stu-id="fecca-107">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

<span data-ttu-id="fecca-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fecca-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fecca-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fecca-109">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="fecca-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fecca-110">Property value</span></span>

<span data-ttu-id="fecca-111">Pointeur vers une valeur booléenne qui indique si la page Web active se trouve dans une zone de sécurité d’URL Internet Explorer approuvée.</span><span class="sxs-lookup"><span data-stu-id="fecca-111">A pointer to a Boolean value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="fecca-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fecca-112">Requirements</span></span>



| <span data-ttu-id="fecca-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fecca-113">Requirement</span></span> | <span data-ttu-id="fecca-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="fecca-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fecca-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fecca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fecca-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fecca-116">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fecca-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fecca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fecca-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fecca-118">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="fecca-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fecca-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fecca-120"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fecca-120"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fecca-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fecca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fecca-122">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="fecca-122">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

 





