---
title: WM/WMADRCPeakReference
description: L’attribut WM/WMADRCPeakReference contient le niveau de volume maximal du fichier encodé. Cette valeur est utilisée par le lecteur Windows Media pour le contrôle de plage dynamique. Cette valeur est définie par le codec et est en lecture seule.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- Format Windows Media WM/WMADRCPeakReference
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380848"
---
# <a name="wmwmadrcpeakreference"></a>WM/WMADRCPeakReference

L’attribut **WM/WMADRCPeakReference** contient le niveau de volume maximal du fichier encodé. Cette valeur est utilisée par le lecteur Windows Media pour le contrôle de plage dynamique. Cette valeur est définie par le codec et est en lecture seule.

## <a name="global-constant"></a>Constante globale

\_wszWMWMADRCPeakReference g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Il existe quatre attributs utilisés par le lecteur Windows Media pour le contrôle de plage dynamique : **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** et **WM/WMADRCPeakTarget**. Toutes ces valeurs sont définies par le writer en fonction des informations du codec lors de l’écriture de flux avec le codec Windows Media Audio 9 ou Windows Media Audio 9 Professional. Les valeurs moyennes sont définies sur le niveau de volume moyen du flux, et les valeurs maximales sont définies sur le niveau de volume maximal dans le flux. Les valeurs de référence sont en lecture seule. Les valeurs cibles sont définies par le lecteur Windows Media lorsque le fichier est lu pour enregistrer les préférences de contrôle de plage dynamique de l’utilisateur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




