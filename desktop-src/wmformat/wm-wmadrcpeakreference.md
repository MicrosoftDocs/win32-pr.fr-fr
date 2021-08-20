---
title: WM/WMADRCPeakReference
description: L’attribut WM/WMADRCPeakReference contient le niveau de volume maximal du fichier encodé. cette valeur est utilisée par Lecteur Windows Media pour le contrôle de plage dynamique. Cette valeur est définie par le codec et est en lecture seule.
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
ms.openlocfilehash: e2e5abf41b52b615030c07b532fc3d75e40bd898a409e0f5ecd2b15541c8c0df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027531"
---
# <a name="wmwmadrcpeakreference"></a>WM/WMADRCPeakReference

L’attribut **WM/WMADRCPeakReference** contient le niveau de volume maximal du fichier encodé. cette valeur est utilisée par Lecteur Windows Media pour le contrôle de plage dynamique. Cette valeur est définie par le codec et est en lecture seule.

## <a name="global-constant"></a>Constante globale

\_wszWMWMADRCPeakReference g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Remarques

il existe quatre attributs utilisés par Lecteur Windows Media pour le contrôle de plage dynamique : **wm/WMADRCAverageReference**, **wm/WMADRCPeakReference**, **wm/WMADRCAverageTarget** et **wm/WMADRCPeakTarget**. toutes ces valeurs sont définies par le writer en fonction des informations du codec lors de l’écriture de flux avec le codec Windows Media Audio 9 ou Windows Media Audio 9 Professional. Les valeurs moyennes sont définies sur le niveau de volume moyen du flux, et les valeurs maximales sont définies sur le niveau de volume maximal dans le flux. Les valeurs de référence sont en lecture seule. les valeurs cibles sont définies par Lecteur Windows Media lors de la lecture du fichier pour enregistrer les préférences de contrôle de plage dynamique de l’utilisateur.

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

 

 




