---
title: HasAttachedImages
description: L’attribut HasAttachedImages est un attribut de niveau fichier qui spécifie si le fichier est un fichier MP3 avec des frames ID3 APIC attachés.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Format Windows Media HasAttachedImages
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509835"
---
# <a name="hasattachedimages"></a>HasAttachedImages

L’attribut **HasAttachedImages** est un attribut de niveau fichier qui spécifie si le fichier est un fichier mp3 avec des frames ID3 APIC attachés.

## <a name="global-constant"></a>Constante globale

\_wszWMHasAttachedImages g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

**HasAttachedImages** a été conçu pour informer une application que des images étaient présentes afin qu’elles puissent être récupérées à l’aide de l’interface [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) . Maintenant que les images sont prises en charge à l’aide de l’attribut [**WM/Picture**](wmpicture.md) , **HasAttachedImages** n’est plus nécessaire.

Pour déterminer si un fichier contient des images, appelez [**IWMHeaderInfo3 :: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) en spécifiant l’attribut **WM/Picture** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




