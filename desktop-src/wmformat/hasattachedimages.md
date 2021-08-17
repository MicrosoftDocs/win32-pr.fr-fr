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
ms.openlocfilehash: 46ec38d0961ffc6ffc50434cdecf69e6dde663dfeaff5e331455a9575b3426e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930859"
---
# <a name="hasattachedimages"></a>HasAttachedImages

L’attribut **HasAttachedImages** est un attribut de niveau fichier qui spécifie si le fichier est un fichier mp3 avec des frames ID3 APIC attachés.

## <a name="global-constant"></a>Constante globale

\_wszWMHasAttachedImages g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

**HasAttachedImages** a été conçu pour informer une application que des images étaient présentes afin qu’elles puissent être récupérées à l’aide de l’interface [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) . Maintenant que les images sont prises en charge à l’aide de l’attribut [**WM/Picture**](wmpicture.md) , **HasAttachedImages** n’est plus nécessaire.

Pour déterminer si un fichier contient des images, appelez [**IWMHeaderInfo3 :: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) en spécifiant l’attribut **WM/Picture** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




