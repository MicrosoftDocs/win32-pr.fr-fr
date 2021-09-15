---
title: HasAudio
description: L’attribut HasAudio est un attribut de niveau fichier qui spécifie si le fichier contient des flux audio.
ms.assetid: 104c9634-611b-4cd9-8493-cfdaddd49b72
keywords:
- Format Windows Media HasAudio
topic_type:
- apiref
api_name:
- HasAudio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0930ffea67ee100528cf9d592a25f98aa6c92a55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294446"
---
# <a name="hasaudio"></a>HasAudio

L’attribut **HasAudio** est un attribut de niveau fichier qui spécifie si le fichier contient des flux audio.

## <a name="global-constant"></a>Constante globale

\_wszWMHasAudio g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




