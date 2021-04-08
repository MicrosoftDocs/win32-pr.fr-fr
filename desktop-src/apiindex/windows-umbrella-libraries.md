---
description: Une bibliothèque de parapluie est une bibliothèque de liens statiques unique qui exporte un sous-ensemble d’API Win32. Par exemple, une bibliothèque parapluie nommée OneCore. lib fournit les exportations pour le sous-ensemble d’API Win32 qui sont communes à tous les appareils Windows 10.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Bibliothèques parapluies Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 86a8f9b8f3bef5081bd7e0e64300b9295fd85401
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "103734781"
---
# <a name="windows-umbrella-libraries"></a>Bibliothèques parapluies Windows

Une *bibliothèque de parapluie* est une bibliothèque de liens statiques unique qui exporte un sous-ensemble d’API Win32. Par exemple, une bibliothèque de parapluie nommée **OneCore. lib** fournit les exportations pour le sous-ensemble d’API Win32 qui sont communes à tous les appareils Windows 10.

Les API d’une bibliothèque de parapluie peuvent être implémentées dans une série de modules (qu’il s’agisse d’un [ensemble d’API](windows-apisets.md) ou d’une dll), mais la bibliothèque parapluie ne vous écarte pas, ce qui rend votre application plus portable sur les versions de système d’exploitation. Il vous suffit de lier votre application de bureau ou pilote à la bibliothèque parapluie contenant l’ensemble d’API qui vous intéresse, et c’est tout ce que vous devez faire. 

| Bibliothèque | Description |
|------------------------|-------------------------|
| OneCore. lib | Cette bibliothèque fournit les exportations pour le sous-ensemble d’API Win32 qui sont communes à tous les appareils Windows 10. Liez votre application de bureau ou pilote à OneCore. lib (et aucune autre bibliothèque) pour accéder à ces API. Si vous liez votre application ou pilote à OneCore. lib, et que vous appelez uniquement des API Win32 dans cette bibliothèque, votre application ou pilote se chargera correctement sur tous les appareils Windows 10.         |
| OneCore_apiset. lib | Cette bibliothèque fournit la même couverture que OneCore. lib, mais utilise l' [API de réacheminement direct](api-set-loader-operation.md#direct-forwarding). Notez que l’utilisation de cette bibliothèque sera compatible uniquement avec la version de Windows 10 telle que spécifiée par la version du kit de développement logiciel (SDK) que vous ciblez ou une version ultérieure.  |
| OneCoreUap. lib | Cette bibliothèque fournit les exportations pour le sous-ensemble d’API Win32 qui sont communes à tous les appareils Windows 10 qui prennent en charge le Windows Runtime (WinRT). Liez votre application de bureau ou pilote à OneCoreUap. lib (et aucune autre bibliothèque) pour accéder à ces API. Si vous liez votre application ou pilote à OneCoreUap. lib, et que vous appelez uniquement des API Win32 dans cette bibliothèque, votre application ou pilote se chargera correctement sur tous les appareils Windows 10 qui prennent en charge UWP. |
| OneCoreUAP_apiset. lib | Cette bibliothèque fournit la même couverture que OneCoreUAP. lib, mais utilise la technique de [transfert direct de l’API Set](api-set-loader-operation.md#direct-forwarding) . Notez que l’utilisation de cette bibliothèque sera compatible uniquement avec la version Windows 10 telle que spécifiée par le kit de développement logiciel (SDK) que vous ciblez ou supérieur.  |
