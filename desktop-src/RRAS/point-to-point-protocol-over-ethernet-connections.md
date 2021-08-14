---
title: protocole PPP des connexions Ethernet
description: Windows le serveur 2003, Windows XP et les systèmes d’exploitation ultérieurs assurent la prise en charge de protocole PPP via Ethernet (PPPoE). Pour une connexion PPPoE, définissez les valeurs suivantes dans la structure RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92703bac13d129ed29cee1c22328825de67325239c1906c1728b96d53398647b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789809"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>protocole PPP des connexions Ethernet

Windows le serveur 2003, Windows XP et les systèmes d’exploitation ultérieurs assurent la prise en charge de protocole PPP via Ethernet (PPPoE). Pour une connexion PPPoE, définissez les valeurs suivantes dans la structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .



| Membre                      | Valeur             |
|-----------------------------|-------------------|
| RASENTRY.dwType             | \_Haut débit RASET  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | Nom du service. |



 

Utilisez la fonction [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour définir ces valeurs.

Vous pouvez également utiliser [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) et l' \_ indicateur RASEDFLAG NewBroadbandEntry pour [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) pour afficher un Assistant pour la création d’une entrée d’annuaire PPPoE.

 

 