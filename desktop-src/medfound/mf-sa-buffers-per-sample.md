---
description: Spécifie le nombre de mémoires tampons créées par l’allocateur d’échantillon vidéo pour chaque échantillon vidéo.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: Attribut MF_SA_BUFFERS_PER_SAMPLE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6b54cc5b2589649c954d9f2f41923af04fdf4aa7c00714067bee0b11dabbee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740366"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>\_Tampons sa de l' \_ exemple MF \_ par \_ attribut

Spécifie le nombre de mémoires tampons créées par l’allocateur d’échantillon vidéo pour chaque échantillon vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Si vous utilisez l’interface [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) pour allouer des exemples vidéo, vous pouvez utiliser cet attribut pour créer des exemples vidéo qui contiennent plusieurs mémoires tampons. Par exemple, si la valeur de l’attribut est 2, l’allocateur crée deux mémoires tampons vidéo pour chaque échantillon vidéo. Définissez l’attribut dans le paramètre *pAttributes* de la méthode [**IMFVideoSampleAllocatorEx :: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

La valeur par défaut est 1. Si l’attribut n’est pas défini, l’allocateur crée des exemples vidéo qui contiennent une seule mémoire tampon par échantillon.

Cet attribut est principalement destiné aux transformations Media Foundation (MFTs) qui prennent en charge la sortie stéréo 3D, dans la situation suivante :

-   La table MFT prend en charge Microsoft DirectX Graphics infrastructure (DXGI).
-   La table MFT alloue ses propres exemples de sortie.
-   La table MFT utilise l’interface [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) pour allouer les exemples de sortie.
-   Le format vidéo 3D utilise une mémoire tampon distincte pour chaque vue.

Si tous ces critères sont vrais, la table MFT doit définir la valeur de l’attribut sur 2 (une mémoire tampon par vue).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




