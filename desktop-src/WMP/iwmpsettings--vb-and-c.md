---
title: Interface IWMPSettings (VB et C) (WMP. h)
description: Fournit des propriétés et des méthodes qui obtiennent ou définissent les valeurs des paramètres du lecteur Windows Media. L’interface IWMPSettings expose les propriétés suivantes.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- IWMPSettings (VB et C) interface Windows Media Player
- Interface IWMPSettings (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPSettings (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db911cc6d18ba40777e77a803480c7fcab4ff8ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540412"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>Interface IWMPSettings (VB et C#)

Fournit des propriétés et des méthodes qui obtiennent ou définissent les valeurs des paramètres du lecteur Windows Media.

L’interface **IWMPSettings** expose les propriétés suivantes.

## <a name="members"></a>Membres

L’interface **IWMPSettings (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPSettings (VB et C#)** possède ces méthodes.



| Méthode                                                               | Description                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Retourne une valeur indiquant si le mode de boucle ou le mode de lecture aléatoire est actif.<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Définit le mode de boucle ou le mode de lecture aléatoire (actif ou inactif).<br/>               |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPSettings (VB et C#)** a ces propriétés.



| Propriété                                                                                              | Type d’accès           | Description                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Démarrage automatique**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement. <br/>                                     |
| [**équilibrée**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Lecture/écriture<br/> | Obtient ou définit le solde stéréo actuel.<br/>                                                                                          |
| [**baseURL**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Lecture/écriture<br/> | Obtient ou définit l’URL de base utilisée pour la résolution de chemin d’accès relative avec les commandes de script d’URL incorporées dans le contenu multimédia numérique. <br/> |
| [**defaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Lecture/écriture<br/> | Obtient ou définit le nom du frame utilisé pour afficher une URL qui est reçue dans un événement **commande** . <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Lecture/écriture<br/> | Obtient ou définit une valeur indiquant si les boîtes de dialogue d’erreur s’affichent automatiquement.<br/>                                           |
| [**invokeURLs**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit une valeur indiquant si les événements d’URL doivent lancer un navigateur Web. <br/>                                                  |
| [**isAvailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Lecture seule<br/>  | Obtient une valeur indiquant si une action spécifiée peut être exécutée. En C#, il s’agit de la méthode d' **extraction de \_ isAvailable** .<br/>             |
| [**muette**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Lecture/écriture<br/> | Obtient ou définit une valeur indiquant si l’audio est muet. <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit le nombre de fois qu’un élément multimédia doit être lu. <br/>                                                                         |
| [**évaluation**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Lecture/écriture<br/> | Obtient ou définit la vitesse de lecture actuelle pour la vidéo. <br/>                                                                                |
| [**agrégat**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Lecture/écriture<br/> | Obtient ou définit le volume de lecture actuel. <br/>                                                                                        |



 

Procurez-vous une interface **IWMPSettings** à l’aide de la propriété suivante.



| Object                                                                   | Propriété                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Paramètres**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPSettings2 (VB et C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





