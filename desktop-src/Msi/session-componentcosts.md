---
description: La propriété ComponentCosts de l’objet session retourne un objet RecordList énumérant l’espace disque par lecteur requis pour installer un composant.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Session. ComponentCosts, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 643996bccd352695651fb55f2ddcb33c0888773f4d99283f646a7fcb498c4074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629519"
---
# <a name="sessioncomponentcosts-property"></a>Session. ComponentCosts, propriété

La propriété ComponentCosts de l’objet [**session**](session-object.md) retourne un objet [**RecordList**](recordlist-object.md) énumérant l’espace disque par lecteur requis pour installer un composant. Ces informations sont utilisées par l’interface utilisateur pour afficher l’espace disque requis pour tous les lecteurs. Les coûts d’espace disque retournés sont de multiples de 512 octets.

La propriété ComponentCosts doit être utilisée uniquement une fois que le programme d’installation a terminé le [coût des fichiers](file-costing.md) et après l' [action CostFinalize](costfinalize-action.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Pour obtenir le coût total, ajoutez les coûts pour tous les composants ainsi que le coût du moteur d’installation (composant = "").

ComponentCosts retourne un [**objet RecordList**](recordlist-object.md). Chaque enregistrement de l’objet RecordList retourné contient les champs suivants :



| Champ | Description                                          |
|-------|------------------------------------------------------|
| 1     | Nom du lecteur/volume                                    |
| 2     | Coût de l’espace disque final en multiples de 512 octets.     |
| 3     | Coût de l’espace disque temporaire en multiples de 512 octets. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




