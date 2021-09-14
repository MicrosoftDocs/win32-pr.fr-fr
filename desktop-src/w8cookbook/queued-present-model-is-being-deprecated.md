---
title: Le modèle actuel mis en file d’attente est déconseillé
description: Le modèle actuel mis en file d’attente est déconseillé
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295270"
---
# <a name="queued-present-model-is-being-deprecated"></a>Le modèle actuel mis en file d’attente est déconseillé

## <a name="platforms"></a>Plateformes

**Clients** – après Windows 8  
**Serveurs** – après Windows Server 2012  


## <a name="description"></a>Description

dans la version Windows après Windows 8, ces api retournent E \_ NOTIMPL :

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

En outre, cette API n’accepte que la valeur NULL pour le paramètre HWND :

-   DwmGetCompositionTimingInfo

Nous allons arrêter de prendre en charge DwmGetCompositionTimingInfo avec HWND ! = NULL et supprimer les fonctionnalités associées. Si vous spécifiez une valeur non NULL pour HWND, cette API retourne E \_ INVALIDARG.

Nous déconseillons également l’utilisation de l’API DwmGetCompositionTimingInfo et suggérons que les développeurs basculent vers le modèle de retournement DXGI et l’API de statistiques de présentation de DX associée.

## <a name="manifestation"></a>Manifestation

Les applications qui utilisent le modèle présent mis en file d’attente ne fonctionneront pas correctement. La manifeste exacte dépend de l’application particulière, mais peut aller de la durée de présentation incorrecte à l’application se ferme de manière inattendue. Dans la pratique, nous ne pensons pas que de nombreuses applications (le cas échéant). ce modèle a été utilisé par Vista media player, qui ne sera pas utilisé sur Windows 8 (et éventuellement l’ancien Zune player). À ce stade, nous n’avons pas d’informations sur les autres applications qui utilisent réellement ce modèle.

## <a name="solution"></a>Solution

les développeurs doivent utiliser le mode de présentation DXGI à la place de la mise en file d’attente (disponible dans le runtime virtuel dx9 depuis Windows 7, et sur les runtimes facilement et DX11 dans Windows 8).

## <a name="tests"></a>Tests

exécutez des tests généraux pour vous assurer que la boîte de réception Windows composants et les principaux produits continuent de fonctionner sur la prochaine version de Windows.

 

 




