---
description: L’API Power de l’appareil facilite la détermination des appareils qui sont en mesure d’éveil du système à partir d’un état de veille, ainsi que les États de veille pour lesquels ces appareils prennent en charge la mise en éveil. Pour plus d’informations sur les États de veille, consultez États d’alimentation du système.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Gestion de l’alimentation des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007162"
---
# <a name="device-power-management"></a>Gestion de l’alimentation des appareils

L’API Power de l’appareil facilite la détermination des appareils qui sont en mesure d’éveil du système à partir d’un état de veille, ainsi que les États de veille pour lesquels ces appareils prennent en charge la mise en éveil. Pour plus d’informations sur les États de veille, consultez [États d’alimentation du système](system-power-states.md).

La fonction [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) peut être utilisée pour rechercher des appareils qui correspondent à des critères spécifiés dans la liste des appareils. Les critères peuvent inclure la capacité de l’appareil à prendre en charge un État du système ou à sortir de cet État. Les indicateurs actuellement pris en charge sont disponibles dans Winnt. h et DevPower. h.

La fonction [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) active ou désactive un appareil spécifié pour sortir le système d’un état de veille.

L’API d’alimentation des appareils permet aux développeurs de créer une meilleure expérience utilisateur en donnant à l’utilisateur des informations supplémentaires sur ce que le système fait et davantage de contrôle sur les appareils du système. La puissance de l’appareil est utile dans les situations où la consommation d’énergie est essentielle, par exemple dans les appareils portables fonctionnant sur batteries. Par exemple, le schéma de gestion de l’alimentation utilisé dans un ordinateur de bureau peut ne pas être optimal pour un ordinateur portable, de sorte que l’utilisateur peut vouloir désactiver l’éveil du système par certains appareils. Cela peut économiser de l’énergie, car les appareils désactivés ne dessinent pas de puissance pendant que le système est en mode veille.

Pour obtenir un exemple, consultez [utilisation de l’API Power Device](using-the-device-power-api.md).

 

 



