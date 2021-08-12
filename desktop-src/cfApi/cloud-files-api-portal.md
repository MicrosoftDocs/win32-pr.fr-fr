---
description: L’API de filtre Cloud fournit des fonctionnalités à la limite entre le mode utilisateur et le système de fichiers.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Moteurs de synchronisation Cloud
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: 39dd28779c07dfd6e44fde0e53f583e72971d5883205f42581e3b5ac4102c0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551373"
---
# <a name="cloud-sync-engines"></a>Moteurs de synchronisation Cloud

Voir également [exemple Cloud Mirror](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).

à partir de Windows 10, la version 1709, Windows fournit l' *API de fichiers cloud*. Cette API est constituée de plusieurs API Win32 et WinRT natives qui formalisent la prise en charge des moteurs de synchronisation Cloud et gèrent des tâches telles que la création et la gestion de fichiers et de répertoires d’espaces réservés. les utilisateurs de cette API sont généralement des fournisseurs de synchronisation et, dans une certaine mesure, Windows applications.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique                                                                | Description                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Créer un moteur de synchronisation Cloud qui prend en charge les fichiers d’espace réservé](build-a-cloud-file-sync-engine.md)<br/> | Découvrez comment utiliser l’API de fichiers Cloud pour créer un moteur de synchronisation de fichiers Cloud qui comprend des fichiers d’espace réservé et l’intégration de l’Explorateur de fichiers. <br/> |
| [Référence du filtre Cloud](cloud-filter-reference.md)<br/> | L’API de filtre Cloud est une API Win32 native qui fait partie de l’API de fichiers Cloud plus étendue. L’API de filtre Cloud fournit des fonctionnalités à la limite entre le mode utilisateur et le système de fichiers. Cette API gère la création et la gestion de fichiers et de répertoires d’espace réservé. <br/> |