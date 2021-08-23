---
description: Les \_ constantes d’indicateur de bit LINEGENERATETERM décrivent les conditions dans lesquelles la génération de chiffre ou de tonalité est terminée.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Constantes LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c34d119f503c677e5c251bb494c5ea991dbd0fccf0bfbdb3affecf4c4ff1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518969"
---
# <a name="linegenerateterm_-constants"></a>\_Constantes LINEGENERATETERM

Les constantes d’indicateur de bit **LINEGENERATETERM \_** décrivent les conditions dans lesquelles la génération de chiffre ou de tonalité est terminée.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM \_ Annuler**
</dt> <dd> <dl> <dt>



La demande de génération de chiffres ou de tonalités a été annulée par cette application, par une autre application ou par l’appel terminé. Cette valeur peut également être retournée lorsque la génération d’un chiffre ou d’un ton ne peut pas être effectuée en raison d’une défaillance interne du fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ terminé**
</dt> <dd> <dl> <dt>



Le nombre demandé de chiffres ou de tonalités demandés a été généré pour la durée demandée.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




