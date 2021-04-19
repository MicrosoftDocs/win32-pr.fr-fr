---
description: Dérive une clé de session du secret et chiffre la valeur de la propriété de contenu à l’aide de cette clé. Elle retourne le contenu chiffré sous forme de chaîne encodée.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: EncryptedData. Encrypt, méthode (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523486"
---
# <a name="encrypteddataencrypt-method"></a><span data-ttu-id="627cc-104">EncryptedData. Encrypt, méthode</span><span class="sxs-lookup"><span data-stu-id="627cc-104">EncryptedData.Encrypt method</span></span>

<span data-ttu-id="627cc-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="627cc-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="627cc-106">Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="627cc-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="627cc-107">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="627cc-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="627cc-108">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="627cc-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="627cc-109">La méthode **Encrypt** dérive une clé de session du secret et chiffre la valeur de la propriété de [**contenu**](encrypteddata-content.md) à l’aide de cette clé.</span><span class="sxs-lookup"><span data-stu-id="627cc-109">The **Encrypt** method derives a session key from the secret and encrypts the [**Content**](encrypteddata-content.md) property value using that key.</span></span> <span data-ttu-id="627cc-110">Elle retourne le contenu chiffré sous forme de chaîne encodée.</span><span class="sxs-lookup"><span data-stu-id="627cc-110">It returns the encrypted content as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="627cc-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="627cc-111">Syntax</span></span>


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="627cc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="627cc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="627cc-113">*EncodingType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="627cc-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="627cc-114">Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui indique le type d’encodage utilisé pour encoder les données chiffrées.</span><span class="sxs-lookup"><span data-stu-id="627cc-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the encrypted data.</span></span> <span data-ttu-id="627cc-115">La valeur par défaut est CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="627cc-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="627cc-116">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="627cc-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="627cc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="627cc-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="627cc-118">Signification</span><span class="sxs-lookup"><span data-stu-id="627cc-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="627cc-119"><dt>**\_coder \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="627cc-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="627cc-120">Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu.</span><span class="sxs-lookup"><span data-stu-id="627cc-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="627cc-121">Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place.</span><span class="sxs-lookup"><span data-stu-id="627cc-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="627cc-122">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="627cc-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="627cc-123"><dt>**\_Encode \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="627cc-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="627cc-124">Les données sont enregistrées sous la forme d’une chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="627cc-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="627cc-125"><dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="627cc-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="627cc-126">Les données sont enregistrées sous la forme d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="627cc-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="627cc-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="627cc-127">Return value</span></span>

<span data-ttu-id="627cc-128">Chaîne qui contient les données chiffrées et encodées.</span><span class="sxs-lookup"><span data-stu-id="627cc-128">A string that contains the encrypted, encoded data.</span></span>

## <a name="remarks"></a><span data-ttu-id="627cc-129">Notes</span><span class="sxs-lookup"><span data-stu-id="627cc-129">Remarks</span></span>

<span data-ttu-id="627cc-130">Avant d’appeler la méthode **Encrypt** , définissez la propriété [**content**](encrypteddata-content.md) et appelez la méthode [**SetSecret**](encrypteddata-setsecret.md) .</span><span class="sxs-lookup"><span data-stu-id="627cc-130">Before calling the **Encrypt** method, set the [**Content**](encrypteddata-content.md) property and call the [**SetSecret**](encrypteddata-setsecret.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="627cc-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="627cc-131">Requirements</span></span>



| <span data-ttu-id="627cc-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="627cc-132">Requirement</span></span> | <span data-ttu-id="627cc-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="627cc-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="627cc-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="627cc-134">End of client support</span></span><br/> | <span data-ttu-id="627cc-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="627cc-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="627cc-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="627cc-136">End of server support</span></span><br/> | <span data-ttu-id="627cc-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="627cc-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="627cc-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="627cc-138">Redistributable</span></span><br/>       | <span data-ttu-id="627cc-139">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="627cc-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="627cc-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="627cc-140">Header</span></span><br/>                | <dl> <span data-ttu-id="627cc-141"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="627cc-141"><dt>Infocard.h</dt></span></span> </dl>  |
| <span data-ttu-id="627cc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="627cc-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="627cc-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="627cc-143"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="627cc-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="627cc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627cc-145">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="627cc-145">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="627cc-146">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="627cc-146">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
