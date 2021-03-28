---
UID: NF:ntw.EtwEventUnregister
title: EtwEventUnregister fonction)
description: Annule l’inscription d’un événement.
old-location: ''
ms.assetid: na
ms.date: 02/20/2018
ms.keywords: EtwEventUnregister
ms.topic: reference
req.header: ntetw.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10, version 1803 [desktop apps \| UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntetw.h
api_name:
- EtwEventUnregister
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: e61de5aa1c050aedd2c82dec471765baa7e6cdd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101577"
---
# <a name="etweventunregister-function"></a>EtwEventUnregister fonction)


## <a name="description"></a>Description


Le <b>EtwEventUnregister</b> annule l’inscription d’un événement.
            

Les fournisseurs peuvent uniquement appeler cette fonction à partir de leur fonction <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> .


## <a name="parameters"></a>Paramètres




### <a name="reghandle-in"></a>RegHandle [in]

Handle vers un événement.


## <a name="returns"></a>Retours



Retourne un HRESULT.





## <a name="remarks"></a>Notes



## <a name="see-also"></a>Voir aussi