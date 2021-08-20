---
title: Méthode SystemMonitor. ScaleToFit
description: Mettre à l’échelle les valeurs de compteur pour les adapter au graphique.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Méthode ScaleToFit SysMon
- Méthode ScaleToFit SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode ScaleToFit
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cddb539f8c8d2c6c78f70d96d82da171e11a62afbeaa31d1a011c74c2cb096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881513"
---
# <a name="systemmonitorscaletofit-method"></a>Méthode SystemMonitor. ScaleToFit

Mettre à l’échelle les valeurs de compteur pour les adapter au graphique.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*selectedCountersOnly* \[ dans\]
</dt> <dd>

True pour mettre à l’échelle uniquement les compteurs sélectionnés ; Sinon, false pour mettre à l’échelle tous les compteurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode efface la vue du graphique. SYSMON utilise ensuite le facteur d’échelle spécifié pour chaque compteur pour redessiner le graphique si la source de données est un fichier journal, ou commence à représenter graphiquement les nouvelles valeurs de compteur si la source de données est une activité en temps réel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem. ScaleFactor**](counteritem-scalefactor.md)
</dt> <dt>

[**CounterItem. Selected**](counteritem-selected.md)
</dt> </dl>

 

 





