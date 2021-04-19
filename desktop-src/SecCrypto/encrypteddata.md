---
description: Fournit des propriétés et des méthodes pour chiffrer et déchiffrer des données à l’aide d’une clé de session dérivée d’un secret.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Objet EncryptedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525360"
---
# <a name="encrypteddata-object"></a><span data-ttu-id="a182c-103">Objet EncryptedData</span><span class="sxs-lookup"><span data-stu-id="a182c-103">EncryptedData object</span></span>

<span data-ttu-id="a182c-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a182c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a182c-105">Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="a182c-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="a182c-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="a182c-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="a182c-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="a182c-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="a182c-108">L’objet **EncryptedData** fournit des propriétés et des méthodes pour chiffrer et déchiffrer des données à l’aide d’une [*clé de session*](../secgloss/s-gly.md) dérivée d’un secret.</span><span class="sxs-lookup"><span data-stu-id="a182c-108">The **EncryptedData** object provides properties and methods to encrypt and decrypt data using a [*session key*](../secgloss/s-gly.md) derived from a secret.</span></span>

> [!Note]  
> <span data-ttu-id="a182c-109">CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour **EncryptedData**.</span><span class="sxs-lookup"><span data-stu-id="a182c-109">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for **EncryptedData**.</span></span> <span data-ttu-id="a182c-110">Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM **EncryptedData** .</span><span class="sxs-lookup"><span data-stu-id="a182c-110">Therefore, only CAPICOM can decrypt a CAPICOM **EncryptedData** object.</span></span>

 

## <a name="members"></a><span data-ttu-id="a182c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="a182c-111">Members</span></span>

<span data-ttu-id="a182c-112">L’objet **EncryptedData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a182c-112">The **EncryptedData** object has these types of members:</span></span>

-   [<span data-ttu-id="a182c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a182c-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a182c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a182c-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a182c-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a182c-115">Methods</span></span>

<span data-ttu-id="a182c-116">L’objet **EncryptedData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a182c-116">The **EncryptedData** object has these methods.</span></span>



| <span data-ttu-id="a182c-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="a182c-117">Method</span></span>                                       | <span data-ttu-id="a182c-118">Description</span><span class="sxs-lookup"><span data-stu-id="a182c-118">Description</span></span>                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a182c-119">**Déchiffrer**</span><span class="sxs-lookup"><span data-stu-id="a182c-119">**Decrypt**</span></span>](encrypteddata-decrypt.md)     | <span data-ttu-id="a182c-120">Déchiffre le contenu chiffré à l’aide de la clé secrète.</span><span class="sxs-lookup"><span data-stu-id="a182c-120">Decrypts encrypted content using the secret.</span></span><br/>                                 |
| [<span data-ttu-id="a182c-121">**Encrypt (Chiffrer)**</span><span class="sxs-lookup"><span data-stu-id="a182c-121">**Encrypt**</span></span>](encrypteddata-encrypt.md)     | <span data-ttu-id="a182c-122">Chiffre le contenu à l’aide du secret et de l’algorithme de chiffrement actuels.</span><span class="sxs-lookup"><span data-stu-id="a182c-122">Encrypts the content using the current secret and encryption algorithm.</span></span><br/>      |
| [<span data-ttu-id="a182c-123">**SetSecret**</span><span class="sxs-lookup"><span data-stu-id="a182c-123">**SetSecret**</span></span>](encrypteddata-setsecret.md) | <span data-ttu-id="a182c-124">Définit le secret à partir duquel la clé de session de chiffrement/déchiffrement est dérivée.</span><span class="sxs-lookup"><span data-stu-id="a182c-124">Sets the secret from which the encryption/decryption session key is derived.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a182c-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a182c-125">Properties</span></span>

<span data-ttu-id="a182c-126">L’objet **EncryptedData** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a182c-126">The **EncryptedData** object has these properties.</span></span>



| <span data-ttu-id="a182c-127">Propriété</span><span class="sxs-lookup"><span data-stu-id="a182c-127">Property</span></span>                                                | <span data-ttu-id="a182c-128">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a182c-128">Access type</span></span>           | <span data-ttu-id="a182c-129">Description</span><span class="sxs-lookup"><span data-stu-id="a182c-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a182c-130">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="a182c-130">**Algorithm**</span></span>](encrypteddata-algorithm.md)<br/> | <span data-ttu-id="a182c-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a182c-131">Read-only</span></span><br/>  | <span data-ttu-id="a182c-132">Algorithme utilisé pour le chiffrement/déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="a182c-132">Algorithm used for encryption/decryption.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="a182c-133">**Content**</span><span class="sxs-lookup"><span data-stu-id="a182c-133">**Content**</span></span>](encrypteddata-content.md)<br/>     | <span data-ttu-id="a182c-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a182c-134">Read/write</span></span><br/> | <span data-ttu-id="a182c-135">Contenu à chiffrer ou à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="a182c-135">The content to be encrypted or decrypted.</span></span> <span data-ttu-id="a182c-136">La définition de cette propriété doit être effectuée avant l’appel de la méthode [**Encrypt**](encrypteddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="a182c-136">Setting this property must be done before the [**Encrypt**](encrypteddata-encrypt.md) method is called.</span></span> <br/> <span data-ttu-id="a182c-137">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée et tout contenu chiffré dans l’objet est perdu.</span><span class="sxs-lookup"><span data-stu-id="a182c-137">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="a182c-138">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="a182c-138">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a182c-139">Notes</span><span class="sxs-lookup"><span data-stu-id="a182c-139">Remarks</span></span>

<span data-ttu-id="a182c-140">L’objet **EncryptedData** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="a182c-140">The **EncryptedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="a182c-141">Le ProgID de l’objet **EncryptedData** est CAPICOM. EncryptedData. 1.</span><span class="sxs-lookup"><span data-stu-id="a182c-141">The ProgID for the **EncryptedData** object is CAPICOM.EncryptedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a182c-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a182c-142">Requirements</span></span>



| <span data-ttu-id="a182c-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a182c-143">Requirement</span></span> | <span data-ttu-id="a182c-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="a182c-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a182c-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a182c-145">End of client support</span></span><br/> | <span data-ttu-id="a182c-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a182c-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a182c-147">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a182c-147">End of server support</span></span><br/> | <span data-ttu-id="a182c-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a182c-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a182c-149">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a182c-149">Redistributable</span></span><br/>       | <span data-ttu-id="a182c-150">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a182c-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a182c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a182c-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a182c-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a182c-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a182c-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a182c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a182c-154">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="a182c-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
