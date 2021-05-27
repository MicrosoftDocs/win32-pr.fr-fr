---
description: L’API de filtre Cloud fournit des fonctionnalités à la limite entre le mode utilisateur et le système de fichiers.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Moteurs de synchronisation Cloud
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549594"
---
# <a name="cloud-sync-engines"></a>Moteurs de synchronisation Cloud

Voir également [exemple Cloud Mirror](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).

À compter de Windows 10, version 1709, Windows fournit l' *API de fichiers Cloud*. Cette API est constituée de plusieurs API Win32 et WinRT natives qui formalisent la prise en charge des moteurs de synchronisation Cloud et gèrent des tâches telles que la création et la gestion de fichiers et de répertoires d’espaces réservés. Les utilisateurs de cette API sont généralement des fournisseurs de synchronisation et, dans une certaine mesure, des applications Windows.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique                                                                | Description                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Créer un moteur de synchronisation Cloud qui prend en charge les fichiers d’espace réservé](build-a-cloud-file-sync-engine.md)<br/> | Découvrez comment utiliser l’API de fichiers Cloud pour créer un moteur de synchronisation de fichiers Cloud qui comprend des fichiers d’espace réservé et l’intégration de l’Explorateur de fichiers. <br/> |
| [Référence du filtre Cloud](cloud-filter-reference.md)<br/> | L’API de filtre Cloud est une API Win32 native qui fait partie de l’API de fichiers Cloud plus étendue. L’API de filtre Cloud fournit des fonctionnalités à la limite entre le mode utilisateur et le système de fichiers. Cette API gère la création et la gestion de fichiers et de répertoires d’espace réservé. <br/> |