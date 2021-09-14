---
description: La méthode ViewDialog de l’objet UIPreview affiche une boîte de dialogue d’interface utilisateur créée, stockée dans la base de données active.
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: Méthode UIPreview. ViewDialog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewDialog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d9ad3772ced2dba952a3d3b068aaa307d1c06398
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121574"
---
# <a name="uipreviewviewdialog-method"></a>Méthode UIPreview. ViewDialog

La méthode **ViewDialog** de l’objet [**UIPreview**](uipreview-object.md) affiche une boîte de dialogue d’interface utilisateur créée, stockée dans la base de données active.

## <a name="syntax"></a>Syntaxe


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dialogue* 
</dt> <dd>

Nom requis de la boîte de dialogue, respect de la casse et de la clé primaire de la table de base de données de boîtes de dialogue.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview est défini en tant que 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




