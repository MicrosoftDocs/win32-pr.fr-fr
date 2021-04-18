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
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106522631"
---
# <a name="wmmcdi"></a>WM/MCDI

L’attribut **WM/MCDI** contient l’identificateur de CD de musique. Il s’agit d’un vidage binaire de la table des matières à partir du CD qui est utilisé pour identifier de manière unique le CD.

## <a name="global-constant"></a>Constante globale

\_wszWMMCDI g

## <a name="data-type"></a>Type de données

**\_binaire de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est compatible avec le frame ID3, MCDI. La spécification ID3 du frame MCDI nécessite qu’une seule trame de ce type existe pour chaque fichier et qu’une trame TRCK valide existe. L’éditeur de métadonnées n’effectue aucune validation pour ces règles. En outre, la taille de WM/MCDI n’est pas limitée à 804 octets, tout comme le cadre MCDI ID3.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




