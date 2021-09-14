---
description: Informations de référence sur les commandes COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Informations de référence sur les commandes COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111186"
---
# <a name="copp-command-reference"></a>Informations de référence sur les commandes COPP

Cette section décrit les commandes COPP (Certified Output Protection Protocol). Les commandes suivantes sont définies.



| Commande              | GUID                             |
|----------------------|----------------------------------|
| Définir le niveau de protection | **\_COPPSETPROTECTIONLEVEL DXVA** |
| Définir la signalisation        | **\_COPPSETSIGNALING DXVA**       |



 

Définir le niveau de protection, commande

Définit le niveau de protection pour un mécanisme de protection de sortie spécifié. Selon le connecteur, il peut être possible d’appliquer plusieurs mécanismes de protection sur le même connecteur, avec des paramètres différents pour chaque mécanisme.

**GUID**: DXVA \_ COPPSetProtectionLevel

**Données d’entrée**: une structure [**\_ COPPSetProtectionLevelCmdData DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .

Définir la commande de signalisation

Spécifie des informations sur le signal vidéo autre que le niveau de protection.

Pour CGMS-A, certaines normes de protection requièrent que le signal televsion contient des informations sur les proportions et d’autres informations dans les mêmes paquets de forme d’onde VBI que les bits CGMS-A. Les télévisions peuvent s’afficher mal si les informations sur les proportions ne sont pas cohérentes avec le flux vidéo. L’application peut utiliser cette commande pour spécifier les proportions afin que le pilote Graphics puisse générer les paquets VBI appropriés.

Cette commande est également conçue pour être extensible si des informations de signal supplémentaires sont requises dans les normes futures.

**GUID**: DXVA \_ COPPSetSignaling

**Données d’entrée**: une structure [**\_ COPPSetSignalingCmdData DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



