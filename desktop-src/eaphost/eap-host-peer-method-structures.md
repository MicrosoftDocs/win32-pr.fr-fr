---
title: Structures de méthode homologue EAPHost
description: En savoir plus sur les structures d’API de méthode homologue EAPHost, telles que EapCertificateCredential et EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509680"
---
# <a name="eaphost-peer-method-structures"></a><span data-ttu-id="1c52d-103">Structures de méthode homologue EAPHost</span><span class="sxs-lookup"><span data-stu-id="1c52d-103">EAPHost Peer Method Structures</span></span>

<span data-ttu-id="1c52d-104">Les structures de l’API de méthode homologue EAPHost sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="1c52d-104">The EAPHost Peer Method API structures are as follows.</span></span>



| <span data-ttu-id="1c52d-105">Structure</span><span class="sxs-lookup"><span data-stu-id="1c52d-105">Structure</span></span>                                                              | <span data-ttu-id="1c52d-106">Description</span><span class="sxs-lookup"><span data-stu-id="1c52d-106">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c52d-107">**EapCertificateCredential**</span><span class="sxs-lookup"><span data-stu-id="1c52d-107">**EapCertificateCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | <span data-ttu-id="1c52d-108">Contient des informations sur le certificat utilisé par la méthode EAP pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="1c52d-108">Contains information about the certificate that the EAP method uses for authentication.</span></span>                                                                                                            |
| [<span data-ttu-id="1c52d-109">**EapCredential**</span><span class="sxs-lookup"><span data-stu-id="1c52d-109">**EapCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | <span data-ttu-id="1c52d-110">Contient des informations sur le type d’informations d’identification et les informations d’identification appropriées.</span><span class="sxs-lookup"><span data-stu-id="1c52d-110">Contains information about the credentials type and the appropriate credentials.</span></span> <span data-ttu-id="1c52d-111">Cette valeur est transmise en tant qu’entrée à l’API [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) .</span><span class="sxs-lookup"><span data-stu-id="1c52d-111">This is passed as an input to the [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) API.</span></span> |
| [<span data-ttu-id="1c52d-112">**\_ \_ routines de méthode HOMOLOGUe EAP \_**</span><span class="sxs-lookup"><span data-stu-id="1c52d-112">**EAP\_PEER\_METHOD\_ROUTINES**</span></span>](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | <span data-ttu-id="1c52d-113">Contient un ensemble de pointeurs fonction vers les API de méthode homologue EAPHost.</span><span class="sxs-lookup"><span data-stu-id="1c52d-113">Contains a set of function pointers to the EAPHost Peer Method APIs.</span></span>                                                                                                                               |
| [<span data-ttu-id="1c52d-114">**EapPeerMethodOutput**</span><span class="sxs-lookup"><span data-stu-id="1c52d-114">**EapPeerMethodOutput**</span></span>](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | <span data-ttu-id="1c52d-115">Contient les informations d’action retournées par une méthode homologue EAP.</span><span class="sxs-lookup"><span data-stu-id="1c52d-115">Contains the action information returned by an EAP peer method.</span></span>                                                                                                                                    |
| [<span data-ttu-id="1c52d-116">**EapPeerMethodResult**</span><span class="sxs-lookup"><span data-stu-id="1c52d-116">**EapPeerMethodResult**</span></span>](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | <span data-ttu-id="1c52d-117">Contient les données de résultat générées par une méthode EAP lors de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="1c52d-117">Contains result data generated by an EAP method during authentication.</span></span>                                                                                                                             |
| [<span data-ttu-id="1c52d-118">**EapSimCredential**</span><span class="sxs-lookup"><span data-stu-id="1c52d-118">**EapSimCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | <span data-ttu-id="1c52d-119">Contient des informations sur la carte SIM qui est utilisée par la méthode EAP pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="1c52d-119">Contains information about the SIM that is used by the EAP method for authentication.</span></span>                                                                                                              |
| [<span data-ttu-id="1c52d-120">**EapUsernamePasswordCredential**</span><span class="sxs-lookup"><span data-stu-id="1c52d-120">**EapUsernamePasswordCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | <span data-ttu-id="1c52d-121">Contient le nom d’utilisateur et le mot de passe utilisés par la méthode EAP pour authentifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c52d-121">Contains the username and password that is used by the EAP method for authenticating the user.</span></span>                                                                                                     |



 

 

 




