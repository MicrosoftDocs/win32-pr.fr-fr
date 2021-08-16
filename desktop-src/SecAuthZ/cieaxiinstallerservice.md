---
description: Implémente les interfaces IAxiService et IeAxiServiceCallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Objet CIeAxiInstallerService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: d8e96600762db414fa93316098d5ba87dabfbc3138f516d3d69f1740d0d33d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783085"
---
# <a name="cieaxiinstallerservice-object"></a>Objet CIeAxiInstallerService

L’objet **CIeAxiInstallerService** implémente les interfaces [**IAxiService**](ieaxiservice.md) et [**IeAxiServiceCallback**](ieaxiservicecallback.md) .

Cet objet n’est pas déclaré dans un en-tête public. Les applications doivent les définir elles-mêmes. Le fragment IDL (Interface Definition Language) suivant décrit cet objet, y compris son CLSID.

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Business, Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAxiService**](ieaxiservice.md)
</dt> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

 




