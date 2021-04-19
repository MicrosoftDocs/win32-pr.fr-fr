---
description: Les services de certificats prennent en charge les demandes de certificat basées sur le \# format PKCS 10 et le format keygen (Netscape). Les services de certificats prennent également en charge \# les demandes de renouvellement PKCS 7 et les demandes CMS (Cryptographic Message Syntax).
ms.assetid: 6321ce99-f5d1-4d72-a062-99cffb543731
title: Demandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7870e09d930fb06d50f0cc8acfff1270db1c92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534622"
---
# <a name="requests"></a><span data-ttu-id="a5381-104">Demandes</span><span class="sxs-lookup"><span data-stu-id="a5381-104">Requests</span></span>

<span data-ttu-id="a5381-105">Les services de certificats prennent en charge les [*demandes de certificat*](../secgloss/c-gly.md) basées sur le \# format PKCS 10 et le format keygen (Netscape).</span><span class="sxs-lookup"><span data-stu-id="a5381-105">Certificate Services supports [*certificate requests*](../secgloss/c-gly.md) based on the PKCS \#10 format and the Keygen (Netscape) format.</span></span> <span data-ttu-id="a5381-106">Les services de certificats prennent également en charge \# les demandes de renouvellement PKCS 7 et les demandes CMS (Cryptographic Message Syntax).</span><span class="sxs-lookup"><span data-stu-id="a5381-106">Certificate Services also supports PKCS \#7 renewal requests and Cryptographic Message Syntax (CMS) requests.</span></span>

<span data-ttu-id="a5381-107">Les services de certificats fournissent également une interface [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) , qui contient des méthodes pour soumettre une demande de certificat et (si la demande est approuvée) pour recevoir le certificat émis résultant.</span><span class="sxs-lookup"><span data-stu-id="a5381-107">Certificate Services also provides an [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) interface, which contains methods for submitting a certificate request and (if the request is approved) for receiving the resulting issued certificate.</span></span>

<span data-ttu-id="a5381-108">Des interfaces supplémentaires liées à la sécurité sont disponibles dans le [contrôle d’inscription de certificats](certificate-enrollment-control.md).</span><span class="sxs-lookup"><span data-stu-id="a5381-108">Additional security-related interfaces are available in the [Certificate Enrollment Control](certificate-enrollment-control.md).</span></span>

 

 
