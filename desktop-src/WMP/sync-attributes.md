---
title: Attributs de synchronisation
description: Les attributs Sync01 via Sync16 sont des représentations sous forme de chaîne de valeurs 32 bits que le lecteur Windows Media utilise lorsqu’il synchronise des sélections avec un maximum de 16 périphériques portables.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Attributs de synchronisation lecteur Windows Media
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528031"
---
# <a name="sync-attributes"></a>Attributs de synchronisation

Les attributs **Sync01** via **Sync16** sont des représentations sous forme de chaîne de valeurs 32 bits que le lecteur Windows Media utilise lorsqu’il synchronise des sélections avec un maximum de 16 périphériques portables.

## <a name="applies-to"></a>S'applique à

-   [Sélections](playlist-attributes-ref.md)

## <a name="remarks"></a>Notes

Il s’agit d’attributs en lecture/écriture. La valeur zéro indique que le lecteur Windows Media ne doit pas synchroniser la playlist avec l’appareil associé. Une valeur supérieure à zéro indique une priorité de synchronisation pour la sélection donnée.

En fonction de l’entrée de l’utilisateur, le lecteur Windows Media définit cet attribut pour chacune des sélections dans la bibliothèque. Lorsque le lecteur Windows Media tente de synchroniser une sélection avec un appareil mobile, il examine chaque playlist pour comparer les valeurs des attributs **Sync**_XX_ qui représentent le partenariat de l’appareil. Les sélections qui ont des valeurs de **synchronisation**_XX_ inférieures reçoivent une priorité de synchronisation supérieure.

Par exemple, la bibliothèque peut contenir les quatre sélections suivantes et les valeurs de **synchronisation**_XX_ respectives :



| Nom de la sélection | Valeur Sync01 |
|---------------|--------------|
| GymMusic. WPL  | 0x0000000D   |
| Assouplissez. WPL     | 0x00000020   |
| DriveHome. WPL | 0x00000001   |
| NoGo. WPL      | 0x00000000   |



 

Lorsque le lecteur Windows Media synchronise l’appareil associé à l’attribut, il synchronise les sélections dans l’ordre suivant :

1.  DriveHome. WPL
2.  GymMusic. WPL
3.  Assouplissez. WPL

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**Énumération des sélections de synchronisation**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





