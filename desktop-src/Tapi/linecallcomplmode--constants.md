---
description: Les \_ constantes d’indicateur de bit LINECALLCOMPLMODE décrivent les différentes façons dont un appel peut être effectué.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Constantes LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43f76c9b8012f9ecb60c6b0ffd787d5a0bad87794eb833cc4095c276ba983f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761753"
---
# <a name="linecallcomplmode_-constants"></a>\_Constantes LINECALLCOMPLMODE

Les constantes d’indicateur de bit **LINECALLCOMPLMODE \_** décrivent les différentes façons dont un appel peut être effectué.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_rappel LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Demande à la station appelée de retourner l’appel lorsqu’elle retourne à inactif.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ CAMPON**
</dt> <dd> <dl> <dt>



Met l’appel en file d’attente jusqu’à ce que l’appel puisse être effectué.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ intrus**
</dt> <dd> <dl> <dt>



Ajoute l’application à l’appel existant à la station appelée (chaland dans).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_message LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Conserve un bref message prédéfini pour la station appelée (laisser le mot appelé). Le message à envoyer est spécifié séparément.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




