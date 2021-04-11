---
title: Événement RenderingParametersUpdate
description: Se produit chaque fois qu’un jeu de paramètres de contrôle de rendu est mis à jour sur le DMR.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- API de diffusion de contenu multimédia d’événements RenderingParametersUpdate
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314849"
---
# <a name="renderingparametersupdate-event"></a>Événement RenderingParametersUpdate

Se produit chaque fois qu’un jeu de paramètres de contrôle de rendu est mis à jour sur le DMR.

## <a name="syntax"></a>Syntaxe


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) à l’aide de la méthode [**Add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) . Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .

 

 