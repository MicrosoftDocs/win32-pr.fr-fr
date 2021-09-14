---
description: Lors de l’accès aux données WMI locales ou distantes dans une application ou un script, vous pouvez rencontrer des erreurs allant des classes manquantes à l’accès refusé. Des options de débogage et des classes de dépannage sont également disponibles pour les fournisseurs.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: Dépannage WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58919617c663b52ffb840b3c3382b5707f0a305e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122478"
---
# <a name="wmi-troubleshooting"></a>Dépannage WMI

Lors de l’accès aux données WMI locales ou distantes dans une application ou un script, vous pouvez rencontrer des erreurs allant des classes manquantes à l’accès refusé. Des options de débogage et des classes de dépannage sont également disponibles pour les fournisseurs.

> [!Note]  
> La documentation suivante est destinée aux développeurs et aux administrateurs informatiques. Si vous êtes un utilisateur final qui a rencontré un message d’erreur concernant WMI, vous devez accéder à [support Microsoft](https://support.microsoft.com/) et rechercher le code d’erreur que vous voyez dans le message d’erreur. Pour plus d’informations sur la résolution des problèmes liés aux scripts WMI et au service WMI, consultez [WMI ne fonctionne pas.](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>WMI Diagnosis Utility

l’utilitaire de diagnostic WMI (WMIDiag.exe) n’est plus pris en charge à partir de Windows 8 et Windows Server 2012.

* * Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 : * *

Si WMI renvoie des messages d’erreur, sachez qu’ils ne peuvent pas indiquer des problèmes dans le service WMI ou les fournisseurs WMI. Les échecs peuvent provenir d’autres parties du système d’exploitation et émerger comme des erreurs via WMI. Dans tous les cas, ne supprimez pas le référentiel WMI en tant que première action, car la suppression du dépôt peut endommager le système ou les applications installées.

pour obtenir plus d’informations sur la source du problème, vous pouvez télécharger et exécuter l’outil en ligne de commande [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic. Cet outil génère un rapport qui peut généralement isoler la source du problème et fournir des instructions sur la façon de le résoudre. Le rapport aide également les services de support technique Microsoft à vous aider. vous pouvez télécharger le WMI Diagnosis Utility dans le [centre de téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

Les rédacteurs de fournisseur peuvent également rencontrer des problèmes de débogage, sauf si vous écrivez un [*fournisseur découplé*](gloss-d.md). Pour plus d’informations, consultez [débogage de fournisseurs](debugging-providers.md).

## <a name="logging-and-tracing"></a>Journalisation et suivi

Les fichiers journaux WMI n’existent plus ; ils ont été remplacés par [Suivi d’v nements pour Windows (ETW)](/windows/desktop/ETW/event-tracing-portal). Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md), [journalisation de l’activité WMI](logging-wmi-activity.md)et [fichiers journaux WMI](wmi-log-files.md).

## <a name="troubleshooting-in-scripts-and-applications"></a>Résolution des problèmes dans les scripts et les applications

WMI contient un ensemble de classes permettant de [résoudre les problèmes liés](wmi-troubleshooting-classes.md) aux applications clientes qui utilisent des fournisseurs WMI. Pour plus d’informations, consultez [résolution des problèmes liés aux applications clientes WMI](troubleshooting-wmi-client-applications.md).

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Comment les rédacteurs de fournisseur peuvent empêcher les problèmes WMI

Les rédacteurs de fournisseur peuvent empêcher de nombreux problèmes, qui apparaissent dans les messages d’erreur via WMI, en effectuant les actions suivantes :

-   Inscription correcte de votre fournisseur. Pour plus d’informations, consultez [inscription d’un fournisseur](registering-a-provider.md).
-   Ajout de l’instruction [**\# pragma Autocover**](pragma-autorecover.md) au fichier format MOF (MOF) qui définit vos classes de fournisseur.

Pour plus d’informations, consultez [débogage de fournisseurs](debugging-providers.md), [fourniture de données à WMI](providing-data-to-wmi.md)et [classes de résolution des problèmes](provider-configuration-and-troubleshooting-classes.md)et de configuration du fournisseur.

## <a name="access-denied"></a>accès refusé

Les erreurs de refus d’accès signalées par des scripts et des applications qui accèdent à des espaces de noms et des données WMI appartiennent généralement à trois catégories. Le tableau suivant répertorie les trois catégories d’erreurs, ainsi que les problèmes susceptibles de provoquer des erreurs et des solutions possibles.



| Erreur                                                                                                                        | Problèmes possibles                                                                                                                                                                                                                                                                                                                                                                     | Solution                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Problème de pare-feu ou serveur non disponible.<br/>      | l’ordinateur n’existe pas ou le pare-feu Windows bloque la connexion<br/>                                                                                                                                                                                                                                                                                        | connexion à Vista : **netsh advfirewall firewall set rule group = « windows management instrumentation (wmi) » new enable = oui** connexion au niveau inférieur : autorisez la règle « Administration distante » dans Windows pare-feu.<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **E \_ accès \_ refusé**<br/> Accès refusé par la sécurité DCOM.<br/>                                       | L’utilisateur ne dispose pas d’un accès à distance à l’ordinateur via DCOM. En général, des erreurs DCOM se produisent lors de la connexion à un ordinateur distant avec une version du système d’exploitation différente.<br/>                                                                                                                                                                                          | Accordez à l’utilisateur des autorisations de lancement à distance et d’activation à distance dans DCOMCNFG. Cliquez avec le bouton droit sur Poste de travail Propriétés de >. Sous sécurité COM, cliquez sur « modifier les limites » pour les deux sections. Accordez à l’utilisateur l’accès à distance, le lancement à distance et l’activation à distance. accédez ensuite à la configuration DCOM, recherchez « Windows Management Instrumentation » et accordez à l’utilisateur le lancement à distance et l’Activation à distance. Pour plus d’informations, consultez [connexion entre différents systèmes d’exploitation](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection) .<br/> |
| **accès 0X80041003 \_ WBEM \_ E \_ refusé**<br/> Accès refusé par un [ *fournisseur*](gloss-p.md)<br/> | L’utilisateur n’a pas l’autorisation d’effectuer l’opération dans WMI. Cela peut se produire lorsque vous interrogez certaines classes en tant qu’utilisateur doté de droits limités, mais cela se produit le plus souvent lorsque vous tentez d’appeler des méthodes ou de modifier des instances WMI en tant qu’utilisateur doté de droits limités. L’espace de noms auquel vous vous connectez est chiffré et l’utilisateur tente de se connecter avec une connexion non chiffrée.<br/> | accordez l’accès à l’utilisateur avec le contrôle WMI (assurez-vous que l’accès à distance est \_ défini sur true) Connecter à l’aide d’un client qui prend en charge le chiffrement.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   En général, des erreurs DCOM se produisent lors de la connexion à un ordinateur distant avec une version du système d’exploitation différente.

-   Les fournisseurs peuvent également refuser l’accès aux données dans des espaces de noms spécifiques ou exiger certains niveaux de sécurité de la connexion. Pour plus d’informations, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md) et de l' [hébergement et de la sécurité du fournisseur](provider-hosting-and-security.md).

-   Les erreurs de refus d’accès à partir du pare-feu de connexion Internet (ICF).

    pour plus d’informations, consultez [connexion via un pare-feu Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

-   Une erreur de refus d’accès est retournée par la sécurité DCOM lorsqu’un client de faible intégrité tente d’accéder à WMI. par exemple, un contrôle de ActiveX qui s’exécute dans Internet Explorer, dont le niveau de sécurité est défini sur faible, ne dispose pas d’un accès pour effectuer des opérations WMI locales.

    **Windows 7 :** Les utilisateurs de faible intégrité disposent d’autorisations en lecture seule pour les opérations WMI locales.

## <a name="information-on-errors"></a>Informations sur les erreurs

Lorsque vous recevez un message d’erreur de WMI, vous pouvez localiser le message dans les [**constantes d’erreur WMI**](wmi-error-constants.md) ou, pour les scripts, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum). Toutefois, les informations fournies par l’erreur seule sont généralement insuffisantes pour déterminer ce qui se passe. L’altération de l’espace de stockage WMI peut se faire passer pour des classes ou des instances « introuvable ».

Pour plus d’informations sur les erreurs WMI :

-   Les journaux WMI effectuent le suivi des événements à partir du noyau WMI et des fournisseurs. Pour plus d’informations, consultez [journalisation de l’activité WMI](logging-wmi-activity.md).
-   Utilisez les [classes de résolution des problèmes WMI](wmi-troubleshooting-classes.md) pour vérifier l’état interne de WMI ou pour recevoir des notifications d’événements du fournisseur ou du service WMI. Pour plus d’informations, consultez [classes de dépannage et de configuration de fournisseur](provider-configuration-and-troubleshooting-classes.md) et [résolution des problèmes liés aux applications clientes WMI](troubleshooting-wmi-client-applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

[Suivi de l’activité WMI](tracing-wmi-activity.md)
</dt> <dt>

[Journalisation de l’activité WMI](logging-wmi-activity.md)
</dt> </dl>

 

