---
description: Demande que l’appareil capture ses informations de configuration, d’installation et/ou d’état actuelles dans un magasin de stockage.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Méthode SaveProperties de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e5910ea87a6321872b009003bf18d26910b53627dba6c51647f2896dde2e686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648161"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>Méthode SaveProperties de la \_ classe du LOGICALDEVICE CIM

Demande que l’appareil capture ses informations de configuration, d’installation et/ou d’état actuelles dans un magasin de stockage. L’objectif est d’utiliser ces informations ultérieurement (via la méthode RestoreProperties) pour ramener un appareil à son « état » actuel. Cette méthode peut ne pas être prise en charge par tous les appareils. La méthode doit retourner 0 en cas de réussite, 1 si la demande n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite. Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié, à l’aide d’un qualificateur ValueMap sur la méthode. Les chaînes pour lesquelles le contenu ValueMap est « traduit » peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de valeurs.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

 

 




