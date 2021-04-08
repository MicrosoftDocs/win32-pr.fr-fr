---
description: Cette section contient des informations sur les interfaces et les classes utilisées dans le stylet en temps réel.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Classes et interfaces RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866133"
---
# <a name="realtimestylus-classes-and-interfaces"></a>Classes et interfaces RealTimeStylus

Cette section contient des informations sur les interfaces et les classes utilisées dans le stylet en temps réel.

> [!Note]  
> Les interfaces et les classes de stylet en temps réel ne sont pas conformes à Automation.

 

## <a name="in-this-section"></a>Dans cette section



| Classe                                                      | Description                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**RealTimeStylus, classe**](realtimestylus-class.md)       | Implémente l’interface [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .<br/>                 |
| [**DynamicRenderer (classe)**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | Implémente l’interface d' [**interface IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .<br/>     |
| [**GestureRecognizer, classe**](gesturerecognizer-class.md) | Implémente l’interface d' [**interface IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .<br/> |
| [**StrokeBuilder, classe**](strokebuilder-class.md)         | Implémente l’interface d' [**interface IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .<br/>         |



 

## <a name="interfaces"></a>Interfaces



| Interface                                                                          | Description                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | Expose des méthodes qui vous permettent de contrôler l’affichage des données de stylet en temps réel, car les données sont gérées par l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) .<br/> |
| [**Interface IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | Expose des méthodes qui vous permettent de réagir aux événements en reconnaissant des gestes de stylet et en vous permettant d’ajouter des données à la file d’attente d’entrée.<br/>                                                  |
| [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | Gère les données de paquet du stylet à partir d’un digitaliseur en temps réel.<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | Étend l’interface IRealTimeStylus.<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | Étend l’interface IRealTimeStylus.<br/>                                                                                                                                           |
| [**Interface IRealTimeStylusSynchronization**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | Synchronise l’accès à l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                                                                          |
| [**Interface IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | Expose des méthodes qui vous permettent de créer par programmation des traits.<br/>                                                                                                              |
| [**Interface IStylusPlugin**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | Expose des méthodes vous permettant de recevoir des notifications d’événements et d’effectuer un traitement personnalisé en fonction de ces événements.<br/>                                                          |
| [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | Représente un plug-in asynchrone qui peut être ajouté à la collection de plug-ins asynchrones de la [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                |
| [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | Représente un plug-in synchrone qui peut être ajouté à la collection de plug-ins synchrones de la [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                   |



 

## <a name="return-values"></a>Valeurs de retour

Les méthodes de la bibliothèque COM retournent des valeurs de **HRESULT**. Sauf indication contraire, les significations des valeurs **HRESULT** sont décrites dans le tableau suivant.



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

[Référence RealTimeStylus](realtimestylus-reference.md)
</dt> </dl>

 

 
