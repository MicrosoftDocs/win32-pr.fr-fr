---
description: la connexion à un espace de noms WMI sur un ordinateur distant peut nécessiter la modification des paramètres pour Windows pare-feu, le contrôle de compte d’utilisateur (UAC), DCOM ou le gestionnaire d’objets de Common Information Model (cimom).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Configuration d’une connexion WMI à distance
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b88aa453646e60bf17e31f1197d76506bb4f75453eb800dc0fa272946a3bf8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925701"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Configuration d’une connexion WMI à distance

la connexion à un espace de noms WMI sur un ordinateur distant peut nécessiter la modification des paramètres pour [Windows pare-feu](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [le contrôle de compte d’utilisateur (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM ou le gestionnaire d’objets de Common Information Model (cimom).

Les sections suivantes sont présentées dans cette rubrique :

-   [Windows Paramètres de pare-feu](#windows-firewall-settings)
-   [Paramètres du contrôle de compte d’utilisateur](#user-account-control-settings)
-   [Paramètres DCOM](#dcom-settings)
-   [Paramètres cimom](#cimom-settings)
-   [Rubriques connexes](#related-topics)

## <a name="windows-firewall-settings"></a>Paramètres de pare-feu Windows

les paramètres wmi pour Windows paramètres du pare-feu activent uniquement les connexions WMI, plutôt que d’autres applications DCOM.

Une exception doit être définie dans le pare-feu pour WMI sur l’ordinateur cible distant. L’exception pour WMI permet à WMI de recevoir des connexions à distance et des rappels asynchrones pour Unsecapp.exe. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

Si une application cliente crée son propre récepteur, ce récepteur doit être explicitement ajouté aux exceptions de pare-feu pour permettre aux rappels de fonctionner correctement.

L’exception pour WMI fonctionne également si WMI a été démarré avec un port fixe, à l’aide de la commande **winmgmt/standalonehost** . Pour plus d’informations, consultez [configuration d’un port fixe pour WMI](setting-up-a-fixed-port-for-wmi.md).

vous pouvez activer ou désactiver le trafic WMI par le biais de l’interface utilisateur du pare-feu Windows.

**Pour activer ou désactiver le trafic WMI à l’aide de l’interface utilisateur du pare-feu**

1.  dans le **panneau de configuration**, cliquez sur **sécurité** , puis sur **Windows pare-feu**.
2.  cliquez sur **modifier les Paramètres** , puis sur l’onglet **Exceptions** .
3.  dans la fenêtre Exceptions, activez la case à cocher **Windows Management Instrumentation (wmi)** pour activer le trafic wmi via le pare-feu. Pour désactiver le trafic WMI, désactivez la case à cocher.

Vous pouvez activer ou désactiver le trafic WMI via le pare-feu à partir de l’invite de commandes.

**Pour activer ou désactiver le trafic WMI à l’invite de commandes à l’aide du groupe de règles WMI**

-   Utilisez les commandes suivantes à l’invite de commandes. Tapez la commande suivante pour activer le trafic WMI via le pare-feu.

    **netsh advfirewall firewall set Rule Group = « Windows Management Instrumentation (WMI) » New Enable = Oui**

    Tapez la commande suivante pour désactiver le trafic WMI via le pare-feu.

    **netsh advfirewall firewall set Rule Group = « Windows Management Instrumentation (WMI) » New Enable = no**

Au lieu d’utiliser la commande de groupe de règles WMI unique, vous pouvez également utiliser des commandes individuelles pour chaque DCOM, service WMI et récepteur.

**Pour activer le trafic WMI à l’aide de règles distinctes pour DCOM, WMI, le récepteur de rappel et les connexions sortantes**

1.  Pour établir une exception de pare-feu pour le port DCOM 135, utilisez la commande suivante.

    **netsh advfirewall Firewall Add Rule dir = in Name = "DCOM" programme =% systemroot% \\ system32 \\svchost.exe service = RPCSS action = allow Protocol = TCP localPort = 135**

2.  Pour établir une exception de pare-feu pour le service WMI, utilisez la commande suivante.

    **netsh advfirewall Firewall Add Rule dir = in Name = "WMI" Program =% systemroot% \\ system32 \\svchost.exe service = WinMgmt action = autoriser Protocol = TCP localPort = any**

3.  Pour établir une exception de pare-feu pour le récepteur qui reçoit des rappels à partir d’un ordinateur distant, utilisez la commande suivante.

    **netsh advfirewall Firewall Add Rule dir = in Name = "UnsecApp" programme =% systemroot% \\ system32 \\ WBEM \\unsecapp.exe action = allow**

4.  Pour établir une exception de pare-feu pour les connexions sortantes à un ordinateur distant avec lequel l’ordinateur local communique de façon asynchrone, utilisez la commande suivante.

    **netsh advfirewall Firewall Add Rule dir = out Name = "WMI \_ out" programme =% systemroot% \\ system32 \\svchost.exe service = WinMgmt action = autoriser Protocol = TCP localPort = any**

Pour désactiver les exceptions de pare-feu séparément, utilisez les commandes suivantes.

**Pour désactiver le trafic WMI à l’aide de règles distinctes pour DCOM, WMI, le récepteur de rappel et les connexions sortantes**

1.  Pour désactiver l’exception DCOM.

    **nom de la règle de suppression du pare-feu netsh advfirewall = « DCOM »**

2.  Pour désactiver l’exception du service WMI.

    **nom de la règle de suppression du pare-feu netsh advfirewall = « WMI »**

3.  Pour désactiver l’exception du récepteur.

    **nom de la règle de suppression du pare-feu netsh advfirewall = "UnsecApp"**

4.  Pour désactiver l’exception sortante.

    **nom de la règle de suppression du pare-feu netsh advfirewall = « WMI \_ out »**

## <a name="user-account-control-settings"></a>Paramètres du contrôle de compte d’utilisateur

Le filtrage des jetons d’accès du contrôle de compte d’utilisateur peut avoir un impact sur les opérations autorisées dans les espaces de noms WMI ou sur les données retournées. Sous UAC, tous les comptes du groupe Administrateurs local s’exécutent avec un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly)utilisateur standard, également appelé filtrage des jetons d’accès UAC. Un compte d’administrateur peut exécuter un script avec privilèges élevés, « exécuter en tant qu’administrateur ».

Lorsque vous n’êtes pas connecté au compte administrateur intégré, le contrôle de compte d’utilisateur affecte les connexions à un ordinateur distant différemment selon que les deux ordinateurs se trouvent dans un domaine ou un groupe de travail. Pour plus d’informations sur UAC et les connexions à distance, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).

## <a name="dcom-settings"></a>Paramètres DCOM

Pour plus d’informations sur les paramètres DCOM, consultez [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md). Toutefois, le contrôle de compte d’utilisateur affecte les connexions pour les comptes d’utilisateurs de domaine. Si vous vous connectez à un ordinateur distant à l’aide d’un compte d’utilisateur qui n’est pas un compte de domaine inclus dans le groupe Administrateurs local de l’ordinateur distant, vous devez accorder explicitement les droits d’accès et d’activation DCOM à distance au compte.

## <a name="cimom-settings"></a>Paramètres cimom

Les paramètres CIMOM doivent être mis à jour si la connexion à distance se fait entre des ordinateurs qui n’ont pas de relation d’approbation ; dans le cas contraire, une connexion asynchrone échoue. Ce paramètre ne doit pas être modifié pour les ordinateurs situés dans le même domaine ou dans des domaines approuvés.

L’entrée de Registre suivante doit être modifiée pour permettre les rappels anonymes :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               \_valeur DWORD reg</dd> </dl>

Si la valeur **AllowAnonymousCallback** est définie sur 0, le service WMI empêche les rappels anonymes sur le client. Si la valeur est définie sur 1, le service WMI autorise les rappels anonymes au client.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
