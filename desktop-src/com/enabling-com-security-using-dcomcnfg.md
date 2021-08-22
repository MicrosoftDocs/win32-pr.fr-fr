---
title: Activation de la sécurité COM à l’aide de DCOMCNFG
description: Dcomcnfg.exe fournit une interface utilisateur qui permet de modifier certains paramètres du Registre.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6161cf7418e7eab705203df51710e789ad2ef7d6843051dd35399fb8388f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678689"
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

 

 




