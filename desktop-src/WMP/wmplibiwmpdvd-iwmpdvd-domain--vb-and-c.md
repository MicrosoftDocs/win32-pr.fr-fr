---
title: Propriété de domaine IWMPDVD
description: La propriété de domaine obtient le domaine actuel du DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- propriété de domaine lecteur Windows Media
- propriété de domaine lecteur Windows Media, interface IWMPDVD
- Interface IWMPDVD lecteur Windows Media, propriété de domaine
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
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531099"
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
| <dl> <dt>videoManagerMenu</dt> </dl>  | Affichage des menus pour l’ensemble du disque. Également appelé « menu » pour le lecteur Windows Media. Communément appelé le menu du titre ou le menu supérieur.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Affichage des menus pour l’ensemble de titres actuel. Également appelé titleMenu pour Windows Media Player. Communément appelé menu racine.<br/>          |
| <dl> <dt>title</dt> </dl>             | En général, affichage du titre actuel.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.<br/>                                                                                          |
| <dl> <dt>non défini</dt> </dl>         | Le lecteur Windows Media n’est pas dans un domaine DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Notes

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

 

 





