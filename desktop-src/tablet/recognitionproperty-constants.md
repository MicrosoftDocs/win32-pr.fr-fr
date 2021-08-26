---
description: Définit des valeurs qui spécifient les propriétés d’un substitut de reconnaissance. L’interface de programmation d’applications (API) Tablet PC utilise des identificateurs globaux uniques (GUID) pour identifier les propriétés des paquets, qui sont des chaînes constantes dans Automation.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Constantes RecognitionProperty (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d06d2eed3b28ed99d180dbe3971e9e018554ff5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467986"
---
# <a name="recognitionproperty-constants"></a>Constantes RecognitionProperty

Définit des valeurs qui spécifient les propriétés d’un substitut de reconnaissance. L’interface de programmation d’applications (API) Tablet PC utilise des identificateurs globaux uniques (GUID) pour identifier les propriétés des paquets, qui sont des chaînes constantes dans Automation.

Le tableau suivant répertorie les champs de l’identificateur global unique (GUID) de la propriété de remplacement disponibles. Utilisez ces GUID pour accéder aux propriétés d’un objet [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) en appelant la méthode [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .




| Nom de la constante | Description | 
|---------------|-------------|
| <span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt></dl> | GUID qui identifie la propriété pour le numéro de ligne de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br /> LineNumber spécifie les alternatives avec un numéro de ligne particulier.<br /><blockquote>[!Note]<br />Ce champ n’est pas pris en charge pour les identificateurs de caractères d’Extrême-Orient.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt></dl> | GUID qui identifie la propriété pour la segmentation de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br /> La segmentation spécifie le fragment ou l’unité d’encre de base que le module de reconnaissance utilise pour produire un résultat de reconnaissance.<br /><blockquote>[!Note]<br />Non implémenté.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt></dl> | GUID qui identifie la propriété pour le point réactif de reconnaissance de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt></dl> | GUID qui identifie la propriété pour le nombre de traits maximal du résultat de la reconnaissance pour l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br /><blockquote>[!Note]<br />Non implémenté.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt></dl> | GUID qui identifie la propriété de la métrique point par pouce de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br /><blockquote>[!Note]<br />Non implémenté.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt></dl> | GUID qui identifie la propriété pour le niveau de confiance que le module de reconnaissance a dans le résultat de la reconnaissance.<br /><blockquote>[!Note]<br />l’évaluation de la confiance est disponible uniquement pour États-Unis anglais et tous les module de reconnaissance de mouvement dans Microsoft Windows XP édition Tablet PC et Windows Vista. Les méthodes qui fournissent la propriété confidence pour tout autre module de reconnaissance retournent E_NOTIMPL.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt></dl> | GUID qui identifie la propriété pour les métriques de ligne de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> , qui est la ligne pour laquelle les métriques doivent être récupérées. <br /> | 




## <a name="remarks"></a>Remarques

en C++, vous pouvez accéder à ces constantes dans le fichier d’en-tête Msinkaut. h, situé dans le <systemdrive> \\ répertoire : Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ include si vous avez installé le kit de développement logiciel (sdk) à l’emplacement par défaut.

> [!Note]  
> En C++, ces constantes sont WCHARs, et non BSTR. Convertissez-les en BSTR avant d’utiliser. Pour plus d’informations sur le type de données BSTR, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode AlternatesWithConstantPropertyValues**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[**Propriété ConfidenceAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[**Propriété LineAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[**Interface IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




