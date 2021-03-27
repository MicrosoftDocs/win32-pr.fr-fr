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
# <a name="tiled-resource-creation-parameters"></a>Paramètres de création de ressources en mosaïque

Il existe certaines contraintes sur le type de ressources Direct3D que vous pouvez créer avec l’indicateur de [**\_ \_ \_ mosaïque diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . Cette section fournit les paramètres valides pour la création de ressources en mosaïque.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Type de ressource pris en charge**
</dt> <dd>

\[Tableau Texture2D \] (y compris le \[ tableau TextureCube \] , qui est une variante de Texture2D \[ array \] ) ou buffer.

**Non pris en charge :** Texture1D \[ array \] ou Texture3D, mais Texture3D peut être pris en charge à l’avenir.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilisation des ressources prise en charge**
</dt> <dd>

Utilisation de D3D11 \_ \_ par défaut.

**Non pris en charge :** Utilisation \_ d3d11 \_ dynamique, d3d11 de \_ l’utilisation \_ intermédiaire ou d3d11 \_ \_ .

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Indicateurs divers des ressources pris en charge**
</dt> <dd>

Les \_ ressources \_ d3d11 \_ (par définition), \_ misc \_ TEXTURECUBE, \_ DRAWINDIRECT \_ args, \_ buffer \_ autorisent les \_ \_ affichages bruts, la mise en \_ mémoire tampon \_ , la \_ \_ fixation des ressources ou la génération de \_ \_ mips.

**Non pris en charge :** \_ PARTAGÉ, \_ partagé \_ KEYEDMUTEX, \_ \_ compatible GDI, \_ \_ NTHANDLE partagé, \_ contenu restreint \_ , \_ restreindre \_ les \_ ressources partagées, restreindre le \_ \_ \_ pilote de ressource partagée, service \_ \_ protégé ou \_ pool de mosaïques \_ .

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Indicateurs de liaison pris en charge**
</dt> <dd>

\_ \_ Ressource de nuanceur de liaison d3d11, \_ cible de \_ rendu \_ , \_ \_ stencil de profondeur ou \_ accès non ordonné \_ .

**Non pris en charge :** \_ Mémoire tampon constante \_ , \_ \_ tampon \[ de vertex Notez que la liaison d’une mémoire tampon en mosaïque en tant que SRV/UAV/RTV est toujours OK \] , le tampon d' \_ index, la sortie du \_ \_ flux, le \_ \_ \_ décodeur de liaison ou la liaison de l' \_ \_ \_ encodeur vidéo.

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formats pris en charge**
</dt> <dd>

Tous les formats qui seraient disponibles pour la configuration donnée, quelle que soit la disposition en mosaïque, à quelques exceptions près.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc pris en charge (nombre d’échantillonnages, qualité)**
</dt> <dd>

Tout ce qui serait pris en charge pour la configuration donnée, indépendamment de sa mosaïque, à quelques exceptions près.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Largeur/hauteur prise en charge/Miplevels a/ArraySize**
</dt> <dd>

Étendues complètes prises en charge par Direct3D 11. Les ressources en mosaïque n’ont pas la restriction sur la taille totale de la mémoire imposée sur les ressources non en mosaïque. Les ressources en mosaïque sont limitées par les limites de l’espace d’adressage virtuel global. Pour plus d’informations, consultez [espace d’adressage disponible pour les ressources en mosaïque](address-space-available-for-tiled-resources.md).

</dd> </dl>

Le contenu initial de la mémoire du pool de mosaïques n’est pas défini.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de ressources en mosaïque](creating-tiled-resources.md)
</dt> </dl>

 

 




