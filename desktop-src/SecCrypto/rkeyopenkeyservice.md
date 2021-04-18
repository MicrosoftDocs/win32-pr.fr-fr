---
description: La fonction RKeyOpenKeyService n’est pas prise en charge.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: RKeyOpenKeyService, fonction (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529190"
---
# <a name="rkeyopenkeyservice-function"></a><span data-ttu-id="97d74-103">RKeyOpenKeyService fonction)</span><span class="sxs-lookup"><span data-stu-id="97d74-103">RKeyOpenKeyService function</span></span>

<span data-ttu-id="97d74-104">La fonction **RKeyOpenKeyService** n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="97d74-104">The **RKeyOpenKeyService** function is not supported.</span></span>

<span data-ttu-id="97d74-105">**Windows Server 2003 :** La fonction **RKeyOpenKeyService** établit une connexion à un ordinateur distant et ouvre un handle de service de clé.</span><span class="sxs-lookup"><span data-stu-id="97d74-105">**Windows Server 2003:** The **RKeyOpenKeyService** function establishes a connection to a remote computer and opens a key service handle.</span></span> <span data-ttu-id="97d74-106">Le descripteur de service de clé peut ensuite être utilisé par la fonction [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="97d74-106">The key service handle can subsequently be used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span> <span data-ttu-id="97d74-107">Notez que ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="97d74-107">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="97d74-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97d74-108">Syntax</span></span>


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a><span data-ttu-id="97d74-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97d74-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d74-110">*pszMachineName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97d74-110">*pszMachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d74-111">Pointeur long vers une chaîne terminée par le caractère null qui représente l’ordinateur sur lequel le handle de service de clé doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="97d74-111">Long pointer to a null-terminated string that represents the computer where the key service handle will be opened.</span></span>

</dd> <dt>

<span data-ttu-id="97d74-112">*OwnerType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97d74-112">*OwnerType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d74-113">[**KEYSVC \_**](keysvc-type.md) Valeur de type qui représente le type de clé.</span><span class="sxs-lookup"><span data-stu-id="97d74-113">[**KEYSVC\_TYPE**](keysvc-type.md) value that represents the key type.</span></span> <span data-ttu-id="97d74-114">La seule valeur prise en charge est **KeySvcMachine**.</span><span class="sxs-lookup"><span data-stu-id="97d74-114">The only supported value is **KeySvcMachine**.</span></span>

</dd> <dt>

<span data-ttu-id="97d74-115">*pwszOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97d74-115">*pwszOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d74-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="97d74-116">Reserved.</span></span> <span data-ttu-id="97d74-117">Définissez cette valeur sur **null**.</span><span class="sxs-lookup"><span data-stu-id="97d74-117">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="97d74-118">*pAuthentication* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97d74-118">*pAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d74-119">Pointeur vers un **void** qui représente les paramètres d’authentification.</span><span class="sxs-lookup"><span data-stu-id="97d74-119">A pointer to a **void** that represents the authentication settings.</span></span> <span data-ttu-id="97d74-120">Ce pointeur peut pointer vers une valeur égale à zéro ou la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="97d74-120">This pointer can point to a value of zero or the following value.</span></span>



| <span data-ttu-id="97d74-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="97d74-121">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="97d74-122">Signification</span><span class="sxs-lookup"><span data-stu-id="97d74-122">Meaning</span></span>                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <span data-ttu-id="97d74-123"><dt>**RKEYSVC \_ CONNEXION \_ sécurisée \_ uniquement**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="97d74-123"><dt>**RKEYSVC\_CONNECT\_SECURE\_ONLY**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="97d74-124">Le client nécessite une authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="97d74-124">The client requires mutual authentication.</span></span> <span data-ttu-id="97d74-125">Si cette valeur est spécifiée, le recours à NTLM échouera.</span><span class="sxs-lookup"><span data-stu-id="97d74-125">If this value is specified, fallback to NTLM will fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="97d74-126">*conservé* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="97d74-126">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97d74-127">Réservé.</span><span class="sxs-lookup"><span data-stu-id="97d74-127">Reserved.</span></span> <span data-ttu-id="97d74-128">Définissez cette valeur sur **null**.</span><span class="sxs-lookup"><span data-stu-id="97d74-128">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="97d74-129">*phKeySvcCli* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="97d74-129">*phKeySvcCli* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97d74-130">Pointeur vers un [**\_ handle KEYSVCC**](keysvcc-handle.md) qui reçoit le handle de service de clé ouvert.</span><span class="sxs-lookup"><span data-stu-id="97d74-130">A pointer to a [**KEYSVCC\_HANDLE**](keysvcc-handle.md) that receives the opened key service handle.</span></span> <span data-ttu-id="97d74-131">Lorsque vous avez fini d’utiliser le descripteur, libérez la ressource en appelant la fonction [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="97d74-131">When you have finished using the handle, free the resource by calling the [**RKeyCloseKeyService**](rkeyclosekeyservice.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d74-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97d74-132">Return value</span></span>

<span data-ttu-id="97d74-133">Si la fonction réussit, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="97d74-133">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="97d74-134">Si la fonction échoue, la valeur de retour est un **ULong** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="97d74-134">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d74-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97d74-135">Requirements</span></span>



| <span data-ttu-id="97d74-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97d74-136">Requirement</span></span> | <span data-ttu-id="97d74-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="97d74-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97d74-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97d74-138">Minimum supported client</span></span><br/> | <span data-ttu-id="97d74-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="97d74-139">None supported</span></span><br/>                                                             |
| <span data-ttu-id="97d74-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97d74-140">Minimum supported server</span></span><br/> | <span data-ttu-id="97d74-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97d74-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97d74-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="97d74-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="97d74-143"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="97d74-143"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97d74-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97d74-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d74-145">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="97d74-145">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="97d74-146">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="97d74-146">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




