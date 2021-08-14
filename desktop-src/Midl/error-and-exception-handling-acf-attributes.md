---
title: Attributs ACF de gestion des erreurs et des exceptions
description: Utilisez les attributs suivants pour la gestion des erreurs.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- CCP MIDL, attributs, gestion des erreurs et des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f780145854a463da9a983c7dccbb24b01c2eca16437bf1254f93ec34def5395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384425"
---
# <a name="error-and-exception-handling-acf-attributes"></a>Attributs ACF de gestion des erreurs et des exceptions

Utilisez les attributs suivants pour la gestion des erreurs.



| Attribut                                                                | Usage                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| État de l’erreur d' [**\_ État de communication**](comm-status.md)[**\_**](fault-status.md) | Laissez votre application cliente gérer les exceptions normalement en provoquant le retour des erreurs de communication et de serveur au client en tant que valeurs de paramètre. L’application cliente peut ensuite appeler la fonction runtime RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) pour transmettre un message d’erreur à l’utilisateur. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Importation de fichiers et de bibliothèques de types](importing-files-and-type-libraries.md)
</dt> </dl>

 

 