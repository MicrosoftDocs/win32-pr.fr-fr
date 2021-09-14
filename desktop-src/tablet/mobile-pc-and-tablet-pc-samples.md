---
description: vue d’ensemble des exemples de code de l’interface de programmation d’applications (API) pour les sections Tablet pc et Windows Touch du SDK Windows.
ms.assetid: 4ede7d0e-e826-4b3a-8a46-0f3162c19cb0
title: Exemples tablette et Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8562dcc1baa42f44d6ca675344d658b1bf693cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196248"
---
# <a name="tablet-and-touch-samples"></a>Exemples tablette et Touch

cette section contient des exemples qui montrent comment les applications peuvent être développées avec C \# , Microsoft Visual Basic .net et C++ pour fonctionner avec l’entrée manuscrite et tactile.

Par défaut, les exemples sont installés dans <system drive> : \\ fichiers programme \\ Microsoft Tablet PC Platform SDK \\ Samples \\ lors de l’installation du kit de développement logiciel (SDK) Tablet PC.

> [!Note]  
> lors de l’installation du SDK Windows, du kit de développement logiciel (sdk) Windows Server ou du kit de développement logiciel (sdk) .NET Framework, les exemples s’installent dans le chemin par défaut de ce kit sdk.

 

## <a name="available-samples"></a>Exemples disponibles



| Exemple                                                                           | Description                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconnaissance avancée](advanced-recognition-sample.md)                          | Présente certaines des fonctionnalités de reconnaissance plus avancées, telles que le choix explicite du module de reconnaissance, Factoids et bien plus encore.<br/>                                                                                                                                                             |
| [Formulaire de revendications automatiques](auto-claims-form-sample.md)                                  | Illustre l’utilisation de deux contrôles Ink : le contrôle [InkEdit](/previous-versions/ms552265(v=vs.100)) et le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) .<br/>                                                                                                        |
| [Reconnaissance de base](basic-recognition-sample.md)                                | Montre comment générer une application de reconnaissance de l’écriture manuscrite simple à l’aide de l’objet [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) .<br/>                                                                                                                     |
| [Récepteurs d’événements C++](c---event-sinks-sample.md)                                    | Montre les modèles en C++ pour tous les événements de plateforme Tablet, qui peuvent être sous-classés, ou copiés et collés et utilisés comme code de modèle.<br/>                                                                                                                                   |
| [Saisie semi-automatique des caractères](character-autocomplete-sample.md)                      | Montre comment implémenter la saisie semi-automatique de caractères en japonais à l’aide des API de reconnaissance.<br/>                                                                                                                                                                                 |
| [Exemple de blog manuscrit](ink-blog-web-sample.md)                                   | Montre comment créer un contrôle utilisateur managé qui a une fonctionnalité d’encrage et héberger ce contrôle dans Internet Explorer<br/>                                                                                                                                                         |
| [Presse-papiers manuscrits](ink-clipboard-sample.md)                                        | Illustre l’interopérabilité de l’encre à l’aide du presse-papiers.<br/>                                                                                                                                                                                                                          |
| [Collection d’encres](ink-collection-sample.md)                                      | illustre une application de formulaire Windows simple qui utilise l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) pour collecter l’encre.<br/>                                                                                                                                     |
| [Diviseur d’encre](ink-divider-sample.md)                                            | Montre comment utiliser l’objet [diviseur](/previous-versions/ms839398(v=msdn.10)) pour effectuer une analyse de l’encre.<br/>                                                                                                                                                                            |
| [Effacement d’encre](ink-erasing-sample.md)                                            | illustre la suppression de traits d’encre dans une application de formulaire Windows qui utilise l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) pour collecter de l’encre.<br/>                                                                                                             |
| [Test d’atteinte de l’encre](ink-hit-test-sample.md)                                          | Illustre deux façons d’effectuer des tests d’atteinte de l’encre.<br/>                                                                                                                                                                                                                                       |
| [Reconnaissance de l’encre](ink-recognition-sample.md)                                    | Montre comment vous pouvez créer une application de reconnaissance de l’écriture manuscrite simple.<br/>                                                                                                                                                                                                    |
| [Sérialisation de l’encre](ink-serialization-sample.md)                                | Montre comment sérialiser de l’encre au format ISF (Ink Serialized Format).<br/>                                                                                                                                                                                                           |
| [Exemple de contrôle Web Ink](ink-web-control-sample.md)                             | Montre comment créer un contrôle Ink pour une utilisation dans un navigateur Web.<br/>                                                                                                                                                                                                             |
| [Zoom d’encre](ink-zoom-sample.md)                                                  | Montre comment effectuer un zoom correct de l’encre dans une application.<br/>                                                                                                                                                                                                                        |
| [Exemple de reconnaissance multiple](multiple-recognizers-sample.md)                   | Montre comment effectuer une sélection parmi un large éventail de détecteurs installés, puis utiliser le module de reconnaissance sélectionné.<br/>                                                                                                                                                                        |
| [Exemple de déploiement Web sans toucher](no-touch-deployment-web-sample.md)             | Montre comment utiliser l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) pour simplifier la saisie de texte dans vos applications de formulaire. Étend l’exemple de formulaire de déclaration automatique.<br/>                                                                                      |
| [PenInputPanel](peninputpanel-sample.md)                                        | Montre comment utiliser l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) pour simplifier la saisie de texte dans vos applications de formulaire. Étend l’exemple de formulaire de déclaration automatique.<br/>                                                                                      |
| [Exemple de collection d’encres RealTimeStylus](realtimestylus-ink-collection-sample.md) | Illustre la collecte d’encres à l’aide du RealTimeStylus.<br/>                                                                                                                                                                                                                           |
| [Exemple de plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)               | Illustre l’utilisation d’RealTimeStylus.<br/>                                                                                                                                                                                                                                       |
| [Exemple de formulaire papier numérisé](scanned-paper-form-sample.md)                       | Montre l’utilisation d’un formulaire analysé dans en tant que bitmap et spécifié comme image d’arrière-plan pour un contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) sur le haut d’un formulaire. Plusieurs régions ont été activées pour la collection d’encres (ou, spécifiée sous la forme « inkable »).<br/> |
| [Exemple d’informations sur la plateforme Tablet PC](tablet-pc-platform-info-sample.md)             | illustre l’utilisation de la fonction d’API GetSystemMetrics () Windows pour déterminer si l’application s’exécute sur un Tablet PC.<br/>                                                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de modèle de DLL de reconnaissance](recognizer-dll-sample-template.md)
</dt> </dl>

 

