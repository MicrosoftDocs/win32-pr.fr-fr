---
description: Calcule le bloc de clé utilisé par le protocole EAP (Extensible Authentication Protocol).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: SslComputeEapKeyBlock, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527423"
---
# <a name="sslcomputeeapkeyblock-function"></a><span data-ttu-id="cdd3a-103">SslComputeEapKeyBlock fonction)</span><span class="sxs-lookup"><span data-stu-id="cdd3a-103">SslComputeEapKeyBlock function</span></span>

<span data-ttu-id="cdd3a-104">La fonction **SslComputeEapKeyBlock** calcule le bloc de clé utilisé par le protocole EAP (Extensible Authentication Protocol).</span><span class="sxs-lookup"><span data-stu-id="cdd3a-104">The **SslComputeEapKeyBlock** function computes the key block used by the Extensible Authentication Protocol (EAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd3a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdd3a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cdd3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdd3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd3a-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd3a-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="cdd3a-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="cdd3a-109">*hMasterKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd3a-110">Handle de l’objet de [*clé principale*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="cdd3a-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="cdd3a-111">*pbRandoms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-111">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd3a-112">Pointeur vers une mémoire tampon qui contient une concaténation des valeurs aléatoires \_ aléatoires du client et du serveur \_ de la session SSL.</span><span class="sxs-lookup"><span data-stu-id="cdd3a-112">A pointer to a buffer that contains a concatenation of the client\_random and server\_random values of the SSL session.</span></span>

</dd> <dt>

<span data-ttu-id="cdd3a-113">*cbRandoms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-113">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd3a-114">Longueur, en octets, de la mémoire tampon *pbRandoms* .</span><span class="sxs-lookup"><span data-stu-id="cdd3a-114">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cdd3a-115">*pbOutput* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-115">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd3a-116">Adresse d’une mémoire tampon qui reçoit l’objet BLOB de clé.</span><span class="sxs-lookup"><span data-stu-id="cdd3a-116">The address of a buffer that receives the key BLOB.</span></span> <span data-ttu-id="cdd3a-117">Le paramètre *cbOutput* contient la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cdd3a-117">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="cdd3a-118">Si ce paramètre a la **valeur null**, cette fonction place la taille requise, en octets, dans la **valeur DWORD** pointée par le paramètre *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="cdd3a-118">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cdd3a-119">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-119">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd3a-120">Longueur, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="cdd3a-120">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cdd3a-121">*pcbResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-121">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd3a-122">Pointeur vers une valeur **DWORD** qui spécifie la longueur, en octets, du hachage écrit dans la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="cdd3a-122">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cdd3a-123">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd3a-124">Définissez sur **\_ indicateur de \_ serveur \_ NCRYPT** pour indiquer qu’il s’agit d’un appel de serveur.</span><span class="sxs-lookup"><span data-stu-id="cdd3a-124">Set to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd3a-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdd3a-125">Return value</span></span>

<span data-ttu-id="cdd3a-126">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="cdd3a-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="cdd3a-127">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="cdd3a-127">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="cdd3a-128">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cdd3a-128">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="cdd3a-129">Description</span><span class="sxs-lookup"><span data-stu-id="cdd3a-129">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="cdd3a-130"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cdd3a-130"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="cdd3a-131">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cdd3a-131">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cdd3a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdd3a-132">Requirements</span></span>



| <span data-ttu-id="cdd3a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdd3a-133">Requirement</span></span> | <span data-ttu-id="cdd3a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdd3a-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd3a-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdd3a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd3a-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-136">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cdd3a-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdd3a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd3a-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdd3a-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cdd3a-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdd3a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdd3a-140"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdd3a-140"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="cdd3a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cdd3a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdd3a-142"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdd3a-142"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

