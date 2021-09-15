---
description: 'IInkAnalyzer :: SearchWithLanguageId, méthode-fournit une recherche basée sur une expression approximative et non sensible à la casse pour les traits d’écriture analysés et les traits de dessin analysés qui ont des types reconnus.'
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: 'IInkAnalyzer :: SearchWithLanguageId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 201469933da10b0d68a4d3a50e63c42f8d01d2dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521253"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a>IInkAnalyzer :: SearchWithLanguageId, méthode

Fournit une recherche basée sur une expression approximative et non sensible à la casse pour les traits d’écriture analysés et les traits de dessin analysés qui ont des types reconnus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrPhraseToMatch* \[ dans\]
</dt> <dd>

Expression qui sera trouvée dans les alternatives pour les traits actuellement analysés.

</dd> <dt>

*lSearchStringLanguageId* \[ dans\]
</dt> <dd>

LCID associé à la chaîne qui est passée. Utilisé pour convertir le cas en interne pour prendre en charge les comparaisons qui ne respectent pas la casse.

</dd> <dt>

*pulSearchResultCount* \[ in, out\]
</dt> <dd>

Nombre maximal de résultats retournés par la recherche.

</dd> <dt>

*ppulStrokeCountPerResult* \[ à\]
</dt> <dd>

Pointeur vers un tableau du nombre de traits dans chaque résultat de recherche.

</dd> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Nombre d’ID de trait dans *ppulStrokeIds*.

</dd> <dt>

*ppulStrokeIds* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’ID de trait représentant un jeu de traits.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Cette recherche recherche les sous-chaînes de mots multiples et à mots uniques. Les résultats de la reconnaissance alternative et les autres segments sont recherchés.

Toutes les chaînes entrantes seront converties en une seule casse pour la comparaison utilisant le LCID du thread actuel pour effectuer cette conversion en respectant les conventions de cas culturels.

La chaîne transmise est traitée comme une expression. Les mots et les caractères doivent apparaître dans le alterantes pour les traits dans l’ordre spécifié. Les premier et dernier mots de l’expression peuvent être mis en correspondance en tant que sous-chaînes (le premier mot apparaissant à la fin d’un autre et le dernier mot apparaissant à l’begginging d’un), mais tous les autres mots (ceux qui se trouvent à l’intérieur de l’expression) doivent apparaître en tant que mots entiers.

Si la chaîne passée n’a pas d’espace blanc entre les caractères, la sous-chaîne peut être trouvée n’importe où dans un mot unique dans une autre.

Seule la présence ou l’absence d’espace blanc entre les caractères modifie les résultats de la recherche. Les espaces blancs qui ne sont pas entourés de caractères sont ignorés. Le type de l’espace blanc est ignoré (un onglet ou un espace entre les caractères donnera le même résultat). La quantité d’espace blanc n’a pas d’importance : un espace ou deux espaces entre les caractères donnent le même résultat.

La recherche ne génère pas d’événements PopulateContextNode. Seuls les traits qui ont déjà été remplis sont recherchés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




