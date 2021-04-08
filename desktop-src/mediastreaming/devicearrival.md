---
title: Événement DeviceArrival
description: Se produit lorsqu’un nouvel appareil est ajouté à la liste des appareils retournés par la méthode CachedDevices.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- API de diffusion de contenu multimédia d’événements DeviceArrival
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79fbdd68ae6c77c6a0f3e7bbd3cf976b5d056987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725396"
---
# <a name="devicearrival-event"></a>Événement DeviceArrival

Se produit lorsqu’un nouvel appareil est ajouté à la liste des appareils retournés par la méthode [**CachedDevices**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Syntaxe


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) à l’aide de la méthode [**Add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) . Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .

 

 