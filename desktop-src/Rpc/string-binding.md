---
title: Liaison de chaîne
description: La liaison de chaîne est une chaîne de caractères non signée composée de chaînes qui représentent l’UUID d’objet de liaison, la séquence de protocole RPC, l’adresse réseau et les options de point de terminaison et de point de terminaison.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3f925c03c85be3c47ab174a85f31e72e40d828
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386978"
---
# <a name="string-binding"></a>Liaison de chaîne

La liaison de chaîne est une chaîne de caractères non signée composée de chaînes qui représentent l’UUID d’objet de liaison, la séquence de protocole RPC, l’adresse réseau et les options de point de terminaison et de point de terminaison.

*ObjectUUID* @ *ProtocolSequence*: \[ *point de terminaison* networkAddress,*option*\]

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*
</dt> <dd>

[UUID](/windows/desktop/Midl/uuid) de l’objet géré par l’appel de procédure distante. Sur le serveur, la bibliothèque Runtime RPC mappe le type d’objet à un vecteur de point d’entrée Manager (un tableau de pointeurs de fonction) pour appeler la routine Manager appropriée. Pour plus d’informations sur la façon de mapper les UUID d’objets aux vecteurs de point d’entrée Manager, consultez [inscription des interfaces](registering-interfaces.md).

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

Chaîne de caractères qui représente une combinaison valide d’un protocole RPC (par exemple, ncacn), un protocole de transport (tel que TCP) et un protocole réseau (par exemple, IP). Microsoft RPC prend en charge les protocoles suivants spécifiés dans les [constantes de séquence de protocole](protocol-sequence-constants.md).

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*NetworkAddress*
</dt> <dd>

Adresse réseau du système pour recevoir des appels de procédure distante.

> [!Note]  
> Les séquences de protocole suivantes ne sont pas prises en charge à partir de Windows XP :

 

-   [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ réseaux virtuels \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)
-   [\_IPX ncadg](/windows/desktop/Midl/ncadg-ipx)

Le format et le contenu de l’adresse réseau dépendent de la séquence de protocole spécifiée comme suit.



| Séquence de protocole                       | Adresse du réseau                                                                                                                                  | Exemples                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)     | Nom de l'ordinateur                                                                                                                                    | MyServer                                               |
| [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)     | Nom de l'ordinateur                                                                                                                                    | MyServer                                               |
| [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)       | Nom de l'ordinateur                                                                                                                                    | MyServer                                               |
| [\_TCP IP \_ ncacn](/windows/desktop/Midl/ncacn-ip-tcp)     | Adresse Internet sur quatre octets ou nom d’hôte. Si la pile réseau IPv6 est installée, IPv6 est entièrement pris en charge et une adresse IPv6 est également acceptée. | 128.10.2.30 anynode.microsoft.com                      |
| [ncacn \_ NP](/windows/desktop/Midl/ncacn-np)              | Nom du serveur (les barres obliques inverses doubles de début sont facultatives)                                                                                            | monserveur \\ \\ myotherserver                             |
| [ncacn \_ SPX](/windows/desktop/Midl/ncacn-spx)            | Adresse Internet IPX ou nom du serveur                                                                                                             | ~ 0000000108002B30612C MyServer                         |
| [ncacn \_ dnet \_](/windows/desktop/Midl/ncacn-dnet-nsp) | Syntaxe de zone et de nœud                                                                                                                             | 4,120                                                  |
| [ncacn \_ au \_ fournisseur DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Nom de l’ordinateur, éventuellement suivi de @ et du nom de la zone AppleTalk. La valeur par défaut \* est @, la zone du client, si aucune zone n’est fournie.                     | servername@zonename nom du serveur                         |
| [ncacn \_ réseaux virtuels \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Nom du serveur StreetTalk de la forme item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)              | Nom du serveur                                                                                                                                      | MyServer                                               |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Adresse Internet (nom convivial ou nom de serveur local).                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [\_UDP IP \_ ncadg](/windows/desktop/Midl/ncadg-ip-udp)     | Adresse Internet sur quatre octets ou nom d’hôte                                                                                                        | 128.10.2.30 anynode.microsoft.com                      |
| [\_IPX ncadg](/windows/desktop/Midl/ncadg-ipx)            | Adresse Internet IPX ou nom du serveur                                                                                                             | ~ 0000000108002B30612C MyServer                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Nom de l'ordinateur                                                                                                                                     | thismachine                                            |



 

Le champ adresse réseau est facultatif. Si vous ne spécifiez pas d’adresse réseau, la liaison de chaîne fait référence à votre hôte local. Il est possible de spécifier le nom de l’ordinateur local lorsque vous utilisez la séquence de protocole **Ncalrpc** , mais cela est complètement inutile.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Poste*
</dt> <dd>

Point de terminaison ou adresse du processus pour recevoir des appels de procédure distante. Un point de terminaison peut être précédé du mot clé **Endpoint =**. La spécification du point de terminaison est facultative si le serveur a inscrit ses liaisons auprès du mappeur de point de terminaison. Consultez [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

Le format et le contenu d’un point de terminaison dépendent de la séquence de protocole spécifiée, comme indiqué dans la table de point de terminaison/option suivante.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Option*
</dt> <dd>

Options spécifiques au protocole. Le champ d’option n’est pas obligatoire. Chaque option est spécifiée par une paire {nom, valeur} qui utilise la valeur de l’option nom de l' *option* de syntaxe = . Les options sont définies pour chaque séquence de protocole, comme indiqué dans la table Endpoint/option suivante.



| Séquence de protocole                       | Point de terminaison                                                                                           | Exemples             | Nom d'option                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)     | Entier compris entre 1 et 254. De nombreuses valeurs comprises entre 0 et 32 sont réservées par Microsoft.                 | 100                  | Aucun                                                   |
| [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)     | (comme ci-dessus)                                                                                         | (comme ci-dessus)           | Aucun                                                   |
| [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)       | (comme ci-dessus)                                                                                         | (comme ci-dessus)           | Aucun                                                   |
| [\_TCP IP \_ ncacn](/windows/desktop/Midl/ncacn-ip-tcp)     | Numéro de port Internet.                                                                              | 1025                 | Aucun                                                   |
| [ncacn \_ NP](/windows/desktop/Midl/ncacn-np)              | Canal nommé. Le nom doit commencer par « \\ \\ pipe ».                                                       | \\\\canal \\ \\ pipeName | Sécurité                                               |
| [ncacn \_ SPX](/windows/desktop/Midl/ncacn-spx)            | Entier compris entre 1 et 65535.                                                                       | 5 000                 | Aucun                                                   |
| [ncacn \_ dnet \_](/windows/desktop/Midl/ncacn-dnet-nsp) | Numéro d’objet de la phase IV DECnet (doit être précédé du \# caractère) ou nom de l’objet.              | MailServer \# 17      | Aucun                                                   |
| [ncacn \_ au \_ fournisseur DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Chaîne de caractères, d’une longueur maximale de 22 octets.                                                           | myservicesendpoint   | Aucun                                                   |
| [ncacn \_ réseaux virtuels \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Numéro de port Vines SPP entre 250 et 511.                                                         | 500                  | Aucun                                                   |
| [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)              | Entier compris entre 1 et 65535.                                                                       | 5 000                 | Aucun                                                   |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Numéro de port Internet.                                                                              | 2215                 | Noms des serveurs proxy HTTP et RPC, option HttpConnection |
| [\_UDP IP \_ ncadg](/windows/desktop/Midl/ncadg-ip-udp)     | Numéro de port Internet.                                                                              | 1025                 | Aucun                                                   |
| [\_IPX ncadg](/windows/desktop/Midl/ncadg-ipx)            | Entier compris entre 1 et 65535.                                                                       | 5 000                 | Aucun                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Chaîne spécifiant le nom de l’application ou du service. La chaîne ne peut pas contenir de barres obliques inverses. | mon \_ imprimante          | Sécurité                                               |



 

Le nom de l’option **HttpConnectionOption** , pris en charge pour la \_ séquence de protocole http ncacn, prend la valeur suivante.



| Nom d'option       | Value            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

Le **HttpConnectionOption** vous permet de diriger le comportement des RPC s lors de l’établissement de connexions http. La valeur **UseHttpProxy** indique à RPC de router le trafic via le proxy http à tout moment, y compris lorsque les options Internet sont définies dans Internet Explorer pour ignorer le serveur proxy pour les adresses locales.  Cette option indique au client de se connecter de force au proxy RPC via le proxy http. Cela accélère le temps nécessaire à l’établissement d’une connexion, car il ignore les retards de recherche du serveur RPC directement avant l’utilisation du proxy HTTP.

Si cette option **HttpConnectionOption** est utilisée et qu’Internet Explorer sur le client n’est pas configuré pour utiliser ce proxy http, les connexions peuvent échouer avec les **\_ \_ \_ \_ options réseau non valides RPC**.

``` syntax
HttpConnectOption=UseHttpProxy
```

Pour plus d’informations sur **HttpConnectionOption**, consultez [utilisation de http comme transport RPC](using-http-as-an-rpc-transport.md).

Le nom d’option de **sécurité** , pris en charge pour les séquences de protocole Ncalrpc, ncacn \_ NP, ncadg \_ IP \_ UDP et ncadg \_ IPX, accepte les valeurs d’option suivantes.



| Nom d'option  | Valeur d'option                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Sécurité** | {identifier \| l' \| emprunt d’identité anonyme} { \| statique dynamique} {**true** \| **false**} |



 

Si le nom de l’option de sécurité est spécifié, une entrée de chaque ensemble de valeurs d’option de sécurité doit également être fournie. Les valeurs des options doivent être séparées par un caractère d’espace. Par exemple, les champs d' *option* suivants sont valides :

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

Les valeurs des options de sécurité ont les significations suivantes.



| Valeur de l’option de sécurité | Description                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anonyme             | Le client est anonyme au serveur.                                                                                                                                                                                                                                                                                                                   |
| Dynamique               | Les modifications apportées à l’identité de sécurité du client sont visibles par le serveur lorsque le serveur utilise la sécurité de transport. Il s’agit du mode par défaut pour la sécurité de niveau de transport LRPC (Ncalrpc) et pour la sécurité au niveau du transport de canal nommé local (ncacn \_ NP).                                                                                                             |
| **False**             | Effective = **false**; tous les paramètres de privilèges de jeton, y compris ceux dont la valeur est OFF, sont inclus dans le jeton sur le serveur et peuvent être activés par le serveur. Les privilèges sont pertinents uniquement pour les appels RPC sur un seul ordinateur.                                                                                                                                     |
| **Identification**    | Le serveur contient des informations sur le client, mais ne peut pas emprunter l’identité.                                                                                                                                                                                                                                                                                      |
| **Emprunt d'identité**     | Le serveur peut agir pour le compte du client au sein du système local (la sécurité au niveau du transport ne prend pas en charge la délégation).                                                                                                                                                                                                                               |
| **Statique**            | Les modifications apportées à l’identité de sécurité du client ne sont pas visibles par le serveur lorsque le serveur utilise la sécurité de transport. Il s’agit du seul mode disponible pour la sécurité au niveau du transport de canal nommé distant (ncacn \_ NP). L’identité de l’appelant est enregistrée lors du premier appel de procédure distante sur ce handle de liaison, et non au moment de la création du handle de liaison. |
| **True**              | Effectif = **true**; Seuls les paramètres de privilèges de jeton avec la valeur ON sont inclus dans le jeton sur le serveur. Si cette option est utilisée, les privilèges définis sur désactivé ne peuvent pas être activés par le serveur. Les privilèges sont pertinents uniquement pour les appels RPC sur un seul ordinateur.                                                                                                         |



 

Pour plus d’informations sur les options de sécurité, la [sécurité](security.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’espace blanc n’est pas autorisé dans les liaisons de chaînes, sauf lorsque la syntaxe de l' *option* l’exige. Les paramètres par défaut pour les champs *networkAddress*, *Endpoint* et *option* varient en fonction de la valeur du membre *ProtocolSequence* .

Pour tous les champs de liaison de chaîne, une seule barre oblique inverse ( \\ ) est interprétée comme un caractère d’échappement. Pour spécifier une barre oblique inverse unique, vous devez fournir deux barres obliques inverses ( \\ \\ ).

Une liaison de chaîne contient la représentation sous forme de caractère d’un handle de liaison et parfois des parties d’un handle de liaison. Les liaisons de chaînes sont pratiques pour représenter des parties d’un handle de liaison, mais elles ne peuvent pas être utilisées pour effectuer des appels de procédure distante. Elles doivent d’abord être converties en un handle de liaison en appelant [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).

En outre, une liaison de chaîne ne contient pas toutes les informations d’un handle de liaison. Par exemple, les informations d’authentification, le cas échéant, associées à un handle de liaison ne sont pas converties dans la liaison de chaîne retournée par l’appel de [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).

Lors du développement d’une application distribuée, les serveurs peuvent communiquer leurs informations de liaison aux clients à l’aide de liaisons de chaîne pour établir une relation client-serveur sans utiliser la base de données de mappage de point de terminaison ou de service de nom. Pour établir une telle relation, utilisez la fonction [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) pour convertir un ou plusieurs handles de liaison d’un vecteur de handle de liaison en une liaison de chaîne et fournissez la liaison de chaîne au client.

## <a name="examples"></a>Exemples

Voici des exemples de liaisons de chaînes valides. Dans ces exemples, *obj-UUID* est utilisé pour faciliter la représentation d’un UUID valide sous forme de chaîne. Au lieu d’afficher l’UUID 308FB580-1EB2-11CA-923B-08002B1075A7, les exemples affichent *obj-UUID*.

``` syntax
obj-uuid@ncadg_mq:mymqserver
obj-uuid@ncacn_http:major7.microsoft.com[2225]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80,HttpConnectOption=UseHttpProxy]
obj-uuid@ncacn_ip_tcp:16.20.16.27[2001]
obj-uuid@ncacn_ip_tcp:16.20.16.27[endpoint=2001]
obj-uuid@ncacn_nb_nb:
obj-uuid@ncacn_nb_nb:[100]
obj-uuid@ncacn_np:
obj-uuid@ncacn_np:[\\pipe\\p3,Security=impersonation static true]
obj-uuid@ncacn_np:\\\\marketing[\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\marketing[endpoint=\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\sales
obj-uuid@ncacn_np:\\\\sales[\\pipe\\p1,Security=identification dynamic true]
obj-uuid@ncalrpc:
obj-uuid@ncalrpc:[object1_name_demonstrating_that_these_can_be_lengthy]
obj-uuid@ncalrpc:[object2_name,Security=anonymous static true]
obj-uuid@ncacn_vns_spp:server@group@org[500]
obj-uuid@ncacn_dnet_nsp:took[elf_server]
obj-uuid@ncacn_dnet_nsp:took[endpoint=elf_server]
obj-uuid@ncadg_ip_udp:128.10.2.30
obj-uuid@ncadg_ip_udp:maryos.microsoft.com[1025]
obj-uuid@ncadg_ipx: ~0000000108002B30612C[5000]
obj-uuid@ncadg_ipx:printserver
obj-uuid@ncacn_spx:annaw[4390]
obj-uuid@ncacn_spx:~0000000108002B30612C
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[Utilisation de HTTP comme transport RPC](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

