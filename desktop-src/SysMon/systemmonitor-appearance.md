---
title: SystemMonitor. Appearance, propriété
description: Récupère ou définit l’apparence du contrôle pour inclure ou omettre les effets d’affichage en trois dimensions.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Propriété d’apparence SysMon
- Propriété Appearance SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510117"
---
# <a name="systemmonitorappearance-property"></a>SystemMonitor. Appearance, propriété

Récupère ou définit l’apparence du contrôle pour inclure ou omettre les effets d’affichage en trois dimensions.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property Appearance As Long
```



## <a name="property-value"></a>Valeur de la propriété

Valeur d’apparence qui détermine si le contrôle est peint avec des effets en trois dimensions.

Vous pouvez définir cette propriété sur l’une des valeurs suivantes.



| Valeur                                                                        | Signification                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Peint le contrôle sans effets visuels.<br/>                                    |
| <dl> <dt>1</dt> </dl> | Peint le contrôle avec des effets en trois dimensions. Il s’agit de la valeur par défaut.<br/> |



 

## <a name="exceptions"></a>Exceptions



| Type d'exception               | Condition                                    |
|------------------------------|----------------------------------------------|
| **System.ArgumentException** | La valeur d’apparence spécifiée n’est pas valide. |



 

## <a name="remarks"></a>Notes

Il s’agit d’une propriété ambiante. La valeur de cette propriété est déterminée par le conteneur. La définition de la valeur de cette propriété peut affecter l’illusion du contrôle et du conteneur en tant qu’application unique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





