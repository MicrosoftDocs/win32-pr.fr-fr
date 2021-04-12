---
description: Pour signer un fichier et créer un catalogue pour celui-ci, vous devez d’abord disposer d’un processus de signature des fichiers, d’un certificat et d’une clé publique.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Création de fichiers et de catalogues signés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203182"
---
# <a name="creating-signed-files-and-catalogs"></a><span data-ttu-id="6eefd-103">Création de fichiers et de catalogues signés</span><span class="sxs-lookup"><span data-stu-id="6eefd-103">Creating Signed Files and Catalogs</span></span>

<span data-ttu-id="6eefd-104">Pour signer un fichier et créer un catalogue pour celui-ci, vous devez d’abord disposer d’un processus de signature des fichiers, d’un certificat et d’une clé publique.</span><span class="sxs-lookup"><span data-stu-id="6eefd-104">To sign a file and create a catalog for it, you must first have a process for signing files, a certificate, and a public key.</span></span>

<span data-ttu-id="6eefd-105">**Pour signer un fichier et créer un catalogue**</span><span class="sxs-lookup"><span data-stu-id="6eefd-105">**To sign a file and a create a catalog**</span></span>

1.  <span data-ttu-id="6eefd-106">Utilisez [Pktextract.exe](pktextract-exe.md) pour extraire le [*jeton de clé publique*](p-sbscs-gly.md) du fichier de certificat.</span><span class="sxs-lookup"><span data-stu-id="6eefd-106">Use [Pktextract.exe](pktextract-exe.md) to extract the [*public key token*](p-sbscs-gly.md) from the certificate file.</span></span> <span data-ttu-id="6eefd-107">Le fichier de certificat doit être présent dans le même répertoire que l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="6eefd-107">The certificate file must be present in the same directory as the utility.</span></span>
2.  <span data-ttu-id="6eefd-108">Utilisez la valeur de jeton de clé publique pour mettre à jour l’attribut **PublicKeyToken** de l’élément **assemblyIdentity** dans le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="6eefd-108">Use the public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>
3.  <span data-ttu-id="6eefd-109">Utilisez [MT.exe](mt-exe.md) pour générer des hachages de fichiers contenus dans le manifeste de l’assembly et pour créer le fichier de description du catalogue (. CDF).</span><span class="sxs-lookup"><span data-stu-id="6eefd-109">Use [MT.exe](mt-exe.md) to generate hashes of files contained in the assembly manifest and to create the catalog description file (.cdf).</span></span>
4.  <span data-ttu-id="6eefd-110">Utilisez Makecat.exe avec le. CDF généré pour créer le catalogue de sécurité pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="6eefd-110">Use Makecat.exe with the generated .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="6eefd-111">Cet outil est inclus dans l’CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="6eefd-111">This tool is included in the CryptoAPI.</span></span>
5.  <span data-ttu-id="6eefd-112">Utilisez l’utilitaire [SignTool](/windows/desktop/SecCrypto/signtool) pour signer le catalogue généré avec le certificat utilisé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="6eefd-112">Use the [SignTool](/windows/desktop/SecCrypto/signtool) utility to sign the catalog generated with the certificate used in step 1.</span></span> <span data-ttu-id="6eefd-113">Les étapes 3 et 4 du. CDF peuvent être supprimées une fois le catalogue créé.</span><span class="sxs-lookup"><span data-stu-id="6eefd-113">The .cdf from steps 3 and 4 can be deleted once the catalog is created.</span></span>

<span data-ttu-id="6eefd-114">Voir aussi [exemple de signature d’assembly](assembly-signing-example.md).</span><span class="sxs-lookup"><span data-stu-id="6eefd-114">See also, [Assembly Signing Example](assembly-signing-example.md).</span></span>

 

 
