---
title: DVD. domaine
description: La propriété de domaine récupère le domaine actuel du DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. domain Lecteur Windows Media
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0db8e6e212fec11de5f3619c2c1f97a90f579b34515983b0384d0d08ab0ff60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651169"
---
# <a name="dvddomain"></a>DVD. domaine

La propriété de **domaine** récupère le domaine actuel du DVD.

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule qui contient l’une des valeurs suivantes.



| String            | Description                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| firstPlay         | Exécution de l’initialisation par défaut d’un disque DVD.                                                                                      |
| videoManagerMenu  | Affichage des menus pour l’ensemble du disque. également connu sous le nom de menu de Lecteur Windows Media. Communément appelé le menu du titre ou le menu supérieur. |
| videoTitleSetMenu | Affichage des menus pour le jeu de titres actuel. également connu sous le nom de titleMenu pour Lecteur Windows Media. Communément appelé menu racine.              |
| title             | Affiche généralement le titre actuel.                                                                                                 |
| stop              | Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.                                                                                          |
| non défini         | Le lecteur n’est pas dans un domaine DVD.                                                                                                      |



 

## <a name="remarks"></a>Remarques

Chaque DVD est créé différemment. Certains DVD ne contiennent pas les domaines firstPlay, videoManagerMenu ou videoTitleSetMenu.

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours une chaîne vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| Version<br/>                  | Lecteur Windows Media pour Windows XP ou version ultérieure<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DVD**](dvd-object.md)
</dt> </dl>

 

 





