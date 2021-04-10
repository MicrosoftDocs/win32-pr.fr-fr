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
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726764"
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

## <a name="remarks"></a>Notes

Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) à l’aide de la méthode [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) . Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

 

 