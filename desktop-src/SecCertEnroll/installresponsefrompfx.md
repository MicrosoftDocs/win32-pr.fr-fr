---
description: Installe un certificat inscrit à partir d’un fichier d’échange d’informations personnelles (PFX) dans le magasin de certificats.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952711"
---
# <a name="installresponsefrompfx"></a><span data-ttu-id="65395-103">installResponseFromPFX</span><span class="sxs-lookup"><span data-stu-id="65395-103">installResponseFromPFX</span></span>

<span data-ttu-id="65395-104">L’exemple installResponseFromPFX installe un certificat inscrit à partir d’un fichier d’échange d’informations personnelles (PFX) dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="65395-104">The installResponseFromPFX sample installs an enrolled certificate from a Personal Information Exchange (PFX) file to the certificate store.</span></span>

## <a name="location"></a><span data-ttu-id="65395-105">Emplacement</span><span class="sxs-lookup"><span data-stu-id="65395-105">Location</span></span>

<span data-ttu-id="65395-106">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ installResponseFromPFX VC.</span><span class="sxs-lookup"><span data-stu-id="65395-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\installResponseFromPFX folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="65395-107">Discussions</span><span class="sxs-lookup"><span data-stu-id="65395-107">Discussion</span></span>

<span data-ttu-id="65395-108">Exemple installResponseFromPFX :</span><span class="sxs-lookup"><span data-stu-id="65395-108">The installResponseFromPFX sample:</span></span>

1.  <span data-ttu-id="65395-109">Traite les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="65395-109">Processes the command line arguments.</span></span> <span data-ttu-id="65395-110">La ligne de commande doit contenir :</span><span class="sxs-lookup"><span data-stu-id="65395-110">The command line should contain:</span></span>
    -   <span data-ttu-id="65395-111">Nom de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="65395-111">The name of the sample.</span></span>
    -   <span data-ttu-id="65395-112">Nom du fichier PFX qui contient le certificat inscrit.</span><span class="sxs-lookup"><span data-stu-id="65395-112">The name of the PFX file that contains the enrolled certificate.</span></span>
    -   <span data-ttu-id="65395-113">Mot de passe associé au fichier PFX.</span><span class="sxs-lookup"><span data-stu-id="65395-113">A password associated with the PFX file.</span></span>
2.  <span data-ttu-id="65395-114">Lit le fichier PFX, en commençant par le format Base64 et le format binaire si base64 échoue.</span><span class="sxs-lookup"><span data-stu-id="65395-114">Reads the PFX file, trying the base64 format first and the binary format if base64 fails.</span></span> <span data-ttu-id="65395-115">La fonction DecodeFileW () est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="65395-115">The DecodeFileW() function is defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="65395-116">Convertit le certificat inscrit en **BSTR** et l’utilise pour initialiser un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .</span><span class="sxs-lookup"><span data-stu-id="65395-116">Converts the enrolled certificate to a **BSTR** and uses it to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object.</span></span> <span data-ttu-id="65395-117">La fonction convertWszToBstr est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="65395-117">The convertWszToBstr function is defined in enrollCommon.cpp.</span></span>
4.  <span data-ttu-id="65395-118">Installe le certificat dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="65395-118">Installs the certificate in the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65395-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65395-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65395-120">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="65395-120">enrollEOBOCMC</span></span>](enrolleobocmc.md)
</dt> <dt>

[<span data-ttu-id="65395-121">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="65395-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



