---
description: un fournisseur réseau est une DLL qui permet au système d’exploitation Windows d’interagir avec d’autres types de réseaux, tels que Novell. il s’agit d’un client du pilote Windows WNet.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API du fournisseur réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123369"
---
# <a name="network-provider-api"></a>API du fournisseur réseau

un fournisseur réseau est une DLL qui permet au système d’exploitation Windows d’interagir avec d’autres types de réseaux, tels que Novell. il s’agit d’un client du pilote Windows WNet. Un fournisseur de réseau implémente des actions spécifiques au réseau, telles que l’établissement d’une connexion, et expose une interface commune à Windows. Cette interface est appelée API du fournisseur réseau et est constituée de fonctions implémentées par le fournisseur réseau. Vous pouvez créer une DLL de fournisseur réseau pour prendre en charge de nouveaux protocoles réseau.

étant donné que chaque réseau expose une interface commune par le biais de son fournisseur, Windows peut interagir avec plusieurs types de réseaux sans connaître les détails de l’implémentation propre au réseau.

Le [*routeur de fournisseur multiple*](../secgloss/m-gly.md) (MPR) gère la communication avec tous les différents fournisseurs de réseau sur le système et présente un réseau intégré à l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs de réseau](network-providers.md)
</dt> <dt>

[Gestionnaire d’informations d’identification](credential-manager.md)
</dt> <dt>

[Routeur à plusieurs fournisseurs](multiple-provider-router.md)
</dt> <dt>

[Fonctions implémentées par les fournisseurs de réseau](functions-implemented-by-network-providers.md)
</dt> <dt>

[API de gestion des informations d’identification](credential-management-api.md)
</dt> <dt>

[API de notification de connexion](connection-notification-api.md)
</dt> </dl>

 

 
