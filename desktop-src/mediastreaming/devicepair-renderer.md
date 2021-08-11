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
ms.openlocfilehash: 05707fd65e2ac8998fa2412ec15c12d3b003b88990641aad6510d87bd7692e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236082"
---
# <a name="devicepairrenderer-property"></a>DevicePair :: Renderer, propriété

Obtient le convertisseur pour la paire d’appareils de base active.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Renderer(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Reçoit un objet [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) qui représente l’appareil du convertisseur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

 