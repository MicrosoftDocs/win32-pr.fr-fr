---
title: External. Play, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. la méthode play demande à Lecteur Windows Media de lire un ensemble d’éléments multimédias.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- play, méthode Lecteur Windows Media
- méthode play Lecteur Windows Media, classe externe
- External, classe Lecteur Windows Media, méthode play
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90644b357e56f40bfbdb576908b99aa6941f8153dc339daa996152f63d77372c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648629"
---
# <a name="externalplay-method"></a>External. Play, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

la méthode **play** demande à Lecteur Windows Media de lire un ensemble d’éléments multimédias.

## <a name="syntax"></a>Syntaxe


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LibraryLocationType* \[ dans\]
</dt> <dd>

[Constante d’emplacement de bibliothèque](library-location-constants.md) qui spécifie le type des éléments multimédias à lire. Par exemple, CPAlbumID spécifie qu’un ou plusieurs albums doivent être lus.

</dd> <dt>

*LibraryLocationIDs* \[ dans\]
</dt> <dd>

**Chaîne** contenant les identificateurs, délimités par des points-virgules, des éléments multimédias à lire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





