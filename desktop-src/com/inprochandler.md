---
title: InprocHandler
description: InprocHandler spécifie si une application utilise un gestionnaire personnalisé dans la clé de Registre HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Clé de Registre InprocHandler COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404732"
---
# <a name="inprochandler"></a>InprocHandler

Spécifie si une application utilise un gestionnaire personnalisé.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le gestionnaire personnalisé utilisé par l’application. Si un gestionnaire personnalisé n’est pas utilisé, l’entrée doit être définie sur Ole32.dll.

Si un conteneur recherche un gestionnaire personnalisé dans le registre, la version 16 bits a la priorité sur un conteneur de 16 bits et la version 32 bits a la priorité sur un conteneur de 32 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




