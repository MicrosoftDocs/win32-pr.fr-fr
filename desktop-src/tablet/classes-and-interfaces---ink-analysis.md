---
description: Cette section contient des informations sur les interfaces et les classes utilisées dans l’analyse de l’encre. Les classes et les interfaces d’analyse de l’encre ne sont pas conformes à Automation.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Classes et interfaces d’analyse de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524934"
---
# <a name="ink-analysis-classes-and-interfaces"></a>Classes et interfaces d’analyse de l’encre

Cette section contient des informations sur les interfaces et les classes utilisées dans l’analyse de l’encre. Les classes et les interfaces d’analyse de l’encre ne sont pas conformes à Automation.

## <a name="classes"></a>Classes



| Classe                                    | Description                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**AnalysisRegion**](analysisregion.md) | Implémente l’interface [**IAnalysisRegion**](ianalysisregion.md) .<br/> |
| [**InkAnalyzer**](inkanalyzer.md)       | Implémente l’interface [**IInkAnalyzer**](iinkanalyzer.md) .<br/>       |



 

## <a name="interfaces"></a>Interfaces



| Interface                                                    | Description                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAnalysisAlternate**](ianalysisalternate.md)             | Représente les correspondances possibles pour les mots de reconnaissance de l’écriture manuscrite pour les objets [**IContextNode**](icontextnode.md) .<br/>                                                                                        |
| [**IAnalysisAlternates**](ianalysisalternates.md)           | Contient une collection d’objets qui implémentent l’interface [**IAnalysisAlternate**](ianalysisalternate.md) et qui sont le résultat de l’analyse de l’encre.<br/>                                               |
| [**IAnalysisRegion**](ianalysisregion.md)                   | Expose des méthodes et des propriétés pour une zone qui représente une zone d’un document.<br/>                                                                                                                    |
| [**IAnalysisStatus**](ianalysisstatus.md)                   | Représente l’état de l’opération d’analyse de l’encre en décrivant si l’analyse a été effectuée avec succès et si des avertissements se sont produits.<br/>                                                  |
| [**IAnalysisWarning**](ianalysiswarning.md)                 | Représente un avertissement ou une erreur qui se produit pendant une opération d’analyse d’encre.<br/>                                                                                                                           |
| [**IAnalysisWarnings**](ianalysiswarnings.md)               | Contient une collection d’objets qui implémentent l’interface [**IAnalysisWarning**](ianalysiswarning.md) et qui sont le résultat d’une opération d’analyse d’encre.<br/>                                      |
| [**IContextLink**](icontextlink.md)                         | Représente une relation entre deux objets [**IContextNode**](icontextnode.md) .<br/>                                                                                                                   |
| [**IContextLinks**](icontextlinks.md)                       | Contient une collection d’objets qui implémentent l’interface [**IContextLink**](icontextlink.md) .<br/>                                                                                                   |
| [**IContextNode**](icontextnode.md)                         | Représente un nœud dans une arborescence d’objets qui sont créés dans le cadre de l’analyse de l’encre.<br/>                                                                                                                      |
| [**IContextNodes**](icontextnodes.md)                       | Contient une collection d’objets qui implémentent l’interface [**IContextNode**](icontextnode.md) et qui sont le résultat d’une opération d’analyse d’encre.<br/>                                              |
| [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)     | Donne accès aux reconnaissance de l’écriture manuscrite pour une utilisation avec l’analyse de l’encre.<br/>                                                                                                                                 |
| [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)   | Contient une collection d’objets qui implémentent l’interface [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) et qui représentent la capacité de reconnaître l’écriture manuscrite, les objets ou les gestes.<br/> |
| [**IInkAnalyzer**](iinkanalyzer.md)                         | Donne accès à l’analyse de la disposition, à l’écriture et au dessin de la classification et à la reconnaissance de l’écriture manuscrite<br/>                                                                                                  |
| [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) | Expose une méthode pour évaluer si un objet [**IContextNode**](icontextnode.md) satisfait ou échoue à un critère spécifié.<br/>                                                                              |



 

## <a name="return-values"></a>Valeurs de retour

Les méthodes de la bibliothèque COM Tablet PC retournent des valeurs de **HRESULT**. Sauf indication contraire, les significations des valeurs **HRESULT** sont décrites dans ce tableau.



| Valeur HRESULT                                   | Description                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| \_OK<br/>                                | Opération réussie.<br/>                                                                      |
| \_pointeur E<br/>                           | Au moins un pointeur (pour un paramètre d’entrée ou de sortie) n’est pas valide.<br/> |
| E \_ INVALIDARG<br/>                        | Le membre a tenté de passer un argument non valide.<br/>                              |
| \_exception encre \_ E<br/>                    | Une exception s’est produite.<br/>                                                           |
| \_OUTOFMEMORY E<br/>                       | Le système ne peut pas allouer de mémoire pour terminer l’opération.<br/>                      |
| E \_ échec<br/>                              | Une erreur non spécifiée s’est produite.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | Le membre a tenté d’utiliser une opération non valide.<br/>                                 |
| TPC \_ E \_ mode non valide \_<br/>                | Le membre a tenté d’utiliser un mode non valide.<br/>                                      |
| \_configuration TPC E \_ non valide \_<br/>       | Le membre a tenté d’utiliser une configuration non valide.<br/>                             |
| \_Description du paquet TPC E \_ non valide \_ \_<br/> | Le membre a tenté d’utiliser une description de paquet non valide.<br/>                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




