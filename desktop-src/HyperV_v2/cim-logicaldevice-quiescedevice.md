---
description: La méthode QuiesceDevice a été dépréciée à la place de la méthode RequestStateChange plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Méthode QuiesceDevice de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320098"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>Méthode QuiesceDevice de la \_ classe du LOGICALDEVICE CIM

La méthode **QuiesceDevice** a été dépréciée à la place de la méthode **RequestStateChange** plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.

## <a name="syntax"></a>Syntaxe


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suspendre* \[ dans\]
</dt> <dd>

Si la valeur est **true** , arrête correctement toute l’activité, si l’activité de reprise est **false** .

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

 

 




