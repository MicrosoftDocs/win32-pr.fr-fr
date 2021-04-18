---
title: Session. identify, méthode (WSManDisp. h)
description: Interroge un ordinateur distant pour déterminer s’il prend en charge le protocole WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Identifiez la méthode Windows Remote Management
- Identifier la méthode Windows Remote Management, objet session
- Windows Remote Management d’objet de session, méthode d’identification
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509355"
---
# <a name="sessionidentify-method"></a><span data-ttu-id="9e15d-106">Session. identify, méthode</span><span class="sxs-lookup"><span data-stu-id="9e15d-106">Session.Identify method</span></span>

<span data-ttu-id="9e15d-107">La méthode **session. identify** interroge un ordinateur distant pour déterminer s’il prend en charge le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="9e15d-107">The **Session.Identify** method queries a remote computer to determine if it supports the WS-Management protocol.</span></span> <span data-ttu-id="9e15d-108">Pour plus d’informations, consultez [détection de la prise en charge de WS-Management protocole par un ordinateur distant](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="9e15d-108">For more information, see [Detecting Whether a Remote Computer Supports WS-Management Protocol](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e15d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e15d-109">Syntax</span></span>


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9e15d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e15d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e15d-111">*indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9e15d-111">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e15d-112">Pour envoyer la demande en mode authentifié, utilisez la constante Authentication à partir de l’énumération **WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="9e15d-112">To send the request in authenticated mode use authentication constant from the **WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="9e15d-113">Pour envoyer en mode non authentifié, utilisez **WSManFlagUseNoAuthentication**.</span><span class="sxs-lookup"><span data-stu-id="9e15d-113">To send in unauthenticated mode, use **WSManFlagUseNoAuthentication**.</span></span> <span data-ttu-id="9e15d-114">Pour plus d’informations, consultez [**constantes d’authentification**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9e15d-114">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e15d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e15d-115">Return value</span></span>

<span data-ttu-id="9e15d-116">Chaîne XML qui spécifie la version du protocole WS-Management, le fournisseur du système d’exploitation et, si la demande a été envoyée, la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e15d-116">An XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e15d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9e15d-117">Remarks</span></span>

<span data-ttu-id="9e15d-118">**Session. identifier** est basé sur l’opération [protocole WS-Management](ws-management-protocol.md) définie en tant que wsmanIdentity.</span><span class="sxs-lookup"><span data-stu-id="9e15d-118">**Session.Identify** is based on the [WS-Management Protocol](ws-management-protocol.md) operation defined as wsmanIdentity.</span></span> <span data-ttu-id="9e15d-119">Cela est spécifié dans le paquet SOAP comme suit :</span><span class="sxs-lookup"><span data-stu-id="9e15d-119">This is specified in the SOAP packet as follows:</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a><span data-ttu-id="9e15d-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="9e15d-120">Examples</span></span>

<span data-ttu-id="9e15d-121">L’exemple VBScript suivant envoie une demande d’identification non authentifiée à l’ordinateur distant nommé Remote dans le même domaine.</span><span class="sxs-lookup"><span data-stu-id="9e15d-121">The following VBScript example sends an unauthenticated Identify request to the remote computer named Remote in the same domain.</span></span>


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a><span data-ttu-id="9e15d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e15d-122">Requirements</span></span>



| <span data-ttu-id="9e15d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e15d-123">Requirement</span></span> | <span data-ttu-id="9e15d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e15d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e15d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e15d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9e15d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e15d-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9e15d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e15d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9e15d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e15d-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9e15d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e15d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e15d-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e15d-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e15d-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="9e15d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e15d-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e15d-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9e15d-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e15d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e15d-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9e15d-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9e15d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9e15d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e15d-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e15d-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e15d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e15d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e15d-138">**session**</span><span class="sxs-lookup"><span data-stu-id="9e15d-138">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="9e15d-139">**IWSManSession :: identifier**</span><span class="sxs-lookup"><span data-stu-id="9e15d-139">**IWSManSession::Identify**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[<span data-ttu-id="9e15d-140">Protocole Gestion des services web</span><span class="sxs-lookup"><span data-stu-id="9e15d-140">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

 





