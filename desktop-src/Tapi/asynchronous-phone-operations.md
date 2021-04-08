---
description: Neuf opérations asynchrones sont liées aux téléphones.
ms.assetid: b255bdde-1677-401f-b02d-4850e0e98dc4
title: Opérations de téléphone asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4a70a1d980c4f0d42d5160ee020531b538f488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866598"
---
# <a name="asynchronous-phone-operations"></a>Opérations de téléphone asynchrones

Neuf opérations asynchrones sont liées aux téléphones. Celles-ci sont initiées par les fonctions [**TSPI \_ phoneDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific), [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo), [**TSPI \_ phoneSetData**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata), [**TSPI \_ phoneSetDisplay**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay), [**TSPI \_ phoneSetGain**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain), [**TSPI \_ phoneSetHookSwitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch), [**TSPI \_ phoneSetLamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp), [**TSPI \_ phoneSetRing**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring)et [**TSPI \_ phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) . Si une application appelle la fonction TAPI [**phoneClose**](/windows/win32/api/tapi/nf-tapi-phoneclose) et a le seul descripteur au téléphone, TAPI appelle la fonction [**TSPI \_ phoneClose**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) pour indiquer au fournisseur de services de mettre fin aux opérations asynchrones et appeler la fonction de rappel de la [*\_ procédure d’achèvement*](/windows/win32/api/tspi/nc-tspi-async_completion) . Si l’application n’a pas le seul handle vers le téléphone, le fournisseur de services ne reçoit aucune notification de la demande et toutes les opérations asynchrones en suspens restent actives.

 

 
