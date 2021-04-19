---
title: ID de clé et de clé
description: ID de clé et de clé
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- gestion des droits numériques (DRM), clés
- DRM (gestion des droits numériques), clés
- gestion des droits numériques (DRM), enfant
- DRM (gestion des droits numériques), enfant
- ID de clé (KID)
- KID (ID de la clé)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106538783"
---
# <a name="key-and-key-id"></a><span data-ttu-id="31dcb-110">ID de clé et de clé</span><span class="sxs-lookup"><span data-stu-id="31dcb-110">Key and Key ID</span></span>

<span data-ttu-id="31dcb-111">Lorsque vous empaquetez un fichier, vous utilisez une clé.</span><span class="sxs-lookup"><span data-stu-id="31dcb-111">When you package a file, you use a key.</span></span> <span data-ttu-id="31dcb-112">Une clé est un élément de données utilisé dans les algorithmes de chiffrement qui protègent le contenu.</span><span class="sxs-lookup"><span data-stu-id="31dcb-112">A key is a piece of data used in the encryption algorithms that protect the content.</span></span> <span data-ttu-id="31dcb-113">Il existe deux parties à chaque clé : une valeur initiale de clé de licence et un ID de clé (souvent abrégé en enfants).</span><span class="sxs-lookup"><span data-stu-id="31dcb-113">There are two parts to each key: a license key seed and a key ID (often abbreviated as KID).</span></span> <span data-ttu-id="31dcb-114">L’ID de clé est public et est stocké dans l’en-tête de fichier pour identifier la clé requise pour déchiffrer le fichier.</span><span class="sxs-lookup"><span data-stu-id="31dcb-114">The key ID is public, and is stored in the file header as a way to identify the key required to decrypt the file.</span></span> <span data-ttu-id="31dcb-115">La valeur initiale de la clé de licence est une valeur secrète qui doit être partagée par le gestionnaire de package de contenu et l’émetteur de licence.</span><span class="sxs-lookup"><span data-stu-id="31dcb-115">The license key seed is a secret value that must be shared by the content packager and the license issuer.</span></span>

<span data-ttu-id="31dcb-116">Un ID de clé identifie le contenu protégé du point de vue de la licence.</span><span class="sxs-lookup"><span data-stu-id="31dcb-116">A key ID identifies protected content from the perspective of the license.</span></span> <span data-ttu-id="31dcb-117">Bien que vous puissiez utiliser le même ID de clé pour plusieurs fichiers, il est recommandé de toujours utiliser un ID de clé unique pour chaque élément de contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="31dcb-117">Although you can use the same key ID for multiple files, it is recommended that you always use a unique key ID for each piece of protected content.</span></span>

<span data-ttu-id="31dcb-118">La plupart des méthodes décrites dans cette documentation utilisent des chaînes d’ID de clé pour sélectionner des licences.</span><span class="sxs-lookup"><span data-stu-id="31dcb-118">Many of the methods described in this documentation use key ID strings to select licenses.</span></span> <span data-ttu-id="31dcb-119">Ces chaînes contiennent l’ID de clé encodé en base64.</span><span class="sxs-lookup"><span data-stu-id="31dcb-119">These strings contain the key ID encoded in base64.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31dcb-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31dcb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31dcb-121">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="31dcb-121">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




