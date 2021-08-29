---
description: Demande que l’appareil rétablit la configuration, l’installation et/ou les informations d’État à partir d’un magasin de stockage.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Méthode RestoreProperties de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2472ca36acbc152340dc0b47a2a353d6ad168f88af560f1753994df70a81dde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046849"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a>Méthode RestoreProperties de la \_ classe du LOGICALDEVICE CIM

Demande que l’appareil rétablit la configuration, l’installation et/ou les informations d’État à partir d’un magasin de stockage. L’objectif est de capturer ces informations à un moment antérieur (via la méthode SaveProperties) et de les utiliser pour retourner un appareil à cette « condition » antérieure. Cette méthode peut ne pas être prise en charge par tous les appareils. La méthode doit retourner 0 en cas de réussite, 1 si la demande n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite. Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié, à l’aide d’un qualificateur ValueMap sur la méthode. Les chaînes pour lesquelles le contenu ValueMap est « traduit » peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de valeurs.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

 

 




