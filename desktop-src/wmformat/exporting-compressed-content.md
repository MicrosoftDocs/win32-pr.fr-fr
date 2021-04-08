---
title: Exportation du contenu compressé
description: Exportation du contenu compressé
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media Format SDK, exportation DRM
- Windows Media Format SDK, exporter
- Windows Media Format SDK, contenu compressé
- gestion des droits numériques (DRM), exportation
- DRM (gestion des droits numériques), exportation
- gestion des droits numériques (DRM), contenu compressé
- DRM (gestion des droits numériques), contenu compressé
- API étendues du client DRM, contenu compressé
- API étendues du client, contenu compressé
- API étendues du client DRM, exporter
- API étendues clientes, exporter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839802"
---
# <a name="exporting-compressed-content"></a><span data-ttu-id="f272f-114">Exportation du contenu compressé</span><span class="sxs-lookup"><span data-stu-id="f272f-114">Exporting Compressed Content</span></span>

<span data-ttu-id="f272f-115">Cette section décrit l’exportation de médias protégés par DRM Windows Media sur un fichier Windows Media où l’application reçoit des données multimédias numériques compressées.</span><span class="sxs-lookup"><span data-stu-id="f272f-115">This section describes exporting Windows Media DRM protected media on a Windows Media file where the application receives compressed digital media data.</span></span> <span data-ttu-id="f272f-116">Pour ce faire, votre application doit effectuer un déchiffrement en ligne de toutes les charges utiles chiffrées DRM Windows Media dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="f272f-116">To do this, your application must perform inline decryption of all Windows Media DRM encrypted payloads in an ASF file.</span></span>

> [!Note]  
> <span data-ttu-id="f272f-117">Une bibliothèque d’analyse ASF vous est fournie dans le cadre de l’accord d’exportation DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f272f-117">An ASF parsing library is supplied to you as part of the Windows Media DRM Export agreement.</span></span>

 

<span data-ttu-id="f272f-118">Les principales étapes impliquées dans l’exportation de contenu compressé sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f272f-118">The primary steps involved in exporting compressed content are:</span></span>

1.  <span data-ttu-id="f272f-119">Effectuez l’individualisation DRM, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f272f-119">Perform DRM individualization, if needed.</span></span>
2.  <span data-ttu-id="f272f-120">Vérifiez que le schéma de protection de contenu cible est explicitement autorisé.</span><span class="sxs-lookup"><span data-stu-id="f272f-120">Verify that the target content protection scheme is explicitly permitted.</span></span>
3.  <span data-ttu-id="f272f-121">Créez un objet déchiffreur pour déchiffrer chaque charge utile ASF.</span><span class="sxs-lookup"><span data-stu-id="f272f-121">Create a decryptor object to decrypt each ASF payload.</span></span>
4.  <span data-ttu-id="f272f-122">Le système DRM transforme chaque charge utile ASF de Windows Media DRM en RC4 avant de la transmettre à votre application.</span><span class="sxs-lookup"><span data-stu-id="f272f-122">The DRM system transcrypts each ASF payload from Windows Media DRM into RC4 before passing it to your application.</span></span>

<span data-ttu-id="f272f-123">Si votre application modifie la taille d’une charge utile ASF pendant la transchiffrement, vous devez également Remultiplexer le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="f272f-123">If your application changes the size of an ASF payload during transcryption, you must also remultiplex the ASF file.</span></span>

<span data-ttu-id="f272f-124">Transmettez à la bibliothèque stub un certificat d’application Windows Media DRM export.</span><span class="sxs-lookup"><span data-stu-id="f272f-124">Pass to the stub library a Windows Media DRM Export Application Certificate.</span></span> <span data-ttu-id="f272f-125">Le certificat est vérifié et, s’il est valide, le système DRM génère un vecteur d’initialisation et le chiffre à l’aide de RSA OAEP.</span><span class="sxs-lookup"><span data-stu-id="f272f-125">The certificate is verified, and if it is valid, the DRM system generates an initialization vector and encrypts it using RSA OAEP.</span></span>

-   <span data-ttu-id="f272f-126">Une clé de session RC4 est créée pour chaque charge utile en concaténant le vecteur d’initialisation et une valeur salt.</span><span class="sxs-lookup"><span data-stu-id="f272f-126">An RC4 session key is created for each payload by concatenating the initialization vector and a salt value.</span></span> <span data-ttu-id="f272f-127">Vous fournissez la valeur Salt à l’API de déchiffrement, et vous devez l’incrémenter par une valeur entière positive différente de zéro pour chaque charge utile.</span><span class="sxs-lookup"><span data-stu-id="f272f-127">You supply the salt value to the decryption API, and you must increment it by a positive non-zero integer value for each payload.</span></span>

<span data-ttu-id="f272f-128">Microsoft vous fournira un outil de Microsoft dans le cadre de l’accord d’exportation Windows Media DRM qui vous permettra de générer votre propre paire de clés publique/privée RSA.</span><span class="sxs-lookup"><span data-stu-id="f272f-128">You will be provided a tool by Microsoft as part of the Windows Media DRM export agreement that will enable you to generate your own RSA public/private key pair.</span></span> <span data-ttu-id="f272f-129">Vous allez envoyer la clé publique à Microsoft, où Microsoft l’intégrera dans un certificat d’application DRM Windows Media signé et la renverra.</span><span class="sxs-lookup"><span data-stu-id="f272f-129">You will send the public key to Microsoft, where Microsoft will incorporate it into a signed Windows Media DRM Application Certificate, and return it.</span></span>

<span data-ttu-id="f272f-130">Chaque charge utile, une fois déchiffrée à l’aide de la clé de déchiffrement RC4, doit être immédiatement chiffrée dans le CPS de sortie.</span><span class="sxs-lookup"><span data-stu-id="f272f-130">Each payload, after it is decrypted using the RC4 decryption key, must be immediately encrypted into the output CPS.</span></span> <span data-ttu-id="f272f-131">D’autres restrictions s’appliquent à la gestion des charges utiles non chiffrées qui sont décrites dans les règles de robustesse et de conformité, qui accompagnent le contrat d’exportation DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f272f-131">There are other restrictions on handling of unencrypted payloads that are outlined in the robustness and compliance rules, which accompany the Windows Media DRM Export agreement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f272f-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f272f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f272f-133">**Déchiffrement et rechiffrement de la charge utile ASF**</span><span class="sxs-lookup"><span data-stu-id="f272f-133">**ASF Payload Decryption and Re-encryption**</span></span>](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[<span data-ttu-id="f272f-134">**Exportation DRM**</span><span class="sxs-lookup"><span data-stu-id="f272f-134">**DRM Export**</span></span>](drm-export.md)
</dt> <dt>

[<span data-ttu-id="f272f-135">**Réalisation de l’individualisation DRM**</span><span class="sxs-lookup"><span data-stu-id="f272f-135">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> <dt>

[<span data-ttu-id="f272f-136">**Vérification et initialisation**</span><span class="sxs-lookup"><span data-stu-id="f272f-136">**Verification and Initialization**</span></span>](verification-and-initialization.md)
</dt> </dl>

 

 




