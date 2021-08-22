---
title: ClosedCaption.captioningID
description: La propriété captioningID spécifie ou récupère le nom de l’élément affichant le sous-titrage.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- ClosedCaption. captioningID Lecteur Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da667e5479cc33312375920c1d573f0e2c19607b2399ff6f4fe34b130ca61e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580987"
---
# <a name="closedcaptioncaptioningid"></a>ClosedCaption.captioningID

La propriété **captioningID** spécifie ou récupère le nom de l’élément affichant le sous-titrage.

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Le nom d’élément spécifié peut être n’importe quel élément HTML dans la page Web, à condition qu’il prenne en charge l’attribut innerHTML. Si la page Web contient plusieurs frames, le nom de l’élément ne peut faire référence qu’à un élément du même frame que le contrôle du lecteur.

**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule et retourne toujours une chaîne vide.

## <a name="examples"></a>Exemples

l’exemple de JScript Microsoft suivant utilise *ClosedCaption*. **captioningID** pour choisir la zone d’une page Web utilisée pour afficher les sous-titres. Deux éléments HTML DIV ont été créés, respectivement avec ID = CC1 et ID = CC2. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objet ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





