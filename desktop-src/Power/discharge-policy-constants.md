---
description: La liste suivante décrit les constantes de stratégie de déchargement.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Constantes de stratégie de déchargement (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a05237b7555cc7281f132f02110a10cb5b58cd342d6872b16c1a6319773ea8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961869"
---
# <a name="discharge-policy-constants"></a>Constantes de stratégie de déchargement

La liste suivante décrit les constantes de stratégie de déchargement.



| Constante/valeur                                                                                                                                                                                                                                            | Description                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> En <dt>**charge \_ STRATÉGIE \_ critique**</dt> <dt>0</dt> </dl> | Lequel des paramètres de stratégie de déchargement de la batterie (structures de [**\_ \_ niveau d’alimentation du système**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) est utilisé lorsque la batterie se décharge au-dessous du seuil critique.<br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> En <dt>**charge \_ STRATÉGIE \_ faible**</dt> <dt>1</dt> </dl>                | Lequel des paramètres de stratégie de déchargement de la batterie (structures de [**\_ \_ niveau d’alimentation du système**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) est utilisé lorsque la batterie est déchargée au-dessous du seuil inférieur.<br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <dt>**Nombre \_ \_Stratégies de rejet**</dt> <dt>4</dt> </dl>          | Nombre de paramètres de [**stratégie de \_ \_**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) déchargement de batterie spécifiés.<br/>                                                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>winnt. h (inclure Windows. h)</dt> </dl> |



 

 




