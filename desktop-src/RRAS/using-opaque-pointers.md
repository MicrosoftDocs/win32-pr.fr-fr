---
title: Utilisation de pointeurs opaques
description: Les clients doivent souvent stocker des informations supplémentaires spécifiques au client sur les destinations.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d24524f64fca7062ffb35ed6f4d5e6a2bc935ef7fee0c7fa141cb2e823e70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025069"
---
# <a name="using-opaque-pointers"></a>Utilisation de pointeurs opaques

Les clients doivent souvent stocker des informations supplémentaires spécifiques au client sur les destinations. Le gestionnaire de tables de routage permet aux clients de stocker ces informations dans les structures de destination dans la table de routage. Les informations sont stockées et récupérées à l’aide de *pointeurs opaques*. Les informations stockées sont privées et accessibles uniquement au client propriétaire du pointeur opaque.

Par exemple, le gestionnaire de groupe de multidiffusion conserve une liste des entrées de transfert de multidiffusion qui dépendent d’une destination particulière. Le gestionnaire de groupe de multidiffusion utilise un pointeur opaque dans cette destination. Dans un autre exemple, un protocole de routage qui publie une destination particulière peut conserver les informations relatives à sa propre publication de route de la destination à l’aide d’un pointeur opaque, même s’il ne possède pas le meilleur itinéraire.

Le nombre de pointeurs opaques est limité ; ces pointeurs sont alloués aux clients sur la base du premier arrivé, premier servi. L’administrateur de routeur doit allouer le nombre correct de pointeurs pendant la configuration du routeur. par conséquent, les protocoles de routage et les autres clients doivent documenter leur utilisation de pointeurs opaques.

 

 




