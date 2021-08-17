---
title: SystemMonitor. OnDblClick, événement
description: Vous avertit quand un utilisateur double-clique sur la ligne de graphique, sur la barre d’histogramme ou sur l’élément de rapport avec le bouton gauche de la souris.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Événement OnDblClick SysMon
- OnDblClick, événement SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, OnDblClick, événement
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef829fad368e7d8cf3b65ab70db4600f6d635b1d36bcc5e3f50fcdbaf429a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883958"
---
# <a name="systemmonitorondblclick-event"></a>SystemMonitor. OnDblClick, événement

Vous avertit quand un utilisateur double-clique sur la ligne de graphique, sur la barre d’histogramme ou sur l’élément de rapport avec le bouton gauche de la souris.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ in, out\]
</dt> <dd>

Index du compteur sélectionné dans l’objet de collection de [**compteurs**](counters.md) . La valeur d’index 0 est retournée si aucun compteur n’a été sélectionné ; dans le cas contraire, l’index du compteur sélectionné est retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Lorsque cet événement est déclenché, le compteur sélectionné par l’utilisateur dans le graphique linéaire et l’histogramme est également sélectionné dans le volet légende. Cela permet à l’utilisateur du moniteur système de voir plus facilement le compteur sélectionné lorsque plusieurs valeurs de compteur sont affichées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





