---
title: TlsServerUseAllPurposeCert
description: La clé de Registre TlsServerUseAllPurposeCert détermine si les certificats polyvalents sont utilisés pour l’authentification EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2f9d47b4e80409c27c71fe3655a1d3266571e0f8a8dd757e5334b0ef9fec40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085694"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

La clé de Registre TlsServerUseAllPurposeCert détermine si les certificats polyvalents sont utilisés pour l’authentification EAP-TLS.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur        | Description                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.     |
| Autres valeurs | Les certificats à usage général dans le magasin de certificats du client ou du serveur ne sont pas sélectionnés pour l’authentification PEAP. |



 

Si cette valeur de Registre n’est pas présente, les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification EAP-TLS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




