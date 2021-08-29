---
description: CSourcePosition est une classe abstraite pour l’implémentation de l’interface IMediaPosition sur un filtre source.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: CSourcePosition, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5264bd28e40c8bf20d2c5c514b24d5150eec261a6a25422ff5b1bafc91a13e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687439"
---
# <a name="csourceposition-class"></a>CSourcePosition, classe

`CSourcePosition` est une classe abstraite pour l’implémentation de l’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) sur un filtre source.

Cette classe est obsolète. Si votre filtre source est recherché, il doit exposer l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) au lieu de **IMediaPosition**. Vous pouvez utiliser la classe de base [**CSourceSeeking**](csourceseeking.md) à cet effet.

 

 



