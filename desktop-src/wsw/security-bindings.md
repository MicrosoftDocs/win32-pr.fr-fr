---
title: Liaisons de sécurité
description: Une liaison de sécurité est la spécification d’un jeton de sécurité et indique au runtime comment obtenir et utiliser un jeton de sécurité pour la sécurité du canal.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Services Web des liaisons de sécurité pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102561"
---
# <a name="security-bindings"></a><span data-ttu-id="3dad0-106">Liaisons de sécurité</span><span class="sxs-lookup"><span data-stu-id="3dad0-106">Security Bindings</span></span>

<span data-ttu-id="3dad0-107">Une liaison de sécurité est la spécification d’un jeton de sécurité et indique au runtime comment obtenir et utiliser un jeton de sécurité pour la sécurité du canal.</span><span class="sxs-lookup"><span data-stu-id="3dad0-107">A security binding is the specification of a security token, and tells the runtime how to obtain and use a security token for channel security.</span></span> <span data-ttu-id="3dad0-108">Le jeton de sécurité contient des informations sur le droit d’accéder aux ressources.</span><span class="sxs-lookup"><span data-stu-id="3dad0-108">The security token contains information that vouches for the right to access resources.</span></span> <span data-ttu-id="3dad0-109">Elle peut également avoir une clé de chiffrement associée pour effectuer des signatures et un chiffrement.</span><span class="sxs-lookup"><span data-stu-id="3dad0-109">It may also have an associated cryptographic key for performing signatures and encryption.</span></span>


<span data-ttu-id="3dad0-110">Chaque liaison de sécurité contient sa propre collection de [paramètres de liaison de sécurité](security-binding-settings.md) facultatifs qui sont étendus au jeton de sécurité qu’elle définit.</span><span class="sxs-lookup"><span data-stu-id="3dad0-110">Each security binding contains its own collection of optional [security binding settings](security-binding-settings.md) that are scoped to the security token it defines.</span></span> <span data-ttu-id="3dad0-111">Il contient également des [informations d’identification de sécurité](security-credentials.md), qui représentent les preuves de sécurité (telles que le nom d’utilisateur et les mots de passe ou les certificats) nécessaires à la création de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3dad0-111">It also contains [security credentials](security-credentials.md), representing the security evidence (such as username and passwords, or certificates) needed to create security tokens.</span></span>

<span data-ttu-id="3dad0-112">Les rappels suivants font partie de la liaison de sécurité :</span><span class="sxs-lookup"><span data-stu-id="3dad0-112">The following callbacks are part of the security binding:</span></span>

-   [<span data-ttu-id="3dad0-113">**\_validation du \_ rappel SAML WS Validate \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-113">**WS\_VALIDATE\_SAML\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

<span data-ttu-id="3dad0-114">Les énumérations suivantes font partie de la liaison de sécurité :</span><span class="sxs-lookup"><span data-stu-id="3dad0-114">The following enumerations are part of the security binding:</span></span>

-   [<span data-ttu-id="3dad0-115">**utilisation de la \_ sécurité WS message \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-115">**WS\_MESSAGE\_SECURITY\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [<span data-ttu-id="3dad0-116">**TYPE d’authentificateur de WS \_ SAML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-116">**WS\_SAML\_AUTHENTICATOR\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [<span data-ttu-id="3dad0-117">**\_type de \_ liaison de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-117">**WS\_SECURITY\_BINDING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [<span data-ttu-id="3dad0-118">**\_type de \_ handle de clé de sécurité WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-118">**WS\_SECURITY\_KEY\_HANDLE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

<span data-ttu-id="3dad0-119">Les fonctions suivantes font partie de la liaison de sécurité :</span><span class="sxs-lookup"><span data-stu-id="3dad0-119">The following functions are part of the security binding:</span></span>

-   [<span data-ttu-id="3dad0-120">**WsCreateXmlSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="3dad0-120">**WsCreateXmlSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [<span data-ttu-id="3dad0-121">**WsFreeSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="3dad0-121">**WsFreeSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

<span data-ttu-id="3dad0-122">Les structures suivantes font partie de la liaison de sécurité :</span><span class="sxs-lookup"><span data-stu-id="3dad0-122">The following structures are part of the security binding:</span></span>

-   [<span data-ttu-id="3dad0-123">**\_handle de \_ \_ clé de sécurité asymétrique WS CAPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-123">**WS\_CAPI\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [<span data-ttu-id="3dad0-124">**\_ \_ \_ AUTHENTIFICATEUR SAML signé WS \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="3dad0-124">**WS\_CERT\_SIGNED\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [<span data-ttu-id="3dad0-125">**\_liaison de \_ sécurité d’authentification d’en-tête WS http \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-125">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [<span data-ttu-id="3dad0-126">**\_liaison de \_ \_ sécurité de message WS Kerberos APREQ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-126">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [<span data-ttu-id="3dad0-127">**\_liaison de \_ \_ sécurité de transport SSPI WS NAMEDPIPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-127">**WS\_NAMEDPIPE\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="3dad0-128">**\_handle de \_ \_ clé de sécurité asymétrique WS NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-128">**WS\_NCRYPT\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [<span data-ttu-id="3dad0-129">**\_handle de \_ \_ clé de sécurité symétrique WS brut \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-129">**WS\_RAW\_SYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [<span data-ttu-id="3dad0-130">**\_authentificateur SAML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="3dad0-130">**WS\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [<span data-ttu-id="3dad0-131">**\_liaison de \_ sécurité de message WS SAML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-131">**WS\_SAML\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [<span data-ttu-id="3dad0-132">**\_liaison de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-132">**WS\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [<span data-ttu-id="3dad0-133">**\_liaison de \_ sécurité de message de contexte de sécurité WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-133">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [<span data-ttu-id="3dad0-134">**\_handle de \_ clé de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-134">**WS\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [<span data-ttu-id="3dad0-135">**\_liaison de \_ sécurité de transport WS SSL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-135">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [<span data-ttu-id="3dad0-136">**liaison de sécurité de transport de WS \_ TCP \_ SSPI \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-136">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [<span data-ttu-id="3dad0-137">**\_liaison de \_ sécurité de message WS username \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-137">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [<span data-ttu-id="3dad0-138">**\_liaison de \_ \_ sécurité de message de jeton XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="3dad0-138">**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




