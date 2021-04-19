---
description: Génère une clé de session et chiffre les données et enveloppes.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData. Encrypt, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542319"
---
# <a name="envelopeddataencrypt-method"></a><span data-ttu-id="4290d-103">EnvelopedData. Encrypt, méthode</span><span class="sxs-lookup"><span data-stu-id="4290d-103">EnvelopedData.Encrypt method</span></span>

<span data-ttu-id="4290d-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4290d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4290d-105">Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="4290d-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="4290d-106">La méthode **Encrypt** génère une clé de session, utilise cette clé pour chiffrer le contenu, encapsule le contenu chiffré pour chaque destinataire en chiffrant la clé de session avec la clé publique de chaque destinataire, puis retourne l' [*objet BLOB*](../secgloss/b-gly.md) qui contient le contenu chiffré et les clés de session chiffrées sous la forme d’une chaîne encodée.</span><span class="sxs-lookup"><span data-stu-id="4290d-106">The **Encrypt** method generates a session key, uses that key to encrypt the contents, envelops the encrypted content for each recipient by encrypting the session key with each recipient's public key, and then returns the [*BLOB*](../secgloss/b-gly.md) that contains the encrypted contents and the encrypted session keys as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4290d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4290d-107">Syntax</span></span>


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4290d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4290d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4290d-109">*EncodingType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4290d-109">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4290d-110">Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui indique le type d’encodage utilisé pour encoder les données enveloppées.</span><span class="sxs-lookup"><span data-stu-id="4290d-110">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the enveloped data.</span></span> <span data-ttu-id="4290d-111">La valeur d’encodage par défaut est CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="4290d-111">The default encoding value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="4290d-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4290d-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4290d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4290d-113">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="4290d-114">Signification</span><span class="sxs-lookup"><span data-stu-id="4290d-114">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="4290d-115"><dt>**\_coder \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="4290d-115"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="4290d-116">Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu.</span><span class="sxs-lookup"><span data-stu-id="4290d-116">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="4290d-117">Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place.</span><span class="sxs-lookup"><span data-stu-id="4290d-117">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="4290d-118">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="4290d-118">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="4290d-119"><dt>**\_Encode \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="4290d-119"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="4290d-120">Les données sont enregistrées sous la forme d’une chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="4290d-120">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="4290d-121"><dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="4290d-121"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="4290d-122">Les données sont enregistrées sous la forme d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="4290d-122">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4290d-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4290d-123">Return value</span></span>

<span data-ttu-id="4290d-124">Cette méthode retourne un objet BLOB qui contient les données enveloppées dans une chaîne encodée.</span><span class="sxs-lookup"><span data-stu-id="4290d-124">This method returns a BLOB that contains the enveloped data in an encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="4290d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="4290d-125">Remarks</span></span>

<span data-ttu-id="4290d-126">L’objet BLOB retourné contient le contenu chiffré et une clé de session chiffrée pour chaque destinataire prévu.</span><span class="sxs-lookup"><span data-stu-id="4290d-126">The returned BLOB contains the encrypted content and an encrypted session key for each intended recipient.</span></span> <span data-ttu-id="4290d-127">Ces clés de session sont chiffrées à l’aide de la clé publique de chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="4290d-127">These session keys are encrypted using the public key of each recipient.</span></span> <span data-ttu-id="4290d-128">Les clés de session chiffrées ne peuvent être déchiffrées qu’avec la clé privée d’un destinataire.</span><span class="sxs-lookup"><span data-stu-id="4290d-128">The encrypted session keys can be decrypted only with a recipient's private key.</span></span>

<span data-ttu-id="4290d-129">Si la propriété [**Recipients**](envelopeddata-recipients.md) ne contient aucune information, cette méthode recherche les destinataires potentiels dans le magasin de certificats AddressBook de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="4290d-129">If the [**Recipients**](envelopeddata-recipients.md) property does not contain any information, this method searches the current user's AddressBook certificate store for potential recipients.</span></span> <span data-ttu-id="4290d-130">Si plusieurs destinataires potentiels sont trouvés, l’utilisateur est invité à sélectionner un destinataire dans une boîte de dialogue de sélection.</span><span class="sxs-lookup"><span data-stu-id="4290d-130">If more than one potential recipient is found, the user is prompted to select a recipient from a selection dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="4290d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4290d-131">Requirements</span></span>



| <span data-ttu-id="4290d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4290d-132">Requirement</span></span> | <span data-ttu-id="4290d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4290d-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4290d-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4290d-134">End of client support</span></span><br/> | <span data-ttu-id="4290d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4290d-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4290d-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4290d-136">End of server support</span></span><br/> | <span data-ttu-id="4290d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4290d-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4290d-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4290d-138">Redistributable</span></span><br/>       | <span data-ttu-id="4290d-139">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="4290d-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4290d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4290d-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4290d-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4290d-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4290d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4290d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4290d-143">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="4290d-143">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="4290d-144">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="4290d-144">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
