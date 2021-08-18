---
description: Les \_ constantes d’indicateur de bit LINEADDRESSSHARING décrivent les différentes façons dont une adresse peut être partagée entre les lignes.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Constantes LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fe92c92efd75a4f6e731944c487acff2ffd70e173dd04b03244ec9d55e8aba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003127"
---
# <a name="lineaddresssharing_-constants"></a>\_Constantes LINEADDRESSSHARING

Les constantes d’indicateur de bit **LINEADDRESSSHARING \_** décrivent les différentes façons dont une adresse peut être partagée entre les lignes.

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ privé**
</dt> <dd> <dl> <dt>



L’adresse est privée pour la ligne de l’utilisateur ; elle n’est attribuée à aucune autre station.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**
</dt> <dd> <dl> <dt>



L’adresse est reliée à une ou plusieurs autres stations. La première ligne permettant d’activer un appel sur la ligne aura un accès exclusif à l’adresse et aux appels qui peuvent exister sur celle-ci. Les autres lignes ne pourront pas utiliser l’adresse de pont lorsqu’elle est en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**
</dt> <dd> <dl> <dt>



L’adresse est reliée à une ou plusieurs autres stations. La première ligne pour activer un appel sur la ligne aura uniquement un accès exclusif à l’appel correspondant. Les autres applications qui utilisent l’adresse entraînent des apparences d’appel nouvelles et séparées.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**
</dt> <dd> <dl> <dt>



L’adresse est reliée par une ou plusieurs autres lignes. Toutes les parties de pont peuvent partager des appels sur l’adresse, qui fonctionne alors comme une conférence.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ surveillé**
</dt> <dd> <dl> <dt>



Il s’agit d’une adresse dont l’état inactif/occupé est rendu disponible pour cette ligne.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

Le mode de partage d’une adresse entre les lignes peut affecter le comportement de cette adresse. [**Ligne \_**](line-callstate.md) Les messages CALLSTATE et [**line \_ ADDRESSSTATE**](line-addressstate.md) sont envoyés à l’application en réponse aux activités des stations de pontage. Ces messages permettent à une application d’effectuer le suivi de l’état de l’adresse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ADDRESSSTATE de ligne \_**](line-addressstate.md)
</dt> <dt>

[**CALLSTATE de ligne \_**](line-callstate.md)
</dt> </dl>

 

 




