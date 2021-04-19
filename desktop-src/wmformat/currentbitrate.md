---
title: CurrentBitrate
description: L’attribut CurrentBitrate contient la vitesse de transmission totale actuelle des flux actifs dans le fichier.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Format Windows Media CurrentBitrate
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106543042"
---
# <a name="currentbitrate"></a>CurrentBitrate

L’attribut CurrentBitrate contient la vitesse de transmission totale actuelle des flux actifs dans le fichier.

## <a name="global-constant"></a>Constante globale

\_wszWMCurrentBitrate g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

La valeur récupérée pour **CurrentBitrate** est différente selon l’objet utilisé. Dans le lecteur ou l’objet lecteur synchrone, la valeur est la vitesse de transmission réelle au moment de l’appel. Dans l’objet de l’éditeur de métadonnées, la valeur correspond à la vitesse de transmission moyenne du fichier.

La vitesse de transmission réelle d’un fichier est égale à la vitesse de transmission de tous les flux actifs, plus une surcharge. Il s’agit de la valeur qui, par exemple, est affichée lors de la lecture d’un fichier avec le lecteur Windows Media.

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




