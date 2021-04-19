---
title: Création et initialisation d’un enregistreur DRM
description: Création et initialisation d’un enregistreur DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media Format SDK, enregistreurs DRM
- gestion des droits numériques (DRM), création d’enregistreurs DRM
- DRM (gestion des droits numériques), création d’enregistreurs DRM
- gestion des droits numériques (DRM), initialisation des enregistreurs DRM
- DRM (gestion des droits numériques), initialisation des enregistreurs DRM
- API étendues du client DRM, enregistreurs DRM
- API étendues clientes, enregistreurs DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106509687"
---
# <a name="creating-and-initializing-a-drm-writer"></a><span data-ttu-id="eb67d-110">Création et initialisation d’un enregistreur DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-110">Creating and Initializing a DRM Writer</span></span>

<span data-ttu-id="eb67d-111">Les étapes suivantes sont requises pour initialiser un objet Writer ASF pour l’importation de fichiers multimédias chiffrés dans Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="eb67d-111">The following steps are required to initialize an ASF writer object for importing encrypted media samples in Windows Media DRM.</span></span>

1.  <span data-ttu-id="eb67d-112">Suivez les étapes 1 à 4 de la [licence d’importation et du matériel de clé](importing-license-and-key-material.md).</span><span class="sxs-lookup"><span data-stu-id="eb67d-112">Follow steps 1 to 4 of [Importing License and Key Material](importing-license-and-key-material.md).</span></span>
2.  <span data-ttu-id="eb67d-113">Créez et initialisez un objet Writer ASF à l’aide du matériel de clé DRM Windows Media approprié.</span><span class="sxs-lookup"><span data-stu-id="eb67d-113">Create and initialize an ASF writer object using the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="eb67d-114">Pour plus d’informations, consultez Activation de la [prise en charge de DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="eb67d-114">For more information, see [Enabling DRM Support](enabling-drm-support.md).</span></span>
3.  <span data-ttu-id="eb67d-115">Définissez chacun des attributs suivants en appelant [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span><span class="sxs-lookup"><span data-stu-id="eb67d-115">Set each of the following attributes by calling [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span></span>
    -   <span data-ttu-id="eb67d-116">\_HEADERSIGNPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-116">DRM\_HeaderSignPrivKey</span></span>
    -   <span data-ttu-id="eb67d-117">\_V1LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-117">DRM\_V1LicenseAcqURL</span></span>
    -   <span data-ttu-id="eb67d-118">\_KEYID DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-118">DRM\_KeyID</span></span>
    -   <span data-ttu-id="eb67d-119">\_LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-119">DRM\_LicenseAcqURL</span></span>
4.  <span data-ttu-id="eb67d-120">Si une version sous licence de Windows Media Rights Manager n’est pas installée sur l’ordinateur exécutant votre logiciel, les quatre attributs suivants doivent également être définis :</span><span class="sxs-lookup"><span data-stu-id="eb67d-120">If a licensed version of Windows Media Rights Manager is not installed on the computer running your software, then the following four attributes must also be set:</span></span>
    -   <span data-ttu-id="eb67d-121">\_LASIGNATUREROOTCERT DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-121">DRM\_LASignatureRootCert</span></span>
    -   <span data-ttu-id="eb67d-122">\_LASIGNATURECERT DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-122">DRM\_LASignatureCert</span></span>
    -   <span data-ttu-id="eb67d-123">\_LASIGNATURELICSRVCERT DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-123">DRM\_LASignatureLicSrvCert</span></span>
    -   <span data-ttu-id="eb67d-124">\_LASIGNATUREPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="eb67d-124">DRM\_LASignaturePrivKey</span></span>
    -   <span data-ttu-id="eb67d-125">L’application pour les certificats de chiffrement nécessaires peut être effectuée en complétant le [contrat de licence Windows Media (WMLA)](https://www.microsoft.com/licensing/default) en ligne.</span><span class="sxs-lookup"><span data-stu-id="eb67d-125">Application for the necessary encryption certificates can be completed by filling out the [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online.</span></span>
5.  <span data-ttu-id="eb67d-126">Créer une clé de session et remplir une structure de [**\_ clé de \_ session \_ d’importation WMDRM**](wmdrm-import-session-key.md) .</span><span class="sxs-lookup"><span data-stu-id="eb67d-126">Create a session key and fill out a [**WMDRM\_IMPORT\_SESSION\_KEY**](wmdrm-import-session-key.md) structure.</span></span> <span data-ttu-id="eb67d-127">La clé de session est utilisée pour chiffrer une clé de contenu.</span><span class="sxs-lookup"><span data-stu-id="eb67d-127">The session key will be used for encrypting a content key.</span></span> <span data-ttu-id="eb67d-128">Pour obtenir un exemple, consultez [exemple de création de clé de session](create-session-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="eb67d-128">For an example, see [Create Session Key Example](create-session-key-example.md).</span></span>
6.  <span data-ttu-id="eb67d-129">Créer une clé de contenu à partir d’un vecteur d’initialisation RC4 aléatoire et remplir une structure de [**\_ clé de \_ contenu \_ d’importation WMDRM**](wmdrm-import-content-key.md) .</span><span class="sxs-lookup"><span data-stu-id="eb67d-129">Create a content key from a random RC4 initialization vector, and fill out a [**WMDRM\_IMPORT\_CONTENT\_KEY**](wmdrm-import-content-key.md) structure.</span></span> <span data-ttu-id="eb67d-130">La clé de contenu est utilisée pour chiffrer les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="eb67d-130">The content key is used for encrypting the media samples.</span></span> <span data-ttu-id="eb67d-131">Pour obtenir un exemple, consultez [créer un exemple de clé de contenu](create-content-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="eb67d-131">For an example, see [Create Content Key Example](create-content-key-example.md).</span></span>
7.  <span data-ttu-id="eb67d-132">Chiffrez la clé de contenu avec la clé de session, à l’aide du chiffrement RC4.</span><span class="sxs-lookup"><span data-stu-id="eb67d-132">Encrypt the content key with the session key, using RC4 encryption.</span></span>
8.  <span data-ttu-id="eb67d-133">Extrayez la clé de collection de certificats de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="eb67d-133">Extract the machine certificate collection key.</span></span> <span data-ttu-id="eb67d-134">Pour obtenir un exemple, consultez [obtenir un exemple de certificat d’ordinateur](get-machine-certificate-example.md).</span><span class="sxs-lookup"><span data-stu-id="eb67d-134">For an example, see [Get Machine Certificate Example](get-machine-certificate-example.md).</span></span>
9.  <span data-ttu-id="eb67d-135">Chiffrez la clé de session avec la clé publique extraite du certificat.</span><span class="sxs-lookup"><span data-stu-id="eb67d-135">Encrypt the session key with the public key extracted from the certificate.</span></span>
10. <span data-ttu-id="eb67d-136">Remplir une structure [**d' \_ \_ initialisation d' \_ importation WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="eb67d-136">Fill out a [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>
11. <span data-ttu-id="eb67d-137">Appelez la méthode [**IWMDRMWriter3 :: SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) pour indiquer au kit de développement logiciel (SDK) que les exemples qui arrivent dans le writer sont déjà protégés et doivent être envoyés directement au client Windows Media DRM pour l’importation.</span><span class="sxs-lookup"><span data-stu-id="eb67d-137">Call the [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) method to notify the SDK that samples coming into the writer are already protected and should be sent directly to the Windows Media DRM client for import.</span></span>
12. <span data-ttu-id="eb67d-138">Appelez [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="eb67d-138">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="eb67d-139">Les étapes restantes pour créer un fichier protégé par DRM sont documentées dans le Guide de programmation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="eb67d-139">The remaining steps for creating a DRM-protected file are documented in the Windows Media Format SDK Programming Guide.</span></span> <span data-ttu-id="eb67d-140">Pour plus d’informations, consultez [création de fichiers protégés](creating-protected-files.md).</span><span class="sxs-lookup"><span data-stu-id="eb67d-140">For more information, see [Creating Protected Files](creating-protected-files.md).</span></span>

<span data-ttu-id="eb67d-141">L’étape suivante consiste à itérer au sein de chaque exemple de support, à le chiffrer et à le transmettre à l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="eb67d-141">The next step is to iterate through each media sample, encrypt it, and pass it to the writer object.</span></span> <span data-ttu-id="eb67d-142">Pour plus d’informations, consultez les [exemples de média de chiffrement et d’importation](encrypting-and-importing-media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="eb67d-142">For more information, see the [Encrypting and Importing Media Samples](encrypting-and-importing-media-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb67d-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb67d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb67d-144">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="eb67d-144">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="eb67d-145">**Importation DRM**</span><span class="sxs-lookup"><span data-stu-id="eb67d-145">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




