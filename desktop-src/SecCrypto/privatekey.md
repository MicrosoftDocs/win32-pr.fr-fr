---
description: Représente la clé privée associée à un certificat.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Objet PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525359"
---
# <a name="privatekey-object"></a><span data-ttu-id="c0915-103">Objet PrivateKey</span><span class="sxs-lookup"><span data-stu-id="c0915-103">PrivateKey object</span></span>

<span data-ttu-id="c0915-104">\[L’objet **PrivateKey** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c0915-104">\[The **PrivateKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c0915-105">Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c0915-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c0915-106">L’objet **PrivateKey** représente la [*clé privée*](../secgloss/p-gly.md) associée à un certificat.</span><span class="sxs-lookup"><span data-stu-id="c0915-106">The **PrivateKey** object represents the [*private key*](../secgloss/p-gly.md) associated with a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c0915-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="c0915-107">When to use</span></span>

<span data-ttu-id="c0915-108">L’objet **PrivateKey** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0915-108">The **PrivateKey** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="c0915-109">Récupérez les informations relatives à la clé privée.</span><span class="sxs-lookup"><span data-stu-id="c0915-109">Retrieve information about the private key.</span></span>
-   <span data-ttu-id="c0915-110">Ouvrez le conteneur de clé privée.</span><span class="sxs-lookup"><span data-stu-id="c0915-110">Open the private key container.</span></span>
-   <span data-ttu-id="c0915-111">Supprimez la clé privée.</span><span class="sxs-lookup"><span data-stu-id="c0915-111">Delete the private key.</span></span>

## <a name="members"></a><span data-ttu-id="c0915-112">Membres</span><span class="sxs-lookup"><span data-stu-id="c0915-112">Members</span></span>

<span data-ttu-id="c0915-113">L’objet **PrivateKey** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c0915-113">The **PrivateKey** object has these types of members:</span></span>

-   [<span data-ttu-id="c0915-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0915-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0915-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0915-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0915-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0915-116">Methods</span></span>

<span data-ttu-id="c0915-117">L’objet **PrivateKey** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c0915-117">The **PrivateKey** object has these methods.</span></span>



| <span data-ttu-id="c0915-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="c0915-118">Method</span></span>                                                  | <span data-ttu-id="c0915-119">Description</span><span class="sxs-lookup"><span data-stu-id="c0915-119">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0915-120">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="c0915-120">**Delete**</span></span>](privatekey-delete.md)                     | <span data-ttu-id="c0915-121">Supprime le conteneur de clé privée référencé par l’objet **PrivateKey** .</span><span class="sxs-lookup"><span data-stu-id="c0915-121">Deletes the private key container referenced by the **PrivateKey** object.</span></span><br/>                                                                                |
| [<span data-ttu-id="c0915-122">**IsAccessible**</span><span class="sxs-lookup"><span data-stu-id="c0915-122">**IsAccessible**</span></span>](privatekey-isaccessible.md)         | <span data-ttu-id="c0915-123">Récupère une valeur booléenne qui indique si la clé privée est accessible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c0915-123">Retrieves a Boolean value that indicates whether the private key is accessible by the user.</span></span> <span data-ttu-id="c0915-124">Si la valeur est true, l’utilisateur peut accéder à la clé privée.</span><span class="sxs-lookup"><span data-stu-id="c0915-124">If true, the user can access the private key.</span></span><br/>                 |
| [<span data-ttu-id="c0915-125">**IsExportable**</span><span class="sxs-lookup"><span data-stu-id="c0915-125">**IsExportable**</span></span>](privatekey-isexportable.md)         | <span data-ttu-id="c0915-126">Récupère une valeur booléenne qui indique si la clé privée peut être exportée.</span><span class="sxs-lookup"><span data-stu-id="c0915-126">Retrieves a Boolean value that indicates whether the private key can be exported.</span></span> <span data-ttu-id="c0915-127">Si la valeur est true, la clé privée peut être exportée.</span><span class="sxs-lookup"><span data-stu-id="c0915-127">If true, the private key can be exported.</span></span><br/>                               |
| [<span data-ttu-id="c0915-128">**IsHardwareDevice**</span><span class="sxs-lookup"><span data-stu-id="c0915-128">**IsHardwareDevice**</span></span>](privatekey-ishardwaredevice.md) | <span data-ttu-id="c0915-129">Récupère une valeur booléenne qui indique si la clé privée est stockée sur un périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="c0915-129">Retrieves a Boolean value that indicates whether the private key is stored on a hardware device.</span></span> <span data-ttu-id="c0915-130">Si la valeur est true, la clé privée est stockée sur un périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="c0915-130">If true, the private key is stored on a hardware device.</span></span><br/> |
| [<span data-ttu-id="c0915-131">**IsMachineKeyset**</span><span class="sxs-lookup"><span data-stu-id="c0915-131">**IsMachineKeyset**</span></span>](privatekey-ismachinekeyset.md)   | <span data-ttu-id="c0915-132">Récupère une valeur booléenne qui indique si la clé privée est une clé d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c0915-132">Retrieves a Boolean value that indicates whether the private key is a machine key.</span></span> <span data-ttu-id="c0915-133">Si la valeur est true, la clé privée est une clé d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c0915-133">If true, the private key is a machine key.</span></span><br/>                             |
| [<span data-ttu-id="c0915-134">**IsProtected**</span><span class="sxs-lookup"><span data-stu-id="c0915-134">**IsProtected**</span></span>](privatekey-isprotected.md)           | <span data-ttu-id="c0915-135">Récupère une valeur booléenne qui indique si la clé privée est protégée.</span><span class="sxs-lookup"><span data-stu-id="c0915-135">Retrieves a Boolean value that indicates whether the private key is protected.</span></span> <span data-ttu-id="c0915-136">Si la valeur est true, la clé privée est protégée.</span><span class="sxs-lookup"><span data-stu-id="c0915-136">If true, the private key is protected.</span></span><br/>                                     |
| [<span data-ttu-id="c0915-137">**IsRemovable**</span><span class="sxs-lookup"><span data-stu-id="c0915-137">**IsRemovable**</span></span>](privatekey-isremovable.md)           | <span data-ttu-id="c0915-138">Récupère une valeur booléenne qui indique si la clé privée est sur un appareil amovible.</span><span class="sxs-lookup"><span data-stu-id="c0915-138">Retrieves a Boolean value that indicates whether the private key is on a removable device.</span></span> <span data-ttu-id="c0915-139">Si la valeur est true, la clé privée se trouve sur un périphérique amovible.</span><span class="sxs-lookup"><span data-stu-id="c0915-139">If true, the private key is on a removable device.</span></span><br/>             |
| [<span data-ttu-id="c0915-140">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="c0915-140">**Open**</span></span>](privatekey-open.md)                         | <span data-ttu-id="c0915-141">Accède à un conteneur de clé existant.</span><span class="sxs-lookup"><span data-stu-id="c0915-141">Accesses an existing key container.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="c0915-142">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0915-142">Properties</span></span>

<span data-ttu-id="c0915-143">L’objet **PrivateKey** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c0915-143">The **PrivateKey** object has these properties.</span></span>



| <span data-ttu-id="c0915-144">Propriété</span><span class="sxs-lookup"><span data-stu-id="c0915-144">Property</span></span>                                                                 | <span data-ttu-id="c0915-145">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c0915-145">Access type</span></span>          | <span data-ttu-id="c0915-146">Description</span><span class="sxs-lookup"><span data-stu-id="c0915-146">Description</span></span>                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0915-147">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="c0915-147">**ContainerName**</span></span>](privatekey-containername.md)<br/>             | <span data-ttu-id="c0915-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0915-148">Read-only</span></span><br/> | <span data-ttu-id="c0915-149">Récupère une chaîne qui contient le nom du conteneur de clé privée.</span><span class="sxs-lookup"><span data-stu-id="c0915-149">Retrieves a string that contains the private key container name.</span></span> <span data-ttu-id="c0915-150">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="c0915-150">This is the default property.</span></span><br/> |
| [<span data-ttu-id="c0915-151">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="c0915-151">**KeySpec**</span></span>](privatekey-keyspec.md)<br/>                         | <span data-ttu-id="c0915-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0915-152">Read-only</span></span><br/> | <span data-ttu-id="c0915-153">Récupère la spécification de clé.</span><span class="sxs-lookup"><span data-stu-id="c0915-153">Retrieves the key specification.</span></span><br/>                                                               |
| [<span data-ttu-id="c0915-154">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="c0915-154">**ProviderName**</span></span>](privatekey-providername.md)<br/>               | <span data-ttu-id="c0915-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0915-155">Read-only</span></span><br/> | <span data-ttu-id="c0915-156">Récupère une chaîne qui contient le nom du fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="c0915-156">Retrieves a string that contains the name of the CSP.</span></span><br/>                                          |
| [<span data-ttu-id="c0915-157">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="c0915-157">**ProviderType**</span></span>](privatekey-providertype.md)<br/>               | <span data-ttu-id="c0915-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0915-158">Read-only</span></span><br/> | <span data-ttu-id="c0915-159">Récupère une valeur d’énumération qui spécifie le type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c0915-159">Retrieves an enumeration value that specifies the type of provider.</span></span><br/>                            |
| [<span data-ttu-id="c0915-160">**UniqueContainerName**</span><span class="sxs-lookup"><span data-stu-id="c0915-160">**UniqueContainerName**</span></span>](privatekey-uniquecontainername.md)<br/> | <span data-ttu-id="c0915-161">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0915-161">Read-only</span></span><br/> | <span data-ttu-id="c0915-162">Récupère une chaîne qui contient le nom unique du conteneur de clé privée.</span><span class="sxs-lookup"><span data-stu-id="c0915-162">Retrieves a string that contains the unique private key container name.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="c0915-163">Notes</span><span class="sxs-lookup"><span data-stu-id="c0915-163">Remarks</span></span>

<span data-ttu-id="c0915-164">L’objet **PrivateKey** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="c0915-164">The **PrivateKey** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="c0915-165">Le ProgID de l’objet **PrivateKey** est CAPICOM. PrivateKey. 1.</span><span class="sxs-lookup"><span data-stu-id="c0915-165">The ProgID for the **PrivateKey** object is CAPICOM.PrivateKey.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0915-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0915-166">Requirements</span></span>



| <span data-ttu-id="c0915-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0915-167">Requirement</span></span> | <span data-ttu-id="c0915-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0915-168">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0915-169">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c0915-169">Redistributable</span></span><br/> | <span data-ttu-id="c0915-170">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0915-170">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c0915-171">DLL</span><span class="sxs-lookup"><span data-stu-id="c0915-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="c0915-172"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0915-172"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
