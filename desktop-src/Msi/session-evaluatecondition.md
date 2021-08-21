---
description: La méthode EvaluateCondition de l’objet session évalue une expression logique qui contient des symboles et des valeurs. Cette méthode utilise la fonction MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Session. EvaluateCondition, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fa5807314092c6245c23a329deb44a644ed54b22640292a06e08a9944f54e4dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629329"
---
# <a name="sessionevaluatecondition-method"></a>Session. EvaluateCondition, méthode

La méthode **EvaluateCondition** de l’objet [**session**](session-object.md) évalue une expression logique qui contient des symboles et des valeurs. Cette méthode utilise la fonction [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .

## <a name="syntax"></a>Syntaxe


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*condition* 
</dt> <dd>

Chaîne obligatoire qui contient l’expression logique. Pour plus d’informations, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un entier qui indique l’évaluation de la condition.



| Constante                  | Valeur | Description                               |
|---------------------------|-------|-------------------------------------------|
| msiEvaluateConditionFalse | 0     | La condition prend la valeur false.         |
| msiEvaluateConditionTrue  | 1     | La condition prend la valeur true.          |
| msiEvaluateConditionNone  | 2     | Une expression conditionnelle n’est pas fournie. |
| msiEvaluateConditionError | 3     | La condition contient une erreur de syntaxe.    |



 

## <a name="remarks"></a>Remarques

Les expressions conditionnelles peuvent être utilisées pour comparer les États des fonctionnalités et des composants. Le tableau suivant présente les États des fonctionnalités et des composants utilisés par la méthode EvaluateCondition.



| État                 | Valeur | Description                                              |
|-----------------------|-------|----------------------------------------------------------|
| Null                  | Null  | Aucune action effectuée sur la fonctionnalité ou le composant.                 |
| msiInstallStateAbsent | 2     | La fonctionnalité ou le composant n’est pas présent.                     |
| msiInstallStateLocal  | 3     | La fonctionnalité ou le composant est installé sur l’ordinateur local. |
| msiInstallStateSource | 4     | La fonctionnalité ou le composant est installé pour s’exécuter à partir de la source.    |



 

> [!Note]  
> Les États ne sont pas définis tant que la méthode [**SetInstallLevel**](session-setinstalllevel.md) n’est pas appelée, soit directement, soit par l' [action CostFinalize](costfinalize-action.md). Par conséquent, la vérification de l’État n’est utile que dans une expression conditionnelle dans une table de séquences d’actions.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe d’instruction conditionnelle](conditional-statement-syntax.md)
</dt> </dl>

 

 




