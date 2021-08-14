---
description: Cette rubrique décrit des conseils de dépannage pour l’utilisation des API du Service Broker d’authentification Web pour vos pages Web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problèmes d’authentification web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c722aefa35849485d2c8958e17c654b5bb6477479ac1765e76e648fe15f9826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785865"
---
# <a name="web-authentication-problems"></a>Problèmes d’authentification web

Cette rubrique décrit des conseils de dépannage pour l’utilisation des API du Service Broker d’authentification Web pour vos pages Web.

-   [Journaux des opérations](#operational-logs)
-   [Utilisation de Fiddler avec le Service Broker d’authentification Web](#using-fiddler-with-web-authentication-broker)
-   [Rubriques connexes](#related-topics)

## <a name="operational-logs"></a>Journaux des opérations

Il est souvent possible de déterminer ce qui ne fonctionne pas à l’aide des journaux des opérations. il existe un canal de journal des événements dédié, Microsoft-Windows-webauth \\ opérationnel, qui permet aux développeurs de sites web de comprendre comment leurs pages web sont traitées par le répartiteur d’authentification web. pour l’activer, lancez eventvwr.exe et activez le journal des opérations sous l’Application et les Services \\ Microsoft \\ Windows \\ webauth. En outre, le répartiteur d’authentification Web ajoute une chaîne unique à la chaîne de l’agent utilisateur pour s’identifier sur le serveur Web. Cette chaîne est « MSAuthHost/1.0 ». Notez que le numéro de version est susceptible de changer dans le futur. Vous ne devez donc pas nécessairement utiliser ce numéro de version dans votre code. Voici un exemple de la chaîne complète de l’agent utilisateur :

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

Exemple d’utilisation des journaux des opérations

1.  Activer les journaux des opérations
2.  Exécuter une application sociale contoso![Observateur d’événements affichant les journaux opérationnels WebAuth](images/wab-figure15.png)
3.  Les entrées de journaux générées peuvent être utilisées pour comprendre le comportement du Service Broker d’authentification Web plus en détail. Dans ce cas, ces entrées peuvent être les suivantes :
    -   Début de la navigation : consigne le moment où AuthHost démarre, et contient des informations sur les URL de démarrage et de terminaison.
    -   ![Illustration des détails de la section Début de la navigation](images/wab-figure16.png)
    -   Achèvement de la navigation : consigne l’achèvement du chargement d’une page web.
    -   Balise META : consigne le moment où une balise META est rencontrée, y compris les détails.
    -   Arrêt de la navigation : navigation arrêtée par l’utilisateur.
    -   Erreur de navigation : AuthHost rencontre une erreur de navigation au niveau d’une URL incluant HttpStatusCode.
    -   Fin de la navigation : une URL de terminaison est rencontrée.

## <a name="using-fiddler-with-web-authentication-broker"></a>Utilisation de Fiddler avec le Service Broker d’authentification Web

le débogueur web Fiddler peut être utilisé avec les applications Windows 8.

1.  Étant donné qu’AuthHost s’exécute dans son propre conteneur d’application pour lui donner la fonctionnalité réseau privé, vous devez définir une clé de Registre : Windows Registry Editor Version 5.00

    **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001<dl> <dt>

                     Data type
</dt> <dd>                     DWORD</dd> </dl>

2.  Ajoutez une règle pour AuthHost, car c’est de là que provient le trafic sortant.
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  Ajoutez une règle de pare-feu pour le trafic entrant vers Fiddler.

pour plus d’informations, consultez [le Blog sur l’utilisation du débogueur web Fiddler avec les applications Windows store](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur le développement de pages web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Forum aux questions sur le Service Broker d’authentification Web](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Exemple d’application du SDK du Broker d’authentification Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041&preserve-view=true)
</dt> </dl>

 

 
