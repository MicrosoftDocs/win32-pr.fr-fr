---
title: Événement ConnectionStatusChanged
description: Se produit lorsque l’état de la connexion réseau de l’appareil change.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API de diffusion de contenu multimédia d’événements ConnectionStatusChanged
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ccc19c71b56977a77ac5ec05448ea72eaff79d9e96b42f4f297d7046079f571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060429"
---
# <a name="connectionstatuschanged-event"></a>Événement ConnectionStatusChanged

Se produit lorsque l’état de la connexion réseau de l’appareil change.

## <a name="syntax"></a>Syntaxe


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) à l’aide de la méthode [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) . Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

 

 