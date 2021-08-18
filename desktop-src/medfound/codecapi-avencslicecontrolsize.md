---
description: Spécifie la taille de la tranche en unités de mégaoctets (Mo), de bits ou de ligne Mo.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: CODECAPI_AVEncSliceControlSize, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d068d8b2c5fc15fdb82c3ffe068e6926d28228a19367114067e02ebc44b03726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035347"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>CODECAPI \_ propriété AVEncSliceControlSize

Spécifie la taille de la tranche en unités de mégaoctets (Mo), de bits ou de ligne Mo.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncSliceControlSize**

## <a name="remarks"></a>Remarques

**Encodeurs H. 264/AVC :**

La signification de la valeur de CODECAPI \_ AVEncSliceControlSize est contrôlée par la propriété [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) . Le tableau suivant illustre la façon dont les \_ Propriétés CODECAPI AVEncSliceControlSize et CODECAPI \_ AVEncSliceControlMode contrôlent la taille et le nombre de secteurs dans un frame.



| \_Paramètre CODECAPI AVEncSliceControlMode | Signification de la valeur                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | Il s’agit d’un entier qui indique la taille de chaque tranche dans le frame en unités de blocs macros. <br/> L’encodeur doit rejeter le paramètre lorsque la valeur est supérieure au nombre de blocs macros dans le frame.<br/>                                                                                                                                                                         |
| 1                                       | Il s’agit d’un entier qui indique la taille de chaque tranche dans le frame en unités de bits. <br/> L’encodeur doit démarrer une nouvelle tranche au niveau du bloc macro qui entraîne le dépassement de cette valeur du nombre de bits dans la tranche (la taille de chaque tranche sera toujours inférieure ou égale à cette valeur). Cela signifie que la taille de la dernière tranche peut être beaucoup plus petite que cette valeur. <br/> |
| 2                                       | Il s’agit d’un entier qui indique la taille de chaque tranche dans le frame en unités de lignes bloc macro. <br/> L’encodeur doit rejeter le paramètre lorsque la valeur est supérieure au nombre de lignes bloc macro dans le frame.<br/>                                                                                                                                                                 |



 

Si l’application ne définit pas de valeur pour [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), l’encodeur doit renvoyer une erreur.

La valeur par défaut recommandée consiste à avoir une seule tranche pour l’ensemble du frame.

Certains encodeurs peuvent coder les tranches en parallèle et, par conséquent, les performances peuvent être affectées en fonction des paramètres de contrôle de la tranche. Par exemple, l’encodage d’un frame en tant que tranche unique peut être plus lent que si le frame était encodé comme plusieurs tranches.

Les paramètres de contrôle de la tranche sont dynamiques et peuvent être modifiés au cours de la session d’encodage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




