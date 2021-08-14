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
ms.openlocfilehash: d3d638c88505233d479445b05267927f72ae077f9c46c99f9e3713fd2980afdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198407"
---
# <a name="hasaudio"></a>HasAudio

L’attribut **HasAudio** est un attribut de niveau fichier qui spécifie si le fichier contient des flux audio.

## <a name="global-constant"></a>Constante globale

\_wszWMHasAudio g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




