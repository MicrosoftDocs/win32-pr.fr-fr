---
title: Exemple de valeurs de Registre
description: L’exemple suivant montre des données possibles pour certaines des valeurs de Registre du protocole d’authentification.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104030648"
---
# <a name="registry-values-example"></a>Exemple de valeurs de Registre

L’exemple suivant montre des données possibles pour certaines des valeurs de Registre du protocole d’authentification.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| Nom de la clé            | Datatype        | Valeur                                  |
|---------------------|-----------------|----------------------------------------|
| Chemin d’accès                | REG \_ développer \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| FriendlyName        | SZ de REG \_         | Exemple de protocole EAP                    |
| ConfigUIPath        | REG \_ développer \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| IdentityPath        | REG \_ développer \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| InteractiveUIPath   | REG \_ développer \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| RequireConfigUI     | \_valeur DWORD reg      | 1                                      |
| ConfigCLSID         | SZ de REG \_         | {0000031A-0000-0000-C000-000000000046} |
| StandaloneSupported | \_valeur DWORD reg      | 1                                      |



 

 

 




