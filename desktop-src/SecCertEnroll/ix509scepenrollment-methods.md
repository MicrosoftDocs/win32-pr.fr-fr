---
description: L’interface IX509SCEPEnrollment expose les méthodes suivantes.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Méthodes IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533982"
---
# <a name="ix509scepenrollment-methods"></a><span data-ttu-id="d4cd6-103">Méthodes IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="d4cd6-103">IX509SCEPEnrollment Methods</span></span>

<span data-ttu-id="d4cd6-104">L’interface [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4cd6-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4cd6-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d4cd6-105">In this section</span></span>



| <span data-ttu-id="d4cd6-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d4cd6-106">Topic</span></span>                                                                                                              | <span data-ttu-id="d4cd6-107">Description</span><span class="sxs-lookup"><span data-stu-id="d4cd6-107">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4cd6-108">**Méthode CreateRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="d4cd6-108">**CreateRequestMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | <span data-ttu-id="d4cd6-109">Créez un message de demande PKCS10 avec un mot de passe de stimulation.</span><span class="sxs-lookup"><span data-stu-id="d4cd6-109">Create a PKCS10 request message with a challenge password.</span></span> <span data-ttu-id="d4cd6-110">Le message de demande se trouve dans un PKCS7 enveloppé chiffré avec le certificat de chiffrement de serveur SCEP et signé par le certificat de signature du serveur.</span><span class="sxs-lookup"><span data-stu-id="d4cd6-110">The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.</span></span><br/> |
| [<span data-ttu-id="d4cd6-111">**Méthode CreateRetrieveCertificateMessage**</span><span class="sxs-lookup"><span data-stu-id="d4cd6-111">**CreateRetrieveCertificateMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | <span data-ttu-id="d4cd6-112">Récupérez un certificat émis précédemment.</span><span class="sxs-lookup"><span data-stu-id="d4cd6-112">Retrieve a previously issued certificate.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="d4cd6-113">**Méthode CreateRetrievePendingMessage**</span><span class="sxs-lookup"><span data-stu-id="d4cd6-113">**CreateRetrievePendingMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | <span data-ttu-id="d4cd6-114">Créez un message pour l’interrogation de certificat (inscription manuelle).</span><span class="sxs-lookup"><span data-stu-id="d4cd6-114">Create a message for certificate polling (manual enrollment).</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="d4cd6-115">**Méthode DeleteRequest**</span><span class="sxs-lookup"><span data-stu-id="d4cd6-115">**DeleteRequest method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | <span data-ttu-id="d4cd6-116">Supprimez les certificats ou les clés créés pour la demande.</span><span class="sxs-lookup"><span data-stu-id="d4cd6-116">Delete any certificates or keys created for the request.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="d4cd6-117">**Initialize (méthode)**</span><span class="sxs-lookup"><span data-stu-id="d4cd6-117">**Initialize method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | <span data-ttu-id="d4cd6-118">Initialisez l’instance en vue d’une nouvelle demande.</span><span class="sxs-lookup"><span data-stu-id="d4cd6-118">Initialize the instance in preparation for a new request.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="d4cd6-119">**Méthode InitializeForPending**</span><span class="sxs-lookup"><span data-stu-id="d4cd6-119">**InitializeForPending method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | <span data-ttu-id="d4cd6-120">Initialisez l’instance pour préparer la génération d’un message pour récupérer un certificat émis ou installez une réponse pour une demande précédente de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="d4cd6-120">Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.</span></span><br/>                                              |
| [<span data-ttu-id="d4cd6-121">**Méthode ProcessResponseMessage**</span><span class="sxs-lookup"><span data-stu-id="d4cd6-121">**ProcessResponseMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | <span data-ttu-id="d4cd6-122">Traite un message de réponse et retourne la disposition du message.</span><span class="sxs-lookup"><span data-stu-id="d4cd6-122">Process a response message and return the disposition of the message.</span></span><br/>                                                                                                                                       |



 

 

 




