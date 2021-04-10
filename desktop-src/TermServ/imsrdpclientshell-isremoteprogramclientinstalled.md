---
title: IMsRdpClientShell propriété IsRemoteProgramClientInstalled
description: Récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp de Windows Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété IsRemoteProgramClientInstalled
- Services Bureau à distance de la propriété IsRemoteProgramClientInstalled, interface IMsRdpClientShell
- Services Bureau à distance de l’interface IMsRdpClientShell, propriété IsRemoteProgramClientInstalled
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103269"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a><span data-ttu-id="4f4bc-106">IMsRdpClientShell :: IsRemoteProgramClientInstalled, propriété</span><span class="sxs-lookup"><span data-stu-id="4f4bc-106">IMsRdpClientShell::IsRemoteProgramClientInstalled property</span></span>

<span data-ttu-id="4f4bc-107">Récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-107">Retrieves whether the Remote Desktop Connection (RDC) client supports Windows Server 2008 R2 RemoteApp functionality.</span></span>

<span data-ttu-id="4f4bc-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4bc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f4bc-109">Syntax</span></span>


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a><span data-ttu-id="4f4bc-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4f4bc-110">Property value</span></span>

<span data-ttu-id="4f4bc-111">Récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-111">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4bc-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f4bc-112">Requirements</span></span>



| <span data-ttu-id="4f4bc-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f4bc-113">Requirement</span></span> | <span data-ttu-id="4f4bc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f4bc-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4bc-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f4bc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4bc-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f4bc-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4f4bc-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f4bc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4bc-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f4bc-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4f4bc-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4f4bc-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f4bc-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f4bc-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f4bc-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4f4bc-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f4bc-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f4bc-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f4bc-123">IID</span><span class="sxs-lookup"><span data-stu-id="4f4bc-123">IID</span></span><br/>                      | <span data-ttu-id="4f4bc-124">IID \_ IMsRdpClientShell est défini en tant que d012ae6d-C19A-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="4f4bc-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="4f4bc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f4bc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4bc-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="4f4bc-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





