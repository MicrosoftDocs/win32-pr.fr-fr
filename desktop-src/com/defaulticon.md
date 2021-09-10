---
title: DefaultIcon
description: Fournit des informations sur l’icône par défaut pour les présentations sous forme d’objets.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- Clé de Registre DefaultIcon COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363436"
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

 

 