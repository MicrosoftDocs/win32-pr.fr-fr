---
description: La numérotation prédictive est une application qui s’exécute généralement sur un serveur de téléphonie du centre d’appels.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Numérotation prédictive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576ebffff5d4b9925fd50ecce082e4f515065c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521890"
---
# <a name="predictive-dialing"></a>Numérotation prédictive

La numérotation prédictive est une application qui s’exécute généralement sur un serveur de téléphonie du centre d’appels. Elle utilise une liste de numéros de téléphone, souvent obtenue à partir d’une base de données, pour tenter d’effectuer des appels sortants. Lorsqu’un appel est *terminé*, l’appel est automatiquement affecté à un agent à des fins de gestion. L’application peut utiliser un port de *numérotation prédictif* sur un commutateur, qui est un appareil qui peut effectuer des appels sortants et qui a des capacités spéciales (par le biais de DSP, etc.) pour détecter les tonalités de progression des appels et d’autres indications audibles de l’état d’appel. Lorsqu’un appel est effectué sur un port de numérotation prédictif, en général, il est automatiquement transféré à un autre appareil sur le commutateur lorsque l’appel atteint un état particulier ou lors de la détection d’un type de média particulier. Cet appareil cible peut être une file d’attente pour les agents gérant les appels sortants.

Les applications identifient un appareil comme disposant d’une fonctionnalité de numérotation prédictive par le \_ bit LINEADDRCAPFLAGS PREDICTIVEDIALER dans le membre **DwAddrCapFlags** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). Le membre **dwPredictiveAutoTransferStates** dans **LINEADDRESSCAPS** indique les États sur lesquels le port de numérotation prédictif peut être utilisé pour transférer automatiquement un appel ; Si ce membre est égal à zéro, il indique que le transfert automatique n’est pas disponible et qu’il est de la responsabilité de l’application de transférer les appels explicitement sur la détection de l’état d’appel approprié (ou du type de média ou d’autres critères). De préférence, les fabricants de commutateurs rendent disponibles le transfert automatique et manuel, et permettent aux applications de sélectionner le mécanisme préféré, mais les fournisseurs de services doivent modéliser le comportement de l’équipement hérité. Un port de numérotation prédictif unique (périphérique de ligne/adresse) peut prendre en charge plusieurs appels sortants simultanément, comme indiqué par le membre **dwMaxNumActiveCalls** dans **LINEADDRESSCAPS**. La fonctionnalité de numérotation prédictive peut également être mise à la disposition de n’importe quel appareil, à l’aide d’un pool partagé de processeurs de signal de numérotation prédictifs, qui sont reliés à la ligne en cours de numérotation sur demande.

Lorsque la fonction [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) est utilisée sur une ligne qui prend en charge la numérotation prédictive (un port avec le \_ jeu de PREDICTIVEDIALER LINEADDRCAPFLAGS) et la numérotation prédictive est demandée à l’aide de LINECALLPARAMFLAGS \_ PREDICTIVEDIAL, l’appel est effectué de manière prédictive avec la détection de progression de l’appel audible améliorée. Les champs et constantes supplémentaires sont définis dans la structure [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) transmise à **lineMakeCall** pour contrôler le comportement du port de numérotation prédictif. Le membre **dwPredictiveAutoTransferStates** indique que l’appel de ligne indique que, lors de l’entrée de l’appel dans l’un d’eux, le port de numérotation prédictif doit transférer automatiquement l’appel vers la cible désignée (les bits doivent être un sous-ensemble approprié des États de transfert automatique pris en charge indiqués dans [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)); l’application peut conserver le champ avec la valeur 0 s’il souhaite surveiller les États d’appel lui-même et utiliser [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) pour transférer l’appel lorsqu’il atteint la condition souhaitée. L’application doit spécifier l’adresse souhaitée vers laquelle l’appel doit être automatiquement transféré dans le champ de variable défini par les membres **dwTargetAddressSize** et **dwTargetAddressOffset** dans **LINECALLPARAMS**.

Les applications peuvent également définir un délai d’attente pour les appels sortants afin que le fournisseur de services les passe automatiquement à l’état déconnecté s’ils n’ont pas de réponse. Cela est contrôlé à l’aide du membre **dwNoAnswerTimeout** dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).

 

 



