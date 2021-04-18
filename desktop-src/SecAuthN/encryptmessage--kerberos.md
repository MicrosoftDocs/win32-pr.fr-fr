---
description: Chiffre un message pour fournir la confidentialité à l’aide de Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: EncryptMessage (Kerberos) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210032"
---
# <a name="encryptmessage-kerberos-function"></a><span data-ttu-id="b5611-103">EncryptMessage (Kerberos) (fonction)</span><span class="sxs-lookup"><span data-stu-id="b5611-103">EncryptMessage (Kerberos) function</span></span>

<span data-ttu-id="b5611-104">La fonction **EncryptMessage (Kerberos)** chiffre un message pour fournir la [*confidentialité*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b5611-104">The **EncryptMessage (Kerberos)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="b5611-105">**EncryptMessage (Kerberos)** permet à une application de choisir parmi les [*algorithmes de chiffrement*](../secgloss/c-gly.md) pris en charge par le mécanisme choisi.</span><span class="sxs-lookup"><span data-stu-id="b5611-105">**EncryptMessage (Kerberos)** allows an application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="b5611-106">La fonction **EncryptMessage (Kerberos)** utilise le [*contexte de sécurité*](../secgloss/s-gly.md) référencé par le handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="b5611-106">The **EncryptMessage (Kerberos)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="b5611-107">Certains packages n’ont pas de messages à chiffrer ou à déchiffrer, mais fournissent plutôt un [*hachage*](../secgloss/h-gly.md) d’intégrité qui peut être vérifié.</span><span class="sxs-lookup"><span data-stu-id="b5611-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

> [!Note]  
> <span data-ttu-id="b5611-108">**EncryptMessage (Kerberos)** et [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre.</span><span class="sxs-lookup"><span data-stu-id="b5611-108">**EncryptMessage (Kerberos)** and [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="b5611-109">Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.</span><span class="sxs-lookup"><span data-stu-id="b5611-109">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5611-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5611-110">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a><span data-ttu-id="b5611-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5611-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5611-112">*phContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5611-112">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5611-113">Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour chiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="b5611-113">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="b5611-114">*fQOP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5611-114">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5611-115">Indicateurs spécifiques au package qui indiquent la qualité de la protection.</span><span class="sxs-lookup"><span data-stu-id="b5611-115">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="b5611-116">Un [*package de sécurité*](../secgloss/s-gly.md) peut utiliser ce paramètre pour activer la sélection d' [*algorithmes de chiffrement*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b5611-116">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="b5611-117">Ce paramètre peut être l’indicateur suivant.</span><span class="sxs-lookup"><span data-stu-id="b5611-117">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="b5611-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5611-118">Value</span></span></th><th><span data-ttu-id="b5611-119">Signification</span><span class="sxs-lookup"><span data-stu-id="b5611-119">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="b5611-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b5611-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="b5611-121">Générez un en-tête ou un code de fin, mais ne chiffrez pas le message.</span><span class="sxs-lookup"><span data-stu-id="b5611-121">Produce a header or trailer but do not encrypt the message.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="b5611-122">KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</span><span class="sxs-lookup"><span data-stu-id="b5611-122">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

</dd> <dt>

<span data-ttu-id="b5611-123">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b5611-123">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5611-124">Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="b5611-124">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="b5611-125">En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui peuvent être de type SecBuffer \_ .</span><span class="sxs-lookup"><span data-stu-id="b5611-125">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="b5611-126">Cette mémoire tampon contient le message à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="b5611-126">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="b5611-127">Le message est chiffré sur place, remplaçant le contenu d’origine de la structure.</span><span class="sxs-lookup"><span data-stu-id="b5611-127">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="b5611-128">La fonction ne traite pas les tampons avec l' \_ attribut SECBUFFER ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="b5611-128">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="b5611-129">La longueur de la structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui contient le message ne doit pas être supérieure à **cbMaximumMessage**, qui est obtenue à partir de la fonction [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ attr \_ Stream \_ sizes).</span><span class="sxs-lookup"><span data-stu-id="b5611-129">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="b5611-130">Les applications qui n’utilisent pas SSL doivent fournir un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de type SecBuffer \_ Padding.</span><span class="sxs-lookup"><span data-stu-id="b5611-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="b5611-131">*MessageSeqNo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5611-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5611-132">Numéro de séquence que l’application de transport a affecté au message.</span><span class="sxs-lookup"><span data-stu-id="b5611-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="b5611-133">Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b5611-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5611-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5611-134">Return value</span></span>

<span data-ttu-id="b5611-135">Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5611-135">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="b5611-136">Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="b5611-136">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="b5611-137">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b5611-137">Return code</span></span>                                                                                                    | <span data-ttu-id="b5611-138">Description</span><span class="sxs-lookup"><span data-stu-id="b5611-138">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5611-139"><dt>**\_tampon s \_ E \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="b5611-139"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="b5611-140">La mémoire tampon de sortie est trop petite.</span><span class="sxs-lookup"><span data-stu-id="b5611-140">The output buffer is too small.</span></span> <span data-ttu-id="b5611-141">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b5611-141">For more information, see Remarks.</span></span>                                                                                                                                                                 |
| <dl> <span data-ttu-id="b5611-142"><dt>**\_contexte E/s \_ \_ expiré**</dt></span><span class="sxs-lookup"><span data-stu-id="b5611-142"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="b5611-143">L’application fait référence à un contexte qui a déjà été fermé.</span><span class="sxs-lookup"><span data-stu-id="b5611-143">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="b5611-144">Une application correctement écrite ne doit pas recevoir cette erreur.</span><span class="sxs-lookup"><span data-stu-id="b5611-144">A properly written application should not receive this error.</span></span>                                                                                               |
| <dl> <span data-ttu-id="b5611-145"><dt>**SEC \_ E \_ système de chiffrement \_ \_ non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="b5611-145"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="b5611-146">Le [*chiffrement*](../secgloss/c-gly.md) choisi pour le [*contexte de sécurité*](../secgloss/s-gly.md) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b5611-146">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span>                                                                                                         |
| <dl> <span data-ttu-id="b5611-147"><dt>**s \_ E \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5611-147"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="b5611-148">La mémoire disponible est insuffisante pour terminer l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="b5611-148">There is not enough memory available to complete the requested action.</span></span>                                                                                                                                                             |
| <dl> <span data-ttu-id="b5611-149"><dt>**SEC \_ E \_ handle non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5611-149"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="b5611-150">Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* .</span><span class="sxs-lookup"><span data-stu-id="b5611-150">A context handle that is not valid was specified in the *phContext* parameter.</span></span>                                                                                                                                                     |
| <dl> <span data-ttu-id="b5611-151"><dt>**s \_ E \_ jeton non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5611-151"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="b5611-152">Aucune \_ mémoire tampon de type de données SECBUFFER n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="b5611-152">No SECBUFFER\_DATA type buffer was found.</span></span>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b5611-153"><dt>**SEC \_ E \_ QoP \_ non \_ pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="b5611-153"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="b5611-154">La confidentialité et l' [*intégrité*](../secgloss/i-gly.md) ne sont pas prises en charge par le [*contexte de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b5611-154">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="b5611-155">Notes</span><span class="sxs-lookup"><span data-stu-id="b5611-155">Remarks</span></span>

<span data-ttu-id="b5611-156">La fonction **EncryptMessage (Kerberos)** chiffre un message basé sur le message et la [*clé de session*](../secgloss/s-gly.md) à partir d’un contexte de [*sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b5611-156">The **EncryptMessage (Kerberos)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="b5611-157">Si l’application de transport a créé le [*contexte de sécurité*](../secgloss/s-gly.md) pour prendre en charge la détection de séquence et que l’appelant fournit un numéro de séquence, la fonction inclut ces informations avec le message chiffré.</span><span class="sxs-lookup"><span data-stu-id="b5611-157">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="b5611-158">L’inclusion de ces informations protège la relecture, l’insertion et la suppression des messages.</span><span class="sxs-lookup"><span data-stu-id="b5611-158">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="b5611-159">Le [*package de sécurité*](../secgloss/s-gly.md) intègre le numéro de séquence passé à partir de l’application de transport.</span><span class="sxs-lookup"><span data-stu-id="b5611-159">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

> [!Note]  
> <span data-ttu-id="b5611-160">Ces mémoires tampons doivent être fournies dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="b5611-160">These buffers must be supplied in the order shown.</span></span>

| <span data-ttu-id="b5611-161">Type de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="b5611-161">Buffer type</span></span>                           | <span data-ttu-id="b5611-162">Description</span><span class="sxs-lookup"><span data-stu-id="b5611-162">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5611-163">\_ \_< en-tête de flux SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="b5611-163">SECBUFFER\_STREAM\_HEADER<</span></span>  | <span data-ttu-id="b5611-164">Utilisé en interne.</span><span class="sxs-lookup"><span data-stu-id="b5611-164">Used internally.</span></span> <span data-ttu-id="b5611-165">Aucune initialisation n’est requise.</span><span class="sxs-lookup"><span data-stu-id="b5611-165">No initialization required.</span></span>                                                                       |
| <span data-ttu-id="b5611-166">\_données SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="b5611-166">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="b5611-167">Contient le message de [*texte en clair*](../secgloss/s-gly.md) à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="b5611-167">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span> |
| <span data-ttu-id="b5611-168">Code de fin de \_ flux SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="b5611-168">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="b5611-169">Utilisé en interne.</span><span class="sxs-lookup"><span data-stu-id="b5611-169">Used internally.</span></span> <span data-ttu-id="b5611-170">Aucune initialisation n’est requise.</span><span class="sxs-lookup"><span data-stu-id="b5611-170">No initialization required.</span></span>                                                                        |
| <span data-ttu-id="b5611-171">SECBUFFER \_ vide</span><span class="sxs-lookup"><span data-stu-id="b5611-171">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="b5611-172">Utilisé en interne.</span><span class="sxs-lookup"><span data-stu-id="b5611-172">Used internally.</span></span> <span data-ttu-id="b5611-173">Aucune initialisation n’est requise.</span><span class="sxs-lookup"><span data-stu-id="b5611-173">No initialization required.</span></span> <span data-ttu-id="b5611-174">La taille peut être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="b5611-174">Size can be zero.</span></span>                                                      |

<span data-ttu-id="b5611-175">Pour des performances optimales, les structures *pMessage* doivent être allouées à partir de la mémoire contiguë.</span><span class="sxs-lookup"><span data-stu-id="b5611-175">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="b5611-176">**Windows XP :** Cette fonction était également connue sous le nom de **SealMessage**.</span><span class="sxs-lookup"><span data-stu-id="b5611-176">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="b5611-177">Les applications doivent désormais utiliser **EncryptMessage (Kerberos)** uniquement.</span><span class="sxs-lookup"><span data-stu-id="b5611-177">Applications should now use **EncryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5611-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5611-178">Requirements</span></span>

| <span data-ttu-id="b5611-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5611-179">Requirement</span></span> | <span data-ttu-id="b5611-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5611-180">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="b5611-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5611-181">Minimum supported client</span></span> | <span data-ttu-id="b5611-182">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5611-182">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="b5611-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5611-183">Minimum supported server</span></span> | <span data-ttu-id="b5611-184">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5611-184">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="b5611-185">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5611-185">Header</span></span>                   | <span data-ttu-id="b5611-186">SSPI. h (include Security. h)</span><span class="sxs-lookup"><span data-stu-id="b5611-186">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="b5611-187">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5611-187">Library</span></span>                  | <span data-ttu-id="b5611-188">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="b5611-188">Secur32.lib</span></span>                               |
| <span data-ttu-id="b5611-189">DLL</span><span class="sxs-lookup"><span data-stu-id="b5611-189">DLL</span></span>                      | <span data-ttu-id="b5611-190">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="b5611-190">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="b5611-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5611-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5611-192">Fonctions SSPI</span><span class="sxs-lookup"><span data-stu-id="b5611-192">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="b5611-193">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b5611-193">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b5611-194">**DecryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b5611-194">**DecryptMessage (Kerberos)**</span></span>](decryptmessage--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b5611-195">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b5611-195">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b5611-196">**QueryContextAttributes (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b5611-196">**QueryContextAttributes (Kerberos)**</span></span>](querycontextattributes--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b5611-197">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="b5611-197">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="b5611-198">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="b5611-198">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
