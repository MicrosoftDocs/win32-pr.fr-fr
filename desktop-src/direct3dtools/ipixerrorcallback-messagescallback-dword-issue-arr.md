---
description: Rappel qui avertit l’hôte des messages retournés par la requête associée.
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixErrorCallback :: MessagesCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b95a95a6ef472f2603bfa6b21c85659634074a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514310"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span data-ttu-id="9aac1-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback :: MessagesCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="9aac1-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback::MessagesCallback method</span></span>

<span data-ttu-id="9aac1-104">Rappel qui avertit l’hôte des messages retournés par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="9aac1-104">A callback that notifies the host of messages returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aac1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9aac1-105">Syntax</span></span>


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a><span data-ttu-id="9aac1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9aac1-106">Parameters</span></span>

<span data-ttu-id="9aac1-107">*saut* </span><span class="sxs-lookup"><span data-stu-id="9aac1-107">*count* </span></span>  
<span data-ttu-id="9aac1-108">Nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="9aac1-108">The number of messages.</span></span>

<span data-ttu-id="9aac1-109">*\_messages count0* </span><span class="sxs-lookup"><span data-stu-id="9aac1-109">*count0\_messages* </span></span>  
<span data-ttu-id="9aac1-110">Messages.</span><span class="sxs-lookup"><span data-stu-id="9aac1-110">The messages.</span></span>

## <a name="return-value"></a><span data-ttu-id="9aac1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9aac1-111">Return value</span></span>

<span data-ttu-id="9aac1-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9aac1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9aac1-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9aac1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aac1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9aac1-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9aac1-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="9aac1-115">Header</span></span></p></td><td><span data-ttu-id="9aac1-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9aac1-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9aac1-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9aac1-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9aac1-118">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="9aac1-118">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
