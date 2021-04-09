---
title: protocole PPP des connexions Ethernet
description: Windows Server 2003, Windows XP et les systèmes d’exploitation ultérieurs fournissent une prise en charge de protocole PPP sur Ethernet (PPPoE). Pour une connexion PPPoE, définissez les valeurs suivantes dans la structure RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941291"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>protocole PPP des connexions Ethernet

Windows Server 2003, Windows XP et les systèmes d’exploitation ultérieurs fournissent une prise en charge de protocole PPP sur Ethernet (PPPoE). Pour une connexion PPPoE, définissez les valeurs suivantes dans la structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .



| Membre                      | Valeur             |
|-----------------------------|-------------------|
| RASENTRY.dwType             | \_Haut débit RASET  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | Nom du service. |



 

Utilisez la fonction [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour définir ces valeurs.

Vous pouvez également utiliser [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) et l' \_ indicateur RASEDFLAG NewBroadbandEntry pour [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) pour afficher un Assistant pour la création d’une entrée d’annuaire PPPoE.

 

 