---
title: TlsServerAcceptAllPurposeCert
description: La clé de Registre TlsServerAcceptAllPurposeCert détermine si les certificats polyvalents sont acceptés pour l’authentification EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416047"
---
# <a name="tlsserveracceptallpurposecert"></a>TlsServerAcceptAllPurposeCert

La clé de Registre TlsServerAcceptAllPurposeCert détermine si les certificats polyvalents sont acceptés pour l’authentification EAP-TLS.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur        | Description                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS.       |
| Autres valeurs | Le serveur et le client n’acceptent pas les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS |



 

Si cette valeur de Registre n’est pas présente, le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




