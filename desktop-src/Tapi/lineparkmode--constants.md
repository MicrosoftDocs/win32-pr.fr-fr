---
description: Les \_ constantes d’indicateur de bit LINEPARKMODE décrivent différentes façons de faire des appels de parking.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Constantes LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528945"
---
# <a name="lineparkmode_-constants"></a>\_Constantes LINEPARKMODE

Les constantes d’indicateur de bit **LINEPARKMODE \_** décrivent différentes façons de faire des appels de parking.

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ dirigé**
</dt> <dd> <dl> <dt>



Spécifie le parc d’appels dirigés. L’adresse à laquelle l’appel doit être parqué doit être fournie au commutateur.


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE \_ INdirect**
</dt> <dd> <dl> <dt>



Spécifie un parc d’appels indirect. L’adresse où l’appel est parqué est sélectionnée par le commutateur et fournie par le commutateur à l’application.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Les **\_ constantes LINEPARKMODE** sont utilisées lors du stationnement d’un appel. Consultez les fonctionnalités de l’appareil adresse d’une ligne pour savoir quel mode de parc est disponible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




