---
description: Chiffre un paquet SSL (Single SSL (Secure Sockets Layer) Protocol).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: SslEncryptPacket, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542038"
---
# <a name="sslencryptpacket-function"></a><span data-ttu-id="76f0f-103">SslEncryptPacket fonction)</span><span class="sxs-lookup"><span data-stu-id="76f0f-103">SslEncryptPacket function</span></span>

<span data-ttu-id="76f0f-104">La fonction **SslEncryptPacket** chiffre un paquet SSL (Single [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="76f0f-104">The **SslEncryptPacket** function encrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f0f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76f0f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="76f0f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76f0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f0f-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="76f0f-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="76f0f-109">*HKEY* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-110">Handle de la clé utilisée pour chiffrer le paquet.</span><span class="sxs-lookup"><span data-stu-id="76f0f-110">The handle to the key that is used to encrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="76f0f-111">*pbInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-112">Pointeur vers la mémoire tampon qui contient le paquet à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="76f0f-112">A pointer to the buffer that contains the packet to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="76f0f-113">*cbInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-114">Longueur, en octets, de la mémoire tampon *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="76f0f-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="76f0f-115">*pbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-116">Pointeur vers une mémoire tampon destinée à recevoir le paquet chiffré.</span><span class="sxs-lookup"><span data-stu-id="76f0f-116">A pointer to a buffer to receive the encrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="76f0f-117">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-118">Longueur, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="76f0f-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="76f0f-119">*pcbResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-120">Nombre d’octets écrits dans la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="76f0f-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="76f0f-121"> N \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-122">Numéro de séquence qui correspond à ce paquet.</span><span class="sxs-lookup"><span data-stu-id="76f0f-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="76f0f-123">*dwContentType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-123">*dwContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-124">Type de contenu qui correspond à ce paquet, qui spécifie le protocole de niveau supérieur utilisé pour traiter le paquet délimité.</span><span class="sxs-lookup"><span data-stu-id="76f0f-124">The content type that corresponds to this packet, which specifies the higher level protocol used to process the enclosed packet.</span></span>



| <span data-ttu-id="76f0f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="76f0f-125">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="76f0f-126">Signification</span><span class="sxs-lookup"><span data-stu-id="76f0f-126">Meaning</span></span>                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <span data-ttu-id="76f0f-127"><dt>**CT \_ MODIFIER \_ la \_ spécification de chiffrement**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="76f0f-127"><dt>**CT\_CHANGE\_CIPHER\_SPEC**</dt> <dt>20</dt></span></span> </dl> | <span data-ttu-id="76f0f-128">Indique une modification de la stratégie de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="76f0f-128">Indicates a change in the ciphering strategy.</span></span><br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <span data-ttu-id="76f0f-129"><dt>**CT \_ ALERTE**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="76f0f-129"><dt>**CT\_ALERT**</dt> <dt>21</dt></span></span> </dl>                                          | <span data-ttu-id="76f0f-130">Indique que le paquet délimité contient une alerte.</span><span class="sxs-lookup"><span data-stu-id="76f0f-130">Indicates that the enclosed packet contains an alert.</span></span><br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <span data-ttu-id="76f0f-131"><dt>**CT \_ NÉGOCIATION**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="76f0f-131"><dt>**CT\_HANDSHAKE**</dt> <dt>22</dt></span></span> </dl>                              | <span data-ttu-id="76f0f-132">Indique que le paquet délimité fait partie du protocole de négociation.</span><span class="sxs-lookup"><span data-stu-id="76f0f-132">Indicates that the enclosed packet is part of the handshake protocol.</span></span><br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <span data-ttu-id="76f0f-133"><dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="76f0f-133"><dt>**CT\_APPLICATIONDATA**</dt> <dt>23</dt></span></span> </dl>            | <span data-ttu-id="76f0f-134">Indique que le paquet contient des données d’application.</span><span class="sxs-lookup"><span data-stu-id="76f0f-134">Indicates that the packet contains application data.</span></span><br/>                  |



 

</dd> <dt>

<span data-ttu-id="76f0f-135">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-135">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f0f-136">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="76f0f-136">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76f0f-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76f0f-137">Return value</span></span>

<span data-ttu-id="76f0f-138">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="76f0f-138">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="76f0f-139">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="76f0f-139">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="76f0f-140">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="76f0f-140">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="76f0f-141">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="76f0f-141">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="76f0f-142">Description</span><span class="sxs-lookup"><span data-stu-id="76f0f-142">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="76f0f-143"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="76f0f-143"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="76f0f-144">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="76f0f-144">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="76f0f-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76f0f-145">Requirements</span></span>



| <span data-ttu-id="76f0f-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76f0f-146">Requirement</span></span> | <span data-ttu-id="76f0f-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="76f0f-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76f0f-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76f0f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="76f0f-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-149">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="76f0f-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76f0f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="76f0f-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76f0f-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="76f0f-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="76f0f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="76f0f-153"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f0f-153"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="76f0f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="76f0f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76f0f-155"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76f0f-155"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

