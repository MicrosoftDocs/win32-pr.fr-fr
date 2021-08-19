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
ms.openlocfilehash: 028207ee152acac289da6608c682f5fc14a4fde69603a2aae05b841d0cfb46ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027947"
---
# <a name="currentbitrate"></a>CurrentBitrate

L’attribut CurrentBitrate contient la vitesse de transmission totale actuelle des flux actifs dans le fichier.

## <a name="global-constant"></a>Constante globale

\_wszWMCurrentBitrate g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut codé.

La valeur récupérée pour **CurrentBitrate** est différente selon l’objet utilisé. Dans le lecteur ou l’objet lecteur synchrone, la valeur est la vitesse de transmission réelle au moment de l’appel. Dans l’objet de l’éditeur de métadonnées, la valeur correspond à la vitesse de transmission moyenne du fichier.

La vitesse de transmission réelle d’un fichier est égale à la vitesse de transmission de tous les flux actifs, plus une surcharge. il s’agit de la valeur qui est, par exemple, affichée lors de la création d’un fichier avec le Lecteur Windows Media.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




