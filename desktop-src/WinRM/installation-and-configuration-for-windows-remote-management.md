---
title: Installation et configuration de Windows Remote Management
description: pour les scripts Windows Remote Management (winrm) à exécuter, et pour que l’outil de ligne de commande **WinRM** exécute des opérations de données, Windows Remote Management (winrm) doit être installé et configuré à la fois.
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: c031ad9b9d9c888385527c227b102c64bb4dfb65eaea340e52eac3fb9595e591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997619"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a>Installation et configuration de Windows Remote Management

pour les scripts Windows Remote Management (winrm) à exécuter, et pour que l’outil de ligne de commande **WinRM** exécute des opérations de données, Windows Remote Management (winrm) doit être installé et configuré à la fois.

Ces éléments dépendent également de la configuration de WinRM.

- l’outil en ligne de commande de l' [interpréteur](./windows-remote-management-glossary.md#w) de commandes (**Winrs**) Windows.
- [Transfert d’événements](./windows-remote-management-glossary.md#e).
- Windows PowerShell la communication à distance 2,0.

## <a name="where-winrm-is-installed"></a>Où WinRM est installé

WinRM est installé automatiquement avec toutes les versions actuellement prises en charge du système d’exploitation Windows.

## <a name="configuration-of-winrm-and-ipmi"></a>Configuration de WinRM et IPMI

Ces composants du [fournisseur WMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) de WinRM et de l' [interface de gestion de plateforme intelligente (IPMI)](./windows-remote-management-glossary.md#i) sont installés avec le système d’exploitation.

- le service WinRM démarre automatiquement sur Windows Server 2008 et en amont (sur Windows Vista, vous devez démarrer le service manuellement).
- Par défaut, aucun [écouteur](./windows-remote-management-glossary.md#l) WinRM n’est configuré. Même si le service WinRM est en cours d’exécution, WS-Management [messages](./windows-remote-management-glossary.md#m) de protocole qui demandent des données ne peuvent pas être reçus et envoyés.
- Le pare-feu de connexion Internet (ICF) bloque l’accès aux ports.

Utilisez la commande **WinRM** pour localiser les écouteurs et les adresses en tapant la commande suivante à une invite de commandes.

```console
winrm e winrm/config/listener
```

Pour vérifier l’état des paramètres de configuration, tapez la commande suivante.

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a>Configuration par défaut rapide

Vous pouvez activer le protocole WS-Management sur l’ordinateur local et configurer la configuration par défaut pour la gestion à distance à l’aide de la commande `winrm quickconfig` .

La `winrm quickconfig` commande (ou la version abrégée `winrm qc` ) effectue ces opérations.

- Démarre le service WinRM et définit le type de démarrage du service sur démarrage automatique.
- Configure un écouteur pour les ports qui envoient et reçoivent des [messages](./windows-remote-management-glossary.md#m) de protocole WS-Management à l’aide de HTTP ou https sur n’importe quelle adresse IP.
- Définit les exceptions ICF pour le service WinRM et ouvre les ports pour HTTP et HTTPs.

> [!NOTE]
> La `winrm quickconfig` commande crée une exception de pare-feu uniquement pour le profil utilisateur actuel. Si le profil de pare-feu est modifié pour une raison quelconque, vous devez exécuter `winrm quickconfig` pour activer l’exception de pare-feu pour le nouveau profil ; sinon, l’exception peut ne pas être activée.

Pour récupérer des informations sur la personnalisation d’une configuration, tapez `winrm help config` à l’invite de commandes.

### <a name="to-configure-winrm-with-default-settings"></a>Pour configurer WinRM avec les paramètres par défaut

1. Tapez `winrm quickconfig` à une invite de commandes.

   Si vous n’êtes pas en cours d’exécution sous le compte d’administrateur de l’ordinateur local, vous devez sélectionner **exécuter en tant qu’administrateur** dans le menu **Démarrer** ou utiliser la commande **runas** à partir d’une invite de commandes.

2. Quand l’outil affiche **ces modifications \[ y/n \] ?**, tapez **y**.

   Si la configuration réussit, la sortie suivante s’affiche.

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. Conservez les paramètres par défaut pour les composants client et serveur de WinRM, ou personnalisez-les. Par exemple, vous devrez peut-être ajouter certains ordinateurs distants à la liste TrustedHosts de la configuration du client.

   Vous devez configurer une liste d’hôtes approuvés lorsque l’authentification mutuelle ne peut pas être établie. Kerberos autorise l’authentification mutuelle, mais il ne peut pas être utilisé dans les domaines de groupes de travail &mdash; uniquement. Lorsque vous configurez des hôtes approuvés pour un groupe de travail, il est recommandé de rendre la liste aussi restreinte que possible.

4. Créez un écouteur HTTPs en tapant la commande `winrm quickconfig -transport:https` . N’oubliez pas que vous devez ouvrir le port 5986 pour que le transport HTTPs fonctionne.

## <a name="listener-and-ws-management-protocol-default-settings"></a>Paramètres par défaut de l’écouteur et du protocole WS-Management

Pour obtenir la configuration de l’écouteur, tapez `winrm enumerate winrm/config/listener` à une invite de commandes. Les écouteurs sont définis par un transport (HTTP ou HTTPs) et une adresse IPv4 ou IPv6.

`winrm quickconfig` crée les paramètres par défaut suivants pour un écouteur. Vous pouvez créer plusieurs écouteurs. Pour plus d’informations, tapez `winrm help config` à l’invite de commandes.

### <a name="address"></a>Adresse

Spécifie l'adresse pour laquelle cet écouteur a été créé.

### <a name="transport"></a>Transport

Spécifie le transport à utiliser pour envoyer et recevoir les demandes et les réponses du protocole WS-Management. La valeur doit être *http* ou *https*. La valeur par défaut est *http*.

### <a name="port"></a>Port

Spécifie le port TCP pour lequel cet écouteur est créé.

**WinRM 2,0 :** Le port HTTP par défaut est 5985.

### <a name="hostname"></a>Nom d’hôte

Spécifie le nom d’hôte de l’ordinateur sur lequel le service WinRM est en cours d’exécution. La valeur doit être un nom de domaine complet, une chaîne littérale IPv4 ou IPv6, ou un caractère générique.

### <a name="enabled"></a>activé

Spécifie si l'écouteur est activé ou désactivé. La valeur par défaut est *True*.

### <a name="urlprefix"></a>URLPrefix

Spécifie un préfixe d’URL sur lequel accepter les requêtes HTTP ou HTTPs. Il s’agit d’une chaîne contenant uniquement les caractères a-z, A-Z, 9-0, le trait de soulignement ( \_ ) et la barre oblique (/). La chaîne ne doit pas commencer par une barre oblique (/). Par exemple, si le nom d’ordinateur est Exemplemachine, le client WinRM spécifie https://SampleMachine/< *URLPrefix*> dans l’adresse de destination. Le préfixe d’URL par défaut est « WSMan ».

### <a name="certificatethumbprint"></a>CertificateThumbprint

Spécifie l'empreinte numérique du certificat de service. Cette valeur représente une chaîne de valeurs hexadécimales à deux chiffres trouvée dans le champ empreinte numérique du certificat. Cette chaîne contient le hachage SHA-1 du certificat. Les certificats sont utilisés dans l'authentification par certificat client. Les certificats peuvent être mappés uniquement aux comptes d’utilisateurs locaux et ne fonctionnent pas avec les comptes de domaine.

### <a name="listeningon"></a>ListeningOn

Spécifie les adresses IPv4 et IPv6 que l’écouteur utilise. Par exemple : « 111.0.0.1, 111.222.333.444, :: 1, 1000:2000:2C : 3 : C19:9ec8 : A715:5e24, 3FFE : 8311 : FFFF : f70f : 0:5efe : 111.222.333.444, FE80 :: 5efe : 111.222.333.444% 8, FE80 :: C19:9ec8 : A715:5e24% 6 ».

## <a name="protocol-default-settings"></a>Paramètres par défaut du protocole

La plupart des paramètres de configuration, tels que MaxEnvelopeSizekb ou SoapTraceEnabled, déterminent la façon dont les composants serveur et client WinRM interagissent avec le protocole WS-Management. La liste suivante décrit les paramètres de configuration disponibles.

### <a name="maxenvelopesizekb"></a>MaxEnvelopeSizekb

Spécifie la quantité maximale de données SOAP (Simple Object Access Protocol), en kilo-octets. La valeur par défaut est de 150 kilo-octets.

> [!NOTE]  
> Le comportement n’est pas pris en charge si MaxEnvelopeSizekb est défini sur une valeur supérieure à 1039440.

### <a name="maxtimeoutms"></a>MaxTimeoutms

Spécifie le délai d’attente maximal, en millisecondes, qui peut être utilisé pour toute autre requête que les requêtes de tirage. La valeur par défaut est 60000.

### <a name="maxbatchitems"></a>MaxBatchItems

Spécifie le nombre maximal d'éléments qui peuvent être utilisés dans une réponse de collecte. La valeur par défaut est 32000.

### <a name="maxproviderrequests"></a>MaxProviderRequests

Spécifie le nombre maximal de demandes simultanées autorisées par le service. La valeur par défaut est 25.

**WinRM 2,0 :** Ce paramètre est déconseillé et est défini en lecture seule.

## <a name="winrm-client-default-configuration-settings"></a>Paramètres de configuration par défaut du client WinRM

La version client de WinRM possède les paramètres de configuration par défaut suivants.

### <a name="networkdelayms"></a>NetworkDelayms

Spécifie le temps supplémentaire, en millisecondes, pendant lequel l'ordinateur client attend pour prendre en compte pour la durée du délai réseau. La valeur par défaut est 5000 millisecondes.

### <a name="urlprefix"></a>URLPrefix

Spécifie un préfixe d’URL sur lequel accepter les requêtes HTTP ou HTTPs. Le préfixe d’URL par défaut est « WSMan ».

### <a name="allowunencrypted"></a>AllowUnencrypted

Permet à l'ordinateur client demander un trafic non chiffré. Par défaut, l’ordinateur client nécessite un trafic réseau chiffré et ce paramètre est défini sur *false*.

### <a name="basic"></a>De base

Permet à l'ordinateur client d'utiliser l'authentification de base. L'authentification de base est un modèle dans lequel le nom d'utilisateur et le mot de passe sont envoyés en texte clair au serveur ou au proxy. Cette méthode est la méthode d'authentification la moins sécurisée. La valeur par défaut est *True*.

### <a name="digest"></a>Digest

Permet à l'ordinateur client d'utiliser l'authentification Digest. L'authentification Digest est un modèle stimulation-réponse qui utilise une chaîne de données spécifiée par le serveur pour la stimulation. Seul l'ordinateur client peut initier une demande d'authentification Digest. L’ordinateur client envoie une demande au serveur pour s’authentifier et reçoit une chaîne de jeton du serveur. L’ordinateur client envoie ensuite la demande de ressource, y compris le nom d’utilisateur et un hachage de chiffrement du mot de passe associé à la chaîne de jeton. L'authentification Digest est prise en charge pour HTTP et HTTPS. Les applications et scripts du client WinRM Shell peuvent spécifier l’authentification Digest, mais le service WinRM n’accepte pas l’authentification Digest. La valeur par défaut est *True*.

> [!NOTE]
> L'authentification Digest sur HTTP n'est pas considérée comme étant sécurisée.

### <a name="certificate"></a>Certificat

Permet au client d’utiliser l’authentification par certificat client. L’authentification basée sur les certificats est un schéma dans lequel le serveur authentifie un client identifié par un certificat x509. La valeur par défaut est *True*.

### <a name="kerberos"></a>Kerberos

Permet à l'ordinateur client d'utiliser l'authentification Kerberos. L'authentification Kerberos est un modèle dans lequel le client et le serveur s'authentifient mutuellement à l'aide de certificats Kerberos. La valeur par défaut est *True*.

### <a name="negotiate"></a>Negotiate

Permet au client d'utiliser l'authentification par négociation. L'authentification par négociation est un modèle dans lequel le client envoie une demande au serveur pour s'authentifier. Le serveur détermine s'il faut utiliser le protocole Kerberos ou NTLM. Le protocole Kerberos est sélectionné pour authentifier un compte de domaine, et NTLM est sélectionné pour les comptes d'ordinateur local. Le nom d’utilisateur doit être spécifié au \\ \_ format de nom d’utilisateur de domaine pour un utilisateur de domaine. Le nom d’utilisateur doit être spécifié au format « nom \_ du serveur nom \\ \_ d’utilisateur » pour un utilisateur local sur un ordinateur serveur. La valeur par défaut est *True*.

### <a name="credssp"></a>CredSSP

Permet au client d’utiliser l’authentification CredSSP (Credential Security Support Provider). CredSSP permet à une application de déléguer les informations d’identification de l’utilisateur de l’ordinateur client au serveur cible. La valeur par défaut est *False*.

### <a name="defaultports"></a>DefaultPorts

Spécifie les ports qui seront utilisés par le client pour HTTP ou HTTPs.

**WinRM 2,0 :** Le port HTTP par défaut est 5985 et le port HTTPs par défaut est 5986.

### <a name="trustedhosts"></a>TrustedHosts

Spécifie la liste des ordinateurs distants approuvés. D’autres ordinateurs d’un groupe de travail ou des ordinateurs d’un autre domaine doivent être ajoutés à cette liste.

> [!Note]
> Les ordinateurs de la liste TrustedHosts ne sont pas authentifiés. Le client peut envoyer des informations d’identification à ces ordinateurs.

Si une adresse IPv6 est spécifiée pour un TrustedHost, l’adresse doit être placée entre crochets, comme le montre la commande WinRM Utility suivante : `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` .

Pour plus d’informations sur l’ajout d’ordinateurs à la liste TrustedHosts, tapez `winrm help config` .

## <a name="winrm-service-default-configuration-settings"></a>Paramètres de configuration par défaut du service WinRM

La version de service de WinRM possède les paramètres de configuration par défaut suivants.

### <a name="rootsddl"></a>RootSDDL

Spécifie le descripteur de sécurité qui contrôle l’accès à distance à l’écouteur. La valeur par défaut est «O :NSG : BAD : P (A ;; GA ;;; BA) (A ;; GR ;;; ER) S :P (AU ; FA ; GA ;;; WD) (AU ; SA ; GWGX;;; WD)».

### <a name="maxconcurrentoperations"></a>MaxConcurrentOperations

Nombre maximal d’opérations simultanées. La valeur par défaut est 100.

**WinRM 2,0 :** Le paramètre MaxConcurrentOperations est déconseillé et est défini en lecture seule. Ce paramètre a été remplacé par propriétés MaxConcurrentOperationsPerUser.

### <a name="maxconcurrentoperationsperuser"></a>Propriétés MaxConcurrentOperationsPerUser

Spécifie le nombre maximal d’opérations simultanées qu’un utilisateur peut ouvrir à distance sur le même système. La valeur par défaut est 1500.

### <a name="enumerationtimeoutms"></a>EnumerationTimeoutms

Spécifie le délai d’inactivité, en millisecondes, entre les messages d’extraction. La valeur par défaut est 60000.

### <a name="maxconnections"></a>MaxConnections

Spécifie le nombre maximal de demandes actives que le service peut traiter simultanément. La valeur par défaut est 300.

**WinRM 2,0 :** La valeur par défaut est 25.

### <a name="maxpacketretrievaltimeseconds"></a>MaxPacketRetrievalTimeSeconds

Spécifie la durée maximale, en secondes, que le service WinRM effectue pour récupérer un paquet. La valeur par défaut est 120 secondes.

### <a name="allowunencrypted"></a>AllowUnencrypted

Permet à l'ordinateur client demander un trafic non chiffré. La valeur par défaut est *False*.

### <a name="basic"></a>De base

Autorise le service WinRM à utiliser l’authentification de base. La valeur par défaut est *False*.

### <a name="certificate"></a>Certificat

Autorise le service WinRM à utiliser l’authentification par certificat client. La valeur par défaut est *False*.

### <a name="kerberos"></a>Kerberos

Autorise le service WinRM à utiliser l’authentification Kerberos. La valeur par défaut est *True*.

### <a name="negotiate"></a>Negotiate

Autorise le service WinRM à utiliser l’authentification par négociation. La valeur par défaut est *True*.

### <a name="credssp"></a>CredSSP

Permet au service WinRM d’utiliser l’authentification CredSSP (Credential Security Support Provider). La valeur par défaut est *False*.

### <a name="cbthardeninglevel"></a>CbtHardeningLevel

Définit la stratégie pour les spécifications requises des jetons de liaison de canal dans les demandes d'authentification. La valeur par défaut est *assouplie*.

### <a name="defaultports"></a>DefaultPorts

Spécifie les ports qui seront utilisés par le service WinRM pour HTTP ou HTTPs.

**WinRM 2,0 :** Le port HTTP par défaut est 5985 et le port HTTPs par défaut est 5986.

### <a name="ipv4filter-and-ipv6filter"></a>IPv4Filter et IPv6Filter

Spécifie les adresses IPv4 ou IPv6 que les écouteurs peuvent utiliser. Les valeurs par défaut sont IPv4Filter = \* et IPv6Filter = \* .

**IPv4 :** Une chaîne littérale IPv4 se compose de quatre nombres décimaux séparés par des points, chacun compris entre 0 et 255. Par exemple : 192.168.0.0.

**IPv6 :** Une chaîne littérale IPv6 est placée entre crochets et contient des nombres hexadécimaux séparés par des signes deux-points. Par exemple :: \[ 1 \] ou \[ 3FFE : FFFF :: 6ECB : 0101 \] .

### <a name="enablecompatibilityhttplistener"></a>EnableCompatibilityHttpListener

Spécifie si l’écouteur HTTP de compatibilité est activé. Si ce paramètre a la *valeur true*, l’écouteur écoute le port 80 en plus du port 5985. La valeur par défaut est *False*.

### <a name="enablecompatibilityhttpslistener"></a>EnableCompatibilityHttpsListener

Spécifie si l’écouteur HTTPs de compatibilité est activé. Si ce paramètre a la *valeur true*, l’écouteur écoute le port 443 en plus du port 5986. La valeur par défaut est *False*.

## <a name="winrs-default-configuration-settings"></a>Paramètres de Configuration par défaut de Winrs

`winrm quickconfig` configure également les paramètres par défaut de **Winrs** .

### <a name="allowremoteshellaccess"></a>AllowRemoteShellAccess

Permet d'accéder aux interpréteurs de commandes distants. Si vous définissez ce paramètre sur *false*, les nouvelles connexions de l’interpréteur de commandes à distance seront rejetées par le serveur. La valeur par défaut est *True*.

### <a name="idletimeout"></a>IdleTimeout

Spécifie la durée maximale, en millisecondes, que l'interpréteur de commandes distant reste ouvert quand il n'y a aucune activité utilisateur dans l'interpréteur de commandes distant. L'interpréteur de commandes distant est automatiquement supprimé après la durée spécifiée.

**WinRM 2,0 :** La valeur par défaut est 180000. La valeur minimale est 60000. La définition de cette valeur inférieure à 60000 n’aura aucun effet sur le délai d’expiration.

### <a name="maxconcurrentusers"></a>MaxConcurrentUsers

Spécifie le nombre maximal d'utilisateurs pouvant effectuer simultanément des opérations à distance sur le même ordinateur via un interpréteur de commandes distant. Les nouvelles connexions de shell distant seront rejetées si elles dépassent la limite spécifiée. La valeur par défaut est 5.

### <a name="maxshellruntime"></a>MaxShellRunTime

Spécifie la durée maximale, en millisecondes, pendant laquelle la commande ou le script distant est autorisé à s’exécuter. La valeur par défaut est 28,8 millions.

**WinRM 2,0 :** Le paramètre MaxShellRunTime est défini sur lecture seule. La modification de la valeur de MaxShellRunTime n’aura aucun effet sur les shells distants.

### <a name="maxprocessespershell"></a>MaxProcessesPerShell

Spécifie le nombre maximal de processus qu'une opération d'interpréteur de commandes est autorisée à démarrer. Une valeur de 0 autorise un nombre illimité de processus. La valeur par défaut est 15.

### <a name="maxmemorypershellmb"></a>MaxMemoryPerShellMB

Spécifie la quantité maximale de mémoire allouée par Shell, y compris les processus enfants de l’interpréteur de commandes. La valeur par défaut est 150 Mo.

### <a name="maxshellsperuser"></a>MaxShellsPerUser

Indique le nombre maximal de shells simultanés qu'un utilisateur peut ouvrir à distance sur le même ordinateur. Si ce paramètre de stratégie est activé, l’utilisateur ne peut pas ouvrir de nouveaux shells distants si le nombre dépasse la limite spécifiée. Si ce paramètre de stratégie est désactivé ou s'il n'est pas configuré, la limite par défaut est définie à 5 shells à distance par utilisateur.

## <a name="configuring-winrm-with-group-policy"></a>Configuration de WinRM avec stratégie de groupe

utilisez l’éditeur de stratégie de groupe pour configurer Windows Shell distant et WinRM pour les ordinateurs de votre entreprise.

### <a name="to-configure-with-group-policy"></a>Pour configurer avec stratégie de groupe

1. Ouvrez une fenêtre d’invite de commandes en tant qu’administrateur.
2. À l’invite de commandes, tapez `gpedit.msc`. La fenêtre de l' **éditeur d’objets stratégie de groupe** s’ouvre.
3. recherchez les **Windows Remote Management** et Windows objets de l' **interpréteur de commandes à distance** stratégie de groupe, sous **Configuration ordinateur \\ Modèles d’administration \\ Windows composants**.
4. Sous l’onglet **étendue** , sélectionnez un paramètre pour afficher une description. Double-cliquez sur un paramètre pour le modifier.

## <a name="windows-firewall-and-winrm-20-ports"></a>Windows Ports pare-feu et WinRM 2,0

À partir de WinRM 2,0, les ports de l’écouteur par défaut configurés par `Winrm quickconfig` sont le port 5985 pour le transport http et le port 5986 pour HTTPS. Les écouteurs WinRM peuvent être configurés sur n’importe quel port arbitraire.

Si un ordinateur est mis à niveau vers WinRM 2,0, les écouteurs configurés précédemment sont migrés et continuent de recevoir le trafic.

## <a name="winrm-installation-and-configuration-notes"></a>Remarques sur l’installation et la configuration de WinRM

WinRM n’est pas dépendant de tout autre service, à l’exception de WinHttp. si le Service d’administration IIS est installé sur le même ordinateur, vous pouvez voir des messages indiquant que WinRM ne peut pas être chargé avant Internet Information Services (IIS). Toutefois, WinRM ne dépend en fait pas d’IIS &mdash; , car l’ordre de chargement s’assure que le service IIS démarre avant le service http. WinRM requiert qu' `WinHTTP.dll` il soit inscrit.

Si le client de pare-feu ISA2004 est installé sur l’ordinateur, il peut provoquer le blocage d’un client WS-Management (Web Services for Management). Pour éviter ce problème, installez ISA2004 Firewall SP1.

Si deux services d’écoute avec des adresses IP différentes sont configurés avec le même numéro de port et le même nom d’ordinateur, WinRM écoute ou reçoit les messages sur une seule adresse. Cela est dû au fait que les préfixes d’URL utilisés par le protocole WS-Management sont identiques.

## <a name="ipmi-driver-and-provider-installation-notes"></a>Notes d’installation du fournisseur et du pilote IPMI

Il se peut que le pilote ne détecte pas l’existence de pilotes IPMI qui ne proviennent pas de Microsoft. Si le pilote ne parvient pas à démarrer, vous devrez peut-être le désactiver.

Si les ressources du contrôleur de gestion de la carte de configuration [(BMC)](./windows-remote-management-glossary.md#b) s’affichent dans le BIOS du système, ACPI (plug-and-Play) détecte le matériel BMC et installe automatiquement le pilote IPMI. La prise en charge de Plug-and-Play n’est peut-être pas disponible dans tous les contrôleurs BMC. Si le contrôleur BMC est détecté par Plug-and-Play, un appareil inconnu s’affiche dans Gestionnaire de périphériques avant l’installation du composant de gestion du matériel. Lorsque le pilote est installé, un nouveau composant, l’appareil compatible IPMI Microsoft ACPI Generic, s’affiche dans Gestionnaire de périphériques.

Si votre système ne détecte pas automatiquement le contrôleur BMC et installe le pilote, mais qu’un contrôleur BMC a été détecté pendant le processus d’installation, vous devez créer l’appareil BMC. Pour ce faire, tapez la commande suivante à l’invite de commandes : `Rundll32 ipmisetp.dll, AddTheDevice` . Une fois cette commande exécutée, l’appareil IPMI est créé et s’affiche dans Gestionnaire de périphériques. Si vous désinstallez le composant de gestion du matériel, l’appareil est supprimé.

Pour plus d’informations, consultez Introduction à la [gestion du matériel](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

Le fournisseur IPMI place les classes de matériel dans l' [espace de noms](/windows/desktop/WmiSdk/gloss-n) de **\\ matériel racine** de WMI. Pour plus d’informations sur les classes de matériel, consultez [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). Pour plus d’informations sur les *espaces de noms* WMI, voir [architecture WMI](/windows/desktop/WmiSdk/wmi-architecture).

## <a name="wmi-plug-in-configuration-notes"></a>Remarques sur la configuration du plug-in WMI

à partir de Windows 8 et Windows Server 2012, les [plug-ins WMI](./windows-remote-management-glossary.md#w) ont leurs propres configurations de sécurité. Pour qu’un utilisateur normal ou d’alimentation (non-administrateur) puisse utiliser le *plug-in WMI*, vous devez activer l’accès pour cet utilisateur une fois que l' [écouteur](./windows-remote-management-glossary.md#l) a été configuré. Tout d’abord, vous devez configurer l’utilisateur pour l’accès à distance à [WMI](./windows-remote-management-glossary.md#w) par le biais de l’une de ces étapes.

- Exécutez `lusrmgr.msc` pour ajouter l’utilisateur au groupe **WinRMRemoteWMIUsers \_ \_** dans la fenêtre **utilisateurs et groupes locaux** , ou
- Utilisez l’outil en ligne de commande **WinRM** pour configurer le descripteur de sécurité de l' [*espace de noms*](./windows-remote-management-glossary.md#n) du [plug-in WMI](./windows-remote-management-glossary.md#w), comme suit : `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` .

Lorsque l’interface utilisateur s’affiche, ajoutez l’utilisateur.

Après avoir configuré l’utilisateur pour l’accès à distance à [WMI](./windows-remote-management-glossary.md#w), vous devez configurer *WMI* pour permettre à l’utilisateur d’accéder au plug-in. Pour ce faire, exécutez `wmimgmt.msc` pour modifier la sécurité *WMI* de l' [espace de noms](./windows-remote-management-glossary.md#n) à accéder dans la fenêtre de **contrôle WMI** .

La majorité des classes WMI pour la gestion se trouvent dans l’espace de noms **\\ cimv2 racine** .