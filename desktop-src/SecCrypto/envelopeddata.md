---
description: L’objet EnvelopedData fournit des propriétés et des méthodes pour encapsuler les données en vue de leur confidentialité par chiffrement.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Objet EnvelopedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542538"
---
# <a name="envelopeddata-object"></a><span data-ttu-id="8f905-103">Objet EnvelopedData</span><span class="sxs-lookup"><span data-stu-id="8f905-103">EnvelopedData object</span></span>

<span data-ttu-id="8f905-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f905-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8f905-105">Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="8f905-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="8f905-106">L’objet **EnvelopedData** fournit des propriétés et des méthodes pour encapsuler les données en vue de leur confidentialité par chiffrement.</span><span class="sxs-lookup"><span data-stu-id="8f905-106">The **EnvelopedData** object provides properties and methods to envelop data for privacy by encryption.</span></span> <span data-ttu-id="8f905-107">Pour encapsuler des données, une clé de chiffrement de session est générée.</span><span class="sxs-lookup"><span data-stu-id="8f905-107">To envelop data, a session cryptographic key is generated.</span></span> <span data-ttu-id="8f905-108">Cette [*clé de session*](../secgloss/s-gly.md) est ensuite chiffrée pour chaque destinataire prévu à l’aide de la [*clé publique*](../secgloss/p-gly.md) de ce destinataire prévu du certificat du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8f905-108">That [*session key*](../secgloss/s-gly.md) is then encrypted for each intended recipient using the [*public key*](../secgloss/p-gly.md) of that intended recipient from the recipient's certificate.</span></span> <span data-ttu-id="8f905-109">Les données chiffrées et l’ensemble des clés de session chiffrées peuvent être envoyés à tous les destinataires prévus.</span><span class="sxs-lookup"><span data-stu-id="8f905-109">The encrypted data and the set of encrypted session keys can be sent to all intended recipients.</span></span> <span data-ttu-id="8f905-110">Le message généré est au \# format PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="8f905-110">The message generated is in PKCS \#7 format.</span></span>

## <a name="members"></a><span data-ttu-id="8f905-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8f905-111">Members</span></span>

<span data-ttu-id="8f905-112">L’objet **EnvelopedData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8f905-112">The **EnvelopedData** object has these types of members:</span></span>

-   [<span data-ttu-id="8f905-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8f905-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f905-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f905-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f905-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8f905-115">Methods</span></span>

<span data-ttu-id="8f905-116">L’objet **EnvelopedData** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8f905-116">The **EnvelopedData** object has these methods.</span></span>



| <span data-ttu-id="8f905-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="8f905-117">Method</span></span>                                   | <span data-ttu-id="8f905-118">Description</span><span class="sxs-lookup"><span data-stu-id="8f905-118">Description</span></span>                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f905-119">**Déchiffrer**</span><span class="sxs-lookup"><span data-stu-id="8f905-119">**Decrypt**</span></span>](envelopeddata-decrypt.md) | <span data-ttu-id="8f905-120">Déchiffre le contenu enveloppé.</span><span class="sxs-lookup"><span data-stu-id="8f905-120">Decrypts enveloped content.</span></span><br/>                                                                      |
| [<span data-ttu-id="8f905-121">**Encrypt (Chiffrer)**</span><span class="sxs-lookup"><span data-stu-id="8f905-121">**Encrypt**</span></span>](envelopeddata-encrypt.md) | <span data-ttu-id="8f905-122">Chiffre le contenu, chiffre une clé de session pour chaque destinataire et retourne l’objet BLOB chiffré.</span><span class="sxs-lookup"><span data-stu-id="8f905-122">Encrypts the content, encrypts a session key for each recipient, and returns the encrypted BLOB.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8f905-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f905-123">Properties</span></span>

<span data-ttu-id="8f905-124">L’objet **EnvelopedData** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8f905-124">The **EnvelopedData** object has these properties.</span></span>



| <span data-ttu-id="8f905-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="8f905-125">Property</span></span>                                                  | <span data-ttu-id="8f905-126">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="8f905-126">Access type</span></span>           | <span data-ttu-id="8f905-127">Description</span><span class="sxs-lookup"><span data-stu-id="8f905-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f905-128">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="8f905-128">**Algorithm**</span></span>](envelopeddata-algorithm.md)<br/>   | <span data-ttu-id="8f905-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f905-129">Read/write</span></span><br/> | <span data-ttu-id="8f905-130">Algorithme de chiffrement et [*longueur de clé*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8f905-130">Encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="8f905-131">**Content**</span><span class="sxs-lookup"><span data-stu-id="8f905-131">**Content**</span></span>](envelopeddata-content.md)<br/>       | <span data-ttu-id="8f905-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f905-132">Read/write</span></span><br/> | <span data-ttu-id="8f905-133">Contenu en texte clair d’un message à envelopper.</span><span class="sxs-lookup"><span data-stu-id="8f905-133">The plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="8f905-134">La définition de cette propriété doit être effectuée avant l’appel de la méthode [**Encrypt**](envelopeddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="8f905-134">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span><br/> <span data-ttu-id="8f905-135">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée et tout contenu chiffré dans l’objet est perdu.</span><span class="sxs-lookup"><span data-stu-id="8f905-135">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="8f905-136">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f905-136">This is the default property.</span></span><br/> |
| [<span data-ttu-id="8f905-137">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="8f905-137">**Recipients**</span></span>](envelopeddata-recipients.md)<br/> | <span data-ttu-id="8f905-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f905-138">Read-only</span></span><br/>  | <span data-ttu-id="8f905-139">Collection d’objets de [**certificat**](certificate.md) pour recevoir le message enveloppé.</span><span class="sxs-lookup"><span data-stu-id="8f905-139">Collection of [**Certificate**](certificate.md) objects to receive the enveloped message.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="8f905-140">Notes</span><span class="sxs-lookup"><span data-stu-id="8f905-140">Remarks</span></span>

<span data-ttu-id="8f905-141">L’objet **EnvelopedData** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="8f905-141">The **EnvelopedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="8f905-142">Le ProgID de l’objet **EnvelopedData** est CAPICOM. EnvelopedData. 1.</span><span class="sxs-lookup"><span data-stu-id="8f905-142">The ProgID for the **EnvelopedData** object is CAPICOM.EnvelopedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f905-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f905-143">Requirements</span></span>



| <span data-ttu-id="8f905-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f905-144">Requirement</span></span> | <span data-ttu-id="8f905-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f905-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f905-146">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8f905-146">End of client support</span></span><br/> | <span data-ttu-id="8f905-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f905-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8f905-148">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8f905-148">End of server support</span></span><br/> | <span data-ttu-id="8f905-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f905-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8f905-150">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8f905-150">Redistributable</span></span><br/>       | <span data-ttu-id="8f905-151">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f905-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8f905-152">DLL</span><span class="sxs-lookup"><span data-stu-id="8f905-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8f905-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f905-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f905-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f905-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f905-155">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="8f905-155">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
