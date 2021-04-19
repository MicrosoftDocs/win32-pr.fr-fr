---
title: Glossaire Windows Remote Management
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106523768"
---
# <a name="windows-remote-management-glossary"></a>Glossaire Windows Remote Management


<dl> <dt>

WSMan : éléments * * * *
</dt> <dd>

Élément de protocole WS-Management retourné dans une énumération qui obtient à la fois les instances et l’instance [*ERP*](/windows). **WSMan : items** est un conteneur qui contient une instance et son EPR. Ce type d’énumération est initié lorsque l’indicateur **WSManFlagReturnObjectAndEPR** est défini dans la demande.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**contrôleur BMC (Baseboard Management Controller)**
</dt> <dd>

Microcontrôleur attaché localement à un serveur. Les contrôleurs BMC ont des capteurs qui surveillent l’état physique du serveur et une connexion réseau distincte qui peut communiquer sur le réseau, même si le serveur est hors connexion. Vous avez accès aux données BMC via le fournisseur WMI [*de l’interface de gestion de plateforme intelligente (IPMI)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Authentification de base**
</dt> <dd>

Nom d’utilisateur et mot de passe envoyés dans l’échange d’authentification. L’authentification de base peut être configurée pour utiliser le transport HTTP ou HTTPs dans un domaine ou un groupe de travail. Cette méthode est la méthode d'authentification la moins sécurisée.

</dd> <dt>

**BMC**
</dt> <dd>

Consultez [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**MODÈLE**
</dt> <dd>

Voir [*Common Information Model (CIM)*](windows-remote-management-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

L’application cliente qui utilise le protocole WS-Management pour accéder au service de gestion sur l’ordinateur local ou distant.

</dd> <dt>

**Common Information Model (CIM)**
</dt> <dd>

Le modèle [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md) qui décrit comment représenter des objets ordinateur et réseau réels. CIM utilise un paradigme orienté objet, où les objets managés sont modelés à l'aide des concepts de classes et d'instances.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Authentification Digest**
</dt> <dd>

Échange sur lequel le serveur reçoit une demande d’un client et envoie des données sur le client à un serveur d’authentification, généralement un contrôleur de domaine. Si le client est authentifié, le serveur reçoit une clé de session Digest utilisée pour authentifier les demandes ultérieures du client.

</dd> <dt>

**DMTF (Distributed Management Task Force)**
</dt> <dd>

L’organisation de l’industrie développant les normes de gestion et la technologie d’intégration pour les environnements d’entreprise et Internet.

</dd> <dt>

**DMTF**
</dt> <dd>

Voir [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**endpoint**
</dt> <dd>

Ressource qui peut être traitée par une [*référence de point de terminaison (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**Référence du point de terminaison (EPR)**
</dt> <dd>

Combinaison de WS-Addressing et WS-Management éléments d’adressage qui décrivent ensemble une adresse pour une ressource dans l’en-tête SOAP du message. Il s’agit d’un terme de service Web.

</dd> <dt>

**énumération**
</dt> <dd>

Un ensemble ou une collection d’instances de [*ressource*](windows-remote-management-glossary.md) ou l’action de demander un tel ensemble. Dans WS-Management protocole, [*WS-Enumeration*](windows-remote-management-glossary.md) est utilisé pour obtenir la collection. Dans l’implémentation de script de service WinRM de l’énumération, [**session. Enumerate**](session-enumerate.md) et l’objet [**énumérateur**](enumerator.md) sont utilisés. La méthode et l’interface C++ correspondantes sont [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) et [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

**EPR**
</dt> <dd>

Consultez [*Référence du point de terminaison (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**Service de collecte d’événements**
</dt> <dd>

Composant du système d’exploitation qui reçoit les événements du BMC et d’autres composants ou applications du système d’exploitation.

</dd> <dt>

**transfert d’événements**
</dt> <dd>

Une notification d’événements qui se produisent sur des ordinateurs distants peut être envoyée aux applications d’abonnement. Le transfert d’événements n’est pas une fonctionnalité de WinRM, mais du [Journal des événements Windows](/windows/desktop/WES/windows-event-log). Le transfert d’événements devient disponible pour la première fois dans Windows Vista. Les applications de gestion, telles que les Microsoft Operations Manager (MOM) utilisent le transfert d’événements.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Mécanisme de requête permettant de spécifier un ensemble limité d’instances dans la demande d’une [*ressource*](windows-remote-management-glossary.md). Vous pouvez spécifier un paramètre de *filtre* sur les appels à [**session. Enumerate**](session-enumerate.md) ou [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

**dialecte de filtre**
</dt> <dd>

Chaîne XML qui identifie le dialecte XML utilisé pour spécifier un [*filtre*](windows-remote-management-glossary.md) dans un appel à [**session. Enumerate**](session-enumerate.md) ou [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate). Le service WinRM prend en charge [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) comme dialecte de filtre lors de la réception des demandes.

</dd> <dt>

**échantillon**
</dt> <dd>

Chaîne XML qui identifie une partie d’une instance d’une ressource plutôt que l’intégralité de la ressource. La prise en charge des fragments est trouvée dans l’objet [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**dialecte de fragment**
</dt> <dd>

Chaîne XML qui identifie le dialecte XML utilisé pour spécifier un [*fragment*](windows-remote-management-glossary.md). La prise en charge des fragments est trouvée dans l’objet [**ResourceLocator**](resourcelocator.md) . Le service WinRM prend en charge [*XPath*](windows-remote-management-glossary.md) pour le dialecte de fragment lors de la réception des demandes.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**intrabande**
</dt> <dd>

L’application cliente obtient les données BMC via l' [*écouteur*](windows-remote-management-glossary.md) WinRM dans le système d’exploitation.

</dd> <dt>

**Interface de gestion de plateforme intelligente (IPMI)**
</dt> <dd>

Une norme de l’industrie informatique pour l’architecture du [*contrôleur BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md). Les fonctionnalités de gestion du matériel Windows fournissent un [*pilote IPMI*](windows-remote-management-glossary.md) et un [*fournisseur IPMI*](windows-remote-management-glossary.md) WMI qui permettent aux scripts de gestion, aux outils en ligne de commande et aux applications d’obtenir des données BMC. Le fournisseur IPMI a des [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.

</dd> <dt>

**IPMI**
</dt> <dd>

Voir [*interface de gestion de plateforme intelligente (IMPI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Pilote IPMI**
</dt> <dd>

Pilote du noyau qui permet d’accéder aux périphériques du contrôleur de gestion de la carte de configuration [*(BMC)*](windows-remote-management-glossary.md) à partir des composants du système d’exploitation.

</dd> <dt>

**Fournisseur IPMI**
</dt> <dd>

Fournisseur WMI standard qui définit les classes de modélisation de l' [*interface IPMI*](windows-remote-management-glossary.md) et de ses données. Le [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) est une dll com qui obtient des données à partir du BMC.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**KCS**
</dt> <dd>

Voir [*style de contrôleur clavier (KCS)*](windows-remote-management-glossary.md).

</dd> <dt>

**Authentification Kerberos**
</dt> <dd>

Méthode d’authentification mutuelle entre le client et le serveur qui utilise des clés chiffrées. Pour les ordinateurs qui s’exécutent sur un système d’exploitation Windows, le compte client doit être un compte de domaine dans le même domaine que le serveur. Lorsqu’un client utilise des informations d’identification par défaut, Kerberos est la méthode d’authentification si la chaîne de connexion ne correspond pas à l’un des éléments suivants : localhost, 127.0.0.1 ou \[ :: 1 \] .

</dd> <dt>

**Style de contrôleur de clavier (KCS)**
</dt> <dd>

Protocole utilisé par le [*pilote IPMI*](windows-remote-management-glossary.md) pour communiquer avec le [*contrôleur BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Service de gestion qui implémente WS-Management protocole pour envoyer et recevoir des messages. WinRM est un service d’écoute. Un écouteur est défini par un transport (HTTP ou HTTPs) et une adresse IPv4 ou IPv6. Vous pouvez créer plusieurs instances de l’écouteur WinRM sur un seul ordinateur en leur attribuant une adresse TCP/IP ou un numéro de port différent.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**message**
</dt> <dd>

Un package d’informations transmises entre des ordinateurs ou des réseaux distincts construits à l’aide du protocole [*SOAP*](windows-remote-management-glossary.md) . Le package possède un en-tête, qui décrit la cible et le transport du message, ainsi qu’un corps qui contient le contenu à utiliser lors de l’arrivée du message. Un message est une combinaison d’éléments provenant de spécifications telles que [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)et [*WS-Management*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**namespace**
</dt> <dd>

Un espace de noms [*WMI*](windows-remote-management-glossary.md) , qui est un regroupement logique de classes et d’instances WMI pour contrôler l’étendue et l’accès. La source de données de gestion la plus fréquente pour les systèmes exécutant Windows est l' \\ espace de noms CIMV2 racine, qui contient des classes telles que le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process). Les espaces de noms apparaissent dans l’URI de ressource pour les classes WMI, par exemple https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .

</dd> <dt>

**Négocier l’authentification**
</dt> <dd>

Type d’authentification unique négocié, qui est l’implémentation Windows d’un mécanisme de [*négociation GSSAPI simple et protégé (SPNEGO)*](windows-remote-management-glossary.md). La négociation SPNEGO détermine si l’authentification est gérée par Kerberos ou NTLM. Kerberos est le mécanisme préféré. L’authentification par négociation sur les systèmes Windows est également appelée authentification intégrée de Windows.

</dd> <dt>

**capteur numérique**
</dt> <dd>

Type numérique de capteur dans un contrôleur de gestion de la [*carte de baseboard (BMC)*](windows-remote-management-glossary.md), par exemple la température ou la tension.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**option**
</dt> <dd>

Données supplémentaires requises par le fournisseur de ressources pour traiter une demande. Par exemple, certains fournisseurs WMI requièrent des données supplémentaires fournies sous forme d’objets [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) . La prise en charge des options se trouve dans l’objet [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**hors bande**
</dt> <dd>

L’application cliente obtient les données directement à partir du contrôleur de gestion de la carte de configuration [*(BMC)*](windows-remote-management-glossary.md) d’un autre ordinateur, plutôt que via l' [*écouteur*](windows-remote-management-glossary.md) WinRM dans le système d’exploitation.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**collecter**
</dt> <dd>

Un message d’extraction [*WS-Enumeration*](windows-remote-management-glossary.md) est envoyé pour continuer une énumération démarrée par un appel initial à WS-Enumeration : Enumerate. L’opération d’extraction dans le service WinRM est effectuée par [**Enumerator. ReadItem**](enumerator-readitem.md) ou [**IWSManEnumerator :: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**resource**
</dt> <dd>

[*Point de terminaison*](windows-remote-management-glossary.md) qui représente un type distinct d’opération ou de valeur de gestion. Un service expose une ou plusieurs ressources et certaines ressources peuvent avoir plusieurs instances. Une ressource de gestion est semblable à une classe WMI ou à une table de base de données, et une instance est semblable à une instance de la classe ou à une ligne de la table. Par exemple, la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) représente une ressource. `Win32_LogicalDisk="C:\"` est une instance spécifique de la ressource.

</dd> <dt>

**URI de ressource**
</dt> <dd>

L' [*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md) utilisé pour identifier un type spécifique de ressource, tel que des disques ou des processus, sur un système.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**SÉLECTION**
</dt> <dd>

Consultez [*Journal des événements système (sel)*](windows-remote-management-glossary.md).

</dd> <dt>

**Adaptateur SEL**
</dt> <dd>

Adaptateur qui envoie les données du [*contrôleur BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) au [*collecteur d’événements*](windows-remote-management-glossary.md).

</dd> <dt>

**sélection**
</dt> <dd>

Paire nom/valeur qui représente une instance particulière d’une [*ressource*](windows-remote-management-glossary.md). Il s’agit essentiellement d’un filtre ou d’une « clé » qui identifie l’instance souhaitée de la ressource. La prise en charge du sélecteur se trouve dans l’objet [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**capteur**
</dt> <dd>

Un appareil de mesure dans un contrôleur de gestion de la [*carte de baseboard (BMC)*](windows-remote-management-glossary.md).

</dd> <dt>

**service**
</dt> <dd>

Application qui fournit des services de gestion aux clients via le protocole WS-Management et d’autres [*services Web*](windows-remote-management-glossary.md). Un service est généralement identique à l' [*écouteur*](windows-remote-management-glossary.md) d’un réseau. Le service a une adresse de transport physique.

</dd> <dt>

**session**
</dt> <dd>

Une connexion entre un Windows Remote Management [*client*](windows-remote-management-glossary.md) et l' [*écouteur*](windows-remote-management-glossary.md)WinRM local ou distant, ou le service. Cette connexion est semblable à la connexion entre un script client WMI et WMI sur un serveur distant. Les opérations de session, telles que l’énumération d’une ressource (énumération), l’obtention d’une instance d’une ressource (obtenir) ou l’exécution d’une méthode de ressource (Invoke) sont des méthodes de l’objet de **session** . Un objet de **session** est créé par [**WSMan. CreateSession**](wsman-createsession.md).

</dd> <dt>

**Interface SPNEGO (simple and Protected GSS-API Negotiation Mechanism)**
</dt> <dd>

Mécanisme d’authentification utilisé par le client ou le serveur pour recevoir des demandes de données via le WinRM dans un contexte de Active Directory. SPNEGO est basé sur un protocole RFC (Request for Comments) produit par l’IETF (Internet Engineering Task Force). SPNEGO est également connu sous le nom [*d’authentification intégrée de Windows*](windows-remote-management-glossary.md), le terme utilisé dans les rubriques d’aide Windows Remote Management.

</dd> <dt>

**protocole SOAP (Simple Object Access Protocol) ;**
</dt> <dd>

Protocole XML utilisé par les services Web.

</dd> <dt>

**SOAP**
</dt> <dd>

Voir [*protocole SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md).

</dd> <dt>

**SPNEGO**
</dt> <dd>

Consultez [*le mécanisme SPNEGO (simple and Protected GSS-API Negotiation Mechanism)*](windows-remote-management-glossary.md).

</dd> <dt>

**Journal des événements système (SEL)**
</dt> <dd>

La base de données des événements dans le matériel du contrôleur de gestion de la carte de base [*(BMC)*](windows-remote-management-glossary.md) . L' [*adaptateur sel*](windows-remote-management-glossary.md) transmet ces événements au système d’exploitation.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**URI (Uniform Resource Identifier)**
</dt> <dd>

Chaîne qui identifie une ressource dans l’entreprise, telle qu’un ordinateur, un processus, un lecteur de disque ou un capteur de température dans un [*contrôleur de gestion de la carte de baseboard (BMC)*](windows-remote-management-glossary.md). L’URI est le mécanisme d’adressage de service Web défini dans IETF (Internet Engineering Task Force) Uniform Resource Identifier (URI) : syntaxe générique \[ norme RFC 3986 \] .

</dd> <dt>

**URI**
</dt> <dd>

Consultez [*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**service Web**
</dt> <dd>

Application logicielle utilisée pour l’interaction entre les ordinateurs sur Internet ou sur un réseau. Les services Web sont décrits par le [*langage WSDL (Web Service Description Language)*](windows-remote-management-glossary.md). La description spécifique du service Web indique aux autres services comment interagir avec le service Web à l’aide de messages SOAP. Les messages sont acheminés entre les ordinateurs par un transport, en général HTTP ou HTTPs. [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)et [*WS-Management*](windows-remote-management-glossary.md) sont des exemples de protocoles utilisés par les applications de service Web pour communiquer entre elles.

</dd> <dt>

**WSDL (Web Service Description Language)**
</dt> <dd>

Langage basé sur XML utilisé pour définir le mode d’interaction avec un service Web. En général, le WSDL décrit les messages SOAP requis par le service Web pour retourner des données ou effectuer des opérations. Le WSDL permet à une implémentation d’un système d’exploitation de communiquer avec le service Web implémenté sur un autre système d’exploitation, à condition que les spécifications du WSDL soient remplies.

</dd> <dt>

**Authentification Windows intégrée**
</dt> <dd>

Consultez [*négociation de l’authentification*](windows-remote-management-glossary.md).

</dd> <dt>

**Windows Management Instrumentation (WMI)**
</dt> <dd>

L’implémentation Microsoft de la norme WBEM (Web-Based Enterprise Management) publiée par la [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md). WMI vous permet de gérer des ordinateurs locaux et distants et de modéliser des objets ordinateur et réseau à l’aide d’une extension de la norme [*Common Information Model (CIM)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Windows Remote Management (WinRM)**
</dt> <dd>

L’implémentation Microsoft d’un service Web de gestion basée sur le protocole de [*gestion des services*](windows-remote-management-glossary.md) Web standard public.

</dd> <dt>

**Windows Remote Shell (WinRS)**
</dt> <dd>

Outil shell qui s’appuie sur [*Windows Remote Management*](windows-remote-management-glossary.md) pour exécuter des commandes distantes, en particulier pour les serveurs headless. L’outil en ligne de commande est Winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Voir [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Plug-in WMI**
</dt> <dd>

Le plug-in WinRM qui rend les données WMI disponibles pour les clients WinRM.

</dd> <dt>

**WS-Addressing (WSA)**
</dt> <dd>

Protocole public standard, qui est basé sur SOAP, qui crée un système d’adressage utilisé dans les en-têtes de messages envoyés sur Internet. La norme définit la manière dont les ressources peuvent être situées sur des réseaux et des pare-feu. WS-Addressing est l’un des protocoles de service Web qui composent le protocole WS-Management.

</dd> <dt>

**WS-Enumeration (wsen)**
</dt> <dd>

Protocole public standard, qui est basé sur SOAP, pour l’énumération d’une séquence d’éléments XML pouvant représenter des collections de données, des journaux ou d’autres structures d’informations linéaires. WS-Enumeration est l’un des protocoles de service Web qui composent le protocole WS-Management.

</dd> <dt>

**WS-Eventing (WSE)**
</dt> <dd>

Protocole public standard, qui est basé sur SOAP, qui permet à un service Web (l’abonné) de s’abonner et d’accepter des messages de notification d’événement d’un autre service Web (la source de l’événement). WS-Eventing est l’un des protocoles de service Web qui composent le protocole WS-Management.

</dd> <dt>

**Gestion des services Web**
</dt> <dd>

Protocole public standard, qui est basé sur SOAP, pour le partage des données de gestion entre tous les systèmes d’exploitation, les ordinateurs et les périphériques. Tous les [*messages*](windows-remote-management-glossary.md) envoyés par les composants du client ou du serveur WinRM utilisent ce protocole.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Protocole public standard, qui est basé sur SOAP, pour accéder aux représentations XML des ressources basées sur les services Web via un ensemble simple de verbes, par exemple, obtenir, placer, appeler ou supprimer. WS-Transfer définit des opérations pour l’envoi et la réception de la représentation d’une ressource particulière et des opérations pour la création ou la suppression d’une ressource et de sa représentation correspondante.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Une notation de chemin d’accès pour l’adressage des parties d’un document XML, similaire à une URL. Une expression XPath est une séquence d’expressions à obtenir à partir de l’emplacement actuel dans le document XML vers un autre nœud ou un ensemble de nœuds. Les expressions sont séparées par des barres obliques inverses (« / »). Le service WinRM prend en charge [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) pour le [*dialecte de fragment*](windows-remote-management-glossary.md).

</dd> </dl>

 

 