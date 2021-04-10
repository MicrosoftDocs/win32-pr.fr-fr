---
title: Interrogation pour obtenir des informations détaillées sur les droits
description: Interrogation pour obtenir des informations détaillées sur les droits
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows Media Format SDK, interroger des droits détaillés
- Windows Media Format SDK, requêtes de droits détaillés
- gestion des droits numériques (DRM), interrogation des droits détaillés
- DRM (Digital Rights Management), interrogation des droits détaillés
- gestion des droits numériques (DRM), requêtes de droits détaillés
- DRM (gestion des droits numériques), requêtes de droits détaillés
- API étendues du client DRM, interrogation des droits détaillés
- API étendues du client, interrogation des droits détaillés
- API étendues du client DRM, requêtes de droits détaillées
- API étendues clientes, requêtes de droits détaillées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196874"
---
# <a name="querying-for-detailed-rights-information"></a><span data-ttu-id="e78eb-113">Interrogation pour obtenir des informations détaillées sur les droits</span><span class="sxs-lookup"><span data-stu-id="e78eb-113">Querying for Detailed Rights Information</span></span>

<span data-ttu-id="e78eb-114">À l’aide de la méthode [**IWMDRMLicenseQuery :: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) , vous pouvez obtenir des informations détaillées sur les droits accordés par les licences pour un ID de clé.</span><span class="sxs-lookup"><span data-stu-id="e78eb-114">By using the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method, you can obtain detailed information about the rights granted by licenses for a key ID.</span></span> <span data-ttu-id="e78eb-115">Les informations que vous recevez de cette méthode sont agrégées à partir de toutes les licences dans le magasin de licences local qui s’appliquent à l’ID de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="e78eb-115">The information that you get from this method is aggregated from all licenses in the local license store that apply to the specified key ID.</span></span>

<span data-ttu-id="e78eb-116">**QueryLicenseState** utilise la structure de [**\_ données d' \_ état \_ de licence DRM**](drmdrm-license-state-data.md) pour afficher des informations agrégées sur toutes les licences pour l’ID de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="e78eb-116">**QueryLicenseState** uses the [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure to display aggregate information about all the licenses for the specified key ID.</span></span> <span data-ttu-id="e78eb-117">Cette utilisation est différente de celle des autres objets du kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e78eb-117">This usage is different than by other objects in the Windows Media Format SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e78eb-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e78eb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e78eb-119">**Obtention d’informations à partir de licences dans le magasin de licences local**</span><span class="sxs-lookup"><span data-stu-id="e78eb-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




