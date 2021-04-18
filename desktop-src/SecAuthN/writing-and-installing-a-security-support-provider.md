---
description: La conception de SSPI permet d’écrire et d’ajouter des SSP supplémentaires au système.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Écriture et installation d’un fournisseur de support de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526123"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Écriture et installation d’un fournisseur de support de sécurité

La conception de SSPI permet d’écrire et d’ajouter des SSP supplémentaires au système. Un [*SSP*](../secgloss/s-gly.md) spécifique à un modèle de sécurité peut être développé avec une simplicité ou une complexité relativement importante, selon le niveau d’intégration avec le système d’exploitation. Un fournisseur SSP client qui autorise les connexions à un nouveau type de serveur peut être développé très rapidement, alors qu’un SSP complet qui fournit l’emprunt d’identité local nécessiterait plus d’efforts.

Les SSP sont installés en mettant à jour une valeur **reg \_ SZ** dans le registre, comme suit :

**HKEY \_ \_** \\Provider1.dll du contrôle CurrentControlSet du **système** de l’ordinateur local \\  \\  \\ **SecurityProviders**  =  *, Provider2.dll*    <dl> <dt>

            Data type
</dt> <dd>            SZ de REG \_</dd> </dl>

Une seule DLL peut contenir plusieurs SSP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Restrictions concernant l’inscription et l’installation d’un package de sécurité](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
