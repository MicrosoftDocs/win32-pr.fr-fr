---
title: TlsServerUseAllPurposeCert
description: La clé de Registre TlsServerUseAllPurposeCert détermine si les certificats polyvalents sont utilisés pour l’authentification EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313813"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

La clé de Registre TlsServerUseAllPurposeCert détermine si les certificats polyvalents sont utilisés pour l’authentification EAP-TLS.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur        | Description                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.     |
| Autres valeurs | Les certificats à usage général dans le magasin de certificats du client ou du serveur ne sont pas sélectionnés pour l’authentification PEAP. |



 

Si cette valeur de Registre n’est pas présente, les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification EAP-TLS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du Registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




