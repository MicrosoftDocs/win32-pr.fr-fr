---
description: Génère un ensemble de clés de session de protocole SSL (Secure Sockets Layer) (SSL).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: SslGenerateSessionKeys, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531227"
---
# <a name="sslgeneratesessionkeys-function"></a><span data-ttu-id="fbedc-103">SslGenerateSessionKeys fonction)</span><span class="sxs-lookup"><span data-stu-id="fbedc-103">SslGenerateSessionKeys function</span></span>

<span data-ttu-id="fbedc-104">La fonction **SslGenerateSessionKeys** génère un ensemble de clés de session de [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="fbedc-104">The **SslGenerateSessionKeys** function generates a set of [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) session keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbedc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbedc-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fbedc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbedc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbedc-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbedc-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbedc-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="fbedc-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="fbedc-109">*hMasterKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbedc-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbedc-110">Handle de l’objet de [*clé principale*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="fbedc-110">The handle to the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="fbedc-111">*phReadKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fbedc-111">*phReadKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbedc-112">Pointeur vers le handle de la clé de lecture retournée.</span><span class="sxs-lookup"><span data-stu-id="fbedc-112">A pointer to the returned read key handle.</span></span>

</dd> <dt>

<span data-ttu-id="fbedc-113">*phWriteKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fbedc-113">*phWriteKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbedc-114">Pointeur vers le handle de clé d’écriture retourné.</span><span class="sxs-lookup"><span data-stu-id="fbedc-114">A pointer to the returned write key handle.</span></span>

</dd> <dt>

<span data-ttu-id="fbedc-115">*pParameterList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbedc-115">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbedc-116">Pointeur vers un tableau de mémoires tampons [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) qui contiennent des informations utilisées dans le cadre de l’opération d’échange de clés.</span><span class="sxs-lookup"><span data-stu-id="fbedc-116">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="fbedc-117">L’ensemble précis de mémoires tampons dépend du protocole et de la suite de chiffrement utilisés.</span><span class="sxs-lookup"><span data-stu-id="fbedc-117">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="fbedc-118">Au minimum, la liste contient des mémoires tampons qui contiennent les valeurs aléatoires fournies par le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="fbedc-118">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="fbedc-119">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbedc-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbedc-120">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="fbedc-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbedc-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbedc-121">Return value</span></span>

<span data-ttu-id="fbedc-122">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="fbedc-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="fbedc-123">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="fbedc-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="fbedc-124">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="fbedc-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="fbedc-125">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fbedc-125">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="fbedc-126">Description</span><span class="sxs-lookup"><span data-stu-id="fbedc-126">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbedc-127"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="fbedc-127"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="fbedc-128">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="fbedc-128">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="fbedc-129"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fbedc-129"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="fbedc-130">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="fbedc-130">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="fbedc-131"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fbedc-131"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="fbedc-132">Le paramètre *phReadKey* ou *phWriteKey* a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="fbedc-132">The *phReadKey* or *phWriteKey* parameter is null.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="fbedc-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbedc-133">Requirements</span></span>



| <span data-ttu-id="fbedc-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbedc-134">Requirement</span></span> | <span data-ttu-id="fbedc-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbedc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbedc-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbedc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fbedc-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbedc-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fbedc-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbedc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fbedc-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbedc-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fbedc-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbedc-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbedc-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbedc-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="fbedc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fbedc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbedc-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbedc-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

