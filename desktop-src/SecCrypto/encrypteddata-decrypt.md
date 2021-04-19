---
description: Déchiffre une chaîne de données chiffrée et encodée.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: EncryptedData. Decrypt, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528400"
---
# <a name="encrypteddatadecrypt-method"></a><span data-ttu-id="8cd12-103">EncryptedData. Decrypt, méthode</span><span class="sxs-lookup"><span data-stu-id="8cd12-103">EncryptedData.Decrypt method</span></span>

<span data-ttu-id="8cd12-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8cd12-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8cd12-105">Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="8cd12-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="8cd12-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="8cd12-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="8cd12-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="8cd12-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="8cd12-108">La méthode **Decrypt** déchiffre une chaîne de données chiffrée et encodée.</span><span class="sxs-lookup"><span data-stu-id="8cd12-108">The **Decrypt** method decrypts an encrypted and encoded data string.</span></span> <span data-ttu-id="8cd12-109">Les données en texte en clair résultantes deviennent la propriété de [**contenu**](encrypteddata-content.md) de l’objet [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd12-109">The resulting plaintext data becomes the [**Content**](encrypteddata-content.md) property of the [**EncryptedData**](encrypteddata.md) object.</span></span> <span data-ttu-id="8cd12-110">Le déchiffrement du contenu échoue, sauf si le secret, défini par la méthode [**SetSecret**](encrypteddata-setsecret.md) , est exactement le même que le secret utilisé pour dériver la clé utilisée pour chiffrer le contenu.</span><span class="sxs-lookup"><span data-stu-id="8cd12-110">Decryption of the content fails unless the secret, set by the [**SetSecret**](encrypteddata-setsecret.md) method, is exactly the same as the secret used to derive the key used to encrypt the content.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd12-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cd12-111">Syntax</span></span>


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="8cd12-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cd12-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cd12-113">*EncryptedMessage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8cd12-113">*EncryptedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd12-114">Chaîne qui contient les données chiffrées encodées à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="8cd12-114">String that contains the encoded, encrypted data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cd12-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8cd12-115">Return value</span></span>

<span data-ttu-id="8cd12-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8cd12-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cd12-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8cd12-117">Remarks</span></span>

<span data-ttu-id="8cd12-118">La clé de session dérivée du secret actuel est utilisée pour le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="8cd12-118">The session key derived from the current secret is used for the decryption.</span></span> <span data-ttu-id="8cd12-119">Cette méthode ne produit pas le texte en clair correct, sauf si le secret actuel correspond exactement au secret utilisé pour chiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="8cd12-119">This method will not produce the correct plaintext unless the current secret exactly matches the secret used to encrypt the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cd12-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cd12-120">Requirements</span></span>



| <span data-ttu-id="8cd12-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cd12-121">Requirement</span></span> | <span data-ttu-id="8cd12-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cd12-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd12-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8cd12-123">End of client support</span></span><br/> | <span data-ttu-id="8cd12-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cd12-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8cd12-125">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8cd12-125">End of server support</span></span><br/> | <span data-ttu-id="8cd12-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cd12-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8cd12-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8cd12-127">Redistributable</span></span><br/>       | <span data-ttu-id="8cd12-128">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="8cd12-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8cd12-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8cd12-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8cd12-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cd12-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cd12-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cd12-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd12-132">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="8cd12-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="8cd12-133">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="8cd12-133">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
