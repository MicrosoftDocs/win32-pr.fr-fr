---
title: Contrôler
description: identifie un objet en tant que contrôle ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Clé de registre de contrôle COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa6a0b131dd5fc2ba10d9aaeabafd06b19b73bb1e9422c28e5bec45ea43cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120509"
---
# <a name="control"></a>Contrôler

identifie un objet en tant que contrôle ActiveX.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Remarques

Cette entrée facultative est utilisée par les conteneurs pour renseigner les boîtes de dialogue. le conteneur utilise cette sous-clé pour déterminer s’il faut inclure un objet dans une boîte de dialogue qui affiche des contrôles de ActiveX. Un contrôle peut omettre cette entrée s’il est conçu pour fonctionner uniquement avec un conteneur spécifique et n’est donc pas destiné à être inséré dans d’autres conteneurs.

 

 




