---
description: Donne accès aux reconnaissance de l’écriture manuscrite pour une utilisation avec l’analyse de l’encre.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interface IInkAnalysisRecognizer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d0736288658c57c1cfd346b8337f91353638b8326ed1d0b29687c812db72efba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350879"
---
# <a name="iinkanalysisrecognizer-interface"></a>Interface IInkAnalysisRecognizer

Donne accès aux reconnaissance de l’écriture manuscrite pour une utilisation avec l’analyse de l’encre.

## <a name="members"></a>Membres

L’interface **IInkAnalysisRecognizer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalysisRecognizer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IInkAnalysisRecognizer** possède ces méthodes.



| Méthode                                                                          | Description                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Récupère les fonctionnalités du module de reconnaissance.<br/>                                                                       |
| [**GetGuid**](iinkanalysisrecognizer-getguid.md)                               | Récupère l’identificateur global unique (GUID) du module de reconnaissance.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Récupère les identificateurs pour les paramètres régionaux pris en charge par ce **IInkAnalysisRecognizer** .<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Récupère le nom du module de reconnaissance.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Récupère les identificateurs globaux uniques (GUID) pour les propriétés prises en charge par ce **IInkAnalysisRecognizer** .<br/> |
| [**GetVendor**](iinkanalysisrecognizer-getvendor.md)                           | Récupère le nom du fournisseur du **IInkAnalysisRecognizer**.<br/>                                                        |



 

## <a name="remarks"></a>Remarques

Un module de reconnaissance possède des attributs et des propriétés spécifiques qui lui permettent d’effectuer la reconnaissance. Les propriétés d’un module de reconnaissance doivent être déterminées avant que la reconnaissance ne se produise. Les types de propriétés qu’un module de reconnaissance prend en charge déterminent les types de reconnaissance qu’il peut effectuer. Par exemple, si un module de reconnaissance ne prend pas en charge l’écriture cursive, il renvoie des résultats inexacts lorsqu’un utilisateur écrit en cursive.

Un module de reconnaissance possède également une fonctionnalité intégrée qui gère automatiquement de nombreux aspects de l’écriture manuscrite. Par exemple, il détermine les métriques pour les lignes sur lesquelles les traits sont dessinés. Vous pouvez retourner le numéro de ligne d’un trait, mais vous n’avez jamais besoin de spécifier la façon dont ces métriques de ligne sont déterminées en raison de la fonctionnalité intégrée du module de reconnaissance.

Le [**IInkAnalyzer**](iinkanalyzer.md) gère une liste des module de reconnaissance disponibles. Pour accéder à cette liste, utilisez la méthode de [**méthode IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: CreateCustomRecognizer, méthode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

