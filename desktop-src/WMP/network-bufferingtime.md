---
title: Network. bufferingTime
description: La propriété bufferingTime spécifie ou récupère la durée (en millisecondes) allouée à la mise en mémoire tampon des données entrantes avant le début de la diffusion.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Lecteur Windows Media Network. bufferingTime
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afe4a68a7ad1ae8a1444f1e2f31ad09461e05d221e8fceae52960bd5927aac0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901729"
---
# <a name="networkbufferingtime"></a>Network. bufferingTime

La propriété **bufferingTime** spécifie ou récupère la durée (en millisecondes) allouée à la mise en mémoire tampon des données entrantes avant le début de la diffusion.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **bufferingTime**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**) compris entre zéro et 60 000 avec une valeur par défaut de 5 000.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **bufferingTime** pour spécifier le nombre de secondes allouées à la mise en mémoire tampon des données entrantes. Les informations sont récupérées à partir d’un élément d’entrée de texte HTML créé avec ID = "bufText". L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> </dl>

 

 





