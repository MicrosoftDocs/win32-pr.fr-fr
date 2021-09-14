---
title: VersionIndependentProgID
description: Associe un ProgID à un CLSID. Cette valeur est utilisée pour déterminer la version la plus récente d’une application d’objet.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- Clé de Registre VersionIndependentProgID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923068"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgID

Associe un ProgID à un CLSID. Cette valeur est utilisée pour déterminer la version la plus récente d’une application d’objet.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie la version la plus récente de l’application de l’objet.

Le ProgID indépendant de la version est stocké et géré uniquement par le code d’application. Lorsqu’il reçoit le ProgID indépendant de la version, la fonction [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retourne le CLSID de la version actuelle.

Vous pouvez utiliser [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) et [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) pour effectuer une conversion entre ces deux représentations.

 

 




