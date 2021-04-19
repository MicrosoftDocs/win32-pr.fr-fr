---
description: Contient des informations sur un fournisseur de services de chiffrement de carte à puce (CSP).
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: Structure KERB_SMARTCARD_CSP_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527521"
---
# <a name="kerb_smartcard_csp_info-structure"></a><span data-ttu-id="fe062-103">\_Structure d' \_ informations du CSP de carte à puce KERB \_</span><span class="sxs-lookup"><span data-stu-id="fe062-103">KERB\_SMARTCARD\_CSP\_INFO structure</span></span>

<span data-ttu-id="fe062-104">La structure des **\_ \_ \_ informations du CSP** de carte à puce KERB contient des informations sur un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) de carte à puce (CSP).</span><span class="sxs-lookup"><span data-stu-id="fe062-104">The **KERB\_SMARTCARD\_CSP\_INFO** structure contains information about a smart card [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="fe062-105">Cette structure n’est pas déclarée dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="fe062-105">This structure is not declared in a public header.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe062-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe062-106">Syntax</span></span>


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a><span data-ttu-id="fe062-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fe062-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe062-108">**dwCspInfoLen**</span><span class="sxs-lookup"><span data-stu-id="fe062-108">**dwCspInfoLen**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-109">Taille, en octets, de cette structure, y compris les données ajoutées.</span><span class="sxs-lookup"><span data-stu-id="fe062-109">The size, in bytes, of this structure, including any appended data.</span></span>

</dd> <dt>

<span data-ttu-id="fe062-110">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="fe062-110">**MessageType**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-111">Type de message passé.</span><span class="sxs-lookup"><span data-stu-id="fe062-111">The type of message being passed.</span></span> <span data-ttu-id="fe062-112">Ce membre doit avoir la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="fe062-112">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="fe062-113">**ContextInformation**</span><span class="sxs-lookup"><span data-stu-id="fe062-113">**ContextInformation**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fe062-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fe062-115">**SpaceHolderForWow64**</span><span class="sxs-lookup"><span data-stu-id="fe062-115">**SpaceHolderForWow64**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fe062-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fe062-117">**flags**</span><span class="sxs-lookup"><span data-stu-id="fe062-117">**flags**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fe062-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fe062-119">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="fe062-119">**KeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-120">Clé privée à utiliser à partir du conteneur de clé spécifié dans la mémoire tampon **bBuffer**.</span><span class="sxs-lookup"><span data-stu-id="fe062-120">The private key to use from the key container specified within the buffer **bBuffer**.</span></span> <span data-ttu-id="fe062-121">La clé peut être l’une des valeurs suivantes, définie dans WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="fe062-121">The key can be one of the following values, defined in WinCrypt.h.</span></span>



| <span data-ttu-id="fe062-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe062-122">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="fe062-123">Signification</span><span class="sxs-lookup"><span data-stu-id="fe062-123">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="fe062-124"><dt>**À \_ KeyExchange**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fe062-124"><dt>**AT\_KEYEXCHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="fe062-125">La clé est une clé d’échange de clé.</span><span class="sxs-lookup"><span data-stu-id="fe062-125">The key is a key-exchange key.</span></span><br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="fe062-126"><dt>**À \_ SIGNATURE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fe062-126"><dt>**AT\_SIGNATURE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="fe062-127">La clé est une clé de signature.</span><span class="sxs-lookup"><span data-stu-id="fe062-127">The key is a signature key.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="fe062-128">**nCardNameOffset**</span><span class="sxs-lookup"><span data-stu-id="fe062-128">**nCardNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-129">Nombre de caractères dans la mémoire tampon **bBuffer** qui précèdent le nom de la carte à puce dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fe062-129">The number of characters in the **bBuffer** buffer that precede the name of the smart card in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe062-130">Si le nom de la carte à puce n’est pas fourni, la mémoire tampon doit contenir une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="fe062-130">If the name of the smart card is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="fe062-131">**nReaderNameOffset**</span><span class="sxs-lookup"><span data-stu-id="fe062-131">**nReaderNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-132">Nombre de caractères dans la mémoire tampon **bBuffer** qui précèdent le nom du lecteur de carte à puce dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fe062-132">The number of characters in the **bBuffer** buffer that precede the name of the smart card reader in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe062-133">Si le nom du lecteur de carte à puce n’est pas fourni, la mémoire tampon doit contenir une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="fe062-133">If the name of the smart card reader is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="fe062-134">**nContainerNameOffset**</span><span class="sxs-lookup"><span data-stu-id="fe062-134">**nContainerNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-135">Nombre de caractères dans la mémoire tampon **bBuffer** qui précèdent le nom du conteneur de clé dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fe062-135">The number of characters in the **bBuffer** buffer that precede the name of the key container in that buffer.</span></span> <span data-ttu-id="fe062-136">Cette chaîne ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="fe062-136">This string cannot be empty.</span></span>

</dd> <dt>

<span data-ttu-id="fe062-137">**nCSPNameOffset**</span><span class="sxs-lookup"><span data-stu-id="fe062-137">**nCSPNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-138">Nombre de caractères dans la mémoire tampon **bBuffer** qui précèdent le nom du fournisseur de services de chiffrement dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fe062-138">The number of characters in the **bBuffer** buffer that precede the name of the CSP in that buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fe062-139">**bBuffer**</span><span class="sxs-lookup"><span data-stu-id="fe062-139">**bBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="fe062-140">Tableau de caractères initialisé à une longueur de `sizeof(DWORD)` .</span><span class="sxs-lookup"><span data-stu-id="fe062-140">An array of characters initialized to a length of `sizeof(DWORD)`.</span></span> <span data-ttu-id="fe062-141">Cette mémoire tampon contient les noms référencés par les membres **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** et **nCSPNameOffset** , ainsi que toutes les données supplémentaires fournies par le fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fe062-141">This buffer contains the names referred to by the **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset**, and **nCSPNameOffset** members, as well as any additional data provided by the CSP.</span></span>

<span data-ttu-id="fe062-142">Les noms qui ne sont pas fournis doivent être représentés dans cette mémoire tampon par des chaînes vides.</span><span class="sxs-lookup"><span data-stu-id="fe062-142">Any names that are not provided must be represented in this buffer by empty strings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe062-143">Notes</span><span class="sxs-lookup"><span data-stu-id="fe062-143">Remarks</span></span>

<span data-ttu-id="fe062-144">Lorsque cette structure est sérialisée, les membres de la structure doivent être alignés sur les limites qui sont des multiples de 2 octets.</span><span class="sxs-lookup"><span data-stu-id="fe062-144">When this structure is serialized, the structure members must be aligned to boundaries that are multiples of 2 bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe062-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe062-145">Requirements</span></span>



| <span data-ttu-id="fe062-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe062-146">Requirement</span></span> | <span data-ttu-id="fe062-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe062-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe062-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe062-148">Minimum supported client</span></span><br/> | <span data-ttu-id="fe062-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe062-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fe062-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe062-150">Minimum supported server</span></span><br/> | <span data-ttu-id="fe062-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe062-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe062-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe062-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe062-153">**\_connexion au certificat KERB \_**</span><span class="sxs-lookup"><span data-stu-id="fe062-153">**KERB\_CERTIFICATE\_LOGON**</span></span>](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
