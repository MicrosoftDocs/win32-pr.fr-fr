---
description: Déchiffre un message à l’aide de Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: DecryptMessage (Negotiate) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524484"
---
# <a name="decryptmessage-negotiate-function"></a><span data-ttu-id="d369b-103">DecryptMessage (Negotiate) (fonction)</span><span class="sxs-lookup"><span data-stu-id="d369b-103">DecryptMessage (Negotiate) function</span></span>

<span data-ttu-id="d369b-104">La fonction **DecryptMessage (Negotiate)** déchiffre un message.</span><span class="sxs-lookup"><span data-stu-id="d369b-104">The **DecryptMessage (Negotiate)** function decrypts a message.</span></span> <span data-ttu-id="d369b-105">Certains packages ne chiffrent et ne déchiffrent pas les messages, mais effectuent et vérifient plutôt un [*hachage*](../secgloss/h-gly.md)d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="d369b-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="d369b-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) et **DecryptMessage (Negotiate)** peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread chiffre et que l’autre déchiffre.</span><span class="sxs-lookup"><span data-stu-id="d369b-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) and **DecryptMessage (Negotiate)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="d369b-107">Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.</span><span class="sxs-lookup"><span data-stu-id="d369b-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="d369b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d369b-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="d369b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d369b-109">Parameters</span></span>

<span data-ttu-id="d369b-110">*phContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d369b-110">*phContext* \[in\]</span></span>

<span data-ttu-id="d369b-111">Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="d369b-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="d369b-112">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d369b-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="d369b-113">Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="d369b-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="d369b-114">En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) .</span><span class="sxs-lookup"><span data-stu-id="d369b-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures .</span></span> <span data-ttu-id="d369b-115">Au moins une de ces données doit être de type SECBUFFER \_ .</span><span class="sxs-lookup"><span data-stu-id="d369b-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="d369b-116">Cette mémoire tampon contient le message chiffré.</span><span class="sxs-lookup"><span data-stu-id="d369b-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="d369b-117">Le message chiffré est déchiffré sur place, remplaçant le contenu d’origine de sa mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d369b-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="d369b-118">*MessageSeqNo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d369b-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="d369b-119">Numéro de séquence attendu par l’application de transport, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d369b-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="d369b-120">Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="d369b-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="d369b-121">*pfQOP* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d369b-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="d369b-122">Pointeur vers une variable de type **ULong** qui reçoit des indicateurs spécifiques au package qui indiquent la qualité de la protection.</span><span class="sxs-lookup"><span data-stu-id="d369b-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="d369b-123">Ce paramètre peut être l’indicateur suivant.</span><span class="sxs-lookup"><span data-stu-id="d369b-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="d369b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d369b-124">Value</span></span></th><th><span data-ttu-id="d369b-125">Signification</span><span class="sxs-lookup"><span data-stu-id="d369b-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="d369b-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d369b-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="d369b-127">Le message n’a pas été chiffré, mais un en-tête ou un code de fin a été créé.</span><span class="sxs-lookup"><span data-stu-id="d369b-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="d369b-128">KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</span><span class="sxs-lookup"><span data-stu-id="d369b-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="d369b-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d369b-129">Return value</span></span>

<span data-ttu-id="d369b-130">Si la fonction vérifie que le message a été reçu dans l’ordre correct, la fonction retourne SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d369b-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="d369b-131">Si la fonction ne parvient pas à déchiffrer le message, elle retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="d369b-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="d369b-132">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d369b-132">Return code</span></span>                     | <span data-ttu-id="d369b-133">Description</span><span class="sxs-lookup"><span data-stu-id="d369b-133">Description</span></span>                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d369b-134">**s \_ E \_ message incomplet \_**</span><span class="sxs-lookup"><span data-stu-id="d369b-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="d369b-135">Les données de la mémoire tampon d’entrée sont incomplètes.</span><span class="sxs-lookup"><span data-stu-id="d369b-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="d369b-136">L’application doit lire plus de données à partir du serveur et appeler à nouveau [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="d369b-136">The application needs to read more data from the server and call [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) again.</span></span> |
| <span data-ttu-id="d369b-137">**SEC \_ E \_ hors \_ \_ séquence**</span><span class="sxs-lookup"><span data-stu-id="d369b-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="d369b-138">Le message n’a pas été reçu dans l’ordre correct.</span><span class="sxs-lookup"><span data-stu-id="d369b-138">The message was not received in the correct sequence.</span></span>                                                                                                                              |

## <a name="remarks"></a><span data-ttu-id="d369b-139">Notes</span><span class="sxs-lookup"><span data-stu-id="d369b-139">Remarks</span></span>

<span data-ttu-id="d369b-140">Parfois, une application lit les données du tiers distant, tente de les déchiffrer à l’aide de **DecryptMessage (Negotiate)** et découvre que **DecryptMessage (Negotiate)** a réussi, mais les mémoires tampons de sortie sont vides.</span><span class="sxs-lookup"><span data-stu-id="d369b-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Negotiate)**, and discover that **DecryptMessage (Negotiate)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="d369b-141">Il s’agit d’un comportement normal, et les applications doivent être en mesure de les gérer.</span><span class="sxs-lookup"><span data-stu-id="d369b-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="d369b-142">**Windows XP :** Cette fonction était également connue sous le nom de **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="d369b-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="d369b-143">Les applications doivent désormais utiliser **DecryptMessage (Negotiate)** uniquement.</span><span class="sxs-lookup"><span data-stu-id="d369b-143">Applications should now use **DecryptMessage (Negotiate)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="d369b-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d369b-144">Requirements</span></span>

| <span data-ttu-id="d369b-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d369b-145">Requirement</span></span> | <span data-ttu-id="d369b-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="d369b-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d369b-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d369b-147">Minimum supported client</span></span> | <span data-ttu-id="d369b-148">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d369b-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="d369b-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d369b-149">Minimum supported server</span></span> | <span data-ttu-id="d369b-150">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d369b-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="d369b-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="d369b-151">Header</span></span>                   | <span data-ttu-id="d369b-152">SSPI. h (include Security. h)</span><span class="sxs-lookup"><span data-stu-id="d369b-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="d369b-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d369b-153">Library</span></span>                  | <span data-ttu-id="d369b-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="d369b-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="d369b-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d369b-155">DLL</span></span>                      | <span data-ttu-id="d369b-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="d369b-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="d369b-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d369b-157">See also</span></span>

- [<span data-ttu-id="d369b-158">Fonctions SSPI</span><span class="sxs-lookup"><span data-stu-id="d369b-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="d369b-159">**EncryptMessage (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="d369b-159">**EncryptMessage (Negotiate)**</span></span>](encryptmessage--negotiate.md)
- [<span data-ttu-id="d369b-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="d369b-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="d369b-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="d369b-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
