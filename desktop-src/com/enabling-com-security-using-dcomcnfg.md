---
title: Activation de la sécurité COM à l’aide de DCOMCNFG
description: Dcomcnfg.exe fournit une interface utilisateur qui permet de modifier certains paramètres du Registre.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363607"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>Activation de la sécurité COM à l’aide de DCOMCNFG

Dcomcnfg.exe fournit une interface utilisateur qui permet de modifier certains paramètres du Registre. En utilisant Dcomcnfg.exe, vous pouvez activer la sécurité à l’échelle de l’ordinateur ou au niveau du processus. Vous pouvez activer la sécurité pour un ordinateur particulier afin que, lorsqu’un processus ne fournit pas ses propres paramètres de sécurité, par programmation ou par le biais de valeurs de Registre, les valeurs définies par Dcomcnfg.exe seront utilisées. Vous pouvez utiliser Dcomcnfg.exe pour activer la sécurité pour une application particulière uniquement.

Lors de l’activation de la sécurité, il existe deux tâches principales à accomplir :

-   Définissez un niveau d’authentification qui n’a pas la valeur None.
-   Définissez les autorisations, y compris les autorisations de lancement et d’accès.

Les étapes à suivre pour accomplir ces tâches varient selon que vous activez la sécurité pour l’ensemble de l’ordinateur ou uniquement pour une application particulière. Vous pouvez également définir d’autres valeurs pour l’ordinateur ou l’application.

> [!Note]  
> Vous devez être administrateur pour exécuter Dcomcnfg.exe.

 

Les rubriques suivantes fournissent des procédures pas à pas pour définir la sécurité avec Dcomcnfg.exe :

-   [Définition de la sécurité System-Wide à l’aide de DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)
-   [Définition de la sécurité échelle à l’aide de DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> <dt>

[Désactivation de la sécurité](turning-off-security.md)
</dt> </dl>

 

 




