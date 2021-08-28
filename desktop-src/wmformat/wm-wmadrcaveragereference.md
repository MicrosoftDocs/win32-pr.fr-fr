---
title: WM/WMADRCAverageReference
description: L’attribut WM/WMADRCAverageReference contient le niveau de volume moyen du fichier encodé.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Format Windows Media WM/WMADRCAverageReference
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9948d71739aaee4f5f24f54701f8e335f8b7b79486c8820f7a5fdf48c068e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026947"
---
# <a name="wmwmadrcaveragereference"></a>WM/WMADRCAverageReference

L’attribut **WM/WMADRCAverageReference** contient le niveau de volume moyen du fichier encodé.

## <a name="global-constant"></a>Constante globale

\_wszWMWMADRCAverageReference g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Remarques

il existe quatre attributs utilisés par Lecteur Windows Media pour le contrôle de plage dynamique : **wm/WMADRCAverageReference**, **wm/WMADRCPeakReference**, **wm/WMADRCAverageTarget** et **wm/WMADRCPeakTarget**. toutes ces valeurs sont définies par le writer en fonction des informations du codec lors de l’écriture de flux avec le codec Windows Media Audio 9 ou Windows Media Audio 9 Professional. Les valeurs moyennes sont définies sur le niveau de volume moyen du flux, et les valeurs maximales sont définies sur le niveau de volume maximal dans le flux. Les valeurs de référence sont en lecture seule. les valeurs cibles sont définies par Lecteur Windows Media lors de la lecture du fichier pour enregistrer les préférences de contrôle de plage dynamique de l’utilisateur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




