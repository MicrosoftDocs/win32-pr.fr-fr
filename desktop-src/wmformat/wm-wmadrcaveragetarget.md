---
title: WM/WMADRCAverageTarget
description: L’attribut WM/WMADRCAverageTarget contient le niveau de volume moyen demandé par l’utilisateur. cette valeur est utilisée par Lecteur Windows Media pour le contrôle de plage dynamique.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Format Windows Media WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd08dd09b6db671a0af1d816162923624cb781148f557ce4bee21fe2dc9a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083913"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

L’attribut **WM/WMADRCAverageTarget** contient le niveau de volume moyen demandé par l’utilisateur. cette valeur est utilisée par Lecteur Windows Media pour le contrôle de plage dynamique.

## <a name="global-constant"></a>Constante globale

\_wszWMWMADRCAverageTarget g

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

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




