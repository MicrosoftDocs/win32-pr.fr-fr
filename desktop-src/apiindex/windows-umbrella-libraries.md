---
description: Une bibliothèque de parapluie est une bibliothèque de liens statiques unique qui exporte un sous-ensemble d’API Win32. par exemple, une bibliothèque parapluie nommée OneCore. lib fournit les exportations pour le sous-ensemble d’api Win32 qui sont communes à tous les appareils Windows 10.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Bibliothèques parapluies Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 8714f7054e11e488c61a01fd3f010faaae8c1403efdce6727e88dc26a9d5f133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737616"
---
# <a name="windows-umbrella-libraries"></a>Bibliothèques parapluies Windows

Une *bibliothèque de parapluie* est une bibliothèque de liens statiques unique qui exporte un sous-ensemble d’API Win32. par exemple, une bibliothèque de parapluie nommée **OneCore. lib** fournit les exportations pour le sous-ensemble d’api Win32 qui sont communes à tous les appareils Windows 10.

Les API d’une bibliothèque de parapluie peuvent être implémentées dans une série de modules (qu’il s’agisse d’un [ensemble d’API](windows-apisets.md) ou d’une dll), mais la bibliothèque parapluie ne vous écarte pas, ce qui rend votre application plus portable sur les versions de système d’exploitation. Il vous suffit de lier votre application de bureau ou pilote à la bibliothèque parapluie contenant l’ensemble d’API qui vous intéresse, et c’est tout ce que vous devez faire. 

| Bibliothèque | Description |
|------------------------|-------------------------|
| OneCore. lib | cette bibliothèque fournit les exportations pour le sous-ensemble d’api Win32 qui sont communes à tous les appareils Windows 10. liez votre application de bureau ou pilote à OneCore. lib (et aucune autre bibliothèque) pour accéder à ces api. si vous liez votre application ou pilote à OneCore. lib et que vous appelez uniquement des api Win32 dans cette bibliothèque, votre application ou pilote se chargera correctement sur tous les appareils Windows 10.         |
| OneCore_apiset. lib | cette bibliothèque fournit la même couverture que OneCore. lib, mais utilise l' [API de redirection directe](api-set-loader-operation.md#direct-forwarding). notez que l’utilisation de cette bibliothèque sera compatible uniquement avec la version de Windows 10, comme spécifié par la version du kit de développement logiciel (SDK) que vous ciblez ou une version ultérieure.  |
| OneCoreUap. lib | cette bibliothèque fournit les exportations pour le sous-ensemble d’api Win32 qui sont communes à tous les appareils Windows 10 qui prennent en charge l’Windows Runtime (WinRT). Liez votre application de bureau ou pilote à OneCoreUap. lib (et aucune autre bibliothèque) pour accéder à ces API. si vous liez votre application ou pilote à OneCoreUap. lib, et que vous appelez uniquement des api Win32 dans cette bibliothèque, votre application ou pilote se chargera correctement sur tous les appareils Windows 10 qui prennent en charge UWP. |
| OneCoreUAP_apiset. lib | Cette bibliothèque fournit la même couverture que OneCoreUAP. lib, mais utilise la technique de [transfert direct de l’API Set](api-set-loader-operation.md#direct-forwarding) . notez que l’utilisation de cette bibliothèque sera compatible uniquement avec la version de Windows 10, comme spécifié par le kit de développement logiciel (SDK) que vous ciblez ou une version ultérieure.  |
