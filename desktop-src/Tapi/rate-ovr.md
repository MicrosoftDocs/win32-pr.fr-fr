---
description: La fréquence ou la bande passante d’un appel spécifie la vitesse de transmission des données. Trois points de données identifient la fréquence actuelle du taux maximal pour un mode de support spécifié et le taux minimal pour le mode porteur.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tarif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0af0b2dd6dfe34759753f52773bafe0bdf2bf8f4472ed863dcc6c8b0f10a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060557"
---
# <a name="rate"></a>Tarif

Le taux (ou la bande passante) d’un appel spécifie la vitesse de transmission des données. Taux d’identification de trois points de données : taux actuel, taux maximal pour un mode de support spécifié et taux minimal pour le mode porteur.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

* * TAPI 2. x : * *[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **DwMinRate** ou **dwMaxRate** membre de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x : * *[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo ::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ MAXRATE**, **CIL \_ MINRATE** ou **CIL \_ rate** Member of [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

* * TSPI : * * message de [**ligne \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) , avec *dwParam1* défini sur le taux de LINECALLINFOSTATE \_

 

 
