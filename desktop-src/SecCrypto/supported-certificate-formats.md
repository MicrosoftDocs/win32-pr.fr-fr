---
description: Répertorie les formats de certificat pris en charge par les services de certificats.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Formats de certificat pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f37f3e4c29ae765f68484aecf0bf9d9b8aea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524680"
---
# <a name="supported-certificate-formats"></a><span data-ttu-id="9b74b-103">Formats de certificat pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b74b-103">Supported Certificate Formats</span></span>

<span data-ttu-id="9b74b-104">Les services de certificats peuvent émettre les types de certificats suivants.</span><span class="sxs-lookup"><span data-stu-id="9b74b-104">Certificate Services can issue the following types of certificates.</span></span>



| <span data-ttu-id="9b74b-105">Terme</span><span class="sxs-lookup"><span data-stu-id="9b74b-105">Term</span></span>                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="9b74b-106">Description</span><span class="sxs-lookup"><span data-stu-id="9b74b-106">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b74b-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X. 509*](../secgloss/x-gly.md) version 3 certificat d’authentification client compatible SSL</span><span class="sxs-lookup"><span data-stu-id="9b74b-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) version 3 SSL-compatible client authentication certificate</span></span><br/> | <span data-ttu-id="9b74b-108">Ce certificat d’authentification client identifie un client et est utilisé par les serveurs pour authentifier un client qui demande l’accès au serveur.</span><span class="sxs-lookup"><span data-stu-id="9b74b-108">This client authentication certificate identifies a client and is used by servers to authenticate a client that requests server access.</span></span><br/>     |
| <span data-ttu-id="9b74b-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificat d’authentification serveur compatible SSL X. 509 v3</span><span class="sxs-lookup"><span data-stu-id="9b74b-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL-compatible server authentication certificate</span></span><br/>                                                                                         | <span data-ttu-id="9b74b-110">Ce certificat d’authentification serveur identifie un serveur et est utilisé par les clients pour authentifier un serveur auquel le client souhaite accéder.</span><span class="sxs-lookup"><span data-stu-id="9b74b-110">This server authentication certificate identifies a server and is used by clients to authenticate a server that the client wants to access.</span></span><br/> |
| <span data-ttu-id="9b74b-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Certificat [*S/MIME*](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="9b74b-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) certificate</span></span><br/>                                                                                                           | <span data-ttu-id="9b74b-112">Ce certificat est utilisé par les clients pour la messagerie sécurisée sous le protocole S/MIME (Secure/Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="9b74b-112">This certificate is used by clients for secure email under the S/MIME (Secure/Multipurpose Internet Mail Extensions) protocol.</span></span><br/>              |



 

<span data-ttu-id="9b74b-113">En plus de ces certificats, vous pouvez également utiliser les services de certificats pour émettre d’autres certificats X. 509 en écrivant un module de stratégie personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9b74b-113">In addition to these certificates, Certificate Services can also be used to issue other X.509 certificates by writing a custom policy module.</span></span>

> [!Note]  
> <span data-ttu-id="9b74b-114">« Certificat d’authentification de serveur » et « certificat de serveur » ainsi que « certificat d’authentification client » et « certificat client » sont des termes interchangeables.</span><span class="sxs-lookup"><span data-stu-id="9b74b-114">"Server authentication certificate" and "server certificate" as well as "client authentication certificate" and "client certificate" are interchangeable terms.</span></span>

 

<span data-ttu-id="9b74b-115">En outre, les services de certificats incluent des modèles de certificats dans la configuration de l’autorité de certification d’entreprise Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9b74b-115">Additionally, Certificate Services includes certificate templates in the Microsoft enterprise certification authority configuration.</span></span> <span data-ttu-id="9b74b-116">Consultez la documentation de l’aide de Windows pour les modèles de certificats pour comprendre comment ils définissent les rôles du certificat.</span><span class="sxs-lookup"><span data-stu-id="9b74b-116">Consult the Windows Help documentation for certificate templates to understand how they define certificate purposes.</span></span>

 

 
