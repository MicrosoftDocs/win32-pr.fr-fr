---
title: Transfert de données entre le demandeur et les méthodes EAP
description: En savoir plus sur le transfert de données entre le demandeur et les méthodes EAP. Le transfert de données entre méthodes s’effectue à l’aide d’attributs EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382883"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a><span data-ttu-id="54bfd-104">Transfert de données entre le demandeur et les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="54bfd-104">Transferring Data Between the Supplicant and EAP Methods</span></span>

<span data-ttu-id="54bfd-105">L’utilisation d’attributs EAP permet d’échanger des données entre les demandeurs et les méthodes EAP.</span><span class="sxs-lookup"><span data-stu-id="54bfd-105">Using EAP attributes allows data to be exchanged between supplicants and EAP methods.</span></span>

## <a name="attribute-consumption"></a><span data-ttu-id="54bfd-106">Consommation d’attribut</span><span class="sxs-lookup"><span data-stu-id="54bfd-106">Attribute Consumption</span></span>

<span data-ttu-id="54bfd-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consomme les attributs EAP transmis directement à la méthode EAP configurée.</span><span class="sxs-lookup"><span data-stu-id="54bfd-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consumes EAP attributes that are passed directly to the configured EAP method.</span></span> <span data-ttu-id="54bfd-108">De même, les méthodes EAP sont gratuites pour retourner un code d’action qui indique au demandeur que les attributs sont disponibles et qu’il doit collecter les attributs à l’aide de [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="54bfd-108">Similarly, EAP methods are free to return an action code that indicates to the supplicant that attributes are available and that it should collect the attributes using [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span></span>

<span data-ttu-id="54bfd-109">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="54bfd-109">For more information, see the following topics.</span></span>

-   <span data-ttu-id="54bfd-110">[Codes d’action du demandeur d’homologue EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="54bfd-110">[EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="54bfd-111">[Codes de raison du demandeur d’homologue EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span><span class="sxs-lookup"><span data-stu-id="54bfd-111">[EAP Peer Supplicant Reason Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span></span>
-   <span data-ttu-id="54bfd-112">[Codes d’action de la méthode d’authentificateur EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span><span class="sxs-lookup"><span data-stu-id="54bfd-112">[EAP Authenticator Method Action Codes](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span></span>

<span data-ttu-id="54bfd-113">Les demandeurs sont censés ignorer les attributs qu’ils ne reconnaissent pas ou ne peuvent pas agir.</span><span class="sxs-lookup"><span data-stu-id="54bfd-113">Supplicants are expected to ignore attributes that they do not recognize or cannot act upon.</span></span> <span data-ttu-id="54bfd-114">À l’aide de [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) , ces attributs ignorés sont renvoyés à EAPHost et à la méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="54bfd-114">Using [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) these ignored attributes are sent back to EAPHost and the EAP method.</span></span>

## <a name="vendor-specific-attributes"></a><span data-ttu-id="54bfd-115">Attributs spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="54bfd-115">Vendor Specific Attributes</span></span>

<span data-ttu-id="54bfd-116">À l’aide de l’attribut EAP spécifique au fournisseur, les méthodes et les demandeurs EAP peuvent intervenir dans l’échange de données à des fins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="54bfd-116">By using the vendor-specific EAP attribute, EAP methods and supplicants can engage in data exchange for a specific purpose.</span></span> <span data-ttu-id="54bfd-117">Les attributs spécifiques au fournisseur sont ignorés par les demandeurs et les méthodes qui ne prennent pas en charge l’attribut propre au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="54bfd-117">Vendor-specific attributes are ignored by supplicants and methods that do not support the vendor-specific attribute.</span></span>

<span data-ttu-id="54bfd-118">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="54bfd-118">For more information, see the following topics.</span></span>

-   <span data-ttu-id="54bfd-119">[Attributs EAP](about-eap-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="54bfd-119">[EAP Attributes](about-eap-attributes.md).</span></span>
-   <span data-ttu-id="54bfd-120">[**Protocole EAP \_ \_type d’attribut**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="54bfd-120">[**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54bfd-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54bfd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54bfd-122">Configuration de l’interface utilisateur de la méthode EAP</span><span class="sxs-lookup"><span data-stu-id="54bfd-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="54bfd-123">Activation de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="54bfd-123">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="54bfd-124">Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="54bfd-124">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="54bfd-125">Implémentation de la prise en charge NAP pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="54bfd-125">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="54bfd-126">Demandeurs EAPHost</span><span class="sxs-lookup"><span data-stu-id="54bfd-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




