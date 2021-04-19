---
description: Les \_ constantes d’indicateur de bit LINEGATHERTERM décrivent les conditions dans lesquelles la collecte de chiffres mis en mémoire tampon est terminée.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Constantes LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541540"
---
# <a name="linegatherterm_-constants"></a>\_Constantes LINEGATHERTERM

Les constantes d’indicateur de bit **LINEGATHERTERM \_** décrivent les conditions dans lesquelles la collecte de chiffres mis en mémoire tampon est terminée.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**
</dt> <dd> <dl> <dt>



Le nombre de chiffres demandé a été collecté. La mémoire tampon est saturée.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ Annuler**
</dt> <dd> <dl> <dt>



La demande a été annulée par cette application, par une autre application ou par l’appel terminé.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**
</dt> <dd> <dl> <dt>



Le premier chiffre d’expiration a expiré. La mémoire tampon ne contient pas de chiffres.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM \_ INTERtimeout**
</dt> <dd> <dl> <dt>



Le délai d’expiration inter-chiffres est arrivé à expiration. La mémoire tampon contient au moins un chiffre.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**
</dt> <dd> <dl> <dt>



L’un des chiffres de fin correspond à un chiffre reçu. Le chiffre d’arrêt mis en correspondance est le dernier chiffre dans la mémoire tampon.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




