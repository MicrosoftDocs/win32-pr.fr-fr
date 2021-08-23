---
title: CallFailureLoggingLevel
description: Définit le niveau de détail des entrées du journal des événements sur les appels ayant échoué aux composants.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valeur de Registre CallFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819d132a8cd0f1741eb3b825a17f02387b200e80f2dba6913821e77f9a0913cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793819"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Définit le niveau de détail des entrées du journal des événements sur les appels ayant échoué aux composants.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur | Description                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Consignez toujours les échecs lors d’un appel dans le processus serveur COM.                           |
| 2     | Ne consigne jamais de défaillances au cours d’un appel dans le processus serveur COM. Il s'agit de la valeur par défaut. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




