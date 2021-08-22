---
title: Événement DomainChange de l’objet AxWindowsMediaPlayer
description: L’événement DomainChange se produit lorsque le domaine DVD change. | Événement DomainChange de l’objet AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- événement DomainChange de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37f10679225fb893fad8bcf6fc6687021256e305e8c5a08e6ebe96d16b74e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136122"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Événement DomainChange de l’objet AxWindowsMediaPlayer

L’événement DomainChange se produit lorsque le domaine DVD change.

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété  | Description                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| strDomain | System. StringIndicates le nouveau domaine. Pour connaître les valeurs possibles, consultez la section Notes.<br/> |



 

## <a name="remarks"></a>Remarques

Le tableau suivant indique les valeurs possibles pour la propriété strDomain.



| String            | Description                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | Exécution de l’initialisation par défaut d’un disque DVD.                     |
| videoManagerMenu  | Affichage des menus pour la totalité du disque. Également appelé menu racine ou menu principal. |
| videoTitleSetMenu | Affichage des menus pour le jeu de titres actuel. Également appelé titleMenu.     |
| title             | Affichage du titre actuel.                                        |
| stop              | Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





