---
title: AuxUserType
description: Spécifie le nom complet et les noms d’application de l’application.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- Clé de Registre AuxUserType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363427"
---
# <a name="auxusertype"></a>AuxUserType

Spécifie le nom complet et les noms d’application de l’application.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>Remarques

La longueur maximale recommandée pour *ShortDisplayName* est de 15 caractères. Ce nom est utilisé dans les menus, y compris les menus contextuels.

*ApplicationName* doit contenir le nom réel de l’application (par exemple, « Acme Draw 2,0 »). Ce nom est utilisé dans le champ **résultats** de la boîte de dialogue **Collage spécial** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IOleObject :: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




