---
title: PeapServerAcceptAllPurposeCert
description: La clé de Registre PeapServerAcceptAllPurposeCert détermine si les certificats à usage général sont acceptés pour l’authentification PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106543044"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

La clé de Registre PeapServerAcceptAllPurposeCert détermine si les certificats à usage général sont acceptés pour l’authentification PEAP.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur        | Description                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS.       |
| Autres valeurs | Le serveur et le client n’acceptent pas les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS |



 

Si cette valeur de Registre n’est pas présente, le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification PEAP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du Registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




