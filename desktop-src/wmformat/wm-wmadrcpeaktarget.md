---
title: WM/WMADRCPeakTarget
description: L’attribut WM/WMADRCPeakTarget contient le niveau de volume maximal demandé par l’utilisateur. cette valeur est utilisée par Lecteur Windows Media pour le contrôle de plage dynamique.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- Format Windows Media WM/WMADRCPeakTarget
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c87c8d62316bfa3e732d0cdc00e0fcb5295c30e675fd9c21fcd5ac766f239f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590679"
---
# <a name="wmwmadrcpeaktarget"></a>WM/WMADRCPeakTarget

L’attribut **WM/WMADRCPeakTarget** contient le niveau de volume maximal demandé par l’utilisateur. cette valeur est utilisée par Lecteur Windows Media pour le contrôle de plage dynamique.

## <a name="global-constant"></a>Constante globale

\_wszWMWMADRCPeakTarget g

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

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




