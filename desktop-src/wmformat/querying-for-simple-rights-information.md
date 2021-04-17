---
title: Interrogation des informations de droits simples
description: Interrogation des informations de droits simples
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows Media Format SDK, interrogation de droits simples
- Kit de développement logiciel (SDK) Windows Media format, requêtes de droits simples
- gestion des droits numériques (DRM), interrogation de droits simples
- DRM (Digital Rights Management), interrogation de droits simples
- gestion des droits numériques (DRM), requêtes de droits simples
- DRM (gestion des droits numériques), requêtes de droits simples
- API étendues du client DRM, interrogation de droits simples
- API étendues clientes, interrogation de droits simples
- API étendues du client DRM, requêtes de droits simples
- API étendues clientes, requêtes de droits simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379956"
---
# <a name="querying-for-simple-rights-information"></a><span data-ttu-id="f6936-113">Interrogation des informations de droits simples</span><span class="sxs-lookup"><span data-stu-id="f6936-113">Querying for Simple Rights Information</span></span>

<span data-ttu-id="f6936-114">Les API étendues du client Windows Media DRM vous permettent d’obtenir rapidement des informations simples sur la possibilité d’accéder à du contenu protégé pour différentes actions.</span><span class="sxs-lookup"><span data-stu-id="f6936-114">The Windows Media DRM Client Extended APIs enable you to quickly get simple information about whether protected content can be accessed for various actions.</span></span>

<span data-ttu-id="f6936-115">La méthode [**IWMDRMLicenseQuery :: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) peut être utilisée pour déterminer rapidement si une action est autorisée par une licence dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="f6936-115">The [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method can be used to determine quickly whether an action is permitted by a license in the local license store.</span></span> <span data-ttu-id="f6936-116">**QueryActionAllowed** a été optimisé pour être beaucoup plus rapide que les requêtes d’informations similaires à l’aide des objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f6936-116">**QueryActionAllowed** has been optimized to be much faster than queries for similar information using the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="f6936-117">Toutefois, ce type de requête agrège les licences dans le magasin de licences local et ne doit être utilisé que pour des fonctionnalités simples, telles que peut être nécessaire pour les éléments de l’interface utilisateur, par exemple l’affichage d’un indicateur d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="f6936-117">However, this type of query aggregates the licenses in the local license store and should be used only for simple features, such as might be needed for user interface elements, for example displaying a permission indicator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6936-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6936-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6936-119">**Obtention d’informations à partir de licences dans le magasin de licences local**</span><span class="sxs-lookup"><span data-stu-id="f6936-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




