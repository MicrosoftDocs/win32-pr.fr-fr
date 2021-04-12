---
description: Enregistre tous les résultats d’analyse pour un IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'IInkAnalyzer :: SaveResults, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318449"
---
# <a name="iinkanalyzersaveresults-method"></a>IInkAnalyzer :: SaveResults, méthode

Enregistre tous les résultats d’analyse pour un [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulSerializedDataSize* \[ à\]
</dt> <dd>

Nombre d’octets dans *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ à\]
</dt> <dd>

Tableau contenant les résultats d’analyse enregistrés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppbSerializedData* lorsque vous n’avez plus besoin des informations.

 

Cette méthode enregistre tous les résultats d’analyse actuels, qui incluent l’indicateur d’analyse actuel et les nœuds de reconnaissance personnalisés (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)). Cette méthode n’enregistre aucune donnée de trait. Il incombe à votre application de synchroniser les résultats de l’analyse et les traits correspondants si elle conserve les données.

Cette méthode retourne un code d’erreur lorsqu’un objet [**IContextNode**](icontextnode.md) à enregistrer est partiellement rempli (consultez [**IContextNode :: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: LoadResults, méthode**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**IInkAnalyzer :: SaveResultsForNodes, méthode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer :: SaveResultsForStrokes, méthode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

