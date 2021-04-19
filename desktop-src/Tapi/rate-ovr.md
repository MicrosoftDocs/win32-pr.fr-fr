---
description: La fréquence ou la bande passante d’un appel spécifie la vitesse de transmission des données. Trois points de données identifient la fréquence actuelle du taux maximal pour un mode de support spécifié et le taux minimal pour le mode porteur.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tarif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40747c26a98d8eb69e8161fb04302c5187121dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538921"
---
# <a name="rate"></a>Tarif

Le taux (ou la bande passante) d’un appel spécifie la vitesse de transmission des données. Taux d’identification de trois points de données : taux actuel, taux maximal pour un mode de support spécifié et taux minimal pour le mode porteur.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

* * TAPI 2. x : * *[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **DwMinRate** ou **dwMaxRate** membre de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x : * *[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo ::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ MAXRATE**, **CIL \_ MINRATE** ou **CIL \_ rate** Member of [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

* * TSPI : * * message de [**ligne \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) , avec *dwParam1* défini sur le taux de LINECALLINFOSTATE \_

 

 
