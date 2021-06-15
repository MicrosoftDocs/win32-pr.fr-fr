---
title: Types d’énumération du client Microsoft Windows Media DRM
description: En savoir plus sur les énumérations qui sont prises en charge par les API étendues du client Microsoft Windows Media DRM.
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media Format SDK, types énumération
- gestion des droits numériques (DRM), types d’énumération
- DRM (gestion des droits numériques), types énumération
- API étendues du client DRM, types énumération
- API étendues clientes, types énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574136f8016161f4d2c208865a72ad2a86d98f68
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068426"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="7ef59-108">Types d’énumération du client Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="7ef59-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="7ef59-109">Le tableau suivant décrit les énumérations qui sont prises en charge par les API étendues du client Microsoft Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="7ef59-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="7ef59-110">Énumération</span><span class="sxs-lookup"><span data-stu-id="7ef59-110">Enumeration</span></span>                                                                      | <span data-ttu-id="7ef59-111">Description</span><span class="sxs-lookup"><span data-stu-id="7ef59-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ef59-112">**\_résultats de \_ la \_ requête \_ autorisés par l’action DRM**</span><span class="sxs-lookup"><span data-stu-id="7ef59-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="7ef59-113">Utilisé par l’interface [**IWMDRMLicenseQuery :: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) pour spécifier la raison pour laquelle une action n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="7ef59-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="7ef59-114">**type de données de l' \_ attr DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7ef59-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="7ef59-115">Définit les types de données utilisés pour les propriétés et les attributs DRM.</span><span class="sxs-lookup"><span data-stu-id="7ef59-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="7ef59-116">**\_type de chiffrement DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7ef59-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="7ef59-117">Définit les types d’algorithmes de chiffrement qui peuvent être utilisés pour chiffrer le contenu.</span><span class="sxs-lookup"><span data-stu-id="7ef59-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="7ef59-118">**\_État http \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="7ef59-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="7ef59-119">Définit une plage d’États HTTP pour une requête DRM.</span><span class="sxs-lookup"><span data-stu-id="7ef59-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="7ef59-120">**État de l' \_ individualisation DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7ef59-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="7ef59-121">Définit les États valides pour l’individualisation DRM.</span><span class="sxs-lookup"><span data-stu-id="7ef59-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="7ef59-122">**\_catégorie d' \_ État de licence DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7ef59-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="7ef59-123">Spécifie le type de restriction de licence qui est décrit par une structure de [**\_ données d' \_ état \_ de licence DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="7ef59-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="7ef59-124">**État de MSDRM \_**</span><span class="sxs-lookup"><span data-stu-id="7ef59-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="7ef59-125">Définit des conditions d’État pour le sous-système DRM.</span><span class="sxs-lookup"><span data-stu-id="7ef59-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="7ef59-126">**\_type de stratégie WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="7ef59-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="7ef59-127">Répertorie les types de stratégies disponibles pour Windows Media DRM pour les opérations sur les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="7ef59-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="7ef59-128">**\_droits WMT**</span><span class="sxs-lookup"><span data-stu-id="7ef59-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="7ef59-129">Définit les droits qui peuvent être spécifiés dans une licence DRM.</span><span class="sxs-lookup"><span data-stu-id="7ef59-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="7ef59-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ef59-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ef59-131">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="7ef59-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




