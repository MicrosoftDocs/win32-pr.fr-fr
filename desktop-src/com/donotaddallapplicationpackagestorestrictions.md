---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Détermine si RPCSS ajoute automatiquement un SID tous \_ les \_ packages d’application aux restrictions com par défaut.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379668"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

Détermine si RPCSS ajoute automatiquement un SID tous \_ les \_ packages d’application aux restrictions com par défaut.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur | Description                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Désactive les applications du Windows Store lors de la migration de Windows 7 vers Windows 8.                   |
| 1     | N’ajoute pas le SID tous les \_ \_ packages d’application aux restrictions com. Il s’agit de la valeur par défaut. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




