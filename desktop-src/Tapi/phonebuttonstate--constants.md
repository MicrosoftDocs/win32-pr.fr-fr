---
description: Les constantes d’indicateur de bit PHONEBUTTONSTATE décrivent les positions des boutons.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Constantes PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011072"
---
# <a name="phonebuttonstate_-constants"></a>Constantes PHONEBUTTONSTATE_

Les constantes d’indicateur de bit **PHONEBUTTONSTATE_** décrivent les positions du bouton.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



Le bouton est à l’état « enfoncé » (enfoncé).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Indique que l’État haut ou de l’état enfoncé du bouton n’est pas connu du fournisseur de services et qu’il ne sera pas connu à un moment ultérieur. (TAPI versions 1,4 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Indique que l’État en haut ou en aval du bouton n’est pas connu pour l’instant, mais peut devenir connu à un moment ultérieur. (TAPI versions 1,4 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



Le bouton est à l’État « haut ».


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur le téléphone et de ne pas utiliser ces PHONEBUTTONSTATE_ valeurs que la version négociée ne prend pas en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




