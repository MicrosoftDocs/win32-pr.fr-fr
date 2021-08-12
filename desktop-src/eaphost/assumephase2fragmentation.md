---
title: AssumePhase2Fragmentation
description: La clé de Registre AssumePhase2Fragmentation détermine si le serveur et le client supposent la fragmentation de la phase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caee785b0c89b92aaf4b01c590425c451b9a977664e915874e7eb5ad1edf46aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275836"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

La clé de Registre AssumePhase2Fragmentation détermine si le serveur et le client supposent la fragmentation de la phase 2.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur   | Description                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | Le serveur et le client supposent que l’autre partie n’est pas en charge de la fragmentation de phase 2 pendant l’authentification PEAP. |
| différente | Le serveur et le client supposent que l’autre partie est en charge de la fragmentation de phase 2 pendant l’authentification PEAP.     |



 

Si cette valeur de Registre n’est pas présente, le serveur et le client supposent que l’autre partie est en charge de la fragmentation de phase 2 pendant l’authentification PEAP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




