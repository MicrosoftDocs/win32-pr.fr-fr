---
title: MiscStatus
description: Spécifie comment créer et afficher un objet.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- Clé de Registre MiscStatus COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029438"
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

## <a name="remarks"></a>Notes

Pour plus d’informations, consultez l’énumération [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) et [**IOleObject :: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Si aucune sous-clé correspondant à un DVASPECT n’est trouvée, la valeur par défaut de **MiscStatus** est utilisée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IOleObject :: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




