---
description: API audio principales
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: API audio principales
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 2cabb462d13786c874401394fa814484f79b0e3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115062"
---
# <a name="core-audio-apis"></a>API audio principales

> [!NOTE]
> Pour obtenir des exemples de code, consultez [le kit de développement logiciel (SDK) qui utilise les API audio principales](./sdk-samples-that-use-the-core-audio-apis.md).

cette documentation fournit des informations sur les interfaces de programmation d’applications (api) audio principales pour la famille de systèmes d’exploitation Microsoft Windows. il fournit des recommandations pour les développeurs de logiciels à suivre dans le développement d’applications qui utilisent les api audio de base dans Windows Vista. ces api sont nouvelles dans Windows Vista et ne sont pas disponibles dans les versions antérieures de Windows.

Les API audio principales permettent aux applications audio d’accéder à des périphériques de point de terminaison audio tels que des casques et des microphones. les api audio principales jouent le rôle de base pour les api audio de niveau supérieur, telles que Microsoft DirectSound et Windows les fonctions **waveXxx** multimedia. La plupart des applications communiquent avec les API de niveau supérieur, mais certaines applications avec des exigences spéciales peuvent avoir besoin de communiquer directement avec les API audio de base.

à partir de Windows 7, les api existantes ont été améliorées et de nouvelles api ont été ajoutées pour prendre en charge de nouveaux scénarios. Les API de gestion de flux et de sessions ont été améliorées afin que l’application puisse désormais énumérer et obtenir un contrôle étendu sur la session audio. En utilisant les nouvelles API, l’application peut implémenter une expérience d’atténuation de flux personnalisée. Les nouvelles API associées aux appareils fournissent un accès aux propriétés du pilote des appareils de point de terminaison.

Cette documentation contient les sections suivantes.

| Section                                                                    | Description                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [à propos des api Audio Windows Core](about-the-windows-core-audio-apis.md) | fournit une vue d’ensemble des api audio Windows core et décrit les concepts de base. |
| [Guide de programmation](programming-guide.md)                                 | Décrit les principales fonctionnalités des API audio principales et comment les utiliser.            |
| [Guide de référence de programmation](programming-reference.md)                         | Fournit des informations de référence sur C++ pour les principales API audio.                       |

## <a name="related-topics"></a>Rubriques connexes

[Technologies multimédias pour Windows](/previous-versions/bg125389(v=msdn.10))

[Exemples de SDK qui utilisent les API audio principales](./sdk-samples-that-use-the-core-audio-apis.md)