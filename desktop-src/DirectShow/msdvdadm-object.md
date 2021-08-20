---
description: Objet MSDVDAdm
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: Objet MSDVDAdm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4001def80bff94920996dc627869ffecfd6dda3fbc679be79f2b321ac33a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072973"
---
# <a name="msdvdadm-object"></a>Objet MSDVDAdm

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

> [!Note]  
> Cette API est déconseillée. pour plus d’informations sur la lecture et la navigation des dvd dans DirectShow, consultez [Applications dvd](dvd-applications.md).

 

les méthodes et les propriétés de l' `MSDVDAdm` objet « administration » permettent à une application de script de modifier ses paramètres par défaut dans le registre Microsoft® Windows®. le registre est une base de données sur tous les systèmes de Windows où les applications peuvent stocker des informations sur elles-mêmes pour les utiliser lors de l’initialisation ou au moment de l’exécution.

La plupart de ces méthodes et propriétés ne définissent pas ou ne récupèrent pas les valeurs actuelles dans l’objet [mswebdvd](mswebdvd-object.md) lui-même. Cela signifie, par exemple, que lorsque vous appelez **GetParentalLevel** , la valeur retournée n’est pas le niveau parental actuel stocké dans l’objet. Au lieu de cela, il s’agit du niveau parental par défaut stocké dans le registre. Pour connaître le niveau parental actuel, appelez la  méthode mswebdvd [**GetPlayerParentalLevel**](getplayerparentallevel-method.md). L’appel de [**SaveParentalLevel**](saveparentallevel-method.md) écrit simplement un nouveau niveau d’accès parental par défaut dans le registre ; vous devez toujours appeler la méthode **mswebdvd** [**SelectParentalLevel**](selectparentallevel-method.md) pour que la modification prenne effet immédiatement dans l’objet **mswebdvd** . Les méthodes par défaut des identificateurs de paramètres régionaux (LCID) fonctionnent de la même façon.

En revanche, les méthodes [**BookmarkOnStop**](bookmarkonstop-property.md) et [**BookmarkOnClose**](bookmarkonclose-property.md) prennent effet immédiatement, car l’objet **mswebdvd** vérifie ces paramètres juste avant que l’utilisateur arrête la lecture ou ferme l’application, plutôt que pendant l’initialisation.

Vous accédez à l' `MSDVDAdm` objet par le biais de la propriété **DVDAdm** de **mswebdvd**. Par exemple, si l’objet **mswebdvd** est nommé « DVD », appelez **ChangePassword** comme indiqué dans l’exemple de code suivant.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Méthodes et propriétés**

Le tableau suivant répertorie les méthodes et les propriétés exposées par les méthodes et propriétés de l’objet MSDVDAdm.



| Méthode                                                          | Description                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Enregistre un nouveau mot de passe d’application dans le registre.                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | Enregistre un nouveau niveau parental par défaut dans le registre.                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | Enregistre le nouveau pays ou la nouvelle région parente de l’application dans le registre.                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | Teste si le mot de passe spécifié correspond au mot de passe enregistré précédemment.                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | Récupère le niveau parental précédemment enregistré dans le registre.                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | Récupère le pays ou la région parente qui a été enregistré pour la dernière fois dans le registre.                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | Restaure les paramètres de l’économiseur d’écran système.                                                                                                                                       |
| Propriété                                                        | Description                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | Active ou désactive l’économiseur d’écran du système.                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | Définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux audio.                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | Définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux de sous-image.                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | Définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour les menus.                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | Définit ou récupère une valeur qui indique à l’objet MSDVDAdm s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur clique sur le bouton **arrêter** . |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | Définit ou récupère une valeur qui indique à l’objet MSDVDAdm s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur ferme l’application.     |



 

 

 



