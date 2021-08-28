---
title: Paramètres de création d’un pool de vignettes
description: Utilisez les paramètres de cette section pour définir des pools de mosaïques via l’API ID3D11Device CreateBuffer.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7350dc01c845542b97674189a120c0d55db95c282dc80b11fda66230618f99b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119469"
---
# <a name="tile-pool-creation-parameters"></a>Paramètres de création d’un pool de vignettes

Utilisez les paramètres de cette section pour définir des pools de mosaïques via l’API [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) .

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Corps**
</dt> <dd>

Taille d’allocation, en tant que multiple de 64 Ko. 0 est valide, car vous pouvez utiliser ultérieurement une opération [**ID3D11DeviceContext2 :: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) .

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Indicateurs divers des ressources pris en charge**
</dt> <dd>

D3D11 \_ \_ pool de \_ mosaïques divers \_ de ressources (identifie la ressource en tant que pool de MOSAÏQUEs), d3d11 partagé \_ divers de la ressource \_ \_ , \_ \_ KEYEDMUTEX partagé ou \_ \_ NTHANDLE partagé.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilisation des ressources prise en charge**
</dt> <dd>

Utilisation de D3D11 \_ \_ par défaut uniquement.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de ressources en mosaïque](creating-tiled-resources.md)
</dt> </dl>

 

 




