---
description: La méthode SetInstallLevel de l’objet session définit le niveau d’installation de l’installation actuelle sur une valeur spécifiée et recalcule les États SELECT et installed pour toutes les fonctionnalités de la table Feature.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Session. SetInstallLevel, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540076"
---
# <a name="sessionsetinstalllevel-method"></a>Session. SetInstallLevel, méthode

La méthode **SetInstallLevel** de l’objet [**session**](session-object.md) définit le niveau d’installation de l’installation actuelle sur une valeur spécifiée et recalcule les États SELECT et installed pour toutes les fonctionnalités de la table Feature. Il définit également l’état d’action de chaque composant dans la [table des composants](component-table.md) en fonction du nouveau niveau.

## <a name="syntax"></a>Syntaxe


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*installLevel* 
</dt> <dd>

Nouveau niveau d’installation demandé requis.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

L' [action CostInitialize](costinitialize-action.md) doit être exécutée avant d’appeler **SetInstallLevel**.

Si 0 est passé pour le paramètre *installLevel* , le niveau d’installation actuel n’est pas modifié, mais toutes les fonctionnalités sont toujours mises à jour en fonction du niveau d’installation actuel. Par exemple, cette fonctionnalité peut être utilisée par le module Handler pour réinitialiser toutes les sélections à leur état initial par défaut à tout moment dans le processus de sélection de l’interface utilisateur.

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




