---
title: EapHostPeerNapInfo, structure (Eaphostpeerapis. h)
description: Contient les informations de protection d’accès réseau (NAP) sur un demandeur EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- EapHostPeerNapInfo, structure EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033176"
---
# <a name="eaphostpeernapinfo-structure"></a><span data-ttu-id="abe8c-104">EapHostPeerNapInfo, structure</span><span class="sxs-lookup"><span data-stu-id="abe8c-104">EapHostPeerNapInfo structure</span></span>

<span data-ttu-id="abe8c-105">La structure **EapHostPeerNapInfo** contient les informations de protection d’accès réseau (NAP) sur un demandeur EAP.</span><span class="sxs-lookup"><span data-stu-id="abe8c-105">The **EapHostPeerNapInfo** structure contains the Network Access Protection (NAP) information on an EAP supplicant.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe8c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abe8c-106">Syntax</span></span>


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a><span data-ttu-id="abe8c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="abe8c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="abe8c-108">**isolationState**</span><span class="sxs-lookup"><span data-stu-id="abe8c-108">**isolationState**</span></span>
</dt> <dd>

<span data-ttu-id="abe8c-109">Structure [**d' \_ État d’isolement**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) qui spécifie l’état d’isolement NAP d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="abe8c-109">An [**ISOLATION\_STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) structure that specifies the NAP isolation state of a computer.</span></span> <span data-ttu-id="abe8c-110">L’état d’isolement détermine le niveau d’accès réseau accordé.</span><span class="sxs-lookup"><span data-stu-id="abe8c-110">The isolation state determines the level of network access granted.</span></span>

</dd> <dt>

<span data-ttu-id="abe8c-111">**probationTime**</span><span class="sxs-lookup"><span data-stu-id="abe8c-111">**probationTime**</span></span>
</dt> <dd>

<span data-ttu-id="abe8c-112">Structure **ProbationTime** qui spécifie le temps nécessaire à la connexion pour sortir de la mise en quarantaine après laquelle la connexion sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="abe8c-112">A **ProbationTime** structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped.</span></span> <span data-ttu-id="abe8c-113">Une structure **ProbationTime** est identique à une structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="abe8c-113">A **ProbationTime** structure is identical to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> <dt>

<span data-ttu-id="abe8c-114">**stringCorrelationIdLength**</span><span class="sxs-lookup"><span data-stu-id="abe8c-114">**stringCorrelationIdLength**</span></span>
</dt> <dd>

<span data-ttu-id="abe8c-115">Longueur, en octets, du [STRINGCORRELATIONID](/windows/desktop/NAP/nap-datatypes) NAP qui suit cette structure.</span><span class="sxs-lookup"><span data-stu-id="abe8c-115">The length, in bytes, of the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) that follows this structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abe8c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="abe8c-116">Remarks</span></span>

<span data-ttu-id="abe8c-117">La structure **EapHostPeerNapInfo** précède le [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) NAP du type de données **WCHAR** dans le flux d’octets RPC.</span><span class="sxs-lookup"><span data-stu-id="abe8c-117">The **EapHostPeerNapInfo** structure precedes the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) of data type **WCHAR** in the RPC byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe8c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abe8c-118">Requirements</span></span>



| <span data-ttu-id="abe8c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abe8c-119">Requirement</span></span> | <span data-ttu-id="abe8c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="abe8c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe8c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abe8c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="abe8c-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abe8c-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="abe8c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abe8c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="abe8c-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abe8c-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="abe8c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="abe8c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="abe8c-126"><dt>Eaphostpeerapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe8c-126"><dt>Eaphostpeerapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe8c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abe8c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe8c-128">Structures du demandeur EAPHost</span><span class="sxs-lookup"><span data-stu-id="abe8c-128">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="abe8c-129">**EapHostPeerGetAuthStatus**</span><span class="sxs-lookup"><span data-stu-id="abe8c-129">**EapHostPeerGetAuthStatus**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[<span data-ttu-id="abe8c-130">**EapHostPeerMethodAuthParams**</span><span class="sxs-lookup"><span data-stu-id="abe8c-130">**EapHostPeerMethodAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

