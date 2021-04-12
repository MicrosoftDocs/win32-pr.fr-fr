---
description: Le mode porteur correspond à la qualité de transmission demandée à partir du réseau pour l’établissement d’un appel.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Mode porteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202195"
---
# <a name="bearer-mode"></a>Mode porteur

Le [**mode porteur**](./linebearermode--constants.md) correspond à la qualité de transmission demandée à partir du réseau pour l’établissement d’un appel. Il est important de conserver le concept de mode porteur distinct de celui du [**type de média**](tapimediatype--constants.md). Par exemple, le réseau téléphonique analogique (RTPC) fournit uniquement un mode de prise en charge de la voix de 3,1 kHz, mais les appels qui l’utilisent peuvent prendre en charge des types de médias tels que la voix, la télécopie ou le modem de données.

Le mode de porteur d’un appel est spécifié lorsque l’appel est configuré ou est fourni lorsque l’appel est proposé. Avec les appareils de ligne capables de représenter des pools de canaux, il est possible qu’un fournisseur de services autorise l’établissement d’appels avec une plus grande bande passante.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** membre de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo ::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ BEARERMODE** Member of [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

**TSPI :** Consultez la [**ligne \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, avec *dwParam1* défini sur LINECALLINFOSTATE \_ BEARERMODE.

 

 
