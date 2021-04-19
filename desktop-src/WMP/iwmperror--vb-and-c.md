---
title: Interface IWMPError (VB et C) (WMP. h)
description: Fournit des propriétés et des méthodes permettant d’accéder à une collection d’interfaces IWMPErrorItem pour la récupération des informations d’erreur. L’interface IWMPError expose les propriétés suivantes.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- IWMPError (VB et C) interface Windows Media Player
- Interface IWMPError (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPError (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289a39093c38e7a4b0cc43cb8f318e321ae8ef53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541333"
---
# <a name="iwmperror-vb-and-c-interface"></a>Interface IWMPError (VB et C#)

Fournit des propriétés et des méthodes permettant d’accéder à une collection d’interfaces **IWMPErrorItem** pour la récupération des informations d’erreur.

L’interface **IWMPError** expose les propriétés suivantes.

## <a name="members"></a>Membres

L’interface **IWMPError (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPError (VB et C#)** possède ces méthodes.



| Méthode                                                                         | Description                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearErrorQueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | Efface les erreurs de la file d’attente des erreurs.<br/>                                                                                            |
| [**aide à la**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | Ouvre la page d’aide Web du lecteur Microsoft Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente d’erreurs.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPError (VB et C#)** a ces propriétés.



| Propriété                                                                        | Type d’accès           | Description                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | Lecture seule<br/>  | Obtient le nombre d’erreurs dans la file d’attente d’erreurs.<br/>                                                                            |
| [**Élément**](iwmperror-item--vb-and-c.md)<br/>                             | Lecture/écriture<br/> | Obtient une interface **IWMPErrorItem** à l’index spécifié dans la file d’attente d’erreurs. En C#, il s’agit de la méthode d' **extraction d' \_ élément** .<br/> |



 

Procurez-vous une interface **IWMPError** à l’aide de la propriété suivante.



| Object                                                                   | Propriété                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [Objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Error**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPErrorItem (VB et C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





