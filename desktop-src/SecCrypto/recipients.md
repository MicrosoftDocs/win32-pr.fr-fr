---
description: Représente une collection d’objets de certificat.
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Objet Recipients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541263"
---
# <a name="recipients-object"></a><span data-ttu-id="35430-103">Objet Recipients</span><span class="sxs-lookup"><span data-stu-id="35430-103">Recipients object</span></span>

<span data-ttu-id="35430-104">\[L’objet **destinataires** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="35430-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="35430-105">Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="35430-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="35430-106">L’objet **Recipients** représente une collection d’objets [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="35430-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="35430-107">Chaque objet représente un destinataire prévu du message enveloppé.</span><span class="sxs-lookup"><span data-stu-id="35430-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="35430-108">Les données d’un objet [**EnvelopedData**](envelopeddata.md) sont chiffrées à l’aide d’une clé de session [*symétrique*](../secgloss/s-gly.md) , et cette clé de session symétrique est ensuite chiffrée pour chaque destinataire à l’aide de la clé publique du certificat du destinataire prévu.</span><span class="sxs-lookup"><span data-stu-id="35430-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="35430-109">Un destinataire ayant accès à la [*clé privée*](../secgloss/p-gly.md) associée à la [*clé publique*](../secgloss/p-gly.md) d’un certificat peut déchiffrer la [*clé de session*](../secgloss/s-gly.md) et utiliser la clé de session déchiffrée pour déchiffrer les données réelles.</span><span class="sxs-lookup"><span data-stu-id="35430-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="35430-110">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="35430-110">When to use</span></span>

<span data-ttu-id="35430-111">L’objet **Recipients** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="35430-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="35430-112">Ajoutez ou supprimez un objet [**certificat**](certificate.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="35430-113">Récupérez le nombre de certificats dans la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="35430-114">Récupérez un objet **destinataires** spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="35430-115">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="35430-116">Membres</span><span class="sxs-lookup"><span data-stu-id="35430-116">Members</span></span>

<span data-ttu-id="35430-117">L’objet **Recipients** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="35430-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="35430-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35430-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="35430-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35430-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="35430-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35430-120">Methods</span></span>

<span data-ttu-id="35430-121">L’objet **Recipients** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="35430-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="35430-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="35430-122">Method</span></span>                              | <span data-ttu-id="35430-123">Description</span><span class="sxs-lookup"><span data-stu-id="35430-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="35430-124">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="35430-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="35430-125">Ajoute un objet [**certificat**](certificate.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="35430-126">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="35430-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="35430-127">Supprime tous les objets de [**certificat**](certificate.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="35430-128">**Installez**</span><span class="sxs-lookup"><span data-stu-id="35430-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="35430-129">Supprime un objet [**certificat**](certificate.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="35430-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35430-130">Properties</span></span>

<span data-ttu-id="35430-131">L’objet **Recipients** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="35430-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="35430-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="35430-132">Property</span></span>                                           | <span data-ttu-id="35430-133">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="35430-133">Access type</span></span>          | <span data-ttu-id="35430-134">Description</span><span class="sxs-lookup"><span data-stu-id="35430-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35430-135">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="35430-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="35430-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35430-136">Read-only</span></span><br/> | <span data-ttu-id="35430-137">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="35430-138">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="35430-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="35430-139">**Saut**</span><span class="sxs-lookup"><span data-stu-id="35430-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="35430-140">Nombre d’objets dans la collection **Recipients** .</span><span class="sxs-lookup"><span data-stu-id="35430-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="35430-141">**Élément**</span><span class="sxs-lookup"><span data-stu-id="35430-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="35430-142">Objet indexé dans la collection.</span><span class="sxs-lookup"><span data-stu-id="35430-142">An indexed object in the collection.</span></span> <span data-ttu-id="35430-143">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="35430-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="35430-144">Notes</span><span class="sxs-lookup"><span data-stu-id="35430-144">Remarks</span></span>

<span data-ttu-id="35430-145">Impossible de créer l’objet **Recipients** .</span><span class="sxs-lookup"><span data-stu-id="35430-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="35430-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35430-146">Requirements</span></span>



| <span data-ttu-id="35430-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35430-147">Requirement</span></span> | <span data-ttu-id="35430-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="35430-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35430-149">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="35430-149">Redistributable</span></span><br/> | <span data-ttu-id="35430-150">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="35430-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="35430-151">DLL</span><span class="sxs-lookup"><span data-stu-id="35430-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="35430-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35430-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35430-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35430-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35430-154">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="35430-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
