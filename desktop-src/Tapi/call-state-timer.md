---
description: À l’heure actuelle, tout le minutage des appels est laissé aux applications.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Minuterie de l’état d’appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544702"
---
# <a name="call-state-timer"></a>Minuterie de l’état d’appel

À l’heure actuelle, tout le minutage des appels est laissé aux applications. Cela peut être fastidieux si l’application surveille un grand nombre d’appels, et si plusieurs applications sont présentes, éventuellement sur plusieurs serveurs, il peut être nécessaire qu’ils maintiennent tous les minuteurs sur les mêmes appels. Il est donc plus judicieux de gérer le minutage de l’état des appels par le serveur.

Le membre **tStateEntryTime** dans [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) permet d’indiquer le minutage des appels dans les États. Le membre (de type **sysTime**) indique l’heure à laquelle l’état actuel a été entré.

 

 



