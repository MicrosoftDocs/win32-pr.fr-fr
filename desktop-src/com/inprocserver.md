---
title: InprocServer
description: Spécifie le chemin d’accès à la DLL du serveur in-process.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- Clé de Registre InprocServer COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363320"
---
# <a name="inprocserver"></a>InprocServer

Spécifie le chemin d’accès à la DLL du serveur in-process.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>Remarques

L’entrée **InprocServer** est relativement rare pour les classes Insertables.

Les serveurs in-process sont actuellement inscrits à l’aide de l’entrée de Registre **InprocServer** . Les serveurs in-process 32 bits et 64 bits doivent utiliser l’entrée [**InprocServer32**](inprocserver32.md) . Si un conteneur recherche un serveur in-process dans le registre, la version 16 bits a la priorité avec un conteneur de 16 bits et la version 32 bits a la priorité avec un conteneur de 32 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




