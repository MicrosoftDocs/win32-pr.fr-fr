---
title: Is_Protected
description: L' \_ attribut is protected est un attribut de niveau fichier qui spécifie si le contenu du fichier a été protégé à l’aide de la gestion des droits numériques (DRM).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Format Windows Media Is_Protected
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511272"
---
# <a name="is_protected"></a>Est \_ protégé

L’attribut **is \_ protected** est un attribut de niveau fichier qui spécifie si le contenu du fichier a été protégé à l’aide de la gestion des droits numériques (DRM).

## <a name="global-constant"></a>Constante globale

\_wszWMProtected g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé. La récupération de cette propriété fournit les mêmes informations que l’appel de [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




