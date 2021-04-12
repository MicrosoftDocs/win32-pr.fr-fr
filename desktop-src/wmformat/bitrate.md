---
title: Bitrate
description: L’attribut de débit binaire est un attribut de niveau fichier qui contient la vitesse de transmission du fichier en bits par seconde.
ms.assetid: 35da0735-db39-4463-8dad-451a77a171b6
keywords:
- Débit Windows Media au format binaire
topic_type:
- apiref
api_name:
- Bitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc5a4711c6fa694735a298f5a884e21120eedd5c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313078"
---
# <a name="bitrate"></a>Bitrate

L’attribut de **débit binaire** est un attribut de niveau fichier qui contient la vitesse de transmission du fichier en bits par seconde.

## <a name="global-constant"></a>Constante globale

\_wszWMBitrate g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




