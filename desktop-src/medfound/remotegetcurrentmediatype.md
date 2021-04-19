---
description: 'Version accessible à distance de la méthode IMFMediaTypeHandler :: GetCurrentMediaType.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: RemoteGetCurrentMediaType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524765"
---
# <a name="remotegetcurrentmediatype"></a><span data-ttu-id="acdf8-103">RemoteGetCurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="acdf8-103">RemoteGetCurrentMediaType</span></span>

<span data-ttu-id="acdf8-104">Version accessible à distance de la méthode [**IMFMediaTypeHandler :: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="acdf8-104">Remotable version of the [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) method.</span></span>

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a><span data-ttu-id="acdf8-105">Notes</span><span class="sxs-lookup"><span data-stu-id="acdf8-105">Remarks</span></span>

<span data-ttu-id="acdf8-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="acdf8-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="acdf8-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="acdf8-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="acdf8-108">Si [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="acdf8-108">If [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

<span data-ttu-id="acdf8-109">Cette interface est disponible sur les plateformes suivantes si les composants redistribuables du kit de développement logiciel (SDK) Windows Media format 11 sont installés :</span><span class="sxs-lookup"><span data-stu-id="acdf8-109">This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:</span></span>

-   <span data-ttu-id="acdf8-110">Windows XP avec Service Pack 2 (SP2) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="acdf8-110">Windows XP with Service Pack 2 (SP2) and later.</span></span>
-   <span data-ttu-id="acdf8-111">Windows XP Media Center Edition 2005 avec KB900325 (Windows XP Media Center Edition 2005) et KB925766 (correctif cumulatif de mise à jour d’octobre 2006 pour Windows XP Édition Media Center) installé.</span><span class="sxs-lookup"><span data-stu-id="acdf8-111">Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="acdf8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acdf8-112">Requirements</span></span>



| <span data-ttu-id="acdf8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acdf8-113">Requirement</span></span> | <span data-ttu-id="acdf8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="acdf8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdf8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acdf8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="acdf8-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="acdf8-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="acdf8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acdf8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="acdf8-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="acdf8-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="acdf8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="acdf8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="acdf8-120"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acdf8-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="acdf8-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="acdf8-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="acdf8-122"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acdf8-122"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="acdf8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acdf8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acdf8-124">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="acdf8-124">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




