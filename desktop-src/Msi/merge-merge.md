---
description: La méthode Merge de l’objet Merge exécute une fusion de la base de données active et du module actuel.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Merge. Merge, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 43644f8ef19b81331f9f2d88d4dac03d654379d51174a50e994d3642cb86eabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804729"
---
# <a name="mergemerge-method"></a>Merge. Merge, méthode

La méthode **Merge** de l’objet [**Merge**](merge-object.md) exécute une fusion de la base de données active et du module actuel. La fusion attache les composants du module à la fonctionnalité identifiée par la *fonctionnalité*. La racine de l’arborescence de répertoires du module est redirigée vers l’emplacement donné par *RedirectDir*.

La méthode **Merge** ne peut être appelée qu’une seule fois pour fusionner une combinaison particulière de fichiers .msi et. msm.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.Merge(
  Feature,
  RedirectDir
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

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une fois la fusion terminée, les composants du module sont attachés à la fonctionnalité identifiée par la *fonctionnalité*. Cette fonctionnalité n’est pas créée et doit être une fonctionnalité existante. Notez que la méthode **Merge** obtient toutes les références de fonctionnalités dans le module et remplace la référence de fonctionnalité pour toutes les occurrences du GUID null dans la base de données du module. Pour plus d’informations, consultez [référencement des fonctionnalités dans les modules de fusion](referencing-features-in-merge-modules.md).

le module peut être attaché à des fonctionnalités supplémentaires à l’aide de la méthode [**Connecter**](merge-connect.md) . notez que l’appel de la méthode **Connecter** crée uniquement des associations fonctionnalité-composant. Elle ne modifie pas les lignes qui ont déjà été fusionnées dans la base de données.

Les modifications apportées à la base de données sont enregistrées si et seulement si la méthode [**FermerBase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) est appelée avec *BCommit* défini sur **true**.

Si des conflits de fusion se produisent, y compris des exclusions, ils sont placés dans l’énumérateur d’erreurs pour une récupération ultérieure, mais n’entraînent pas l’échec de la fusion. Les erreurs peuvent être récupérées par le biais de la propriété [**Errors**](error-object.md) . Les erreurs et les messages d’information sont publiés dans le fichier journal actuel.

### <a name="c"></a>C++

Consultez [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
