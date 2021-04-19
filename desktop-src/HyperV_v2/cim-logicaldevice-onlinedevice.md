---
description: La méthode OnlineDevice a été dépréciée à la place de la méthode RequestStateChange plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Méthode OnlineDevice de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536408"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>Méthode OnlineDevice de la \_ classe du LOGICALDEVICE CIM

La méthode **OnlineDevice** a été dépréciée à la place de la méthode **RequestStateChange** plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.

## <a name="syntax"></a>Syntaxe


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*En ligne* \[ dans\]
</dt> <dd>

Si la **valeur est true**, mettre l’appareil en ligne, si la valeur est **false**, mettre l’appareil hors connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




