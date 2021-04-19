---
title: Settings. rate
description: La propriété rate spécifie ou récupère la vitesse de lecture actuelle des médias vidéo.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Paramètres. Vitesse du lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539638"
---
# <a name="settingsrate"></a>Settings. rate

La propriété **rate** spécifie ou récupère la vitesse de lecture actuelle des médias vidéo.

## <a name="syntax"></a>Syntaxe

Player. Settings. rate

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**double**) avec une valeur par défaut de 1,0.

## <a name="remarks"></a>Notes

Cette propriété agit comme une valeur de multiplicateur qui vous permet de lire un clip à un débit plus rapide ou plus lent. La valeur par défaut 1,0 indique la vitesse créée. Notez qu’une piste audio devient difficile à comprendre à des vitesses inférieures à 0,5 ou supérieures à 1,5. Un taux de lecture de 2 équivaut à deux fois la vitesse de lecture normale.

Le lecteur Windows Media tentera d’utiliser le plus efficace de quatre modes de lecture différents. Il s’agit d’une lecture vidéo en douceur avec un son de conservation, une lecture vidéo en douceur avec un son non géré, une lecture vidéo fluide sans audio et une lecture vidéo d’image clé sans audio. Le mode choisi par le joueur dépend de nombreux facteurs, notamment le type de fichier et l’emplacement, le système d’exploitation, le réseau et le serveur.

D’autres considérations s’appliquent également, en fonction du type de média :

-   Fichiers WMV (Windows Media Format) et ASF : les valeurs optimales pour cette propriété sont comprises entre 1 et 10, ou entre 1 et 10 pour la lecture inversée. Les valeurs comprises entre 0,5 et 1,0 ou de-0,5 à-1,0 peuvent également fonctionner correctement dans les cas où la tonalité audio peut être conservée, par exemple, lors de la lecture de fichiers situés sur l’ordinateur local. Les valeurs avec une magnitude absolue supérieure à 10 sont autorisées, mais elles ne sont pas très explicites.
-   Autres types de médias vidéo : cette propriété peut être comprise entre 0 et 9. Les valeurs négatives ne sont pas autorisées. Les valeurs inférieures à 1 représentent un mouvement lent. Les valeurs supérieures à 9 sont autorisées, mais elles ne sont pas très explicites.

*Contrôles*. la méthode **fastForward** remplace la valeur de **rate** par 5,0, tandis que les *contrôles*. la méthode **fastReverse** change le **taux** sur 5,0.

La vitesse de lecture de certains types de média ne peut pas être modifiée. Utilisez les *paramètres*. méthode **isAvailable** pour déterminer si cette propriété peut être spécifiée pour un élément multimédia particulier.

**Windows Media Player 10 Mobile**: cette propriété accepte ou retourne uniquement les valeurs-5,0, 1,0 ou 5,0.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément SELECT HTML qui permet à l’utilisateur de modifier la vitesse de lecture du média actuel. Les options de sélection offrent des taux de lecture à vitesse normale, à demi-vitesse et à vitesse double. L’objet **Player** a été créé avec ID = "Player".


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. fastReverse**](controls-fastreverse.md)
</dt> <dt>

[**Settings (objet)**](settings-object.md)
</dt> <dt>

[**Settings. isAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





