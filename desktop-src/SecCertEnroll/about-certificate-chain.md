---
description: Une chaîne de certificats est une collection hiérarchique de certificats qui amène l’utilisateur final ou l’ordinateur à se retrouver à la racine de confiance, en général l’autorité de certification racine d’une organisation.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Chaîne de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522829"
---
# <a name="certificate-chain"></a>Chaîne de certificats

Une chaîne de certificats est une collection hiérarchique de certificats qui amène l’utilisateur final ou l’ordinateur à se retrouver à la racine de confiance, en général l’autorité de certification racine d’une organisation. Étant donné que toutes les parties approuvent vraisemblablement le certificat racine, un tiers peut gagner en confiance dans un certificat d’entité finale en vérifiant la chaîne de certificats. En général, la vérification requiert l’établissement de chaque certificat dans la chaîne :

-   Est signé par la clé publique dans le certificat précédent.
-   N’a pas expiré.
-   N’a pas été révoqué.
-   Conforme aux stratégies spécifiées par les certificats précédents.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hiérarchie des certificats](about-certificate-hierarchy.md)
</dt> <dt>

[Certification croisée](about-cross-certification.md)
</dt> <dt>

[Modèles d’approbation](about-trust-models.md)
</dt> </dl>

 

 



