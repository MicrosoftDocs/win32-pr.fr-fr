---
title: VersionIndependentProgID
description: Associe un ProgID à un CLSID. Cette valeur est utilisée pour déterminer la version la plus récente d’une application d’objet.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- Clé de Registre VersionIndependentProgID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe1defaa52df5251d6c021655d6e84c90677e2a2d57f0bfb67f925e0ffa5bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549715"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgID

Associe un ProgID à un CLSID. Cette valeur est utilisée pour déterminer la version la plus récente d’une application d’objet.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie la version la plus récente de l’application de l’objet.

Le ProgID indépendant de la version est stocké et géré uniquement par le code d’application. Lorsqu’il reçoit le ProgID indépendant de la version, la fonction [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retourne le CLSID de la version actuelle.

Vous pouvez utiliser [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) et [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) pour effectuer une conversion entre ces deux représentations.

 

 




