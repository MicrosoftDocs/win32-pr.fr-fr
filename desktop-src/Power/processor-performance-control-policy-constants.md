---
description: Les constantes de stratégie de contrôle des performances du processeur indiquent que l’algorithme de contrôle des performances du processeur est appliqué à un mode de gestion de l’alimentation.
ms.assetid: 928ba485-f767-47df-8b57-7630c68068a7
title: Constantes de la stratégie de contrôle des performances du processeur (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597750f37d9efda80d4bb2bfff7bc121982e7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529109"
---
# <a name="processor-performance-control-policy-constants"></a>Constantes de la stratégie de contrôle des performances du processeur

Les constantes de stratégie de contrôle des performances du processeur indiquent que l’algorithme de contrôle des performances du processeur est appliqué à un mode de gestion de l’alimentation.



| Constante/valeur                                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PO_THROTTLE_ADAPTIVE"></span><span id="po_throttle_adaptive"></span><dl> <dt>**Bon de commande \_ LIMITATION \_ adaptative**</dt> <dt>3</dt> </dl> | Tente de faire correspondre les performances du processeur à la demande actuelle. Cette stratégie utilise à la fois les États haute et basse tension et fréquence. Cette stratégie permet de réduire les performances du processeur à la plus faible tension disponible lorsque la demande est insuffisante pour justifier une tension supérieure. Cette stratégie va impliquer la limitation de l’horloge du processeur si l’État C3 n’est pas utilisé, et en réponse à des événements thermiques.<br/> |
| <span id="PO_THROTTLE_CONSTANT"></span><span id="po_throttle_constant"></span><dl> <dt>**Bon de commande \_ \_Constante de limitation**</dt> <dt>1</dt> </dl> | N’autorise pas le processeur à utiliser des États de performances haute tension. Cette stratégie n’implique pas la limitation de l’horloge du processeur, sauf en réponse aux événements thermiques.<br/>                                                                                                                                                                                                                                                                 |
| <span id="PO_THROTTLE_DEGRADE"></span><span id="po_throttle_degrade"></span><dl> <dt>**Bon de commande \_ \_Baisse**</dt> de la limitation <dt>2</dt> </dl>    | N’autorise pas le processeur à utiliser des États de performances haute tension. Cette stratégie va impliquer la limitation de l’horloge du processeur lorsque la batterie est inférieure à un certain seuil, si l’État C3 n’est pas utilisé ou en réponse à des événements thermiques.<br/>                                                                                                                                                                                    |
| <span id="PO_THROTTLE_NONE"></span><span id="po_throttle_none"></span><dl> <dt>**Bon de commande \_ LIMITATION \_ None**</dt> <dt>0</dt> </dl>             | Aucun contrôle des performances du processeur n’est appliqué. Cette stratégie exécute toujours le processeur à son niveau de performance le plus élevé possible. Cette stratégie n’implique pas la limitation de l’horloge du processeur, sauf en réponse aux événements thermiques.<br/>                                                                                                                                                                                                            |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Winnt. h (inclure Windows. h)</dt> </dl> |



 

 




