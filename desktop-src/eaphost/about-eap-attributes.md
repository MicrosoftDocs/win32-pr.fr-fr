---
title: Attributs EAP
description: Est une \_ structure d’attribut EAP qui contient un type de données prédéterminé relatif à une session d’authentification.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "106512348"
---
# <a name="eap-attributes"></a><span data-ttu-id="a1c39-103">Attributs EAP</span><span class="sxs-lookup"><span data-stu-id="a1c39-103">EAP Attributes</span></span>

<span data-ttu-id="a1c39-104">Un attribut EAP est une structure d' [**\_ attributs EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) qui contient un type de données prédéterminé relatif à une session d’authentification.</span><span class="sxs-lookup"><span data-stu-id="a1c39-104">An EAP attribute is an [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure that contains a predetermined type of data relating to an authentication session.</span></span> <span data-ttu-id="a1c39-105">Les attributs sont utilisés pour communiquer des informations entre les méthodes EAP et les demandeurs ou entre les méthodes et les authentificateurs EAP.</span><span class="sxs-lookup"><span data-stu-id="a1c39-105">Attributes are used to communicate information between EAP methods and supplicants or between EAP methods and authenticators.</span></span> <span data-ttu-id="a1c39-106">Les implémentations d’homologue et d’authentificateur d’une méthode EAP peuvent échanger ces attributs sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="a1c39-106">Peer and authenticator implementations of an EAP method may exchange these attributes over a network.</span></span>

<span data-ttu-id="a1c39-107">La liste complète des types d’attributs pris en charge s’affiche dans la rubrique [**\_ \_ type d’attribut EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="a1c39-107">A complete list of supported attribute types appears in the topic [**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="attributes-consumed-by-supplicants"></a><span data-ttu-id="a1c39-108">Attributs consommés par les demandeurs</span><span class="sxs-lookup"><span data-stu-id="a1c39-108">Attributes Consumed by Supplicants</span></span>

<span data-ttu-id="a1c39-109">Les types d’attributs suivants sont consommés par les demandeurs 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="a1c39-109">The following attribute types are consumed by 802.1X supplicants.</span></span>

-   <span data-ttu-id="a1c39-110">**eatVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="a1c39-110">**eatVendorSpecific**</span></span>

<span data-ttu-id="a1c39-111">Les types d’attributs suivants sont consommés par les demandeurs clients PPP.</span><span class="sxs-lookup"><span data-stu-id="a1c39-111">The following attribute types are consumed by PPP client supplicants.</span></span>

-   <span data-ttu-id="a1c39-112">**eatMinimum**</span><span class="sxs-lookup"><span data-stu-id="a1c39-112">**eatMinimum**</span></span>
-   <span data-ttu-id="a1c39-113">**eatEAPTLV**</span><span class="sxs-lookup"><span data-stu-id="a1c39-113">**eatEAPTLV**</span></span>

<span data-ttu-id="a1c39-114">Les types d’attributs suivants sont consommés par les demandeurs de serveur PPP.</span><span class="sxs-lookup"><span data-stu-id="a1c39-114">The following attribute types are consumed by PPP server supplicants.</span></span>

-   <span data-ttu-id="a1c39-115">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="a1c39-115">**eatUserName**</span></span>
-   <span data-ttu-id="a1c39-116">**eatReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="a1c39-116">**eatReplyMessage**</span></span>
-   <span data-ttu-id="a1c39-117">**eatState**</span><span class="sxs-lookup"><span data-stu-id="a1c39-117">**eatState**</span></span>
-   <span data-ttu-id="a1c39-118">**eatSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="a1c39-118">**eatSessionTimeout**</span></span>
-   <span data-ttu-id="a1c39-119">**eatEAPMessage**</span><span class="sxs-lookup"><span data-stu-id="a1c39-119">**eatEAPMessage**</span></span>

## <a name="attributes-exported-by-methods"></a><span data-ttu-id="a1c39-120">Attributs exportés par des méthodes</span><span class="sxs-lookup"><span data-stu-id="a1c39-120">Attributes Exported by Methods</span></span>

<span data-ttu-id="a1c39-121">Les types d’attributs suivants peuvent être exportés par les méthodes EAP.</span><span class="sxs-lookup"><span data-stu-id="a1c39-121">The following attribute types could be exported by EAP methods.</span></span>

-   <span data-ttu-id="a1c39-122">**eatClearTextPassword**</span><span class="sxs-lookup"><span data-stu-id="a1c39-122">**eatClearTextPassword**</span></span>
-   <span data-ttu-id="a1c39-123">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="a1c39-123">**eatQuarantineSoH**</span></span>
-   <span data-ttu-id="a1c39-124">**eatMethodId**</span><span class="sxs-lookup"><span data-stu-id="a1c39-124">**eatMethodId**</span></span>

<span data-ttu-id="a1c39-125">Le type d’attribut suivant est exporté par les méthodes TLS (EAP [Transport Level Security)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS).</span><span class="sxs-lookup"><span data-stu-id="a1c39-125">The following attribute type is exported by EAP [Transport Level Security (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) methods.</span></span>

-   <span data-ttu-id="a1c39-126">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="a1c39-126">**eatCertificateOID**</span></span>

<span data-ttu-id="a1c39-127">Les types d’attributs suivants sont exportés par les méthodes [Microsoft Challenge Handshake Authentication Protocol version 2,0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2).</span><span class="sxs-lookup"><span data-stu-id="a1c39-127">The following attribute types are exported by [Microsoft Challenge Handshake Authentication Protocol version 2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2) methods.</span></span>

-   <span data-ttu-id="a1c39-128">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="a1c39-128">**eatUserName**</span></span>
-   <span data-ttu-id="a1c39-129">**eatCredentialsChanged**</span><span class="sxs-lookup"><span data-stu-id="a1c39-129">**eatCredentialsChanged**</span></span>

<span data-ttu-id="a1c39-130">Le type d’attribut suivant est consommé par le serveur NPS (Network Policy Server).</span><span class="sxs-lookup"><span data-stu-id="a1c39-130">The following attribute type is consumed by Network Policy Server (NPS).</span></span>

-   <span data-ttu-id="a1c39-131">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="a1c39-131">**eatCertificateOID**</span></span>

<span data-ttu-id="a1c39-132">Les types d’attributs suivants sont exportés par les méthodes [PEAP (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a1c39-132">The following attribute types are exported by [Protected Extensible Authentication Protocol (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) methods.</span></span>

-   <span data-ttu-id="a1c39-133">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="a1c39-133">**eatUserName**</span></span>
-   <span data-ttu-id="a1c39-134">**eatPEAPEmbeddedEAPTypeId**</span><span class="sxs-lookup"><span data-stu-id="a1c39-134">**eatPEAPEmbeddedEAPTypeId**</span></span>
-   <span data-ttu-id="a1c39-135">**eatPEAPFastRoamedSession**</span><span class="sxs-lookup"><span data-stu-id="a1c39-135">**eatPEAPFastRoamedSession**</span></span>
-   <span data-ttu-id="a1c39-136">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="a1c39-136">**eatQuarantineSoH**</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1c39-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1c39-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1c39-138">**\_attribut EAP**</span><span class="sxs-lookup"><span data-stu-id="a1c39-138">**EAP\_ATTRIBUTE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[<span data-ttu-id="a1c39-139">**\_type d’attribut EAP \_**</span><span class="sxs-lookup"><span data-stu-id="a1c39-139">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 