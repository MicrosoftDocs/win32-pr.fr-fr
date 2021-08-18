---
title: Événement TransportParametersUpdate
description: Se produit chaque fois qu’un ensemble de paramètres de transport est mis à jour sur le DMR.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- API de diffusion de contenu multimédia d’événements TransportParametersUpdate
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e3a600b7345b2cf05b5fb76f20b968e1af9ddecfb72f8442ada34dfd98ae3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034517"
---
# <a name="transportparametersupdate-event"></a>Événement TransportParametersUpdate

Se produit chaque fois qu’un ensemble de paramètres de transport est mis à jour sur le DMR.

## <a name="syntax"></a>Syntaxe


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) à l’aide de la méthode [**Add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) . Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .

 

 