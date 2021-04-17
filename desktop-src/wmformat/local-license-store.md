---
title: Magasin de licences local
description: Magasin de licences local
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
keywords:
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, licences pour DRM
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), gestion des licences de fichiers protégés
- DRM (gestion des droits numériques), gestion des licences de fichiers protégés
- licences, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380372"
---
# <a name="local-license-store"></a><span data-ttu-id="c3308-111">Magasin de licences local</span><span class="sxs-lookup"><span data-stu-id="c3308-111">Local License Store</span></span>

<span data-ttu-id="c3308-112">Lorsqu’une licence DRM est remise à l’ordinateur client, elle est placée dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="c3308-112">When a DRM license is delivered to the client computer it is put into the local license store.</span></span> <span data-ttu-id="c3308-113">Il s’agit d’un fichier protégé sur le disque dur qui contient toutes les licences émises à l’utilisateur, ainsi que d’autres informations DRM.</span><span class="sxs-lookup"><span data-stu-id="c3308-113">This is a protected file on the hard disk that contains all the licenses issued to the user along with other DRM information.</span></span>

<span data-ttu-id="c3308-114">Vous pouvez manipuler des données dans le magasin de licences local de plusieurs façons, à l’aide des API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="c3308-114">You can manipulate data in the local license store in a few, limited ways by using the Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="c3308-115">En plus du magasin de licences local, certains objets utilisent un magasin de licences temporaire.</span><span class="sxs-lookup"><span data-stu-id="c3308-115">In addition to the local license store, some objects make use of a temporary license store.</span></span> <span data-ttu-id="c3308-116">Une licence dans un magasin temporaire existe uniquement pendant une brève période.</span><span class="sxs-lookup"><span data-stu-id="c3308-116">A license in a temporary store exists only for a short period of time.</span></span> <span data-ttu-id="c3308-117">Toutefois, certaines licences qui commencent dans un magasin temporaire peuvent être enregistrées dans le magasin de licences local normal.</span><span class="sxs-lookup"><span data-stu-id="c3308-117">However, some licenses that begin in a temporary store can be saved to the regular local license store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3308-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3308-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3308-119">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="c3308-119">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




