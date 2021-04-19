---
title: Le modèle actuel mis en file d’attente est déconseillé
description: Le modèle actuel mis en file d’attente est déconseillé
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "106511108"
---
# <a name="queued-present-model-is-being-deprecated"></a>Le modèle actuel mis en file d’attente est déconseillé

## <a name="platforms"></a>Plateformes

**Clients** – après Windows 8  
**Serveurs** – après Windows Server 2012  


## <a name="description"></a>Description

Dans la version Windows ultérieure à Windows 8, ces API retournent E \_ NOTIMPL :

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

En outre, cette API n’accepte que la valeur NULL pour le paramètre HWND :

-   DwmGetCompositionTimingInfo

Nous allons arrêter de prendre en charge DwmGetCompositionTimingInfo avec HWND ! = NULL et supprimer les fonctionnalités associées. Si vous spécifiez une valeur non NULL pour HWND, cette API retourne E \_ INVALIDARG.

Nous déconseillons également l’utilisation de l’API DwmGetCompositionTimingInfo et suggérons que les développeurs basculent vers le modèle de retournement DXGI et l’API de statistiques de présentation de DX associée.

## <a name="manifestation"></a>Manifestation

Les applications qui utilisent le modèle présent mis en file d’attente ne fonctionneront pas correctement. La manifeste exacte dépend de l’application particulière, mais peut aller de la durée de présentation incorrecte à l’application se ferme de manière inattendue. Dans la pratique, nous ne pensons pas que de nombreuses applications (le cas échéant). Ce modèle a été utilisé par Vista Media Player, qui ne sera pas utilisé sur Windows 8 (et éventuellement l’ancien lecteur Zune). À ce stade, nous n’avons pas d’informations sur les autres applications qui utilisent réellement ce modèle.

## <a name="solution"></a>Solution

Les développeurs doivent utiliser le mode de présentation DXGI à la place de la mise en file d’attente (disponible dans le runtime virtuel DX9 depuis Windows 7, ainsi que sur les runtimes facilement et DX11 dans Windows 8).

## <a name="tests"></a>Tests

Exécutez des tests généraux pour vous assurer que les composants Windows de la boîte de réception et les produits principaux continuent de fonctionner sur la prochaine version de Windows.

 

 




