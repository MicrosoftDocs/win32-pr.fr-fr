---
title: Attributs de synchronisation
description: les attributs Sync01 via Sync16 sont des représentations sous forme de chaîne de valeurs 32 bits que Lecteur Windows Media utilise lorsqu’il synchronise des listes de lecture avec un maximum de 16 périphériques portables.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- attributs de synchronisation Lecteur Windows Media
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e720598b17db6b073524d80afc8f39dd6e6f87e777246b5bdb60294b161fa1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134752"
---
# <a name="sync-attributes"></a>Attributs de synchronisation

les attributs **Sync01** via **Sync16** sont des représentations sous forme de chaîne de valeurs 32 bits que Lecteur Windows Media utilise lorsqu’il synchronise des listes de lecture avec un maximum de 16 périphériques portables.

## <a name="applies-to"></a>S'applique à

-   [Sélections](playlist-attributes-ref.md)

## <a name="remarks"></a>Remarques

Il s’agit d’attributs en lecture/écriture. la valeur zéro indique que Lecteur Windows Media ne doit pas synchroniser la playlist avec l’appareil associé. Une valeur supérieure à zéro indique une priorité de synchronisation pour la sélection donnée.

en fonction de l’entrée de l’utilisateur, Lecteur Windows Media définit cet attribut pour chacune des sélections dans la bibliothèque. lorsque Lecteur Windows Media tente de synchroniser une playlist avec un appareil mobile, il examine chaque playlist pour comparer les valeurs des attributs **Sync**_XX_ qui représentent le partenariat de l’appareil. Les sélections qui ont des valeurs de **synchronisation**_XX_ inférieures reçoivent une priorité de synchronisation supérieure.

Par exemple, la bibliothèque peut contenir les quatre sélections suivantes et les valeurs de **synchronisation**_XX_ respectives :



| Nom de la sélection | Valeur Sync01 |
|---------------|--------------|
| GymMusic. WPL  | 0x0000000D   |
| Assouplissez. WPL     | 0x00000020   |
| DriveHome. WPL | 0x00000001   |
| NoGo. WPL      | 0x00000000   |



 

lorsque Lecteur Windows Media synchronise l’appareil associé à l’attribut, il synchronise les playlists dans l’ordre suivant :

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

 

 





