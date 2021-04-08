---
title: IMsRdpPreferredRedirectionInfo propriété UseRedirectionServerName
description: Obtient et définit s’il faut utiliser le nom du serveur de redirection.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété UseRedirectionServerName
- Services Bureau à distance de la propriété UseRedirectionServerName, interface IMsRdpPreferredRedirectionInfo
- Services Bureau à distance de l’interface IMsRdpPreferredRedirectionInfo, propriété UseRedirectionServerName
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740757"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a><span data-ttu-id="29965-106">IMsRdpPreferredRedirectionInfo :: UseRedirectionServerName, propriété</span><span class="sxs-lookup"><span data-stu-id="29965-106">IMsRdpPreferredRedirectionInfo::UseRedirectionServerName property</span></span>

<span data-ttu-id="29965-107">Obtient et définit s’il faut utiliser le nom du serveur de redirection.</span><span class="sxs-lookup"><span data-stu-id="29965-107">Gets and sets whether to use the redirection server name.</span></span>

<span data-ttu-id="29965-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="29965-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="29965-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29965-109">Syntax</span></span>


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a><span data-ttu-id="29965-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="29965-110">Property value</span></span>

<span data-ttu-id="29965-111">Indique s’il faut utiliser le nom du serveur de redirection.</span><span class="sxs-lookup"><span data-stu-id="29965-111">Whether to use the redirection server name.</span></span>

## <a name="requirements"></a><span data-ttu-id="29965-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29965-112">Requirements</span></span>



| <span data-ttu-id="29965-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29965-113">Requirement</span></span> | <span data-ttu-id="29965-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="29965-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29965-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29965-115">Minimum supported client</span></span><br/> | <span data-ttu-id="29965-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29965-116">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="29965-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29965-117">Minimum supported server</span></span><br/> | <span data-ttu-id="29965-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29965-118">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="29965-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="29965-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="29965-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29965-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="29965-121">DLL</span><span class="sxs-lookup"><span data-stu-id="29965-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29965-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29965-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="29965-123">IID</span><span class="sxs-lookup"><span data-stu-id="29965-123">IID</span></span><br/>                      | <span data-ttu-id="29965-124">IID \_ IMsRdpPreferredRedirectionInfo est défini en tant que FDD029F9-9574-4def-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="29965-124">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29965-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29965-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29965-126">**IMsRdpPreferredRedirectionInfo**</span><span class="sxs-lookup"><span data-stu-id="29965-126">**IMsRdpPreferredRedirectionInfo**</span></span>](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





