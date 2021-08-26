---
title: MiscStatus
description: Spécifie comment créer et afficher un objet.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- Clé de Registre MiscStatus COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41aa5a5ab7f777eb6aa19d919c69ca219c9364cd1d6e5e9471cb677300d4ebb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992349"
---
# <a name="miscstatus"></a>MiscStatus

Spécifie comment créer et afficher un objet.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Remarques

Pour plus d’informations, consultez l’énumération [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) et [**IOleObject :: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Si aucune sous-clé correspondant à un DVASPECT n’est trouvée, la valeur par défaut de **MiscStatus** est utilisée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IOleObject :: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




