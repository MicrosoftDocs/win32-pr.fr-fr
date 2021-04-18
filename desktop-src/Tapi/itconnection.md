---
description: La fonctionnalité de l’interface ITConnection est illustrée ci-dessous.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interface ITConnection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540082"
---
# <a name="itconnection-interface"></a><span data-ttu-id="0279d-103">Interface ITConnection</span><span class="sxs-lookup"><span data-stu-id="0279d-103">ITConnection interface</span></span>

<span data-ttu-id="0279d-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0279d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0279d-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="0279d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0279d-106">L’interface **ITConnection** fournit les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="0279d-106">The **ITConnection** interface provides the following functionality:</span></span>

-   <span data-ttu-id="0279d-107">Permet d’accéder aux informations relatives à l’adresse et à la durée de vie (TTL) de la session.</span><span class="sxs-lookup"><span data-stu-id="0279d-107">Provides access to the address and time to live (TTL) information for the session.</span></span>
-   <span data-ttu-id="0279d-108">Fournit l’accès aux informations de bande passante.</span><span class="sxs-lookup"><span data-stu-id="0279d-108">Provides access to the bandwidth information.</span></span>
-   <span data-ttu-id="0279d-109">Active la manipulation de la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0279d-109">Enables manipulation of the encryption key.</span></span>

<span data-ttu-id="0279d-110">L’interface **ITConnection** est créée en appelant **QueryInterface** sur [**ITConferenceBlob**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="0279d-110">The **ITConnection** interface is created by calling **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

## <a name="members"></a><span data-ttu-id="0279d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="0279d-111">Members</span></span>

<span data-ttu-id="0279d-112">L’interface **ITConnection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0279d-112">The **ITConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0279d-113">**ITConnection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0279d-113">**ITConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="0279d-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0279d-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0279d-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0279d-115">Methods</span></span>

<span data-ttu-id="0279d-116">L’interface **ITConnection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0279d-116">The **ITConnection** interface has these methods.</span></span>



| <span data-ttu-id="0279d-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="0279d-117">Method</span></span>                                                               | <span data-ttu-id="0279d-118">Description</span><span class="sxs-lookup"><span data-stu-id="0279d-118">Description</span></span>                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0279d-119">**Obtient \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="0279d-119">**get\_AddressType**</span></span>](itconnection-get-addresstype.md)             | <span data-ttu-id="0279d-120">Obtient le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="0279d-120">Gets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0279d-121">**bénéficier de \_ la bande passante**</span><span class="sxs-lookup"><span data-stu-id="0279d-121">**get\_Bandwidth**</span></span>](itconnection-get-bandwidth.md)                 | <span data-ttu-id="0279d-122">Obtient la valeur de bande passante.</span><span class="sxs-lookup"><span data-stu-id="0279d-122">Gets bandwidth value.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="0279d-123">**Obtient \_ BandwidthModifier**</span><span class="sxs-lookup"><span data-stu-id="0279d-123">**get\_BandwidthModifier**</span></span>](itconnection-get-bandwidthmodifier.md) | <span data-ttu-id="0279d-124">Obtient le modificateur de bande passante.</span><span class="sxs-lookup"><span data-stu-id="0279d-124">Gets the bandwidth modifier.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="0279d-125">**Obtient \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="0279d-125">**get\_NetworkType**</span></span>](itconnection-get-networktype.md)             | <span data-ttu-id="0279d-126">Obtient le type de réseau.</span><span class="sxs-lookup"><span data-stu-id="0279d-126">Gets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0279d-127">**Obtient \_ NumAddresses**</span><span class="sxs-lookup"><span data-stu-id="0279d-127">**get\_NumAddresses**</span></span>](itconnection-get-numaddresses.md)           | <span data-ttu-id="0279d-128">Obtient le nombre d’adresses à utiliser pour la session.</span><span class="sxs-lookup"><span data-stu-id="0279d-128">Gets the number of addresses to be used for the session.</span></span><br/>                                                                            |
| [<span data-ttu-id="0279d-129">**Obtient \_ STARTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="0279d-129">**get\_StartAddress**</span></span>](itconnection-get-startaddress.md)           | <span data-ttu-id="0279d-130">Obtient la première adresse à utiliser pour la session.</span><span class="sxs-lookup"><span data-stu-id="0279d-130">Gets the first address to be used for the session.</span></span><br/>                                                                                  |
| [<span data-ttu-id="0279d-131">**Obtient la \_ durée de vie**</span><span class="sxs-lookup"><span data-stu-id="0279d-131">**get\_Ttl**</span></span>](itconnection-get-ttl.md)                             | <span data-ttu-id="0279d-132">Obtient l’étendue de la [*durée de*](t-tapgloss.md) vie (TTL) pour les transmissions sur les adresses.</span><span class="sxs-lookup"><span data-stu-id="0279d-132">Gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span><br/> |
| [<span data-ttu-id="0279d-133">**GetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="0279d-133">**GetEncryptionKey**</span></span>](itconnection-getencryptionkey.md)            | <span data-ttu-id="0279d-134">Obtient la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0279d-134">Gets the encryption key.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="0279d-135">**put \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="0279d-135">**put\_AddressType**</span></span>](itconnection-put-addresstype.md)             | <span data-ttu-id="0279d-136">Définit le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="0279d-136">Sets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0279d-137">**put \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="0279d-137">**put\_NetworkType**</span></span>](itconnection-put-networktype.md)             | <span data-ttu-id="0279d-138">Définit le type de réseau.</span><span class="sxs-lookup"><span data-stu-id="0279d-138">Sets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0279d-139">**SetAddressInfo**</span><span class="sxs-lookup"><span data-stu-id="0279d-139">**SetAddressInfo**</span></span>](itconnection-setaddressinfo.md)                | <span data-ttu-id="0279d-140">Définit les informations d’adresse.</span><span class="sxs-lookup"><span data-stu-id="0279d-140">Sets address information.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="0279d-141">**SetBandwidthInfo**</span><span class="sxs-lookup"><span data-stu-id="0279d-141">**SetBandwidthInfo**</span></span>](itconnection-setbandwidthinfo.md)            | <span data-ttu-id="0279d-142">Définit la valeur de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="0279d-142">Sets the bandwidth value.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="0279d-143">**SetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="0279d-143">**SetEncryptionKey**</span></span>](itconnection-setencryptionkey.md)            | <span data-ttu-id="0279d-144">Définit la clé de chiffrement nécessaire pour déchiffrer la session ou une indication à un mécanisme pour obtenir une clé utilisable par un moyen externe.</span><span class="sxs-lookup"><span data-stu-id="0279d-144">Sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="0279d-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0279d-145">Requirements</span></span>



| <span data-ttu-id="0279d-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0279d-146">Requirement</span></span> | <span data-ttu-id="0279d-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="0279d-147">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0279d-148">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="0279d-148">TAPI version</span></span><br/> | <span data-ttu-id="0279d-149">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0279d-149">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0279d-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="0279d-150">Header</span></span><br/>       | <dl> <span data-ttu-id="0279d-151"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0279d-151"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0279d-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0279d-152">Library</span></span><br/>      | <dl> <span data-ttu-id="0279d-153"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0279d-153"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0279d-154">DLL</span><span class="sxs-lookup"><span data-stu-id="0279d-154">DLL</span></span><br/>          | <dl> <span data-ttu-id="0279d-155"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0279d-155"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

