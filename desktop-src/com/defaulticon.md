---
title: DefaultIcon
description: Fournit des informations sur l’icône par défaut pour les présentations sous forme d’objets.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- Clé de Registre DefaultIcon COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680994bdd4d4cd6ec6a3d192ca737af27f9190f6179571b3c8aaca5d86b55c5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501259"
---
# <a name="defaulticon"></a>DefaultIcon

Fournit des informations sur l’icône par défaut pour les présentations sous forme d’objets.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le chemin d’accès complet au nom de l’exécutable de l’application d’objet et l’index de ressource de l’icône dans l’exécutable.

**DefaultIcon** identifie l’icône à utiliser lorsque, par exemple, un contrôle est réduit à une icône. Cette entrée contient le chemin d’accès complet au nom de l’exécutable de l’application serveur et l’index de ressource de l’icône dans l’exécutable. Les applications peuvent utiliser les informations fournies par **DefaultIcon** pour obtenir un descripteur d’icône avec [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).

 

 