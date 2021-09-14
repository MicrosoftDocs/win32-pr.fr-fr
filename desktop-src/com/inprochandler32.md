---
title: InprocHandler32
description: InprocHandler32 spécifie si une application utilise un gestionnaire personnalisé dans la clé de Registre HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Clé de Registre InprocHandler32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998896"
---
# <a name="inprochandler32"></a>InprocHandler32

Spécifie si une application utilise un gestionnaire personnalisé.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le gestionnaire personnalisé utilisé par l’application. Si un gestionnaire personnalisé n’est pas utilisé, l’entrée doit être définie sur Ole32.dll.

Si un conteneur recherche un gestionnaire personnalisé dans le registre, la version 16 bits a la priorité sur un conteneur de 16 bits et la version 32 bits a la priorité sur un conteneur de 32 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 




