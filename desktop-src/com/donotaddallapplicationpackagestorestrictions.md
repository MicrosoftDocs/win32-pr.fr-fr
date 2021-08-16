---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Détermine si RPCSS ajoute automatiquement un SID tous \_ les \_ packages d’application aux restrictions com par défaut.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1608d49d7e5bebc977ace8e59e4b31c5b13da8ab4f743e89095b9f31632453c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737005"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

Détermine si RPCSS ajoute automatiquement un SID tous \_ les \_ packages d’application aux restrictions com par défaut.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur | Description                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | désactive Windows les applications du windows Store lors de la migration de Windows 7 à Windows 8.                   |
| 1     | N’ajoute pas le SID tous les \_ \_ packages d’application aux restrictions com. Il s’agit de la valeur par défaut. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




