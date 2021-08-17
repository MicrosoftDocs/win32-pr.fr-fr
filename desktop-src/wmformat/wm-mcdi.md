---
title: WM/MCDI
description: L’attribut WM/MCDI contient l’identificateur de CD de musique. Il s’agit d’un vidage binaire de la table des matières à partir du CD qui est utilisé pour identifier de manière unique le CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Format Windows Media WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccf4a081141c1902fe93680937a3196e015e6690acf76d69f3a3d8a016c092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963748"
---
# <a name="wmmcdi"></a>WM/MCDI

L’attribut **WM/MCDI** contient l’identificateur de CD de musique. Il s’agit d’un vidage binaire de la table des matières à partir du CD qui est utilisé pour identifier de manière unique le CD.

## <a name="global-constant"></a>Constante globale

\_wszWMMCDI g

## <a name="data-type"></a>Type de données

**\_binaire de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut est compatible avec le frame ID3, MCDI. La spécification ID3 du frame MCDI nécessite qu’une seule trame de ce type existe pour chaque fichier et qu’une trame TRCK valide existe. L’éditeur de métadonnées n’effectue aucune validation pour ces règles. En outre, la taille de WM/MCDI n’est pas limitée à 804 octets, tout comme le cadre MCDI ID3.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




