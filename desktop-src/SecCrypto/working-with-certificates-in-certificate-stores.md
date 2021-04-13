---
description: Plusieurs fonctions ajoutent un contexte de certificat ou un lien vers un contexte vers un \[ Kit de développement logiciel (SDK) de plateforme de magasin \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Utilisation de certificats dans les magasins de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320041"
---
# <a name="working-with-certificates-in-certificate-stores"></a><span data-ttu-id="ed8f8-103">Utilisation de certificats dans les magasins de certificats</span><span class="sxs-lookup"><span data-stu-id="ed8f8-103">Working with Certificates in Certificate Stores</span></span>

<span data-ttu-id="ed8f8-104">Plusieurs fonctions ajoutent un contexte de certificat ou un lien vers un contexte dans un magasin.</span><span class="sxs-lookup"><span data-stu-id="ed8f8-104">Several functions add a certificate context or a link to a context to a store.</span></span>

<span data-ttu-id="ed8f8-105">Pour les certificats déjà sous forme de contexte de certificat :</span><span class="sxs-lookup"><span data-stu-id="ed8f8-105">For certificates already in certificate context form:</span></span>

-   [<span data-ttu-id="ed8f8-106">**CertAddCertificateContextToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-106">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [<span data-ttu-id="ed8f8-107">**CertAddCRLContextToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-107">**CertAddCRLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [<span data-ttu-id="ed8f8-108">**CertAddCTLContextToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-108">**CertAddCTLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [<span data-ttu-id="ed8f8-109">**CertAddCertificateLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-109">**CertAddCertificateLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [<span data-ttu-id="ed8f8-110">**CertAddCRLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-110">**CertAddCRLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [<span data-ttu-id="ed8f8-111">**CertAddCTLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-111">**CertAddCTLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

<span data-ttu-id="ed8f8-112">Pour les certificats qui sont au format codé, mais pas les contextes de certificat complet :</span><span class="sxs-lookup"><span data-stu-id="ed8f8-112">For certificates that are in encoded form but not full certificate contexts:</span></span>

-   [<span data-ttu-id="ed8f8-113">**CertAddEncodedCertificateToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-113">**CertAddEncodedCertificateToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [<span data-ttu-id="ed8f8-114">**CertAddEncodedCRLToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-114">**CertAddEncodedCRLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [<span data-ttu-id="ed8f8-115">**CertAddEncodedCTLToStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-115">**CertAddEncodedCTLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

<span data-ttu-id="ed8f8-116">Les fonctions suivantes suppriment un certificat, une liste de révocation de certificats ou une liste CTL d’un magasin en décrémentant son décompte de références d’une unité.</span><span class="sxs-lookup"><span data-stu-id="ed8f8-116">The following functions delete a certificate, CRL, or CTL from a store by decrementing its reference count by one.</span></span> <span data-ttu-id="ed8f8-117">Si le nombre de références est alors égal à zéro, la mémoire utilisée pour stocker le certificat, la liste de révocation de certificats ou la liste CTL est libérée.</span><span class="sxs-lookup"><span data-stu-id="ed8f8-117">If this causes the reference count to become zero, the memory used to store the certificate, CRL, or CTL is freed.</span></span>

-   [<span data-ttu-id="ed8f8-118">**CertDeleteCertificateFromStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-118">**CertDeleteCertificateFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [<span data-ttu-id="ed8f8-119">**CertDeleteCRLFromStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-119">**CertDeleteCRLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [<span data-ttu-id="ed8f8-120">**CertDeleteCTLFromStore**</span><span class="sxs-lookup"><span data-stu-id="ed8f8-120">**CertDeleteCTLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



