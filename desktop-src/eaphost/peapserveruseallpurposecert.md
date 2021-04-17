---
title: PeapServerUseAllPurposeCert
description: La clé de Registre PeapServerUseAllPurposeCert détermine si les certificats à usage général sont utilisés pour l’authentification PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313834"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

La clé de Registre PeapServerUseAllPurposeCert détermine si les certificats à usage général sont utilisés pour l’authentification PEAP.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur        | Description                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.     |
| Autres valeurs | Les certificats à usage général dans le magasin de certificats du client ou du serveur ne sont pas sélectionnés pour l’authentification PEAP. |



 

Si cette valeur de Registre n’est pas présente, les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du Registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




