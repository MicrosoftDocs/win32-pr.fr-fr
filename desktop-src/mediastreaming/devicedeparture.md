---
title: Événement DeviceDeparture
description: Se produit lorsqu’un nouvel appareil est supprimé de la liste des appareils retournés par la méthode CachedDevices.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- API de diffusion de contenu multimédia d’événements DeviceDeparture
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511683"
---
# <a name="devicedeparture-event"></a>Événement DeviceDeparture

Se produit lorsqu’un nouvel appareil est supprimé de la liste des appareils retournés par la méthode [**CachedDevices**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Syntaxe


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) à l’aide de la méthode [**Add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) . Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .

 

 