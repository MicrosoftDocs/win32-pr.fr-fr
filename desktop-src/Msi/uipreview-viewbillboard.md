---
description: La méthode ViewBillboard de l’objet UIPreview affiche un panneau d’affichage créé à l’aide du contrôle hôte dans la boîte de dialogue actuellement affichée.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Méthode UIPreview. ViewBillboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9892dc68ae5edb66759e4c19499af56d06fb6efac56b823821cd74c4a28644b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810369"
---
# <a name="uipreviewviewbillboard-method"></a>Méthode UIPreview. ViewBillboard

La méthode **ViewBillboard** de l’objet [**UIPreview**](uipreview-object.md) affiche un panneau d’affichage créé à l’aide du contrôle hôte dans la boîte de dialogue actuellement affichée.

## <a name="syntax"></a>Syntaxe


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*control* 
</dt> <dd>

Nom requis du contrôle qui héberge le panneau, qui respecte la casse, ainsi que la boîte de dialogue, et les clés primaires de la table de base de données de contrôle.

</dd> <dt>

*blanc* 
</dt> <dd>

Nom requis du panneau d’affichage à afficher à l’aide du contrôle spécifié et de la boîte de dialogue active, ainsi que de la clé primaire de la table de base de données de tableau blanc.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview est défini en tant que 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




