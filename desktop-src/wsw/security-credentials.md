---
title: Informations d'identification de sécurité
description: Les informations d’identification de sécurité sont un élément de preuve qu’une partie communicante possède qui peut être utilisée pour créer ou obtenir un jeton de sécurité.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Services Web des informations d’identification de sécurité pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106511916"
---
# <a name="security-credentials"></a><span data-ttu-id="605e0-106">Informations d'identification de sécurité</span><span class="sxs-lookup"><span data-stu-id="605e0-106">Security Credentials</span></span>

<span data-ttu-id="605e0-107">Les informations d’identification de sécurité sont un élément de preuve qu’une partie communicante possède qui peut être utilisée pour créer ou obtenir un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="605e0-107">Security credentials are a piece of evidence that a communicating party possesses that can be used to create or obtain a security token.</span></span> <span data-ttu-id="605e0-108">Ainsi, les informations d’identification sont généralement plus longues que les jetons de sécurité, et un jeton de sécurité peut être affiché en tant que manifeste d’exécution des informations d’identification de sécurité.</span><span class="sxs-lookup"><span data-stu-id="605e0-108">Thus, credentials are typically longer-lived than security tokens, and a security token can be viewed as the runtime manifestation of the security credentials.</span></span> <span data-ttu-id="605e0-109">Voici un exemple d’informations d’identification : un certificat d’ordinateur (qui peut être converti en un jeton de sécurité X. 509 au moment de l’exécution) ou une paire nom d’utilisateur/mot de passe pour un domaine (qui peut être utilisé pour obtenir un jeton de sécurité Kerberos).</span><span class="sxs-lookup"><span data-stu-id="605e0-109">Example of credentials include a machine certificate (which can be converted into an X.509 security token at runtime) or a username/password pair for a domain (which can be used to obtain a Kerberos security token).</span></span>


<span data-ttu-id="605e0-110">Les informations d’identification sont spécifiées dans le cadre des [liaisons de sécurité](security-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="605e0-110">Credentials are specified as part of the [security bindings](security-bindings.md).</span></span>

<span data-ttu-id="605e0-111">Les éléments d’API suivants sont utilisés avec les informations d’identification de sécurité.</span><span class="sxs-lookup"><span data-stu-id="605e0-111">The following API elements are used with security credentials.</span></span>

| <span data-ttu-id="605e0-112">Rappel</span><span class="sxs-lookup"><span data-stu-id="605e0-112">Callback</span></span>                                                                  | <span data-ttu-id="605e0-113">Description</span><span class="sxs-lookup"><span data-stu-id="605e0-113">Description</span></span>                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="605e0-114">**le \_ \_ rappel du certificat \_ WS**</span><span class="sxs-lookup"><span data-stu-id="605e0-114">**WS\_GET\_CERT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | <span data-ttu-id="605e0-115">Fournit un certificat au runtime de sécurité.</span><span class="sxs-lookup"><span data-stu-id="605e0-115">Provides a certificate to the security runtime.</span></span>          |
| [<span data-ttu-id="605e0-116">**le \_ \_ rappel de mot de passe WS Validate \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-116">**WS\_VALIDATE\_PASSWORD\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | <span data-ttu-id="605e0-117">Valide une paire nom d’utilisateur/mot de passe côté récepteur.</span><span class="sxs-lookup"><span data-stu-id="605e0-117">Validates a username/password pair on the receiver side.</span></span> |



 



| <span data-ttu-id="605e0-118">Énumération</span><span class="sxs-lookup"><span data-stu-id="605e0-118">Enumeration</span></span>                                                                                           | <span data-ttu-id="605e0-119">Description</span><span class="sxs-lookup"><span data-stu-id="605e0-119">Description</span></span>                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="605e0-120">**\_ \_ type d’informations d’identification WS CERT \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-120">**WS\_CERT\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | <span data-ttu-id="605e0-121">Type des informations d’identification du certificat.</span><span class="sxs-lookup"><span data-stu-id="605e0-121">The type of the certificate credential.</span></span>                       |
| [<span data-ttu-id="605e0-122">**\_ \_ type d’informations d’identification WS username \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-122">**WS\_USERNAME\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | <span data-ttu-id="605e0-123">Type des informations d’identification du nom d’utilisateur/mot de passe.</span><span class="sxs-lookup"><span data-stu-id="605e0-123">The type of the username/password credential.</span></span>                 |
| [<span data-ttu-id="605e0-124">**\_ \_ \_ \_ type d’informations d’identification de l’authentification intégrée WS Windows \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-124">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | <span data-ttu-id="605e0-125">Type des informations d’identification de l’authentification intégrée de Windows.</span><span class="sxs-lookup"><span data-stu-id="605e0-125">The type of the Windows Integrated Authentication credential.</span></span> |



 



| <span data-ttu-id="605e0-126">Structure</span><span class="sxs-lookup"><span data-stu-id="605e0-126">Structure</span></span>                                                                                                   | <span data-ttu-id="605e0-127">Description</span><span class="sxs-lookup"><span data-stu-id="605e0-127">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="605e0-128">**\_ \_ informations d’identification WS CERT**</span><span class="sxs-lookup"><span data-stu-id="605e0-128">**WS\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | <span data-ttu-id="605e0-129">Type de base abstrait pour tous les types d’informations d’identification de certificat.</span><span class="sxs-lookup"><span data-stu-id="605e0-129">The abstract base type for all certificate credential types.</span></span>                                                          |
| [<span data-ttu-id="605e0-130">**\_ \_ informations d’identification du certificat personnalisé WS \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-130">**WS\_CUSTOM\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | <span data-ttu-id="605e0-131">Type pour spécifier les informations d’identification de certificat qui doivent être fournies par un rappel à l’application.</span><span class="sxs-lookup"><span data-stu-id="605e0-131">The type for specifying a certificate credential that is to be supplied by a callback to the application.</span></span>             |
| [<span data-ttu-id="605e0-132">**\_ \_ \_ \_ informations d’identification de l’authentification intégrée Windows WS par défaut \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-132">**WS\_DEFAULT\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | <span data-ttu-id="605e0-133">Type permettant de fournir des informations d’identification d’authentification intégrée à Windows en fonction du jeton de thread actuel.</span><span class="sxs-lookup"><span data-stu-id="605e0-133">Type for supplying a Windows Integrated Authentication credential based on the current thread token.</span></span>                  |
| [<span data-ttu-id="605e0-134">**\_ \_ \_ \_ informations d’identification de l’authentification intégrée Windows WS opaque \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-134">**WS\_OPAQUE\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | <span data-ttu-id="605e0-135">Type pour fournir les informations d’identification d’authentification intégrée de Windows.</span><span class="sxs-lookup"><span data-stu-id="605e0-135">Type for supplying a Windows Integrated Authentication credential.</span></span>                                                    |
| [<span data-ttu-id="605e0-136">**\_ \_ informations d’identification du nom d’utilisateur WS String \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-136">**WS\_STRING\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | <span data-ttu-id="605e0-137">Type pour fournir une paire nom d’utilisateur/mot de passe sous forme de chaînes.</span><span class="sxs-lookup"><span data-stu-id="605e0-137">The type for supplying a username/password pair as strings.</span></span>                                                           |
| [<span data-ttu-id="605e0-138">**\_ \_ \_ \_ \_ informations d’identification d’authentification intégrée Windows WS String**</span><span class="sxs-lookup"><span data-stu-id="605e0-138">**WS\_STRING\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | <span data-ttu-id="605e0-139">Type pour fournir des informations d’identification Windows sous la forme d’un nom d’utilisateur, d’un mot de passe et de chaînes de domaine</span><span class="sxs-lookup"><span data-stu-id="605e0-139">Type for supplying a Windows credential as username, password, domain strings.</span></span>                                        |
| [<span data-ttu-id="605e0-140">**\_ \_ \_ informations d’identification du certificat WS subject name \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-140">**WS\_SUBJECT\_NAME\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | <span data-ttu-id="605e0-141">Type pour la spécification d’informations d’identification de certificat à l’aide du nom d’objet du certificat, de l’emplacement du magasin et du nom du magasin.</span><span class="sxs-lookup"><span data-stu-id="605e0-141">The type for specifying a certificate credential using the certificate's subject name, store location and store name.</span></span> |
| [<span data-ttu-id="605e0-142">**\_ \_ informations d’identification du certificat WS empreinte \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-142">**WS\_THUMBPRINT\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | <span data-ttu-id="605e0-143">Type permettant de spécifier des informations d’identification de certificat à l’aide de l’empreinte numérique du certificat, de l’emplacement du magasin et du nom du magasin.</span><span class="sxs-lookup"><span data-stu-id="605e0-143">The type for specifying a certificate credential using the certificate's thumbprint, store location and store name.</span></span>   |
| [<span data-ttu-id="605e0-144">**\_ \_ informations d’identification WS username**</span><span class="sxs-lookup"><span data-stu-id="605e0-144">**WS\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | <span data-ttu-id="605e0-145">Type de base abstrait pour toutes les informations d’identification de nom d’utilisateur/mot de passe.</span><span class="sxs-lookup"><span data-stu-id="605e0-145">The abstract base type for all username/password credentials.</span></span>                                                         |
| [<span data-ttu-id="605e0-146">**\_ \_ \_ informations d’identification de l’authentification intégrée WS Windows \_**</span><span class="sxs-lookup"><span data-stu-id="605e0-146">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | <span data-ttu-id="605e0-147">Type de base abstrait pour tous les types d’informations d’identification utilisés avec l’authentification intégrée de Windows.</span><span class="sxs-lookup"><span data-stu-id="605e0-147">The abstract base type for all credential types used with Windows Integrated Authentication.</span></span>                          |



 

 

 




