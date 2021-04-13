---
title: BypassNegotiation
description: La clé de Registre BypassNegotiation détermine si la négociation des fonctionnalités entre le serveur et le client se produit ou si des paramètres préconfigurés sont utilisés.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381289"
---
# <a name="bypassnegotiation"></a>BypassNegotiation

La clé de Registre BypassNegotiation détermine si la négociation des fonctionnalités entre le serveur et le client se produit ou si des paramètres préconfigurés sont utilisés.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur   | Description                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | Serveurs et clients négocient les fonctionnalités EAP.                                                                                                                                                        |
| différente | Le serveur et le client ne négocient pas les fonctionnalités EAP. Le serveur et le client utilisent la valeur de clé de Registre [AssumePhase2Fragmentation](assumephase2fragmentation.md) pour rechercher les fonctionnalités de l’autre partie. |



 

Si cette valeur de Registre n’est pas présente, le serveur et le client négocient les fonctionnalités EAP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du Registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




