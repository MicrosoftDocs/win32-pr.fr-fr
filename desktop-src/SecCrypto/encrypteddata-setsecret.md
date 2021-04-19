---
description: Définit la valeur du secret utilisé pour dériver la clé de session de chiffrement utilisée pour chiffrer et déchiffrer les données.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: EncryptedData. SetSecret, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540998"
---
# <a name="encrypteddatasetsecret-method"></a><span data-ttu-id="15ecc-103">EncryptedData. SetSecret, méthode</span><span class="sxs-lookup"><span data-stu-id="15ecc-103">EncryptedData.SetSecret method</span></span>

<span data-ttu-id="15ecc-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="15ecc-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="15ecc-105">Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="15ecc-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="15ecc-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="15ecc-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="15ecc-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="15ecc-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="15ecc-108">La méthode **SetSecret** définit la valeur du secret utilisé pour dériver la [*clé de session*](../secgloss/s-gly.md) de chiffrement utilisée pour chiffrer et déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="15ecc-108">The **SetSecret** method sets the value of the secret used to derive the cryptographic [*session key*](../secgloss/s-gly.md) used to encrypt and decrypt data.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ecc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15ecc-109">Syntax</span></span>


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="15ecc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15ecc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15ecc-111">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15ecc-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ecc-112">Chaîne qui contient un secret utilisé pour créer une clé de chiffrement de session.</span><span class="sxs-lookup"><span data-stu-id="15ecc-112">A string that contains a secret used to create a session cryptographic key.</span></span>

</dd> <dt>

<span data-ttu-id="15ecc-113">*SecretType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="15ecc-113">*SecretType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15ecc-114">Valeur de l’énumération de [**\_ \_ type secret CAPICOM**](capicom-secret-type.md) qui indique le type de secret utilisé pour générer la clé de session.</span><span class="sxs-lookup"><span data-stu-id="15ecc-114">A value of the [**CAPICOM\_SECRET\_TYPE**](capicom-secret-type.md) enumeration that indicates the kind of secret used to generate the session key.</span></span> <span data-ttu-id="15ecc-115">La valeur par défaut est CAPICOM \_ secret secret \_ .</span><span class="sxs-lookup"><span data-stu-id="15ecc-115">The default value is CAPICOM\_SECRET\_PASSWORD.</span></span> <span data-ttu-id="15ecc-116">Ce paramètre peut avoir la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="15ecc-116">This parameter can be the following value.</span></span>



| <span data-ttu-id="15ecc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="15ecc-117">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="15ecc-118">Signification</span><span class="sxs-lookup"><span data-stu-id="15ecc-118">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <span data-ttu-id="15ecc-119"><dt>**\_ \_ mot de passe secret de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="15ecc-119"><dt>**CAPICOM\_SECRET\_PASSWORD**</dt></span></span> </dl> | <span data-ttu-id="15ecc-120">La clé de chiffrement doit être dérivée d’un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="15ecc-120">The encryption key is to be derived from a password.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15ecc-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15ecc-121">Return value</span></span>

<span data-ttu-id="15ecc-122">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="15ecc-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15ecc-123">Notes</span><span class="sxs-lookup"><span data-stu-id="15ecc-123">Remarks</span></span>

<span data-ttu-id="15ecc-124">Le secret est utilisé pour créer la clé de session pour le chiffrement ou le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="15ecc-124">The secret is used to create the session key for encryption or decryption.</span></span> <span data-ttu-id="15ecc-125">La même clé secrète doit être utilisée pour les deux opérations.</span><span class="sxs-lookup"><span data-stu-id="15ecc-125">The same secret must be used for both operations.</span></span> <span data-ttu-id="15ecc-126">Si le secret utilisé pour chiffrer les données est perdu, les données chiffrées ne peuvent pas être déchiffrées.</span><span class="sxs-lookup"><span data-stu-id="15ecc-126">If the secret used to encrypt data is lost, the encrypted data cannot be decrypted.</span></span>

<span data-ttu-id="15ecc-127">Si c’est approprié pour votre application, envisagez d’utiliser [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) ou [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) pour protéger la clé secrète avant et après l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="15ecc-127">If appropriate for your application, consider using [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) or [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to protect the secret before and after use.</span></span> <span data-ttu-id="15ecc-128">Effacez la mémoire associée à la clé secrète lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="15ecc-128">Clear the memory associated with the secret when done.</span></span>

## <a name="requirements"></a><span data-ttu-id="15ecc-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15ecc-129">Requirements</span></span>



| <span data-ttu-id="15ecc-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15ecc-130">Requirement</span></span> | <span data-ttu-id="15ecc-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="15ecc-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15ecc-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="15ecc-132">End of client support</span></span><br/> | <span data-ttu-id="15ecc-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15ecc-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="15ecc-134">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="15ecc-134">End of server support</span></span><br/> | <span data-ttu-id="15ecc-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15ecc-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="15ecc-136">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="15ecc-136">Redistributable</span></span><br/>       | <span data-ttu-id="15ecc-137">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="15ecc-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="15ecc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="15ecc-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="15ecc-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15ecc-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ecc-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15ecc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ecc-141">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="15ecc-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="15ecc-142">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="15ecc-142">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
