---
title: PeapServerAcceptAllPurposeCert
description: La clé de Registre PeapServerAcceptAllPurposeCert détermine si les certificats à usage général sont acceptés pour l’authentification PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d568ef2cf3e7fd5eeeaa650e5e6e4fd32a8e1c8d6baa0ed91434a5c0aa60ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784681"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

La clé de Registre PeapServerAcceptAllPurposeCert détermine si les certificats à usage général sont acceptés pour l’authentification PEAP.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur        | Description                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS.       |
| Autres valeurs | Le serveur et le client n’acceptent pas les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS |



 

Si cette valeur de Registre n’est pas présente, le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification PEAP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




