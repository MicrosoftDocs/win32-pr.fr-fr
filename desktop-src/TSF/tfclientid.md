---
title: TfClientId (msctf. h)
description: Le type de données TfClientId est utilisé pour identifier le client.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740876"
---
# <a name="tfclientid"></a><span data-ttu-id="d5226-104">TfClientId</span><span class="sxs-lookup"><span data-stu-id="d5226-104">TfClientId</span></span>

<span data-ttu-id="d5226-105">Le type de données **TfClientId** est utilisé pour identifier le client.</span><span class="sxs-lookup"><span data-stu-id="d5226-105">The **TfClientId** data type is used to identify the client.</span></span>


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a><span data-ttu-id="d5226-106">Notes</span><span class="sxs-lookup"><span data-stu-id="d5226-106">Remarks</span></span>

<span data-ttu-id="d5226-107">Dans TSF, les applications et les services de texte sont généralement appelés clients.</span><span class="sxs-lookup"><span data-stu-id="d5226-107">Within TSF, applications and text services are generally referred to as clients.</span></span> <span data-ttu-id="d5226-108">Chaque client reçoit un identificateur unique qu’il utilise pour s’identifier lui-même lors de l’appel de différentes méthodes de gestionnaire TSF.</span><span class="sxs-lookup"><span data-stu-id="d5226-108">Each client receives a unique identifier that it uses to identify itself when calling various TSF manager methods.</span></span> <span data-ttu-id="d5226-109">Cet identificateur est du type **TfClientId** .</span><span class="sxs-lookup"><span data-stu-id="d5226-109">This identifier is of the **TfClientId** type.</span></span>

<span data-ttu-id="d5226-110">Le type de données **TfClientId** est fourni par le gestionnaire TSF.</span><span class="sxs-lookup"><span data-stu-id="d5226-110">The **TfClientId** data type is supplied by the TSF manager.</span></span> <span data-ttu-id="d5226-111">Une application obtient une valeur **TfClientId** lorsqu’elle appelle [ITfThreadMgr :: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="d5226-111">An application obtains a **TfClientId** value when it calls [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span> <span data-ttu-id="d5226-112">La valeur TfClientId d’un service de texte est transmise à la méthode [ITfTextInputProcessor :: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .</span><span class="sxs-lookup"><span data-stu-id="d5226-112">The TfClientId value for a text service is passed to the [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span> <span data-ttu-id="d5226-113">Tout objet qui ne correspond pas aux catégories ci-dessus peut obtenir un identificateur de client en appelant [ITfClientId :: GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span><span class="sxs-lookup"><span data-stu-id="d5226-113">Any object that does not fit the above categories can obtain a client identifier by calling [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5226-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5226-114">Requirements</span></span>



| <span data-ttu-id="d5226-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5226-115">Requirement</span></span> | <span data-ttu-id="d5226-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5226-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5226-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5226-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5226-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d5226-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="d5226-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5226-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5226-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d5226-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d5226-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d5226-121">Redistributable</span></span><br/>          | <span data-ttu-id="d5226-122">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="d5226-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="d5226-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5226-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5226-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5226-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5226-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="d5226-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5226-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5226-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5226-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5226-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5226-128">**ITfClientId::GetClientId**</span><span class="sxs-lookup"><span data-stu-id="d5226-128">**ITfClientId::GetClientId**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[<span data-ttu-id="d5226-129">**ITfTextInputProcessor :: Activate**</span><span class="sxs-lookup"><span data-stu-id="d5226-129">**ITfTextInputProcessor::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="d5226-130">**ITfThreadMgr :: Activate**</span><span class="sxs-lookup"><span data-stu-id="d5226-130">**ITfThreadMgr::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





