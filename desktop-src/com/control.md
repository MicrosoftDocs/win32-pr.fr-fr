---
title: Contrôler
description: Identifie un objet en tant que contrôle ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Clé de registre de contrôle COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380383"
---
# <a name="control"></a>Contrôler

Identifie un objet en tant que contrôle ActiveX.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Notes

Cette entrée facultative est utilisée par les conteneurs pour renseigner les boîtes de dialogue. Le conteneur utilise cette sous-clé pour déterminer s’il faut inclure un objet dans une boîte de dialogue qui affiche des contrôles ActiveX. Un contrôle peut omettre cette entrée s’il est conçu pour fonctionner uniquement avec un conteneur spécifique et n’est donc pas destiné à être inséré dans d’autres conteneurs.

 

 




