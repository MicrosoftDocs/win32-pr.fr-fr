---
title: IMsRdpClientShell propriété PublicMode
description: Spécifie ou récupère si le mode public est activé.
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PublicMode
- Services Bureau à distance de la propriété PublicMode, interface IMsRdpClientShell
- Services Bureau à distance de l’interface IMsRdpClientShell, propriété PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4129b3a9eeb62af0fa6e970c812ea6adf9670c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466003"
---
# <a name="imsrdpclientshellpublicmode-property"></a><span data-ttu-id="bbd4e-106">IMsRdpClientShell ::P propriété ublicMode</span><span class="sxs-lookup"><span data-stu-id="bbd4e-106">IMsRdpClientShell::PublicMode property</span></span>

<span data-ttu-id="bbd4e-107">Spécifie ou récupère si le mode public est activé.</span><span class="sxs-lookup"><span data-stu-id="bbd4e-107">Specifies or retrieves whether public mode is enabled.</span></span>

<span data-ttu-id="bbd4e-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bbd4e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd4e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbd4e-109">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="bbd4e-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bbd4e-110">Property value</span></span>

<span data-ttu-id="bbd4e-111">Spécifie si le mode public est activé.</span><span class="sxs-lookup"><span data-stu-id="bbd4e-111">Specifies whether public mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd4e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbd4e-112">Requirements</span></span>



| <span data-ttu-id="bbd4e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbd4e-113">Requirement</span></span> | <span data-ttu-id="bbd4e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbd4e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd4e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbd4e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd4e-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbd4e-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bbd4e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbd4e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd4e-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbd4e-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bbd4e-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bbd4e-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="bbd4e-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbd4e-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbd4e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="bbd4e-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbd4e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbd4e-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbd4e-123">IID</span><span class="sxs-lookup"><span data-stu-id="bbd4e-123">IID</span></span><br/>                      | <span data-ttu-id="bbd4e-124">IID \_ IMsRdpClientShell est défini en tant que d012ae6d-C19A-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="bbd4e-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="bbd4e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbd4e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd4e-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="bbd4e-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





