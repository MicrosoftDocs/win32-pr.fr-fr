---
title: Utilisation de pointeurs opaques
description: Les clients doivent souvent stocker des informations supplémentaires spécifiques au client sur les destinations.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840417"
---
# <a name="using-opaque-pointers"></a>Utilisation de pointeurs opaques

Les clients doivent souvent stocker des informations supplémentaires spécifiques au client sur les destinations. Le gestionnaire de tables de routage permet aux clients de stocker ces informations dans les structures de destination dans la table de routage. Les informations sont stockées et récupérées à l’aide de *pointeurs opaques*. Les informations stockées sont privées et accessibles uniquement au client propriétaire du pointeur opaque.

Par exemple, le gestionnaire de groupe de multidiffusion conserve une liste des entrées de transfert de multidiffusion qui dépendent d’une destination particulière. Le gestionnaire de groupe de multidiffusion utilise un pointeur opaque dans cette destination. Dans un autre exemple, un protocole de routage qui publie une destination particulière peut conserver les informations relatives à sa propre publication de route de la destination à l’aide d’un pointeur opaque, même s’il ne possède pas le meilleur itinéraire.

Le nombre de pointeurs opaques est limité ; ces pointeurs sont alloués aux clients sur la base du premier arrivé, premier servi. L’administrateur de routeur doit allouer le nombre correct de pointeurs pendant la configuration du routeur. par conséquent, les protocoles de routage et les autres clients doivent documenter leur utilisation de pointeurs opaques.

 

 




