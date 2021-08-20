---
title: WM/Track
description: L’attribut WM/Track contient le numéro de piste du contenu. Cet attribut est de base zéro et est pris en charge pour la compatibilité descendante. Le nouveau contenu doit utiliser l’attribut WM/TrackNumber à la place.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track Windows Media format
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1113fde7b0b29b6f1f7618e9d531df83070725b9e05e70e09f64f93b027abfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026937"
---
# <a name="wmtrack"></a>WM/Track

L’attribut **WM/Track** contient le numéro de piste du contenu. Cet attribut est de base zéro et est pris en charge pour la compatibilité descendante. Le nouveau contenu doit utiliser l’attribut [**WM/TrackNumber**](wm-tracknumber.md) à la place.

## <a name="global-constant"></a>Constante globale

\_wszWMTrack g

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

De nombreuses applications existantes écrivent la valeur de **WM/Track** en tant que **DWORD**. Si vous créez une application qui lit des fichiers provenant de sources inconnues, vous devez inclure du code pour gérer les valeurs de type chaîne et **DWORD** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




