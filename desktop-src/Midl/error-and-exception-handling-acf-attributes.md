---
title: Attributs ACF de gestion des erreurs et des exceptions
description: Utilisez les attributs suivants pour la gestion des erreurs.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- CCP MIDL, attributs, gestion des erreurs et des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510067"
---
# <a name="error-and-exception-handling-acf-attributes"></a>Attributs ACF de gestion des erreurs et des exceptions

Utilisez les attributs suivants pour la gestion des erreurs.



| Attribut                                                                | Utilisation                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| État de l’erreur d' [**\_ État de communication**](comm-status.md)[**\_**](fault-status.md) | Laissez votre application cliente gérer les exceptions normalement en provoquant le retour des erreurs de communication et de serveur au client en tant que valeurs de paramètre. L’application cliente peut ensuite appeler la fonction runtime RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) pour transmettre un message d’erreur à l’utilisateur. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Importation de fichiers et de bibliothèques de types](importing-files-and-type-libraries.md)
</dt> </dl>

 

 