---
title: Configuration d’un abonnement initié par la source
description: Les abonnements initiés par la source vous permettent de définir un abonnement sur un ordinateur du collecteur d’événements sans définir les ordinateurs source des événements, puis plusieurs ordinateurs sources d’événements distants peuvent être configurés (à l’aide d’un paramètre de stratégie de groupe) pour transférer les événements à l’ordinateur du collecteur d’événements.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/04/2020
ms.locfileid: "104381755"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Configuration d’un abonnement initié par la source

Les abonnements initiés par la source vous permettent de définir un abonnement sur un ordinateur du collecteur d’événements sans définir les ordinateurs source des événements, puis plusieurs ordinateurs sources d’événements distants peuvent être configurés (à l’aide d’un paramètre de stratégie de groupe) pour transférer les événements à l’ordinateur du collecteur d’événements. Cela diffère d’un abonnement initié par le collecteur, car dans le modèle d’abonnement initié par le collecteur, le collecteur d’événements doit définir toutes les sources d’événements dans l’abonnement aux événements.

Lors de la configuration d’un abonnement initié par la source, déterminez si les ordinateurs source d’événements se trouvent dans le même domaine que l’ordinateur du collecteur d’événements. Les sections suivantes décrivent les étapes à suivre lorsque les sources d’événements se trouvent dans le même domaine ou non dans le même domaine que l’ordinateur du collecteur d’événements.

> [!Note]  
> Tout ordinateur d’un domaine, local ou distant, peut être un collecteur d’événements. Toutefois, lors du choix d’un collecteur d’événements, il est important de sélectionner un ordinateur proche de la topologie topologique où la majorité des événements seront générés. L’envoi d’événements à un ordinateur situé à un emplacement réseau distant sur un réseau étendu peut réduire les performances globales et l’efficacité de la collecte d’événements.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Configuration d’un abonnement initié par le code source dans lequel les sources d’événements se trouvent dans le même domaine que l’ordinateur du collecteur d’événements

Les ordinateurs source d’événements et l’ordinateur du collecteur d’événements doivent être configurés pour configurer un abonnement initié par la source.

> [!Note]  
> Ces instructions partent du principe que vous disposez d’un accès administrateur au contrôleur de domaine Windows Server desservant le domaine dans lequel l’ordinateur ou les ordinateurs distants sont configurés pour collecter des événements.

### <a name="configuring-the-event-source-computer"></a>Configuration de l’ordinateur source de l’événement

1. Exécutez la commande suivante à partir d’une invite de commandes avec élévation de privilèges sur le contrôleur de domaine Windows Server pour configurer Windows Remote Management :

    **WinRM QC-q**

2. Démarrez la stratégie de groupe en exécutant la commande suivante :

    **% SYSTEMROOT% \\ system32 \\ gpedit. msc**

3. Sous le nœud **configuration** de l’ordinateur, développez le nœud **modèles d’administration** , développez le nœud **composants Windows** , puis sélectionnez le nœud **transfert d’événements** .

4. Cliquez avec le bouton droit sur le paramètre **SubscriptionManager** , puis sélectionnez **Propriétés**. Activez le paramètre **SubscriptionManager** , puis cliquez sur le bouton **Afficher** pour ajouter une adresse de serveur au paramètre. Ajoutez au moins un paramètre qui spécifie l’ordinateur du collecteur d’événements. La fenêtre **Propriétés de SubscriptionManager** contient un onglet **expliquer** qui décrit la syntaxe du paramètre.

5. Une fois le paramètre **SubscriptionManager** ajouté, exécutez la commande suivante pour vous assurer que la stratégie est appliquée :

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Configuration de l’ordinateur du collecteur d’événements

1. Exécutez la commande suivante à partir d’une invite de commandes avec élévation de privilèges sur le contrôleur de domaine Windows Server pour configurer Windows Remote Management :

    **WinRM QC-q**

2. Exécutez la commande suivante pour configurer le service collecteur d’événements :

    **wecutil QC/q**

3. Créez un abonnement initié par la source. Vous pouvez effectuer cette opération par programme, à l’aide de l’observateur d’événements ou à l’aide de [**Wecutil.exe**](wecutil.md). Pour plus d’informations sur la création de l’abonnement par programme, consultez l’exemple de code relatif à la [création d’un abonnement initié](creating-a-source-initiated-subscription.md)par la source. Si vous utilisez Wecutil.exe, vous devez créer un fichier XML d’abonnement aux événements et utiliser la commande suivante :

     *configurationFile.xml* de la ressource.

    Le code XML suivant est un exemple du contenu d’un fichier de configuration d’abonnement qui crée un abonnement initié par la source pour transférer des événements du journal des événements d’application d’un ordinateur distant vers le journal ForwardedEvents sur l’ordinateur du collecteur d’événements.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > Lors de la création d’un abonnement initié par la source, si AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList et DeniedSubjectList sont tous vides, "O :NSG : NSD : (A ;; GA ;;;D C) (A ;; GA ;;; NS)» sera utilisé comme descripteur de sécurité par défaut pour AllowedSourceDomainComputers. Le descripteur par défaut accorde aux membres du groupe de domaine ordinateurs du domaine, ainsi qu’au groupe de service réseau local (pour le redirecteur local), la possibilité de déclencher des événements pour cet abonnement.

### <a name="to-validate-that-the-subscription-works-correctly"></a>Pour valider le bon fonctionnement de l’abonnement

1. Sur l’ordinateur du collecteur d’événements, procédez comme suit :

    1. Exécutez la commande suivante à partir d’une invite de commandes avec élévation de privilèges sur le contrôleur de domaine Windows Server pour récupérer l’état d’exécution de l’abonnement :

        **wecutil gr** *&lt; subscriptionID &gt;*

    2. Vérifiez que la source de l’événement est connectée. Vous devrez peut-être attendre que l’intervalle d’actualisation spécifié dans la stratégie soit dépassé après avoir créé l’abonnement pour la source d’événements à connecter.
    3. Exécutez la commande suivante pour récupérer les informations d’abonnement :

        **wecutil GS** *&lt; subscriptionID &gt;*

    4. Obtient la valeur DeliveryMaxItems à partir des informations d’abonnement.

2. Sur l’ordinateur source de l’événement, déclenchez les événements qui correspondent à la requête de l’abonnement aux événements. Le nombre d’événements DeliveryMaxItems doit être déclenché pour que les événements soient transférés.
3. Sur l’ordinateur du collecteur d’événements, vérifiez que les événements ont été transférés dans le journal ForwardedEvents ou dans le journal spécifié dans l’abonnement.

## <a name="forwarding-the-security-log"></a>Transfert du journal de sécurité

Pour pouvoir transférer le journal de sécurité, vous devez ajouter le compte SERVICE réseau au groupe lecteurs EventLog.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Configuration d’un abonnement initié par la source lorsque les sources d’événements ne se trouvent pas dans le même domaine que l’ordinateur du collecteur d’événements

> [!Note]  
> Ces instructions partent du principe que vous disposez d’un accès administrateur à un contrôleur de domaine Windows Server. Dans ce cas, étant donné que l’ordinateur ou les ordinateurs collecteurs d’événements distants ne sont pas dans le domaine pris en charge par le contrôleur de domaine, il est essentiel de démarrer un client individuel en définissant Windows Remote Management sur « automatique » à l’aide de services (services. msc). Vous pouvez également exécuter « WinRM quickconfig » sur chaque client distant.

Les conditions préalables suivantes doivent être remplies pour que l’abonnement soit créé.

1. Sur l’ordinateur du collecteur d’événements, exécutez les commandes suivantes à partir d’une invite de commandes avec élévation de privilèges pour configurer Windows Remote Management et le service collecteur d’événements :

    **WinRM QC-q**

    **wecutil QC/q**

2. L’ordinateur collecteur doit avoir un certificat d’authentification serveur (certificat avec un rôle d’authentification serveur) dans un magasin de certificats de l’ordinateur local.
3. Sur l’ordinateur source de l’événement, exécutez la commande suivante pour configurer Windows Remote Management :

    **WinRM QC-q**

4. L’ordinateur source doit avoir un certificat d’authentification client (certificat avec un rôle d’authentification du client) dans un magasin de certificats de l’ordinateur local.
5. Le port 5986 est ouvert sur l’ordinateur du collecteur d’événements. Pour ouvrir ce port, exécutez la commande suivante :

    **netsh firewall Add ouverture TCP 5986 "gestion à distance de WinRM HTTPs"**

### <a name="certificates-requirements"></a>Certificats requis

- Un certificat d’authentification serveur doit être installé sur l’ordinateur du collecteur d’événements dans le magasin personnel de l’ordinateur local. L’objet de ce certificat doit correspondre au nom de domaine complet du collecteur.
- Un certificat d’authentification client doit être installé sur les ordinateurs source d’événements dans le magasin personnel de l’ordinateur local. L’objet de ce certificat doit correspondre au nom de domaine complet de l’ordinateur.
- Si le certificat client a été émis par une autorité de certification différente de celle du collecteur d’événements, ces certificats racine et intermédiaires doivent également être installés sur le collecteur d’événements.
- Si le certificat client a été émis par une autorité de certification intermédiaire et que le collecteur exécute Windows 2012 ou une version ultérieure, vous devrez configurer la clé de Registre suivante :

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Vérifiez que le serveur et le client sont correctement en mesure de vérifier l’état de révocation sur tous les certificats. L’utilisation de la commande **certutil** peut aider à résoudre les erreurs éventuelles.

Pour plus d’informations, consultez cet article : https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Configurer l’écouteur sur le collecteur d’événements

1. Définissez l’authentification par certificat à l’aide de la commande suivante :

    **winrm set winrm/config/service/auth @ {Certificate = "true"}**

2. Un écouteur HTTPs WinRM avec le certificat d’authentification serveur Print Thumb doit exister sur l’ordinateur du collecteur d’événements. Vous pouvez le vérifier à l’aide de la commande suivante :

    **WinRM e winrm/config/Listener**

3. Si vous ne voyez pas l’écouteur HTTPs, ou si le curseur de l’écouteur HTTPs n’est pas le même que le curseur d’impression du certificat d’authentification serveur sur l’ordinateur collecteur, vous pouvez supprimer cet écouteur et en créer un nouveau avec l’impression appropriée. Pour supprimer l’écouteur https, utilisez la commande suivante :

    **WinRM supprimer winrm/config/Listener ? Adresse = * + transport = HTTPs**

    Pour créer un nouvel écouteur, utilisez la commande suivante :

    **WinRM créer winrm/config/Listener ? Adresse =&#42;+ transport = HTTPS @ {hostname = "** &lt; _nom de domaine complet du collecteur_ &gt; **"; CertificateThumbprint = "** &lt; _impression au pouce du certificat d’authentification serveur_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Configurer le mappage de certificat sur le collecteur d’événements

1. Créez un utilisateur local et ajoutez-le au groupe Administrateurs local.
2. Créez le mappage de certificat à l’aide d’un certificat qui est présent dans les « autorités de certification racines de confiance » de l’ordinateur ou « autorités de certification intermédiaires ».

    Il s’agit du certificat de l’autorité de certification racine ou intermédiaire qui a émis les certificats installés sur les ordinateurs de la source *d’événements (pour éviter toute confusion, il s’agit de l’autorité de certification située immédiatement au-dessus du certificat dans la chaîne de certificats)*:

    **WinRM créer winrm/config/service/certmapping ?** = &lt; _Empreinte numérique du certificat de l’autorité de certification émettrice_ &gt; **+ Subject =&#42;+ URI =&#42; @ {nom d’utilisateur = "** &lt; _username_ &gt; **"; Password = "** &lt; _mot_de_passe_ &gt; **"}-distant : localhost**

3. À partir d’un client, testez l’écouteur et le mappage de certificat à l’aide de la commande suivante :

    **WinRM g winrm/config-r :https://** &lt; _Nom de domaine complet_ &gt; du collecteur d’événements **: 5986-a :Certificate-Certificat :»** &lt; _Empreinte numérique du certificat_ &gt; d’authentification client **"**

    Elle doit retourner la configuration WinRM du collecteur d’événements. **Ne** dépassez pas cette étape si la configuration n’est pas affichée.

    **Que se passe-t-il à cette étape ?**
    - Le client se connecte au collecteur d’événements et envoie le certificat spécifié
    - Le collecteur d’événements recherche l’autorité de certification émettrice et vérifie si le est un mappage de certificat correspondant
    - Le collecteur d’événements valide l’état de la chaîne de certificats du client et des révocations
    - Si les étapes ci-dessus réussissent, l’authentification est terminée.

> [!NOTE]
> Vous pouvez obtenir une erreur d’accès refusé lors de la méthode d’authentification, ce qui peut être trompeur. Pour résoudre les problèmes, consultez le journal CAPI sur le collecteur d’événements.

4. Répertoriez les entrées certmapping configurées à l’aide de la commande : **WinRM enum winrm/config/service/certmapping**

### <a name="event-source-computer-configuration"></a>Configuration de l’ordinateur source d’événements

1. Ouverture de session avec un compte d’administrateur et ouverture de l’éditeur de stratégie de groupe local (gpedit. msc)
2. Accédez à l’ordinateur local Local\configuration \ modèles d’administration\Composants Components\Event de transfert.
3. Ouvrez la stratégie « configurer l’adresse du serveur, l’intervalle d’actualisation et l’autorité de certification de l’émetteur d’un gestionnaire d’abonnements cible ».
4. Activez la stratégie et cliquez sur le SubscriptionManagers « afficher... » bouton.
5. Dans la fenêtre SubscriptionManagers, entrez la chaîne suivante :

    **Serveur = https://** &lt; _Nom de domaine complet du serveur_ &gt; collecteur d’événements **: 5986/WSMan/SubscriptionManager/WEC, Refresh =** &lt; _Intervalle d’actualisation en secondes_ &gt; **, IssuerCA =** &lt; _Empreinte numérique du certificat de l’autorité de certification émettrice_&gt;

6. Exécutez la ligne de commande suivante pour actualiser les paramètres de stratégie de groupe locaux : gpupdate/force
7. Ces étapes doivent générer l’événement 104 dans votre ordinateur source observateur d’événements journal des applications et des services avec le message suivant :

    « Le redirecteur s’est correctement connecté au gestionnaire d’abonnement au &lt; nom de domaine complet de l’adresse &gt; , suivi de l’événement 100 avec le message suivant : «l’abonnement &lt; sub_name &gt; est correctement créé ».

8. Dans le collecteur d’événements, l’état d’exécution de l’abonnement affiche maintenant 1 ordinateur actif.
9. Ouvrez le journal ForwardedEvents sur le collecteur d’événements et vérifiez si les événements sont transférés à partir des ordinateurs sources.

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>Accorder l’autorisation sur la clé privée du certificat client sur la source de l’événement

1. Ouvrez la console de gestion des certificats pour l’ordinateur local sur l’ordinateur source de l’événement.
2. Cliquez avec le bouton droit sur le certificat client, puis sur gérer les clés privées.
3. Accordez une autorisation de lecture à l’utilisateur du SERVICE réseau.

### <a name="event-subscription-configuration"></a>Configuration de l’abonnement aux événements

1. Ouvrez observateur d’événements dans le collecteur d’événements et accédez au nœud abonnements.
2. Cliquez avec le bouton droit sur abonnements, puis choisissez « créer un abonnement... ».
3. Donnez un nom et une description facultative pour le nouvel abonnement.
4. Sélectionnez l’option « initiée par l’ordinateur source », puis cliquez sur « Sélectionner des groupes d’ordinateurs... ».
5. Dans groupes d’ordinateurs, cliquez sur « Ajouter des ordinateurs non-domaines... ». et tapez le nom d’hôte de la source de l’événement.
6. Cliquez sur « Ajouter des certificats... » et ajoutez le certificat de l’autorité de certification qui émet les certificats clients. Vous pouvez cliquer sur Afficher le certificat pour valider le certificat.
7. Dans autorités de certification, cliquez sur OK pour ajouter le certificat.
8. Lorsque vous avez terminé d’ajouter des ordinateurs, cliquez sur OK.
9. Dans les propriétés de l’abonnement, cliquez dans sélectionner des événements...
10. Configurez le filtre de requête des événements en spécifiant le ou les niveaux d’événement, les journaux des événements ou la ou les sources d’événements, les ID d’événement et toutes les autres options de filtrage.
11. Dans les propriétés de l’abonnement, cliquez sur avancé...
12. Choisissez l’une des options d’optimisation pour la remise d’événements de l’événement source vers le collecteur d’événements, ou laissez la valeur par défaut normal : 
    1. **Réduire la bande passante**: les événements seront remis moins de fréquence pour économiser la bande passante.
    2. **Réduire la latence**: les événements sont remis dès qu’ils se produisent pour réduire la latence des événements.
13. Remplacez le protocole par HTTPs et cliquez sur OK.
14. Cliquez sur OK pour créer le nouvel abonnement.
15. Vérifiez l’état d’exécution de l’abonnement en cliquant avec le bouton droit et en sélectionnant « état de l’exécution ».
