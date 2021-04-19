---
description: L’interface IX509SCEPEnrollment expose les propriétés suivantes.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: Propriétés IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520616"
---
# <a name="ix509scepenrollment-properties"></a><span data-ttu-id="3154a-103">Propriétés IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="3154a-103">IX509SCEPEnrollment Properties</span></span>

<span data-ttu-id="3154a-104">L’interface [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3154a-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3154a-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3154a-105">In this section</span></span>



| <span data-ttu-id="3154a-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3154a-106">Topic</span></span>                                                                                              | <span data-ttu-id="3154a-107">Description</span><span class="sxs-lookup"><span data-stu-id="3154a-107">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3154a-108">**Propriété du certificat**</span><span class="sxs-lookup"><span data-stu-id="3154a-108">**Certificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | <span data-ttu-id="3154a-109">Obtient le certificat pour la demande.</span><span class="sxs-lookup"><span data-stu-id="3154a-109">Gets the certificate for the request.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="3154a-110">**Propriété CertificateFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="3154a-110">**CertificateFriendlyName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | <span data-ttu-id="3154a-111">Obtient ou définit le nom convivial du certificat.</span><span class="sxs-lookup"><span data-stu-id="3154a-111">Gets or sets the friendly name for the certificate.</span></span><br/>                                                                                         |
| [<span data-ttu-id="3154a-112">**Propriété FailInfo**</span><span class="sxs-lookup"><span data-stu-id="3154a-112">**FailInfo property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | <span data-ttu-id="3154a-113">Obtient des informations lorsque la méthode [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) détecte un environnement défaillant.</span><span class="sxs-lookup"><span data-stu-id="3154a-113">Gets information when the [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) method detects a failed environment.</span></span><br/> |
| [<span data-ttu-id="3154a-114">**Propriété OldCertificate**</span><span class="sxs-lookup"><span data-stu-id="3154a-114">**OldCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | <span data-ttu-id="3154a-115">Obtient ou définit un ancien certificat qu’une demande doit remplacer.</span><span class="sxs-lookup"><span data-stu-id="3154a-115">Gets or sets an old certificate that a request is intended to replace.</span></span><br/>                                                                      |
| [<span data-ttu-id="3154a-116">**Propriété de la demande**</span><span class="sxs-lookup"><span data-stu-id="3154a-116">**Request property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | <span data-ttu-id="3154a-117">Obtient la demande interne PKCS10.</span><span class="sxs-lookup"><span data-stu-id="3154a-117">Gets the inner PKCS10 request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="3154a-118">**Propriété ServerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3154a-118">**ServerCapabilities property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | <span data-ttu-id="3154a-119">Définit les algorithmes de chiffrement et de hachage par défaut pour la demande.</span><span class="sxs-lookup"><span data-stu-id="3154a-119">Sets the preferred hash and encryption algorithms for the request.</span></span><br/>                                                                          |
| [<span data-ttu-id="3154a-120">**Propriété SignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="3154a-120">**SignerCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | <span data-ttu-id="3154a-121">Obtient ou définit le certificat de signataire pour la demande.</span><span class="sxs-lookup"><span data-stu-id="3154a-121">Gets or sets the signer certificate for the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="3154a-122">**Silent, propriété**</span><span class="sxs-lookup"><span data-stu-id="3154a-122">**Silent property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | <span data-ttu-id="3154a-123">Obtient ou définit une valeur indiquant s’il faut autoriser l’interface utilisateur pendant la requête.</span><span class="sxs-lookup"><span data-stu-id="3154a-123">Gets or sets whether to allow UI during the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="3154a-124">**Status (propriété)**</span><span class="sxs-lookup"><span data-stu-id="3154a-124">**Status property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | <span data-ttu-id="3154a-125">Obtient l’état de la demande.</span><span class="sxs-lookup"><span data-stu-id="3154a-125">Gets the status of the request.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="3154a-126">**Propriété TransactionId**</span><span class="sxs-lookup"><span data-stu-id="3154a-126">**TransactionId property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | <span data-ttu-id="3154a-127">Obtient ou définit l’ID de transaction de la demande.</span><span class="sxs-lookup"><span data-stu-id="3154a-127">Gets or sets the transaction id for the request.</span></span><br/>                                                                                            |



 

 

 




