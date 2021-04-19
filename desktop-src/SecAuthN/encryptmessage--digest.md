---
description: Chiffre un message pour fournir la confidentialité à l’aide de Digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: EncryptMessage (Digest), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539053"
---
# <a name="encryptmessage-digest-function"></a><span data-ttu-id="dca7d-103">EncryptMessage (Digest) (fonction)</span><span class="sxs-lookup"><span data-stu-id="dca7d-103">EncryptMessage (Digest) function</span></span>

<span data-ttu-id="dca7d-104">La fonction **EncryptMessage (Digest)** chiffre un message pour fournir la [*confidentialité*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dca7d-104">The **EncryptMessage (Digest)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="dca7d-105">**EncryptMessage (Digest)** permet à l’application de choisir parmi les [*algorithmes de chiffrement*](../secgloss/c-gly.md) pris en charge par le mécanisme choisi.</span><span class="sxs-lookup"><span data-stu-id="dca7d-105">**EncryptMessage (Digest)** allows the application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="dca7d-106">La fonction **EncryptMessage (Digest)** utilise le [*contexte de sécurité*](../secgloss/s-gly.md) référencé par le handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="dca7d-106">The **EncryptMessage (Digest)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="dca7d-107">Certains packages n’ont pas de messages à chiffrer ou à déchiffrer, mais fournissent plutôt un [*hachage*](../secgloss/h-gly.md) d’intégrité qui peut être vérifié.</span><span class="sxs-lookup"><span data-stu-id="dca7d-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

<span data-ttu-id="dca7d-108">Cette fonction est uniquement disponible en tant que mécanisme SASL.</span><span class="sxs-lookup"><span data-stu-id="dca7d-108">This function is available as a SASL mechanism only.</span></span>

> [!Note]  
> <span data-ttu-id="dca7d-109">**EncryptMessage (Digest)** et [**DecryptMessage (Digest)**](decryptmessage--digest.md) peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre.</span><span class="sxs-lookup"><span data-stu-id="dca7d-109">**EncryptMessage (Digest)** and [**DecryptMessage (Digest)**](decryptmessage--digest.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="dca7d-110">Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.</span><span class="sxs-lookup"><span data-stu-id="dca7d-110">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dca7d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dca7d-111">Syntax</span></span>


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a><span data-ttu-id="dca7d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dca7d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dca7d-113">*phContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dca7d-113">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dca7d-114">Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour chiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="dca7d-114">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="dca7d-115">*fQOP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dca7d-115">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dca7d-116">Indicateurs spécifiques au package qui indiquent la qualité de la protection.</span><span class="sxs-lookup"><span data-stu-id="dca7d-116">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="dca7d-117">Un [*package de sécurité*](../secgloss/s-gly.md) peut utiliser ce paramètre pour activer la sélection d' [*algorithmes de chiffrement*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dca7d-117">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="dca7d-118">Lorsque vous utilisez le SSP Digest, ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="dca7d-118">When using the Digest SSP, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dca7d-119">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dca7d-119">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dca7d-120">Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="dca7d-120">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="dca7d-121">En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui peuvent être de type SecBuffer \_ .</span><span class="sxs-lookup"><span data-stu-id="dca7d-121">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="dca7d-122">Cette mémoire tampon contient le message à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="dca7d-122">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="dca7d-123">Le message est chiffré sur place, remplaçant le contenu d’origine de la structure.</span><span class="sxs-lookup"><span data-stu-id="dca7d-123">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="dca7d-124">La fonction ne traite pas les tampons avec l' \_ attribut SECBUFFER ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="dca7d-124">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="dca7d-125">La longueur de la structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui contient le message ne doit pas être supérieure à **cbMaximumMessage**, qui est obtenue à partir de la fonction [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG \_ attr \_ Stream \_ sizes).</span><span class="sxs-lookup"><span data-stu-id="dca7d-125">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="dca7d-126">Lorsque vous utilisez le SSP Digest, il doit exister une deuxième mémoire tampon de type SECBUFFER \_ padding ou \_ sec \_ Data buffer pour contenir les informations de [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) .</span><span class="sxs-lookup"><span data-stu-id="dca7d-126">When using the Digest SSP, there must be a second buffer of type SECBUFFER\_PADDING or SEC\_BUFFER\_DATA to hold [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) information.</span></span> <span data-ttu-id="dca7d-127">Pour connaître la taille de la mémoire tampon de sortie, appelez la fonction [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) et spécifiez des \_ tailles d’attr SECPKG \_ .</span><span class="sxs-lookup"><span data-stu-id="dca7d-127">To get the size of the output buffer, call the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specify SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="dca7d-128">La fonction retourne une structure [**de \_ tailles SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="dca7d-128">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="dca7d-129">La taille de la mémoire tampon de sortie est la somme des valeurs des membres **cbMaxSignature** et **cbBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="dca7d-129">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

<span data-ttu-id="dca7d-130">Les applications qui n’utilisent pas SSL doivent fournir un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de type SecBuffer \_ Padding.</span><span class="sxs-lookup"><span data-stu-id="dca7d-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="dca7d-131">*MessageSeqNo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dca7d-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dca7d-132">Numéro de séquence que l’application de transport a affecté au message.</span><span class="sxs-lookup"><span data-stu-id="dca7d-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="dca7d-133">Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="dca7d-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

<span data-ttu-id="dca7d-134">Lorsque vous utilisez le SSP Digest, ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="dca7d-134">When using the Digest SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="dca7d-135">Le SSP Digest gère la numérotation des séquences en interne.</span><span class="sxs-lookup"><span data-stu-id="dca7d-135">The Digest SSP manages sequence numbering internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dca7d-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dca7d-136">Return value</span></span>

<span data-ttu-id="dca7d-137">Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dca7d-137">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="dca7d-138">Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="dca7d-138">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="dca7d-139">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dca7d-139">Return code</span></span>                                                                                                    | <span data-ttu-id="dca7d-140">Description</span><span class="sxs-lookup"><span data-stu-id="dca7d-140">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dca7d-141"><dt>**\_tampon s \_ E \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-141"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="dca7d-142">La mémoire tampon de sortie est trop petite.</span><span class="sxs-lookup"><span data-stu-id="dca7d-142">The output buffer is too small.</span></span> <span data-ttu-id="dca7d-143">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="dca7d-143">For more information, see Remarks.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="dca7d-144"><dt>**\_contexte E/s \_ \_ expiré**</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-144"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="dca7d-145">L’application fait référence à un contexte qui a déjà été fermé.</span><span class="sxs-lookup"><span data-stu-id="dca7d-145">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="dca7d-146">Une application correctement écrite ne doit pas recevoir cette erreur.</span><span class="sxs-lookup"><span data-stu-id="dca7d-146">A properly written application should not receive this error.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="dca7d-147"><dt>**SEC \_ E \_ système de chiffrement \_ \_ non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-147"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="dca7d-148">Le [*chiffrement*](../secgloss/c-gly.md) choisi pour le [*contexte de sécurité*](../secgloss/s-gly.md) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dca7d-148">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="dca7d-149"><dt>**s \_ E \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-149"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="dca7d-150">La mémoire disponible est insuffisante pour terminer l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="dca7d-150">There is not enough memory available to complete the requested action.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="dca7d-151"><dt>**SEC \_ E \_ handle non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-151"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="dca7d-152">Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* .</span><span class="sxs-lookup"><span data-stu-id="dca7d-152">A context handle that is not valid was specified in the *phContext* parameter.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="dca7d-153"><dt>**s \_ E \_ jeton non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-153"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="dca7d-154">Aucune \_ mémoire tampon de type de données SECBUFFER n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="dca7d-154">No SECBUFFER\_DATA type buffer was found.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="dca7d-155"><dt>**SEC \_ E \_ QoP \_ non \_ pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-155"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="dca7d-156">La confidentialité et l' [*intégrité*](../secgloss/i-gly.md) ne sont pas prises en charge par le [*contexte de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dca7d-156">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dca7d-157">Notes</span><span class="sxs-lookup"><span data-stu-id="dca7d-157">Remarks</span></span>

<span data-ttu-id="dca7d-158">La fonction **EncryptMessage (Digest)** chiffre un message basé sur le message et la [*clé de session*](../secgloss/s-gly.md) à partir d’un contexte de [*sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dca7d-158">The **EncryptMessage (Digest)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="dca7d-159">Si l’application de transport a créé le [*contexte de sécurité*](../secgloss/s-gly.md) pour prendre en charge la détection de séquence et que l’appelant fournit un numéro de séquence, la fonction inclut ces informations avec le message chiffré.</span><span class="sxs-lookup"><span data-stu-id="dca7d-159">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="dca7d-160">L’inclusion de ces informations protège la relecture, l’insertion et la suppression des messages.</span><span class="sxs-lookup"><span data-stu-id="dca7d-160">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="dca7d-161">Le [*package de sécurité*](../secgloss/s-gly.md) intègre le numéro de séquence passé à partir de l’application de transport.</span><span class="sxs-lookup"><span data-stu-id="dca7d-161">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

<span data-ttu-id="dca7d-162">Lorsque vous utilisez le SSP Digest, récupérez la taille de la mémoire tampon de sortie en appelant la fonction [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) et en spécifiant des \_ tailles d’attr SECPKG \_ .</span><span class="sxs-lookup"><span data-stu-id="dca7d-162">When you use the Digest SSP, get the size of the output buffer by calling the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specifying SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="dca7d-163">La fonction retourne une structure [**de \_ tailles SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="dca7d-163">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="dca7d-164">La taille de la mémoire tampon de sortie est la somme des valeurs des membres **cbMaxSignature** et **cbBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="dca7d-164">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

> [!Note]  
> <span data-ttu-id="dca7d-165">Ces mémoires tampons doivent être fournies dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="dca7d-165">These buffers must be supplied in the order shown.</span></span>

 



| <span data-ttu-id="dca7d-166">Type de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="dca7d-166">Buffer type</span></span>                           | <span data-ttu-id="dca7d-167">Description</span><span class="sxs-lookup"><span data-stu-id="dca7d-167">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dca7d-168">\_ \_ en-tête de flux SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="dca7d-168">SECBUFFER\_STREAM\_HEADER</span></span><br/>  | <span data-ttu-id="dca7d-169">Utilisé en interne.</span><span class="sxs-lookup"><span data-stu-id="dca7d-169">Used internally.</span></span> <span data-ttu-id="dca7d-170">Aucune initialisation n’est requise.</span><span class="sxs-lookup"><span data-stu-id="dca7d-170">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="dca7d-171">\_données SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="dca7d-171">SECBUFFER\_DATA</span></span><br/>            | <span data-ttu-id="dca7d-172">Contient le message de [*texte en clair*](../secgloss/s-gly.md) à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="dca7d-172">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span><br/> |
| <span data-ttu-id="dca7d-173">Code de fin de \_ flux SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="dca7d-173">SECBUFFER\_STREAM\_TRAILER</span></span><br/> | <span data-ttu-id="dca7d-174">Utilisé en interne.</span><span class="sxs-lookup"><span data-stu-id="dca7d-174">Used internally.</span></span> <span data-ttu-id="dca7d-175">Aucune initialisation n’est requise.</span><span class="sxs-lookup"><span data-stu-id="dca7d-175">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="dca7d-176">SECBUFFER \_ vide</span><span class="sxs-lookup"><span data-stu-id="dca7d-176">SECBUFFER\_EMPTY</span></span><br/>           | <span data-ttu-id="dca7d-177">Utilisé en interne.</span><span class="sxs-lookup"><span data-stu-id="dca7d-177">Used internally.</span></span> <span data-ttu-id="dca7d-178">Aucune initialisation n’est requise.</span><span class="sxs-lookup"><span data-stu-id="dca7d-178">No initialization required.</span></span> <span data-ttu-id="dca7d-179">La taille peut être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="dca7d-179">Size can be zero.</span></span><br/>                                                      |



 

<span data-ttu-id="dca7d-180">Pour des performances optimales, les structures *pMessage* doivent être allouées à partir de la mémoire contiguë.</span><span class="sxs-lookup"><span data-stu-id="dca7d-180">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="dca7d-181">**Windows XP :** Cette fonction était également connue sous le nom de **SealMessage**.</span><span class="sxs-lookup"><span data-stu-id="dca7d-181">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="dca7d-182">Les applications doivent désormais utiliser **EncryptMessage (Digest)** uniquement.</span><span class="sxs-lookup"><span data-stu-id="dca7d-182">Applications should now use **EncryptMessage (Digest)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="dca7d-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dca7d-183">Requirements</span></span>



| <span data-ttu-id="dca7d-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dca7d-184">Requirement</span></span> | <span data-ttu-id="dca7d-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="dca7d-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dca7d-186">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dca7d-186">Minimum supported client</span></span><br/> | <span data-ttu-id="dca7d-187">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dca7d-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="dca7d-188">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dca7d-188">Minimum supported server</span></span><br/> | <span data-ttu-id="dca7d-189">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dca7d-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="dca7d-190">En-tête</span><span class="sxs-lookup"><span data-stu-id="dca7d-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="dca7d-191"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="dca7d-192">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dca7d-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="dca7d-193"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="dca7d-194">DLL</span><span class="sxs-lookup"><span data-stu-id="dca7d-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dca7d-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dca7d-195"><dt>Secur32.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="dca7d-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dca7d-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca7d-197">Fonctions SSPI</span><span class="sxs-lookup"><span data-stu-id="dca7d-197">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="dca7d-198">**AcceptSecurityContext (Digest)**</span><span class="sxs-lookup"><span data-stu-id="dca7d-198">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="dca7d-199">**DecryptMessage (Digest)**</span><span class="sxs-lookup"><span data-stu-id="dca7d-199">**DecryptMessage (Digest)**</span></span>](decryptmessage--digest.md)
</dt> <dt>

[<span data-ttu-id="dca7d-200">**InitializeSecurityContext (condensé)**</span><span class="sxs-lookup"><span data-stu-id="dca7d-200">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="dca7d-201">**QueryContextAttributes (Digest)**</span><span class="sxs-lookup"><span data-stu-id="dca7d-201">**QueryContextAttributes (Digest)**</span></span>](querycontextattributes--digest.md)
</dt> <dt>

[<span data-ttu-id="dca7d-202">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="dca7d-202">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="dca7d-203">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="dca7d-203">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
