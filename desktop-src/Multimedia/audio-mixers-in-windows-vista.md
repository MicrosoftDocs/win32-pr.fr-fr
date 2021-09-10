---
title: mixages Audio dans Windows Vista
description: mixages Audio dans Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- audio multimédia, Windows de mixage audio Vista
- audio, Windows les mixages audio Vista
- mixages audio, Windows Vista
- mélangeurs, Windows Vista
- Windows Mixages audio Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368652"
---
# <a name="audio-mixers-in-windows-vista"></a>mixages Audio dans Windows Vista

à partir de Windows Vista, certains contrôles de mixage sont implémentés dans des logiciels plutôt que sur du matériel. par exemple, les contrôles de volume sont implémentés à l’aide de l’API de session audio Windows (WASAPI). Ces contrôles n’affectent pas directement les paramètres matériels. En outre, ils sont associés à une session audio spécifique au processus, de sorte que les modifications affectent l’application appelante, mais n’affectent pas les autres applications.

Chaque périphérique de point de terminaison audio dispose d’une disposition de mélangeur standard, implémentée dans le logiciel.

-   Chaque point de terminaison de rendu audio contient une ligne de destination qui contient les éléments suivants :
    -   Contrôle du volume
    -   Contrôle muet
    -   Ligne source : sortie Waveform-Audio.
    -   Ligne source : CD audio.
-   Chaque point de terminaison de capture audio contient une ligne de destination qui contient les éléments suivants :
    -   Contrôle du volume
    -   Contrôle muet
    -   Ligne source : entrée Waveform-Audio. Le type de composant dépend de l’appareil d’entrée, par exemple un microphone.

Chaque ligne source contient un contrôle de volume et un contrôle muet. Le diagramme suivant montre les composants des points de terminaison de rendu et de capture.

![dispositions par défaut du mélangeur](images/mixer1.gif)

Tous les contrôles d’un point de terminaison manipulent le même contrôle logiciel sous-jacent. Par conséquent, si vous modifiez les paramètres d’un contrôle, vous recevrez une notification de modification de contrôle sur les autres contrôles. (Voir [**la \_ \_ \_ modification du contrôle mm MIXM**](mm-mixm-control-change.md).)

Cette disposition standard est fournie à des fins de compatibilité avec les applications existantes qui utilisent les fonctions de mixage audio. Les nouvelles applications doivent éviter d’utiliser ces fonctions.

 

 




