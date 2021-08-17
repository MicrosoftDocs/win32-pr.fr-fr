---
description: La bibliothèque DbgHelp est implémentée par DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versions de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5adb00c6442f7ba36f5aeb86e0255e175131492124d08fbf865e57a9721a7893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343859"
---
# <a name="dbghelp-versions"></a>Versions de DbgHelp

La bibliothèque DbgHelp est implémentée par DbgHelp.dll. Bien que cette DLL soit incluse dans toutes les versions prises en charge de Windows, il s’agit rarement de la version la plus récente de DbgHelp disponible. en outre, la version de DbgHelp fournie dans Windows a réduit les fonctionnalités des autres versions, en particulier, elle ne prend pas en charge le serveur de symboles et le serveur Source.

les versions les plus récentes de DbgHelp.dll, SymSrv.dll et SrcSrv.dll sont disponibles dans le cadre des [outils de débogage pour Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) package. Les stratégies de redistribution pour ces dll incluses ont été spécifiquement conçues pour permettre aux utilisateurs d’inclure ces fichiers dans leurs propres packages et mises en production.

> [!Caution]  
> les utilisateurs ne doivent jamais essayer d’installer les [outils de débogage pour Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) versions de DbgHelp.dll dans les répertoires système de Windows, car ils ne sont pas testés dans ce scénario et sont susceptibles de déstabiliser le système. Il existe des versions x64 et x86 distinctes du package de débogage, et les deux sont nécessaires pour les personnes qui souhaitent prendre en charge les deux plateformes.

Pour obtenir la dernière version de DbgHelp.dll, accédez à [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) et téléchargez les outils de débogage pour Windows. Reportez-vous à [la rubrique appel de la bibliothèque dbghelp](calling-the-dbghelp-library.md) pour plus d’informations sur l’installation appropriée.

> [!Note]  
> le fichier DbgHelp.dll fourni dans Windows n’est pas redistribuable.

De nombreuses versions de DbgHelp incluent des fonctionnalités supplémentaires. Pour vous assurer que la version correcte de DbgHelp est disponible pour votre application, passez en revue les informations relatives à la configuration requise dans la documentation de référence sur les API.
