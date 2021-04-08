---
title: Méthode INapServerInfo GetNapServerInfo (NapServerManagement. h)
description: Récupère des informations sur le serveur NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Méthode GetNapServerInfo NAP
- Méthode GetNapServerInfo NAP, interface INapServerInfo
- INapServerInfo interface NAP, méthode GetNapServerInfo
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743885"
---
# <a name="inapserverinfogetnapserverinfo-method"></a><span data-ttu-id="71fb3-106">INapServerInfo :: GetNapServerInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="71fb3-106">INapServerInfo::GetNapServerInfo method</span></span>

> [!Note]  
> <span data-ttu-id="71fb3-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="71fb3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="71fb3-108">La méthode **INapServerInfo :: GetNapServerInfo** récupère des informations sur le serveur NAP.</span><span class="sxs-lookup"><span data-stu-id="71fb3-108">The **INapServerInfo::GetNapServerInfo** method retrieves information about the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="71fb3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71fb3-109">Syntax</span></span>


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="71fb3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71fb3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71fb3-111">*nom du serveur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="71fb3-111">*serverName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71fb3-112">Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="71fb3-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server name.</span></span>

</dd> <dt>

<span data-ttu-id="71fb3-113">*serverDescription* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="71fb3-113">*serverDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71fb3-114">Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la description du serveur.</span><span class="sxs-lookup"><span data-stu-id="71fb3-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server description.</span></span>

</dd> <dt>

<span data-ttu-id="71fb3-115">*protocolVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="71fb3-115">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71fb3-116">Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la version du protocole.</span><span class="sxs-lookup"><span data-stu-id="71fb3-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71fb3-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71fb3-117">Return value</span></span>

<span data-ttu-id="71fb3-118">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="71fb3-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="71fb3-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="71fb3-119">Return code</span></span>                                                                                     | <span data-ttu-id="71fb3-120">Description</span><span class="sxs-lookup"><span data-stu-id="71fb3-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="71fb3-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71fb3-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="71fb3-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="71fb3-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71fb3-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="71fb3-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="71fb3-124">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="71fb3-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="71fb3-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="71fb3-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="71fb3-126">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="71fb3-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="71fb3-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71fb3-127">Requirements</span></span>



| <span data-ttu-id="71fb3-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71fb3-128">Requirement</span></span> | <span data-ttu-id="71fb3-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="71fb3-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71fb3-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71fb3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="71fb3-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="71fb3-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="71fb3-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71fb3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="71fb3-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71fb3-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="71fb3-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="71fb3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="71fb3-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="71fb3-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="71fb3-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="71fb3-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71fb3-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71fb3-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="71fb3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="71fb3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71fb3-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71fb3-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="71fb3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71fb3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71fb3-141">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="71fb3-141">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> <dt>

[<span data-ttu-id="71fb3-142">**CountedString**</span><span class="sxs-lookup"><span data-stu-id="71fb3-142">**CountedString**</span></span>](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





