---
description: Déchiffre un paquet SSL (Single SSL (Secure Sockets Layer) Protocol).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: SslDecryptPacket, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951677"
---
# <a name="ssldecryptpacket-function"></a><span data-ttu-id="6d5ff-103">SslDecryptPacket fonction)</span><span class="sxs-lookup"><span data-stu-id="6d5ff-103">SslDecryptPacket function</span></span>

<span data-ttu-id="6d5ff-104">la fonction **SslDecryptPacket** déchiffre un paquet SSL (Single [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="6d5ff-104">the **SslDecryptPacket** function decrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d5ff-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6d5ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d5ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d5ff-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="6d5ff-109">*HKEY* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-110">Handle de la clé utilisée pour déchiffrer le paquet.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-110">The handle to the key that is used to decrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="6d5ff-111">*pbInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-112">Pointeur vers la mémoire tampon qui contient le paquet à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-112">A pointer to the buffer that contains the packet to be decrypted.</span></span>

</dd> <dt>

<span data-ttu-id="6d5ff-113">*cbInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-114">Longueur, en octets, de la mémoire tampon *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="6d5ff-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6d5ff-115">*pbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-116">Pointeur vers une mémoire tampon destinée à contenir le paquet déchiffré.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-116">A pointer to a buffer to contain the decrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="6d5ff-117">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-118">Longueur, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="6d5ff-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6d5ff-119">*pcbResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-120">Nombre d’octets écrits dans la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="6d5ff-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6d5ff-121"> N \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-122">Numéro de séquence qui correspond à ce paquet.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="6d5ff-123">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ff-124">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-124">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d5ff-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d5ff-125">Return value</span></span>

<span data-ttu-id="6d5ff-126">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="6d5ff-127">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-127">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="6d5ff-128">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-128">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6d5ff-129">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6d5ff-129">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="6d5ff-130">Description</span><span class="sxs-lookup"><span data-stu-id="6d5ff-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="6d5ff-131"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d5ff-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="6d5ff-132">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-132">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d5ff-133">Notes</span><span class="sxs-lookup"><span data-stu-id="6d5ff-133">Remarks</span></span>

<span data-ttu-id="6d5ff-134">La longueur du paquet peut être égale à zéro, par exemple lors du déchiffrement d’un message « HelloRequest ».</span><span class="sxs-lookup"><span data-stu-id="6d5ff-134">The length of the packet can be zero, such as when a "HelloRequest" message is decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d5ff-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d5ff-135">Requirements</span></span>



| <span data-ttu-id="6d5ff-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d5ff-136">Requirement</span></span> | <span data-ttu-id="6d5ff-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d5ff-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d5ff-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d5ff-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6d5ff-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6d5ff-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d5ff-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6d5ff-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d5ff-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d5ff-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d5ff-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d5ff-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6d5ff-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6d5ff-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d5ff-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d5ff-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

