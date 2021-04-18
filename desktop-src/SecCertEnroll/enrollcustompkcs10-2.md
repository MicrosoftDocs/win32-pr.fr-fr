---
description: Crée une demande PKCS \# 10 personnalisée et tente de l’inscrire dans une autorité de certification d’entreprise.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533611"
---
# <a name="enrollcustompkcs10_2"></a><span data-ttu-id="26e01-103">enrollCustomPKCS10 \_ 2</span><span class="sxs-lookup"><span data-stu-id="26e01-103">enrollCustomPKCS10\_2</span></span>

<span data-ttu-id="26e01-104">L' \_ exemple enrollCustomPKCS10 2 crée une demande PKCS \# 10 personnalisée et tente de l’inscrire auprès d’une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="26e01-104">The enrollCustomPKCS10\_2 sample creates a custom PKCS \#10 request and attempts to enroll it in an enterprise [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span>

## <a name="location"></a><span data-ttu-id="26e01-105">Emplacement</span><span class="sxs-lookup"><span data-stu-id="26e01-105">Location</span></span>

<span data-ttu-id="26e01-106">Lorsque vous installez le kit de développement logiciel (SDK) de Microsoft Windows, l’exemple est installé par défaut dans le dossier *% ProgramFiles%* \\ Microsoft SDK Microsoft \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollCustomPKCS10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="26e01-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomPKCS10\_2 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="26e01-107">Discussions</span><span class="sxs-lookup"><span data-stu-id="26e01-107">Discussion</span></span>

<span data-ttu-id="26e01-108">Exemple enrollCustomPKCS10 \_ 2 :</span><span class="sxs-lookup"><span data-stu-id="26e01-108">The enrollCustomPKCS10\_2 sample:</span></span>

1.  <span data-ttu-id="26e01-109">Traite les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="26e01-109">Processes the command line arguments.</span></span> <span data-ttu-id="26e01-110">La ligne de commande doit contenir le nom d’un modèle et le nom d’un fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="26e01-110">The command line should contain the name of a template and the name of a cryptographic provider.</span></span>
2.  <span data-ttu-id="26e01-111">Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) et l’initialise à l’aide du nom du modèle spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="26e01-111">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the name of the template specified on the command line.</span></span>
3.  <span data-ttu-id="26e01-112">Récupère la [*demande de certificat*](/windows/desktop/SecGloss/c-gly) à partir de l’objet d’inscription.</span><span class="sxs-lookup"><span data-stu-id="26e01-112">Retrieves the [*certificate request*](/windows/desktop/SecGloss/c-gly) from the enrollment object.</span></span>
4.  <span data-ttu-id="26e01-113">Récupère la requête PKCS 10 la plus profonde \# de l’objet de demande de certificat obtenu à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="26e01-113">Retrieves the innermost PKCS\#10 request from the certificate request object obtained in step 3.</span></span>
5.  <span data-ttu-id="26e01-114">Récupère une [*clé privée*](/windows/desktop/SecGloss/p-gly) à partir de la \# demande PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="26e01-114">Retrieves a [*private key*](/windows/desktop/SecGloss/p-gly) from the PKCS\#10 request.</span></span>
6.  <span data-ttu-id="26e01-115">Crée une collection [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) et ajoute les fournisseurs de services de chiffrement disponibles à la collection, puis récupère un objet [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) pour le fournisseur spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="26e01-115">Creates an [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) collection and adds the available cryptographic providers to the collection and then retrieves an [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) object for the provider specified on the command line.</span></span>
7.  <span data-ttu-id="26e01-116">Définit l’objet d’État sur la clé privée.</span><span class="sxs-lookup"><span data-stu-id="26e01-116">Sets the status object on the private key.</span></span>
8.  <span data-ttu-id="26e01-117">Tente d’inscrire la [*demande de certificat*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="26e01-117">Attempts to enroll the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26e01-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26e01-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26e01-119">\#Demande PKCS 10</span><span class="sxs-lookup"><span data-stu-id="26e01-119">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="26e01-120">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="26e01-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
