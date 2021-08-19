---
description: Le routeur multifournisseur (MPR) appelle NPGetCaps pour déterminer à quel moment les fournisseurs de réseau démarrent (nIndex est défini sur WNNC \_ Start).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Remplacement de l’intervalle de délai d’attente MPR par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51c2c9db2fb892b7c2fc9646a9328fb9de4b7f9782ff5204ed261b16471ca4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921133"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Remplacement de l’intervalle de délai d’attente MPR par défaut

Le [*routeur multifournisseur*](../secgloss/m-gly.md) (MPR) appelle [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) pour déterminer à quel moment les fournisseurs de réseau démarrent (*nIndex* est défini sur WNNC \_ Start). Le MPR attend ensuite le délai d’expiration le plus long spécifié par tous les fournisseurs de réseau avant de présenter le réseau consolidé à l’utilisateur. Si l’un des fournisseurs de réseau ne sait pas au démarrage, MPR utilise un délai d’expiration par défaut de 60 secondes pour ce fournisseur.

Si nécessaire, l’administrateur peut remplacer le délai d’expiration par défaut en créant le délai d’attente de Registre **\_ DWORD reg** suivant, où *n* est l’intervalle de délai d’attente en millisecondes :

**HKEY \_ \_** Contrôle CurrentControlSet du système de l’ordinateur local \\  \\  \\  \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*

Le pseudo-code suivant montre le déroulement logique complet pour la gestion du délai d’attente par le MPR.


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
