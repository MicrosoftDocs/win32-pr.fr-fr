---
title: Désactivation de la sécurité de l’appel
description: La sécurité de l’appel détermine si un client a l’autorisation d’appeler les méthodes d’un serveur. Il existe deux façons de désactiver la sécurité des appels implique l’utilisation de Dcomcnfg.exe pour modifier le registre, et l’autre requiert des appels à CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379715"
---
# <a name="turning-off-call-security"></a>Désactivation de la sécurité de l’appel

La sécurité de l’appel détermine si un client a l’autorisation d’appeler les méthodes d’un serveur. Il existe deux façons de désactiver la sécurité des appels : l’un implique l’utilisation de Dcomcnfg.exe pour modifier le registre, et l’autre requiert des appels à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

-   [Désactivation de la sécurité des appels à l’aide de DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Désactivation de la sécurité des appels par programmation](#turning-off-call-security-programmatically)
-   [Rubriques connexes](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Désactivation de la sécurité des appels à l’aide de DCOMCNFG

La sécurité de l’appel peut être facilement désactivée à l’aide de Dcomcnfg.exe pour modifier le registre. Toutefois, l’utilisation de Dcomcnfg.exe pour désactiver la sécurité fonctionne uniquement si le client et le serveur n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). En effet, lorsque la méthode **CoInitializeSecurity** est appelée, DCOM ignore les paramètres du Registre et utilise à la place les valeurs fournies à **CoInitializeSecurity** .

Pour désactiver la sécurité avec Dcomcnfg.exe, le client et le serveur doivent tous deux définir leurs niveaux d’authentification sur aucun. Les étapes suivantes doivent être effectuées :

1.  Exécutez Dcomcnfg.exe.
2.  Dans la page **applications** , sélectionnez l’application qui représente le serveur. Cliquez sur le bouton des **Propriétés** (ou double-cliquez sur l’application sélectionnée).
3.  Cliquez sur l’onglet **General** (Général).
4.  Dans la zone de liste **niveau d’authentification par défaut** , sélectionnez **(aucun)**.
5.  Cliquez sur le bouton **appliquer** pour appliquer les modifications. Toutefois, les modifications ne sont pas appliquées aux instances en cours d’exécution de l’application.
6.  Si le client apparaît dans la liste de la page *applications* , répétez les étapes 2 à 5, en choisissant le client au lieu du serveur pour l’étape 2. Cliquez ensuite sur le bouton **OK**. Si le client ne figure pas dans la liste, vous pouvez effectuer l’une des trois opérations suivantes :
    -   Vous pouvez définir le niveau d’authentification du client sur aucun à l’échelle de l’ordinateur à l’aide de Dcomcnfg.exe. (Voir l’avertissement et la procédure ci-dessous.)
    -   Vous pouvez définir le niveau d’authentification du client sur aucun par programme.
    -   Vous pouvez créer une clé [AppID](appid-key.md) pour le client afin d’indiquer le niveau d’authentification None. (Voir [définition de la sécurité Process-Wide dans le registre](setting-processwide-security-through-the-registry.md).)

Pour définir le niveau d’authentification sur la valeur None à l’échelle de l’ordinateur :

> [!Note]  
> La définition du niveau d’authentification à l’échelle de l’ordinateur sur aucun est extrêmement non sécurisée.

 

1.  Exécutez Dcomcnfg.exe.
2.  Choisissez l’onglet **propriétés par défaut** .
3.  Dans la zone de liste **niveau d’authentification par défaut** , choisissez **(aucun)**.
4.  Cliquez sur le bouton **OK** .

## <a name="turning-off-call-security-programmatically"></a>Désactivation de la sécurité des appels par programmation

Pour désactiver la sécurité de l’appel par programmation, le client et le serveur doivent tous les deux appeler **CoInitializeSecurity**, en définissant le niveau d’authentification dans le paramètre *dwAuthnLevel* sur RPC \_ C \_ Authn \_ niveau \_ None.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Désactivation de la sécurité d’activation](turning-off-activation-security.md)
</dt> </dl>

 

 




