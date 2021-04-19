---
description: Détermine si les signatures sur les données signées dans l’objet SignedData sont valides.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData. Verify, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539197"
---
# <a name="signeddataverify-method"></a><span data-ttu-id="30adc-103">SignedData. Verify, méthode</span><span class="sxs-lookup"><span data-stu-id="30adc-103">SignedData.Verify method</span></span>

<span data-ttu-id="30adc-104">\[La méthode **verify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="30adc-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="30adc-105">Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="30adc-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="30adc-106">La méthode **verify** détermine si les [*signatures*](../secgloss/d-gly.md) sur les données signées dans l’objet [**SignedData**](signeddata.md) sont valides.</span><span class="sxs-lookup"><span data-stu-id="30adc-106">The **Verify** method determines whether the [*signatures*](../secgloss/d-gly.md) on signed data in the [**SignedData**](signeddata.md) object are valid.</span></span> <span data-ttu-id="30adc-107">Pour vérifier une signature, le [*hachage*](../secgloss/h-gly.md) chiffré du contenu est déchiffré à l’aide de la clé publique du signataire à partir du certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="30adc-107">To verify a signature, the encrypted [*hash*](../secgloss/h-gly.md) of the contents is decrypted by using the signer's public key from the signer's certificate.</span></span> <span data-ttu-id="30adc-108">Le hachage déchiffré est comparé à un nouveau hachage du contenu des données.</span><span class="sxs-lookup"><span data-stu-id="30adc-108">The decrypted hash is compared to a new hash of the data content.</span></span> <span data-ttu-id="30adc-109">Une signature est valide si les hachages correspondent.</span><span class="sxs-lookup"><span data-stu-id="30adc-109">A signature is valid if the hashes match.</span></span> <span data-ttu-id="30adc-110">En outre, cette méthode génère également une chaîne de certificats pour déterminer la validité du certificat qui fournit la [*clé publique*](../secgloss/p-gly.md) utilisée pour déchiffrer le hachage.</span><span class="sxs-lookup"><span data-stu-id="30adc-110">In addition, this method also builds a certificate chain to determine the validity of the certificate that provides the [*public key*](../secgloss/p-gly.md) used to decrypt the hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="30adc-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30adc-111">Syntax</span></span>


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="30adc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30adc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30adc-113">*SignedMessage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30adc-113">*SignedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30adc-114">Chaîne qui contient le message signé à vérifier.</span><span class="sxs-lookup"><span data-stu-id="30adc-114">A string that contains the signed message to be verified.</span></span>

</dd> <dt>

<span data-ttu-id="30adc-115">*bDetached* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30adc-115">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30adc-116">Si la **valeur est true**, les données à signer sont détachées ; autrement dit, le contenu signé n’est pas inclus dans l’objet signé.</span><span class="sxs-lookup"><span data-stu-id="30adc-116">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="30adc-117">Pour vérifier la signature sur du contenu détaché, une application doit avoir une copie du contenu d’origine.</span><span class="sxs-lookup"><span data-stu-id="30adc-117">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="30adc-118">Le contenu détaché est souvent utilisé pour réduire la taille d’un objet signé à envoyer sur le Web, si le destinataire du message signé contient une copie originale des données signées.</span><span class="sxs-lookup"><span data-stu-id="30adc-118">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="30adc-119">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="30adc-119">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="30adc-120">*VerifyFlag* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30adc-120">*VerifyFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30adc-121">Valeur de l’énumération de l' [indicateur de \_ \_ \_ vérification \_ des données signées CAPICOM](capicom-signed-data-verify-flag.md) qui indique la stratégie de vérification.</span><span class="sxs-lookup"><span data-stu-id="30adc-121">A value of the [CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG](capicom-signed-data-verify-flag.md) enumeration that indicates the verification policy.</span></span> <span data-ttu-id="30adc-122">La valeur par défaut est CAPICOM \_ verify \_ signature \_ et \_ Certificate.</span><span class="sxs-lookup"><span data-stu-id="30adc-122">The default value is CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE.</span></span> <span data-ttu-id="30adc-123">À l’aide de cette valeur, la validité du certificat et la validité de la signature sont vérifiées.</span><span class="sxs-lookup"><span data-stu-id="30adc-123">Using this value, both the validity of the certificate and the validity of the signature are checked.</span></span> <span data-ttu-id="30adc-124">Ce paramètre peut être défini pour vérifier la signature et non le certificat.</span><span class="sxs-lookup"><span data-stu-id="30adc-124">This parameter may be set to verify the signature and not the certificate.</span></span> <span data-ttu-id="30adc-125">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="30adc-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="30adc-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="30adc-126">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="30adc-127">Signification</span><span class="sxs-lookup"><span data-stu-id="30adc-127">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <span data-ttu-id="30adc-128"><dt>**\_signature de vérification CAPICOM \_ \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="30adc-128"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</dt></span></span> </dl>                                   | <span data-ttu-id="30adc-129">Seule la signature est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="30adc-129">Only the signature is checked.</span></span><br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <span data-ttu-id="30adc-130"><dt>**\_vérification \_ de la signature et du \_ \_ certificat de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="30adc-130"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</dt></span></span> </dl> | <span data-ttu-id="30adc-131">La signature et la validité du certificat utilisé pour créer la signature sont vérifiées.</span><span class="sxs-lookup"><span data-stu-id="30adc-131">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30adc-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30adc-132">Return value</span></span>

<span data-ttu-id="30adc-133">Cette méthode retourne une chaîne qui contient les données signées et encodées.</span><span class="sxs-lookup"><span data-stu-id="30adc-133">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="30adc-134">Si cette méthode échoue, une erreur est levée.</span><span class="sxs-lookup"><span data-stu-id="30adc-134">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="30adc-135">L’objet **Err** contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="30adc-135">The **Err** object will contain additional information about the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="30adc-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30adc-136">Requirements</span></span>



| <span data-ttu-id="30adc-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30adc-137">Requirement</span></span> | <span data-ttu-id="30adc-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="30adc-138">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30adc-139">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="30adc-139">Redistributable</span></span><br/> | <span data-ttu-id="30adc-140">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="30adc-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="30adc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="30adc-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="30adc-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30adc-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30adc-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30adc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30adc-144">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="30adc-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="30adc-145">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="30adc-145">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
