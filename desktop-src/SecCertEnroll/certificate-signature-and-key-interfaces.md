---
description: Les interfaces suivantes peuvent être utilisées pour gérer des signatures de certificat et des clés publiques et privées.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Signature de certificat et interfaces clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866670"
---
# <a name="certificate-signature-and-key-interfaces"></a><span data-ttu-id="ef94c-103">Signature de certificat et interfaces clés</span><span class="sxs-lookup"><span data-stu-id="ef94c-103">Certificate Signature and Key Interfaces</span></span>

<span data-ttu-id="ef94c-104">Les interfaces suivantes peuvent être utilisées pour gérer des signatures de certificat et des clés publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="ef94c-104">The following interfaces can be used to manage certificate signatures, and public and private keys.</span></span>



| <span data-ttu-id="ef94c-105">Interface</span><span class="sxs-lookup"><span data-stu-id="ef94c-105">Interface</span></span>                                                      | <span data-ttu-id="ef94c-106">Description</span><span class="sxs-lookup"><span data-stu-id="ef94c-106">Description</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef94c-107">**ISignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="ef94c-107">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | <span data-ttu-id="ef94c-108">Représente un certificat de signature qui vous permet de signer une demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="ef94c-108">Represents a signing certificate that enables you to sign a certificate request.</span></span>                  |
| [<span data-ttu-id="ef94c-109">**ISignerCertificates**</span><span class="sxs-lookup"><span data-stu-id="ef94c-109">**ISignerCertificates**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | <span data-ttu-id="ef94c-110">Gère une collection d’objets [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .</span><span class="sxs-lookup"><span data-stu-id="ef94c-110">Manages a collection of [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) objects.</span></span>                 |
| [<span data-ttu-id="ef94c-111">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="ef94c-111">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | <span data-ttu-id="ef94c-112">Représente une clé privée asymétrique qui peut être utilisée pour le chiffrement, la signature et l’accord de clé.</span><span class="sxs-lookup"><span data-stu-id="ef94c-112">Represents an asymmetric private key that can be used for encryption, signing, and key agreement.</span></span> |
| [<span data-ttu-id="ef94c-113">**IX509PublicKey**</span><span class="sxs-lookup"><span data-stu-id="ef94c-113">**IX509PublicKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | <span data-ttu-id="ef94c-114">Représente une clé publique dans une paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="ef94c-114">Represents a public key in a public/private key pair.</span></span>                                             |
| [<span data-ttu-id="ef94c-115">**IX509SignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="ef94c-115">**IX509SignatureInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | <span data-ttu-id="ef94c-116">Représente les informations utilisées pour signer une demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="ef94c-116">Represents information used to sign a certificate request.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="ef94c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef94c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef94c-118">CertEnroll, interfaces</span><span class="sxs-lookup"><span data-stu-id="ef94c-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



