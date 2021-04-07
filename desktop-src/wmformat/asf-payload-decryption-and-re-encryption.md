---
title: Déchiffrement et rechiffrement de la charge utile ASF
description: Déchiffrement et rechiffrement de la charge utile ASF
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- SDK Windows Media format, déchiffrement et déchiffrement de la charge utile ASF
- Windows Media Format SDK, déchiffrement de la charge utile et rechiffrement
- Windows Media Format SDK, déchiffrement
- Windows Media Format SDK, rechiffrement
- gestion des droits numériques (DRM), déchiffrement et rechiffrement de la charge utile ASF
- DRM (gestion des droits numériques), déchiffrement et rechiffrement de la charge utile ASF
- gestion des droits numériques (DRM), déchiffrement et rechiffrement de la charge utile
- DRM (gestion des droits numériques), déchiffrement et rechiffrement de la charge utile
- gestion des droits numériques (DRM), déchiffrement
- DRM (gestion des droits numériques), déchiffrement
- gestion des droits numériques (DRM), rechiffrement
- DRM (gestion des droits numériques), rechiffrement
- API étendues du client DRM, déchiffrement de la charge utile ASF et rechiffrement
- API étendues clientes, déchiffrement et rechiffrement de la charge utile ASF
- API étendues du client DRM, déchiffrement de la charge utile et rechiffrement
- API étendues clientes, déchiffrement de la charge utile et rechiffrement
- API étendues du client DRM, déchiffrement
- API étendues clientes, déchiffrement
- API étendues du client DRM, rechiffrement
- API étendues du client, rechiffrement
- ASF (Advanced Systems Format), rechiffrement
- ASF (format des systèmes avancés), rechiffrement
- ASF (Advanced Systems Format), déchiffrement
- ASF (format de systèmes avancés), déchiffrement
- ASF (Advanced Systems Format), déchiffrement et rechiffrement de la charge utile
- ASF (format avancé des systèmes), déchiffrement et rechiffrement de la charge utile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671445"
---
# <a name="asf-payload-decryption-and-re-encryption"></a><span data-ttu-id="f6497-129">Déchiffrement et rechiffrement de la charge utile ASF</span><span class="sxs-lookup"><span data-stu-id="f6497-129">ASF Payload Decryption and Re-encryption</span></span>

<span data-ttu-id="f6497-130">Les étapes ci-dessous décrivent les actions qu’une application doit effectuer pour déchiffrer et rechiffrer chaque charge utile :</span><span class="sxs-lookup"><span data-stu-id="f6497-130">The steps below describe the actions that an application must complete to decrypt and re-encrypt each payload:</span></span>

1.  <span data-ttu-id="f6497-131">Incrémentez la valeur salt.</span><span class="sxs-lookup"><span data-stu-id="f6497-131">Increment the salt value.</span></span>
2.  <span data-ttu-id="f6497-132">Transmettez la charge utile (chiffrée avec Windows Media DRM) et la valeur Salt à la fonction de déchiffrement, [**IWMDRMDecrypt ::D ecrypt**](iwmdrmdecrypt-decrypt.md), qui renverra la charge utile, chiffrée à l’aide de la clé publique RC4.</span><span class="sxs-lookup"><span data-stu-id="f6497-132">Pass the payload (encrypted with Windows Media DRM) and the salt value to the decryption function, [**IWMDRMDecrypt::Decrypt**](iwmdrmdecrypt-decrypt.md), which will return the payload, encrypted using the RC4 public key.</span></span>
3.  <span data-ttu-id="f6497-133">Dérivez une clé de transitive RC4 en appliquant un hachage SHA-1 du vecteur d’initialisation concaténé avec la valeur salt.</span><span class="sxs-lookup"><span data-stu-id="f6497-133">Derive a transitory RC4 key by applying an SHA-1 hash of the initialization vector concatenated with the salt value.</span></span>
4.  <span data-ttu-id="f6497-134">Utilisez votre clé transitoire pour déchiffrer la charge utile.</span><span class="sxs-lookup"><span data-stu-id="f6497-134">Use your transitory key to decrypt the payload.</span></span>
5.  <span data-ttu-id="f6497-135">Rechiffrez immédiatement la charge utile avec le schéma de protection de contenu autorisé conformément aux règles de conformité et de robustesse de l’exportation DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f6497-135">Immediately re-encrypt the payload with the authorized content protection scheme according to the Windows Media DRM export compliance and robustness rules.</span></span>
6.  <span data-ttu-id="f6497-136">Recherchez la charge utile suivante.</span><span class="sxs-lookup"><span data-stu-id="f6497-136">Locate the next payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6497-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6497-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6497-138">**Exportation du contenu compressé**</span><span class="sxs-lookup"><span data-stu-id="f6497-138">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




