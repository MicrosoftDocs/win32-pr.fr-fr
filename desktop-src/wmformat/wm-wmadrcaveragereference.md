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
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106538586"
---
# <a name="wmwmadrcaveragereference"></a>WM/WMADRCAverageReference

L’attribut **WM/WMADRCAverageReference** contient le niveau de volume moyen du fichier encodé.

## <a name="global-constant"></a>Constante globale

\_wszWMWMADRCAverageReference g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Il existe quatre attributs utilisés par le lecteur Windows Media pour le contrôle de plage dynamique : **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** et **WM/WMADRCPeakTarget**. Toutes ces valeurs sont définies par le writer en fonction des informations du codec lors de l’écriture de flux avec le codec Windows Media Audio 9 ou Windows Media Audio 9 Professional. Les valeurs moyennes sont définies sur le niveau de volume moyen du flux, et les valeurs maximales sont définies sur le niveau de volume maximal dans le flux. Les valeurs de référence sont en lecture seule. Les valeurs cibles sont définies par le lecteur Windows Media lorsque le fichier est lu pour enregistrer les préférences de contrôle de plage dynamique de l’utilisateur.

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

 

 




