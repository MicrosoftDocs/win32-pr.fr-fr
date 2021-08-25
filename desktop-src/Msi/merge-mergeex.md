---
description: La méthode MergeEx de l’objet Merge équivaut à la fonction Merge, à ceci près qu’elle accepte un argument supplémentaire.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Merge. MergeEx, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7e683597d78e568e6bfec9b59241fe45f922c5346ef83f427598ad0a7c59dcac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926529"
---
# <a name="mergemergeex-method"></a>Merge. MergeEx, méthode

La méthode **MergeEx** de l’objet [**Merge**](merge-object.md) équivaut à la fonction [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , à ceci près qu’elle accepte un argument supplémentaire. L’argument *pConfiguration* est une interface implémentée par le client. L’argument peut avoir la valeur null. La présence de cet argument indique que le client peut prendre en charge la fonctionnalité de configuration, mais n’impose pas au client de fournir des données de configuration pour un élément configurable spécifique.

La méthode [**Merge**](merge-merge.md) exécute une fusion de la base de données active et du module actuel. La fusion attache les composants du module à la fonctionnalité identifiée par la *fonctionnalité*. La racine de l’arborescence de répertoires du module est redirigée vers l’emplacement donné par *RedirectDir*.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Fonctionnalité* 
</dt> <dd>

Nom d’une fonctionnalité dans la base de données.

</dd> <dt>

*RedirectDir* 
</dt> <dd>

Clé d’une entrée dans la [table des répertoires](directory-table.md) de la base de données. Ce paramètre peut avoir la valeur null ou être une chaîne vide.

</dd> <dt>

*pConfiguration* 
</dt> <dd>

L’argument *pConfiguration* est une interface implémentée par le client. L’argument peut avoir la valeur null. La présence de cet argument indique que le client peut prendre en charge la fonctionnalité de configuration, mais n’impose pas au client de fournir des données de configuration pour un élément configurable spécifique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une fois la fusion terminée, les composants du module sont attachés à la fonctionnalité identifiée par la *fonctionnalité*. Cette fonctionnalité n’est pas créée et doit être une fonctionnalité existante. le module peut être attaché à des fonctionnalités supplémentaires à l’aide de la méthode [**Connecter**](merge-connect.md) .

Les modifications apportées à la base de données sont enregistrées si et seulement si la méthode [**FermerBase**](merge-closedatabase.md) est appelée avec *BCommit* défini sur **true**.

Si des conflits de fusion se produisent, y compris des exclusions, ils sont placés dans l’énumérateur d’erreurs pour une récupération ultérieure, mais n’entraînent pas l’échec de la fusion. Les erreurs peuvent être récupérées par le biais de la propriété [**Errors**](merge-errors.md) . Les erreurs et les messages d’information sont publiés dans le fichier journal actuel.

Lorsque la fusion échoue en raison d’une configuration de module incorrecte, la fonction [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) retourne E \_ Fail. Cela comprend les erreurs msmErrorType suivantes : **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** et **msmErrorDataRequestFailed**. Ces erreurs provoquent l’arrêt immédiat de la fusion lorsque l’erreur se produit. L’objet d’erreur est toujours ajouté à l’énumérateur lorsque **MergeEx** retourne E \_ Fail. Pour plus d’informations sur les erreurs msmErrorType, consultez [**obtenir le \_ type, fonction (objet d’erreur)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type). Toutes les autres erreurs  provoquent le renvoi de S \_ false par MergeEx et la poursuite de la fusion.

### <a name="c"></a>C++

Consultez fonction [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
