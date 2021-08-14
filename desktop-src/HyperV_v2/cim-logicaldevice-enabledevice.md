---
description: La méthode EnableDevice a été dépréciée à la place de la méthode RequestStateChange plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Méthode EnableDevice de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a01d1b206d0d38f74c5701c8c088506792cb6ca6f997b9e0280adcc61e5a8633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648524"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>Méthode EnableDevice de la \_ classe du LOGICALDEVICE CIM

La méthode EnableDevice a été dépréciée à la place de la méthode RequestStateChange plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.

Demande que le LogicalDevice soit activé (« Enabled », paramètre d’entrée = TRUE) ou désactivé (= FALSe). En cas de réussite, les propriétés StatusInfo/EnabledState de l’appareil doivent refléter l’état souhaité (activé/désactivé). Notez que la fonction de cette méthode chevauche la propriété RequestedState. RequestedState a été ajouté au modèle pour tenir à jour un enregistrement (c’est-à-dire, une valeur persistante) de la dernière demande d’État. L’appel de la méthode EnableDevice doit définir la propriété RequestedState de manière appropriée.

Le code de retour doit être 0 si la requête a été exécutée avec succès, 1 si la demande n’est pas prise en charge et une autre valeur si une erreur s’est produite. Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié, à l’aide d’un qualificateur ValueMap sur la méthode. Les chaînes pour lesquelles le contenu ValueMap est « traduit » peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de valeurs.

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Activé* \[ dans\]
</dt> <dd>

Si la valeur est TRUE, activez l’appareil, si la valeur FALSe, désactivez l’appareil.

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

 

 




