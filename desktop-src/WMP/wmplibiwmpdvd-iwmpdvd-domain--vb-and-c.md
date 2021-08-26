---
title: Propriété de domaine IWMPDVD
description: La propriété de domaine obtient le domaine actuel du DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Lecteur Windows Media de propriété de domaine
- Lecteur Windows Media de propriété de domaine, interface IWMPDVD
- Lecteur Windows Media de l’interface IWMPDVD, propriété de domaine
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b5f382d7c1db820905b45b924105225c0c5b55a569f85707e4e9f729e59596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000469"
---
# <a name="iwmpdvddomain-property"></a>IWMPDVD ::d propriété omaine

La propriété de **domaine** obtient le domaine actuel du DVD.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est l’une des valeurs suivantes.



| Valeur                                                                                        | Signification                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | Exécution de l’initialisation par défaut d’un disque DVD.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Affichage des menus pour l’ensemble du disque. également connu sous le nom de menu de Lecteur Windows Media. Communément appelé le menu du titre ou le menu supérieur.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Affichage des menus pour l’ensemble de titres actuel. également connu sous le nom de titleMenu pour Lecteur Windows Media. Communément appelé menu racine.<br/>          |
| <dl> <dt>title</dt> </dl>             | En général, affichage du titre actuel.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.<br/>                                                                                          |
| <dl> <dt>non défini</dt> </dl>         | Lecteur Windows Media n’est pas dans un domaine DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Remarques

Chaque DVD est créé différemment. Certains DVD ne contiennent pas les domaines firstPlay, videoManagerMenu ou videoTitleSetMenu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





