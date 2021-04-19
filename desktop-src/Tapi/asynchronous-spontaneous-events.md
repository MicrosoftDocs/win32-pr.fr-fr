---
description: Outre celles décrites ci-dessus, il existe une autre classe d’événements asynchrones.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Événements spontanés asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533977"
---
# <a name="asynchronous-spontaneous-events"></a>Événements spontanés asynchrones

Outre celles décrites ci-dessus, il existe une autre classe d’événements asynchrones. Ces événements sont « spontanés » dans la mesure où ils ne sont pas des résultats directs des demandes correspondantes. Ces événements sont détectés dans de tels cas lorsqu’un appel entrant arrive ou lorsqu’un appel sortant passe d’une « sonnerie » à l’état « réponse ». Lorsque TAPI initialise d’abord les interactions avec le TSPI pour un appareil particulier, il passe un pointeur vers une procédure de rappel à appeler pour signaler ces événements spontanés. Ce pointeur de procédure est un handle d’appareil que le fournisseur de services comprend comme l’un des paramètres réels du rappel.

 

 



