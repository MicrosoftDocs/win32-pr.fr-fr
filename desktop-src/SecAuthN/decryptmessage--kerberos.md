---
description: Déchiffre un message à l’aide de Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: DecryptMessage (Kerberos) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113810"
---
# <a name="decryptmessage-kerberos-function"></a><span data-ttu-id="b49bd-103">DecryptMessage (Kerberos) (fonction)</span><span class="sxs-lookup"><span data-stu-id="b49bd-103">DecryptMessage (Kerberos) function</span></span>

<span data-ttu-id="b49bd-104">La fonction **DecryptMessage (Kerberos)** déchiffre un message.</span><span class="sxs-lookup"><span data-stu-id="b49bd-104">The **DecryptMessage (Kerberos)** function decrypts a message.</span></span> <span data-ttu-id="b49bd-105">Certains packages ne chiffrent et ne déchiffrent pas les messages, mais effectuent et vérifient plutôt un [*hachage*](../secgloss/h-gly.md)d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="b49bd-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="b49bd-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) et **DecryptMessage (Kerberos)** peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre.</span><span class="sxs-lookup"><span data-stu-id="b49bd-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) and **DecryptMessage (Kerberos)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="b49bd-107">Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.</span><span class="sxs-lookup"><span data-stu-id="b49bd-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b49bd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b49bd-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="b49bd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b49bd-109">Parameters</span></span>

<span data-ttu-id="b49bd-110">*phContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49bd-110">*phContext* \[in\]</span></span>

<span data-ttu-id="b49bd-111">Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="b49bd-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="b49bd-112">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b49bd-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="b49bd-113">Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="b49bd-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="b49bd-114">En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui peuvent être de type SecBuffer \_ Data.</span><span class="sxs-lookup"><span data-stu-id="b49bd-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that may be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="b49bd-115">La mémoire tampon contient le message chiffré.</span><span class="sxs-lookup"><span data-stu-id="b49bd-115">The buffer contains the encrypted message.</span></span> <span data-ttu-id="b49bd-116">Le message chiffré est déchiffré sur place, remplaçant le contenu d’origine de sa mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b49bd-116">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="b49bd-117">*MessageSeqNo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49bd-117">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="b49bd-118">Numéro de séquence attendu par l’application de transport, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b49bd-118">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="b49bd-119">Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b49bd-119">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="b49bd-120">*pfQOP* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b49bd-120">*pfQOP* \[out\]</span></span>

<span data-ttu-id="b49bd-121">Pointeur vers une variable de type **ULong** qui reçoit des indicateurs spécifiques au package qui indiquent la qualité de la protection.</span><span class="sxs-lookup"><span data-stu-id="b49bd-121">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="b49bd-122">Ce paramètre peut être l’indicateur suivant.</span><span class="sxs-lookup"><span data-stu-id="b49bd-122">This parameter can be the following flag.</span></span>

| <span data-ttu-id="b49bd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b49bd-123">Value</span></span>                  | <span data-ttu-id="b49bd-124">Signification</span><span class="sxs-lookup"><span data-stu-id="b49bd-124">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b49bd-125">SECQOP_WRAP_NO_ENCRYPT</span><span class="sxs-lookup"><span data-stu-id="b49bd-125">SECQOP_WRAP_NO_ENCRYPT</span></span> | <span data-ttu-id="b49bd-126">le message n’a pas été chiffré, mais un en-tête ou un code de fin a été créé.</span><span class="sxs-lookup"><span data-stu-id="b49bd-126">he message was not encrypted, but a header or trailer was produced.</span></span> |

> [!NOTE]
> <span data-ttu-id="b49bd-127">KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</span><span class="sxs-lookup"><span data-stu-id="b49bd-127">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span>

## <a name="return-value"></a><span data-ttu-id="b49bd-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b49bd-128">Return value</span></span>

<span data-ttu-id="b49bd-129">Si la fonction vérifie que le message a été reçu dans l’ordre correct, la fonction retourne SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b49bd-129">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="b49bd-130">Si la fonction ne parvient pas à déchiffrer le message, elle retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="b49bd-130">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="b49bd-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b49bd-131">Return code</span></span>                     | <span data-ttu-id="b49bd-132">Description</span><span class="sxs-lookup"><span data-stu-id="b49bd-132">Description</span></span>                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b49bd-133">**s \_ E \_ message incomplet \_**</span><span class="sxs-lookup"><span data-stu-id="b49bd-133">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="b49bd-134">Les données de la mémoire tampon d’entrée sont incomplètes.</span><span class="sxs-lookup"><span data-stu-id="b49bd-134">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="b49bd-135">L’application doit lire plus de données à partir du serveur et appeler à nouveau [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="b49bd-135">The application needs to read more data from the server and call [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) again.</span></span> |
| <span data-ttu-id="b49bd-136">**SEC \_ E \_ hors \_ \_ séquence**</span><span class="sxs-lookup"><span data-stu-id="b49bd-136">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="b49bd-137">Le message n’a pas été reçu dans l’ordre correct.</span><span class="sxs-lookup"><span data-stu-id="b49bd-137">The message was not received in the correct sequence.</span></span>                                                                                                                            |

## <a name="remarks"></a><span data-ttu-id="b49bd-138">Notes</span><span class="sxs-lookup"><span data-stu-id="b49bd-138">Remarks</span></span>

<span data-ttu-id="b49bd-139">Parfois, une application lit les données du tiers distant, tente de les déchiffrer à l’aide de **DecryptMessage (Kerberos)** et découvre que **DecryptMessage (Kerberos)** a réussi, mais les tampons de sortie sont vides.</span><span class="sxs-lookup"><span data-stu-id="b49bd-139">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Kerberos)**, and discover that **DecryptMessage (Kerberos)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="b49bd-140">Il s’agit d’un comportement normal, et les applications doivent être en mesure de les gérer.</span><span class="sxs-lookup"><span data-stu-id="b49bd-140">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="b49bd-141">Pour plus d’informations sur l’interopérabilité avec GSSAPI, consultez [interopérabilité SSPI/Kerberos avec GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span><span class="sxs-lookup"><span data-stu-id="b49bd-141">For information about interoperating with GSSAPI, see [SSPI/Kerberos Interoperability with GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span></span>

<span data-ttu-id="b49bd-142">**Windows XP :** Cette fonction était également connue sous le nom de **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="b49bd-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="b49bd-143">Les applications doivent désormais utiliser **DecryptMessage (Kerberos)** uniquement.</span><span class="sxs-lookup"><span data-stu-id="b49bd-143">Applications should now use **DecryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49bd-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b49bd-144">Requirements</span></span>

| <span data-ttu-id="b49bd-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b49bd-145">Requirement</span></span> | <span data-ttu-id="b49bd-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="b49bd-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b49bd-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b49bd-147">Minimum supported client</span></span> | <span data-ttu-id="b49bd-148">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b49bd-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="b49bd-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b49bd-149">Minimum supported server</span></span> | <span data-ttu-id="b49bd-150">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b49bd-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="b49bd-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="b49bd-151">Header</span></span>                   | <span data-ttu-id="b49bd-152">SSPI. h (include Security. h)</span><span class="sxs-lookup"><span data-stu-id="b49bd-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="b49bd-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b49bd-153">Library</span></span>                  | <span data-ttu-id="b49bd-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="b49bd-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="b49bd-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b49bd-155">DLL</span></span>                      | <span data-ttu-id="b49bd-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="b49bd-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="b49bd-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b49bd-157">See also</span></span>

- [<span data-ttu-id="b49bd-158">Fonctions SSPI</span><span class="sxs-lookup"><span data-stu-id="b49bd-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="b49bd-159">**EncryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b49bd-159">**EncryptMessage (Kerberos)**</span></span>](encryptmessage--kerberos.md)
- [<span data-ttu-id="b49bd-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="b49bd-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="b49bd-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="b49bd-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
