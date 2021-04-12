---
title: Propriété de convertisseur DevicePair
description: Obtient le convertisseur pour la paire d’appareils de base active.
ms.assetid: DB2ED5D3-CCDF-4704-A29A-F1A13F7B953A
keywords:
- API de diffusion multimédia en continu des propriétés de convertisseur
- Propriété de convertisseur diffusion multimédia en continu API, interface DevicePair
- API de diffusion multimédia en continu de l’interface DevicePair, propriété de convertisseur
topic_type:
- apiref
api_name:
- DevicePair.Renderer
- DevicePair.get_Renderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f74b212ed4e8ec29b0234a3769c3beff91c0c777
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381830"
---
# <a name="devicepairrenderer-property"></a>DevicePair :: Renderer, propriété

Obtient le convertisseur pour la paire d’appareils de base active.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Renderer(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Reçoit un objet [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) qui représente l’appareil du convertisseur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

 