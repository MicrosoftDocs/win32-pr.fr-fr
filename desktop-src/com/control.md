---
title: Control
description: identifie un objet en tant que contrôle ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Clé de registre de contrôle COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363432"
---
# <a name="control"></a>Control

identifie un objet en tant que contrôle ActiveX.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Remarques

Cette entrée facultative est utilisée par les conteneurs pour renseigner les boîtes de dialogue. le conteneur utilise cette sous-clé pour déterminer s’il faut inclure un objet dans une boîte de dialogue qui affiche des contrôles de ActiveX. Un contrôle peut omettre cette entrée s’il est conçu pour fonctionner uniquement avec un conteneur spécifique et n’est donc pas destiné à être inséré dans d’autres conteneurs.

 

 




