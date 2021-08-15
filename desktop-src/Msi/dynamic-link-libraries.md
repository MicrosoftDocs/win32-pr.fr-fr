---
description: Une action personnalisée peut appeler une fonction définie dans une bibliothèque de liens dynamiques (DLL) écrite en C ou C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: bibliothèques de Dynamic-Link (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd2548851dcef4dcf08c53f168ec0f6b43ee036a1c250f9f65f072427a19e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378261"
---
# <a name="dynamic-link-libraries-windows-installer"></a>bibliothèques de Dynamic-Link (Windows Installer)

Une action personnalisée peut appeler une fonction définie dans une bibliothèque de liens dynamiques (DLL) écrite en C ou C++. La DLL peut exister en tant que fichier installé pendant l’installation actuelle ou en tant que flux binaire temporaire provenant de la [table binaire](binary-table.md) de la base de données d’installation.

Notez que toutes les fonctions appelées, y compris les actions personnalisées dans les dll, doivent spécifier la \_ \_ Convention d’appel StdCall. Par exemple, pour appeler CustomAction, utilisez ce qui suit.


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Pour plus d’informations, consultez [accès à la session de programme d’installation actuelle à partir d’une action personnalisée](accessing-the-current-installer-session-from-inside-a-custom-action.md)

Les types d’actions personnalisées suivants appellent une bibliothèque de liens dynamiques.



| Type d’action personnalisé                                 | Description                               |
|----------------------------------------------------|-------------------------------------------|
| [Type d’action personnalisé 1](custom-action-type-1.md)   | Fichier DLL stocké dans un flux de table binaire. |
| [Type d’action personnalisée 17](custom-action-type-17.md) | Fichier DLL installé avec un produit.        |



 

> [!Note]  
> Pour utiliser COM, vous devez appeler [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) dans l’action personnalisée. Ne quittez pas si vous constatez que le thread a déjà été initialisé. Par exemple, le thread est initialisé dans une installation par ordinateur, mais pas dans une installation par utilisateur.

 

Consultez la [liste récapitulative de tous les types d’actions personnalisées](summary-list-of-all-custom-action-types.md) pour obtenir un résumé de tous les types d’actions personnalisées et la façon dont elles sont encodées dans la [table CustomAction](customaction-table.md).

 

 
