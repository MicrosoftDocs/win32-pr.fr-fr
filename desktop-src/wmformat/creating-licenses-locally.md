---
title: Création de licences localement
description: Création de licences localement
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows Media Format SDK, création de licences localement
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), création de licences localement
- DRM (gestion des droits numériques), création de licences localement
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, création de licences locales
- API étendues clientes, création de licences localement
- licences, créer des licences localement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029829"
---
# <a name="creating-licenses-locally"></a><span data-ttu-id="b3ac0-112">Création de licences localement</span><span class="sxs-lookup"><span data-stu-id="b3ac0-112">Creating Licenses Locally</span></span>

<span data-ttu-id="b3ac0-113">Dans certaines circonstances, par exemple lors de l' [importation de DRM](drm-import.md), vous pouvez créer vos propres licences.</span><span class="sxs-lookup"><span data-stu-id="b3ac0-113">In certain circumstances, such as during [DRM Import](drm-import.md), you can create your own licenses.</span></span> <span data-ttu-id="b3ac0-114">Les licences Windows Media DRM peuvent être écrites de différentes manières, mais pour créer votre propre licence, vous devez utiliser le schéma binaire XMR (extensible Media Rights).</span><span class="sxs-lookup"><span data-stu-id="b3ac0-114">Windows Media DRM licenses can be written a few different ways, but to make your own license, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="b3ac0-115">Pour plus d’informations, consultez [génération d’une licence XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="b3ac0-115">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>

<span data-ttu-id="b3ac0-116">Lorsque vous créez une licence, vous pouvez l’ajouter au magasin de licences local en appelant la méthode [**IWMDRMLicenseManagement :: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="b3ac0-116">When you create a license, you can add it to the local license store by calling the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3ac0-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3ac0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3ac0-118">**Acquisition de licences**</span><span class="sxs-lookup"><span data-stu-id="b3ac0-118">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="b3ac0-119">**Génération d’une licence XMR**</span><span class="sxs-lookup"><span data-stu-id="b3ac0-119">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> </dl>

 

 




