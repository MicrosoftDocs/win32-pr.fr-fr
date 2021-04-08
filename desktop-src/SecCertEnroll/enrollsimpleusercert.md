---
description: Inscrit un utilisateur final auprès d’une autorité de certification à l’aide d’un modèle, du nom de l’objet et de la longueur, en bits, de la clé.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034738"
---
# <a name="enrollsimpleusercert"></a><span data-ttu-id="e14f6-103">enrollSimpleUserCert</span><span class="sxs-lookup"><span data-stu-id="e14f6-103">enrollSimpleUserCert</span></span>

<span data-ttu-id="e14f6-104">L’exemple enrollSimpleUserCert inscrit un utilisateur final auprès d’une autorité de certification à l’aide d’un modèle, du nom de l’objet et de la longueur, en bits, de la clé.</span><span class="sxs-lookup"><span data-stu-id="e14f6-104">The enrollSimpleUserCert sample enrolls an end user with a certification authority (CA) by using a template, the subject name, and the length, in bits, of the key.</span></span>

## <a name="location"></a><span data-ttu-id="e14f6-105">Emplacement</span><span class="sxs-lookup"><span data-stu-id="e14f6-105">Location</span></span>

<span data-ttu-id="e14f6-106">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, une version C++ de l’exemple est installée, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollSimpleUserCert VC.</span><span class="sxs-lookup"><span data-stu-id="e14f6-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollSimpleUserCert folder.</span></span> <span data-ttu-id="e14f6-107">Une version C# est installée dans le dossier *% ProgramFiles%* \\ Microsoft kits de développement logiciel (SDK) \\ exemple d’inscription de \\ \\ \\ certificat x509 \\ \\ EnrollSimpleUserCert.</span><span class="sxs-lookup"><span data-stu-id="e14f6-107">A C# version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\CSharp\\EnrollSimpleUserCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="e14f6-108">Discussions</span><span class="sxs-lookup"><span data-stu-id="e14f6-108">Discussion</span></span>

<span data-ttu-id="e14f6-109">Exemple enrollSimpleUserCert :</span><span class="sxs-lookup"><span data-stu-id="e14f6-109">The enrollSimpleUserCert sample:</span></span>

1.  <span data-ttu-id="e14f6-110">Traite les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e14f6-110">Processes the command line arguments.</span></span> <span data-ttu-id="e14f6-111">La ligne de commande doit contenir le nom du modèle, le nom de l’objet et la longueur de la clé.</span><span class="sxs-lookup"><span data-stu-id="e14f6-111">The command line should contain the name of the template, the subject name, and the key length.</span></span>
2.  <span data-ttu-id="e14f6-112">Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) et l’initialise à l’aide du modèle.</span><span class="sxs-lookup"><span data-stu-id="e14f6-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template.</span></span>
3.  <span data-ttu-id="e14f6-113">Récupère l’objet de demande de certificat interne à partir de l’objet d’inscription et l’interroge pour l’objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="e14f6-113">Retrieves the inner certificate request object from the enrollment object and queries it for the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span> <span data-ttu-id="e14f6-114">La requête la plus profonde est toujours une \# demande PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="e14f6-114">The innermost request is always a PKCS \#10 request.</span></span>
4.  <span data-ttu-id="e14f6-115">Récupère l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) à partir de la \# demande PKCS 10 et définit la longueur de clé spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e14f6-115">Retrieves the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object from the PKCS \#10 request and sets the key length specified on the command line.</span></span>
5.  <span data-ttu-id="e14f6-116">Crée un objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , l’utilise pour encoder le nom d’objet X. 500 et ajoute le nom à la \# demande PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="e14f6-116">Creates an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, uses it to encode the X.500 subject name, and adds the name to the PKCS \#10 request.</span></span>
6.  <span data-ttu-id="e14f6-117">Tente d’inscrire l’utilisateur final auprès de l’autorité de certification et surveille la progression du processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="e14f6-117">Attempts to enroll the end user with the CA and monitors the progress of the enrollment process.</span></span> <span data-ttu-id="e14f6-118">La fonction checkEnrollStatus est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="e14f6-118">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e14f6-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e14f6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e14f6-120">\#Demande PKCS 10</span><span class="sxs-lookup"><span data-stu-id="e14f6-120">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="e14f6-121">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="e14f6-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



