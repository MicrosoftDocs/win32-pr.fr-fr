---
description: La méthode Sequence de l’objet session ouvre une requête sur la table spécifiée, en classant les actions par les nombres de la colonne Sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525646"
---
# <a name="sessionsequence-method"></a>Session. Sequence, méthode

La méthode **Sequence** de l’objet [**session**](session-object.md) ouvre une requête sur la table spécifiée, en classant les actions par les nombres de la colonne Sequence. Pour chaque ligne extraite, la méthode d' [**action**](session-doaction.md) est appelée, à condition que toute expression de condition fournie ne corresponde pas à false. Retourne une énumération msiDoActionStatusEnum, comme décrit dans la méthode d' [**action**](session-doaction.md) .

## <a name="syntax"></a>Syntaxe


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*table* 
</dt> <dd>

Nom de chaîne requis de la table à utiliser pour le séquencement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode est normalement appelée en interne par des actions de niveau supérieur.

Une séquence d’action contenant des actions qui mettent à jour le système, telles que les actions [InstallFiles](installfiles-action.md) et [WriteRegistryValues](writeregistryvalues-action.md) , ne peut pas être exécutée en appelant la méthode **Sequence** . L’exception à cette règle est si la méthode de **séquence** est appelée à partir d’une action personnalisée qui est planifiée dans la [table InstallExecuteSequence](installexecutesequence-table.md) entre les actions [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md). Les actions qui ne mettent pas à jour le système, telles que [AppSearch](appsearch-action.md) ou [CostInitialize](costinitialize-action.md), peuvent être appelées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




