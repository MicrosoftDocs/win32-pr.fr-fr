---
title: interface IWMPError (VB et C) (Wmp. h)
description: Fournit des propriétés et des méthodes permettant d’accéder à une collection d’interfaces IWMPErrorItem pour la récupération des informations d’erreur. L’interface IWMPError expose les propriétés suivantes.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- interface IWMPError (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPError (VB et C), description
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
ms.openlocfilehash: 5f3ff7635e423d70447e371d61fbbadf02aa14c2476e118be79cbb25d974348b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736179"
---
# <a name="iwmperror-vb-and-c-interface"></a>interface IWMPError (VB et C#)

Fournit des propriétés et des méthodes permettant d’accéder à une collection d’interfaces **IWMPErrorItem** pour la récupération des informations d’erreur.

L’interface **IWMPError** expose les propriétés suivantes.

## <a name="members"></a>Membres

l’interface **IWMPError (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPError (VB et C#)** possède ces méthodes.



| Méthode                                                                         | Description                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearErrorQueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | Efface les erreurs de la file d’attente des erreurs.<br/>                                                                                            |
| [**aide à la**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | ouvre la page d’aide Web de Microsoft Lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente d’erreurs.<br/> |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPError (VB et C#)** a ces propriétés.



| Propriété                                                                        | Type d’accès           | Description                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | Lecture seule<br/>  | Obtient le nombre d’erreurs dans la file d’attente d’erreurs.<br/>                                                                            |
| [**Élément**](iwmperror-item--vb-and-c.md)<br/>                             | Lecture/écriture<br/> | Obtient une interface **IWMPErrorItem** à l’index spécifié dans la file d’attente d’erreurs. En C#, il s’agit de la méthode d' **extraction d' \_ élément** .<br/> |



 

Procurez-vous une interface **IWMPError** à l’aide de la propriété suivante.



| Object                                                                   | Propriété                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [Objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Erreur**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPErrorItem (VB et C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





