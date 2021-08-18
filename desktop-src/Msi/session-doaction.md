---
description: La méthode de script de l’objet session exécute la fonction d’action correspondant au nom fourni.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Session. subaction, méthode (photoacquire. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5c3f6451ec6ef920e6c6414a9396d2c4eeb2102ffc161e1ed91ce996752cd345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629389"
---
# <a name="sessiondoaction-method"></a>Session. subaction, méthode

La **méthode de script de** l’objet [**session**](session-object.md) exécute la fonction d’action correspondant au nom fourni. Si un nom d’action null est fourni, le moteur utilise la valeur majuscule de la [propriété action](action.md) comme action à exécuter. Si aucune valeur de propriété n’est définie, l’action par défaut est effectuée, actuellement définie en tant qu’installation. Cette méthode retourne une énumération entière.

## <a name="syntax"></a>Syntaxe


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*action* 
</dt> <dd>

Nom de chaîne obligatoire de l’action à exécuter. Respecte la casse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Les actions qui mettent à jour le système, telles que les actions [InstallFiles](installfiles-action.md) et [WriteRegistryValues](writeregistryvalues-action.md) , ne peuvent pas être exécutées en appelant la méthode d' **action** . L’exception à cette règle est si la méthode d' **action** est appelée à partir d’une action personnalisée qui est planifiée dans la [table InstallExecuteSequence](installexecutesequence-table.md) entre les actions [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md). Les actions qui ne mettent pas à jour le système, telles que [AppSearch](appsearch-action.md) ou [CostInitialize](costinitialize-action.md), peuvent être appelées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| En-tête<br/>  | <dl> <dt>Photoacquire. h</dt> </dl>                                                                                                                                                               |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




