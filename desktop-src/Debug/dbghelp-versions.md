---
description: La bibliothèque DbgHelp est implémentée par DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versions de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747741"
---
# <a name="dbghelp-versions"></a>Versions de DbgHelp

La bibliothèque DbgHelp est implémentée par DbgHelp.dll. Bien que cette DLL soit incluse dans toutes les versions prises en charge de Windows, il s’agit rarement de la version la plus récente de DbgHelp disponible. En outre, la version de DbgHelp fournie dans Windows a réduit les fonctionnalités des autres versions, en particulier, elle ne prend pas en charge le serveur de symboles et le serveur source.

Les versions les plus récentes de DbgHelp.dll, SymSrv.dll et SrcSrv.dll sont disponibles dans le cadre du package [outils de débogage pour Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) . Les stratégies de redistribution pour ces dll incluses ont été spécifiquement conçues pour permettre aux utilisateurs d’inclure ces fichiers dans leurs propres packages et mises en production.

> [!Caution]  
> Les utilisateurs ne doivent jamais essayer d’installer les [outils de débogage pour](https://developer.microsoft.com/windows/downloads/windows-10-sdk) les versions windows de DbgHelp.dll dans les répertoires système Windows, car ils ne sont pas testés dans ce scénario et risquent de déstabiliser le système. Il existe des versions x64 et x86 distinctes du package de débogage, et les deux sont nécessaires pour les personnes qui souhaitent prendre en charge les deux plateformes.

Pour obtenir la dernière version de DbgHelp.dll, accédez à [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) et téléchargez les outils de débogage pour Windows. Reportez-vous à [la rubrique appel de la bibliothèque dbghelp](calling-the-dbghelp-library.md) pour plus d’informations sur l’installation appropriée.

> [!Note]  
> Le fichier DbgHelp.dll fourni dans Windows n’est pas redistribuable.

De nombreuses versions de DbgHelp incluent des fonctionnalités supplémentaires. Pour vous assurer que la version correcte de DbgHelp est disponible pour votre application, passez en revue les informations relatives à la configuration requise dans la documentation de référence sur les API.
