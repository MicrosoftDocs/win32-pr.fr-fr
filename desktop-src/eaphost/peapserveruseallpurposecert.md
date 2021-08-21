---
title: PeapServerUseAllPurposeCert
description: La clé de Registre PeapServerUseAllPurposeCert détermine si les certificats à usage général sont utilisés pour l’authentification PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5086a0067bab70a0e222def34d1adf236b37127c0d1ff6c91ac83b8b28c73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042817"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

La clé de Registre PeapServerUseAllPurposeCert détermine si les certificats à usage général sont utilisés pour l’authentification PEAP.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur        | Description                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.     |
| Autres valeurs | Les certificats à usage général dans le magasin de certificats du client ou du serveur ne sont pas sélectionnés pour l’authentification PEAP. |



 

Si cette valeur de Registre n’est pas présente, les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




