---
title: Paramètres de création de ressources en mosaïque
description: Il existe certaines contraintes sur le type de ressources Direct3D que vous pouvez créer avec l' \_ indicateur de \_ mosaïque diverse de la ressource d3d11 \_ . Cette section fournit les paramètres valides pour la création de ressources en mosaïque.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2019
ms.locfileid: "103679086"
---
# <a name="tiled-resource-creation-parameters"></a><span data-ttu-id="b140e-104">Paramètres de création de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="b140e-104">Tiled resource creation parameters</span></span>

<span data-ttu-id="b140e-105">Il existe certaines contraintes sur le type de ressources Direct3D que vous pouvez créer avec l’indicateur de [**\_ \_ \_ mosaïque diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="b140e-105">There are some constraints on the type of Direct3D resources that you can create with the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> <span data-ttu-id="b140e-106">Cette section fournit les paramètres valides pour la création de ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="b140e-106">This section provides the valid parameters for creating tiled resources.</span></span>

<dl> <dt>

<span data-ttu-id="b140e-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Type de ressource pris en charge**</span><span class="sxs-lookup"><span data-stu-id="b140e-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Supported Resource Type**</span></span>
</dt> <dd>

<span data-ttu-id="b140e-108">\[Tableau Texture2D \] (y compris le \[ tableau TextureCube \] , qui est une variante de Texture2D \[ array \] ) ou buffer.</span><span class="sxs-lookup"><span data-stu-id="b140e-108">Texture2D\[Array\] (including TextureCube\[Array\], which is a variant of Texture2D\[Array\]) or Buffer.</span></span>

<span data-ttu-id="b140e-109">**Non pris en charge :** Texture1D \[ array \] ou Texture3D, mais Texture3D peut être pris en charge à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="b140e-109">**NOT supported:** Texture1D\[Array\] or Texture3D, but Texture3D might be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="b140e-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilisation des ressources prise en charge**</span><span class="sxs-lookup"><span data-stu-id="b140e-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="b140e-111">Utilisation de D3D11 \_ \_ par défaut.</span><span class="sxs-lookup"><span data-stu-id="b140e-111">D3D11\_USAGE\_DEFAULT.</span></span>

<span data-ttu-id="b140e-112">**Non pris en charge :** Utilisation \_ d3d11 \_ dynamique, d3d11 de \_ l’utilisation \_ intermédiaire ou d3d11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b140e-112">**NOT supported:** D3D11\_USAGE\_DYNAMIC, D3D11\_USAGE\_STAGING, or D3D11\_USAGE\_IMMUTABLE.</span></span>

</dd> <dt>

<span data-ttu-id="b140e-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Indicateurs divers des ressources pris en charge**</span><span class="sxs-lookup"><span data-stu-id="b140e-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b140e-114">Les \_ ressources \_ d3d11 \_ (par définition), \_ misc \_ TEXTURECUBE, \_ DRAWINDIRECT \_ args, \_ buffer \_ autorisent les \_ \_ affichages bruts, la mise en \_ mémoire tampon \_ , la \_ \_ fixation des ressources ou la génération de \_ \_ mips.</span><span class="sxs-lookup"><span data-stu-id="b140e-114">D3D11\_RESOURCE\_MISC\_TILED (by definition), \_MISC\_TEXTURECUBE, \_DRAWINDIRECT\_ARGS, \_BUFFER\_ALLOW\_RAW\_VIEWS, \_BUFFER\_STRUCTURED, \_RESOURCE\_CLAMP, or \_GENERATE\_MIPS.</span></span>

<span data-ttu-id="b140e-115">**Non pris en charge :** \_ PARTAGÉ, \_ partagé \_ KEYEDMUTEX, \_ \_ compatible GDI, \_ \_ NTHANDLE partagé, \_ contenu restreint \_ , \_ restreindre \_ les \_ ressources partagées, restreindre le \_ \_ \_ pilote de ressource partagée, service \_ \_ protégé ou \_ pool de mosaïques \_ .</span><span class="sxs-lookup"><span data-stu-id="b140e-115">**NOT supported:** \_SHARED, \_SHARED\_KEYEDMUTEX, \_GDI\_COMPATIBLE, \_SHARED\_NTHANDLE, \_RESTRICTED\_CONTENT, \_RESTRICT\_SHARED\_RESOURCE, \_RESTRICT\_SHARED\_RESOURCE\_DRIVER, \_GUARDED, or \_TILE\_POOL.</span></span>

</dd> <dt>

<span data-ttu-id="b140e-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Indicateurs de liaison pris en charge**</span><span class="sxs-lookup"><span data-stu-id="b140e-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Supported Bind Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b140e-117">\_ \_ Ressource de nuanceur de liaison d3d11, \_ cible de \_ rendu \_ , \_ \_ stencil de profondeur ou \_ accès non ordonné \_ .</span><span class="sxs-lookup"><span data-stu-id="b140e-117">D3D11\_BIND\_SHADER\_RESOURCE, \_RENDER\_TARGET, \_DEPTH\_STENCIL, or \_UNORDERED\_ACCESS.</span></span>

<span data-ttu-id="b140e-118">**Non pris en charge :** \_ Mémoire tampon constante \_ , \_ \_ tampon \[ de vertex Notez que la liaison d’une mémoire tampon en mosaïque en tant que SRV/UAV/RTV est toujours OK \] , le tampon d' \_ index, la sortie du \_ \_ flux, le \_ \_ \_ décodeur de liaison ou la liaison de l' \_ \_ \_ encodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="b140e-118">**NOT supported:** \_CONSTANT\_BUFFER, \_VERTEX\_BUFFER \[note that binding a tiled Buffer as an SRV/UAV/RTV is still ok\], \_INDEX\_BUFFER, \_STREAM\_OUTPUT, \_BIND\_DECODER, or \_BIND\_VIDEO\_ENCODER.</span></span>

</dd> <dt>

<span data-ttu-id="b140e-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formats pris en charge**</span><span class="sxs-lookup"><span data-stu-id="b140e-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Supported Formats**</span></span>
</dt> <dd>

<span data-ttu-id="b140e-120">Tous les formats qui seraient disponibles pour la configuration donnée, quelle que soit la disposition en mosaïque, à quelques exceptions près.</span><span class="sxs-lookup"><span data-stu-id="b140e-120">All formats that would be available for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="b140e-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc pris en charge (nombre d’échantillonnages, qualité)**</span><span class="sxs-lookup"><span data-stu-id="b140e-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Supported SampleDesc (Multisample count, quality)**</span></span>
</dt> <dd>

<span data-ttu-id="b140e-122">Tout ce qui serait pris en charge pour la configuration donnée, indépendamment de sa mosaïque, à quelques exceptions près.</span><span class="sxs-lookup"><span data-stu-id="b140e-122">Whatever would be supported for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="b140e-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Largeur/hauteur prise en charge/Miplevels a/ArraySize**</span><span class="sxs-lookup"><span data-stu-id="b140e-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Supported Width/Height/MipLevels/ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="b140e-124">Étendues complètes prises en charge par Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="b140e-124">Full extents supported by Direct3D 11.</span></span> <span data-ttu-id="b140e-125">Les ressources en mosaïque n’ont pas la restriction sur la taille totale de la mémoire imposée sur les ressources non en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="b140e-125">Tiled resources don't have the restriction on total memory size imposed on non-tiled resources.</span></span> <span data-ttu-id="b140e-126">Les ressources en mosaïque sont limitées par les limites de l’espace d’adressage virtuel global.</span><span class="sxs-lookup"><span data-stu-id="b140e-126">Tiled resources are only constrained by overall virtual address space limits.</span></span> <span data-ttu-id="b140e-127">Pour plus d’informations, consultez [espace d’adressage disponible pour les ressources en mosaïque](address-space-available-for-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="b140e-127">For info, see [Address space available for tiled resources](address-space-available-for-tiled-resources.md).</span></span>

</dd> </dl>

<span data-ttu-id="b140e-128">Le contenu initial de la mémoire du pool de mosaïques n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b140e-128">The initial contents of tile pool memory are undefined.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b140e-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b140e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b140e-130">Création de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="b140e-130">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




