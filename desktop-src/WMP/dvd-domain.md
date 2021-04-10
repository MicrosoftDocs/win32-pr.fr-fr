---
title: DVD. domaine
description: La propriété de domaine récupère le domaine actuel du DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. domaine lecteur Windows Media
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
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317214"
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
| videoManagerMenu  | Affichage des menus pour l’ensemble du disque. Également appelé « menu » pour le lecteur Windows Media. Communément appelé le menu du titre ou le menu supérieur. |
| videoTitleSetMenu | Affichage des menus pour le jeu de titres actuel. Également appelé titleMenu pour Windows Media Player. Communément appelé menu racine.              |
| title             | Affiche généralement le titre actuel.                                                                                                 |
| stop              | Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.                                                                                          |
| non défini         | Le lecteur n’est pas dans un domaine DVD.                                                                                                      |



 

## <a name="remarks"></a>Notes

Chaque DVD est créé différemment. Certains DVD ne contiennent pas les domaines firstPlay, videoManagerMenu ou videoTitleSetMenu.

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours une chaîne vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Version<br/>                  | Lecteur Windows Media pour Windows XP ou version ultérieure<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DVD**](dvd-object.md)
</dt> </dl>

 

 





