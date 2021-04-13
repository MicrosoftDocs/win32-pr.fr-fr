---
title: Duration
description: L’attribut duration contient la durée d’exécution du fichier, en unités de 100 nanosecondes.
ms.assetid: 1d72f826-4087-45f5-a5b9-f31c4e98e9b1
keywords:
- Durée Windows Media format
topic_type:
- apiref
api_name:
- Duration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ea9763bf505394f231ebe7d50943f4336e244c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313102"
---
# <a name="duration"></a>Duration

L’attribut **Duration** contient la durée d’exécution du fichier, en unités de 100 nanosecondes.

## <a name="global-constant"></a>Constante globale

\_wszWMDuration g

## <a name="data-type"></a>Type de données

**\_type WMT \_ QWord**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




