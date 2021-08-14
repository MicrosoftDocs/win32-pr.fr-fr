---
title: Protocole des services d’indexation de contenu
description: Ce document est une spécification du protocole de service d’indexation de contenu.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df48db5dd1b19983b12daeb6747dce92eedcd78674553f11af2e335f08e7de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481125"
---
# <a name="content-indexing-services-protocol"></a>Protocole des services d’indexation de contenu

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

Spécification de protocole, version 0,12

-   [1 Introduction](#1-introduction)
    -   [1.1 Glossaire](#11-glossary)
    -   [1.2 Références](#12-references)
    -   [Vue d’ensemble du protocole 1,3 (synopsis)](#13-protocol-overview-synopsis)
    -   [1.4 Relation aux autres protocoles](#14-relationship-to-other-protocols)
    -   [1,5 conditions préalables et conditions préalables](#15-prerequisites-and-preconditions)
    -   [1.6 Instruction d’applicabilité](#16-applicability-statement)
    -   [1.7 Contrôle de version et négociation de capacité](#17-versioning-and-capability-negotiation)
    -   [1.8 Champs extensibles de fournisseur](#18-vendor-extensible-fields)
    -   [1.9 Affectations de normes](#19-standards-assignments)
-   [2 Messages](#2-messages)
    -   [2.1 Transport](#21-transport)
    -   [2.2 Syntaxe de message](#22-message-syntax)
-   [3 Détails du protocole](#3-protocol-details)
    -   [Détails du serveur 3,1](#31-server-details)
    -   [Détails du client 3,2](#32-client-details)
-   [4 Exemples de protocoles](#4-protocol-examples)
    -   [4,1 exemple 1](#41-example-1)
    -   [4,2 exemple 2](#42-example-2)
-   [5 Sécurité](#5-security)
    -   [5.1 Considérations relatives à la sécurité pour les implémenteurs](#51-security-considerations-for-implementers)
    -   [5.2 Index de paramètres de sécurité](#52-index-of-security-parameters)
-   [6 index du comportement spécifique à la version](#6-index-of-version-specific-behavior)

Ce document est une spécification du protocole de service d’indexation de contenu.

la documentation du programme de protocole du serveur de groupe de travail (WSPP) est destinée à être utilisée conjointement avec la documentation sur les normes publiques, l’art de programmation réseau et les concepts de Windows des systèmes distribués de groupe de travail, et suppose que le lecteur est familiarisé avec le matériel mentionné ci-dessus ou qu’il y accède immédiatement.

Une spécification de protocole WSPP ne nécessite pas l’utilisation d’outils de programmation ou d’environnements de programmation Microsoft pour permettre à un licencié de développer une implémentation. Les titulaires de licences qui ont accès aux outils et aux environnements de programmation de Microsoft sont gratuits pour en tirer parti.

## <a name="1-introduction"></a>1 Introduction

-   [1.1 Glossaire](#11-glossary)
-   [1.2 Références](#12-references)
-   [Vue d’ensemble du protocole 1,3 (synopsis)](#13-protocol-overview-synopsis)
-   [1.4 Relation aux autres protocoles](#14-relationship-to-other-protocols)
-   [1,5 conditions préalables et conditions préalables](#15-prerequisites-and-preconditions)
-   [1.6 Instruction d’applicabilité](#16-applicability-statement)
-   [1.7 Contrôle de version et négociation de capacité](#17-versioning-and-capability-negotiation)
-   [1.8 Champs extensibles de fournisseur](#18-vendor-extensible-fields)
-   [1.9 Affectations de normes](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 Glossaire

> [!Note]  
> Les termes suivants sont définis dans la section Glossaire de \[ ms-sys \] :
>
> -   GUID
> -   Little endian
> -   Canal nommé
> -   Chemin

 

**Binding**: demande d’inclusion d’une **colonne** particulière dans un **ensemble de lignes** retourné. La **liaison** spécifie une propriété à inclure dans les résultats de la recherche.

**Bookmark**: marqueur qui identifie de façon unique une ligne dans un ensemble de lignes.

**Catalogue**: unité de niveau le plus élevé de l’organisation dans le service d’indexation. Il représente un ensemble de documents indexés par rapport auxquels les requêtes peuvent être exécutées à l’aide du protocole du service d’indexation de contenu.

**Category**: regroupement hiérarchique de lignes. Par exemple, un résultat de requête contenant les colonnes auteur et titre peut être classé en fonction de l’auteur. Chaque groupe de lignes contenant la même valeur pour l’auteur constitue une catégorie.

**Chapitre** : plage de **lignes** au sein d’un ensemble de **lignes** .

**Column**: conteneur pour un seul type d’informations dans une **ligne** . Les colonnes sont mappées à des noms de propriété et spécifient les propriétés qui sont utilisées pour les éléments de l' **arborescence** de **commandes** de la requête de recherche.

**Arborescence de commandes**: combinaison des **restrictions** , **catégories** et **ordres de tri** spécifiés pour la requête de recherche.

**Cursor**: entité utilisée comme mécanisme pour travailler avec une **ligne** ou un petit bloc de **lignes** à la fois dans un jeu de données retourné dans un jeu de résultats. Un **curseur** est positionné sur une seule **ligne** dans le jeu de résultats. Une fois que le **curseur** est positionné sur une ligne, les opérations peuvent être effectuées sur cette **ligne** ou sur un bloc de **lignes** commençant à cette position.

**Handle**: jeton qui peut être utilisé pour identifier les **curseurs** , les **chapitres** et les **signets** et y accéder.

**Index**: structure persistante qui contient le texte extrait des fichiers par un service d' **indexation** . Cela comprend la liste des mots, qui sont stockés avec le nom de fichier, l’emplacement de mot et les **paramètres régionaux** qui le contiennent.

**Indexation**: processus d’extraction de texte et de propriétés de fichiers et de stockage des valeurs extraites dans les **index** (pour le texte) et dans le **cache de propriétés** (pour les propriétés).

**Service d’indexation**: service qui crée des **catalogues** indexés pour le contenu et les propriétés des systèmes de fichiers. Les applications peuvent rechercher des informations dans les catalogues à partir des fichiers du système de fichiers indexé.

**Paramètres régionaux**: identificateur, tel que spécifié dans \[ MS-GPSI \] annexe A, qui spécifie les préférences relatives à la langue. Ces préférences indiquent comment les dates et les heures doivent être mises en forme, les éléments doivent être triés par ordre alphabétique, les chaînes doivent être comparées, et ainsi de suite.

**Requête en langage naturel**: requête construite à l’aide de la langue humaine au lieu de la syntaxe de requête.

**Mot parasite**: mot ignoré par le service d’indexation lorsqu’il est présent dans les **restrictions** spécifiées pour la requête de recherche, car il a peu de valeur discriminatoire. Les exemples en anglais incluent « a », « and » et « The ».

**Cache de propriété**: cache des propriétés de fichier extraites par un **service d’indexation** .

**Indexation** des propriétés : processus de création d’un **index** de **Propriétés de type valeur** d’un document, notamment l’auteur, l’objet, le type, le nombre de mots, le nombre de pages imprimées et toutes les autres propriétés.

**Restriction**: ensemble de conditions qu’un fichier doit remplir pour être inclus dans les résultats de recherche retournés par le **service d’indexation** en réponse à une requête de recherche. Une **restriction** réduit le focus d’une requête de recherche, limitant ainsi les fichiers que le **service d’indexation** inclura dans les résultats de la recherche à ceux qui répondent aux conditions.

**Row**: collection de **colonnes** contenant les valeurs de propriété qui décrivent un fichier unique à partir de l’ensemble de fichiers correspondant aux **restrictions** spécifiées dans la requête de recherche envoyée au **service d’indexation** .

**Rowset**: ensemble de **lignes** renvoyées dans les résultats de la recherche.

**Ordre de tri**: ensemble de règles dans une requête de recherche qui définit l’ordre des lignes dans les résultats de la recherche. Chaque règle se compose d’une propriété (nom, taille, etc.) et d’une direction pour le tri (croissant ou décroissant). Plusieurs règles sont appliquées séquentiellement

**Propriété Text-type**: propriété qui décrit le contenu d’un document et dont le texte n’est pas mis en forme et qui est associé à son nom.

**Propriété de type valeur**: propriété qui décrit un attribut unique d’un document entier. Une propriété de type valeur a un ID de type de données et une valeur de ce type de données associé à son nom.

**Racine virtuelle**: autre chemin d’accès à un dossier. Un dossier physique peut avoir zéro ou plusieurs racines virtuelles. Les chemins d’accès commençant par une racine virtuelle sont appelés chemins d’accès virtuels. Par exemple,/Server/vanityroot peut être une racine virtuelle de C : \\ IIS \\ Web \\ dossier1. Ensuite, le fichier C : \\ IIS \\ web \\ dossier1 \\default.htm présenterait le chemin d’accès virtuel/Server/vanityroot/default.htm.

**Peut**, doit, ne doit pas, ne doit pas : ces termes (en majuscules) sont utilisés comme décrit dans \[ rfc2119 \] . Toutes les instructions de comportement facultatif utilisent PEUT, DOIT ou NE DOIT PAS.

### <a name="12-references"></a>1.2 Références

### <a name="121-normative-references"></a>1.2.1 Références normatives

\[IEEE754 \] Institute of Electrical and Electronics Engineers, « Standard for Binary Floating-Point arithmétique », IEEE 754-1985, octobre 1985, https://standards.ieee.org/standard/754-1985.html

\[MS-DCOM \] Microsoft Corporation, « protocoles distants de modèle objet de composant distribué », juin 2006.

\[MS-GPSI \] Microsoft Corporation, « Extension installation des logiciels de la stratégie de groupe », juin 2006.

\[MS-SMB \] Microsoft Corporation, « protocole et extensions Microsoft Server Message Block (SMB) », mai 2006.

\[MS-SYS \] Microsoft Corporation, « System Overview v4 », juillet 2006.

\[SALTON \] Salton, G., "traitement automatique du texte : analyse de la transformation et récupération des informations par l’ordinateur", 1988, ISBN 0-201-2227-8.

\[UNICODE \] consortium Unicode, « la norme Unicode, Version 2,0 », 1996, https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 Références informatives

\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .

\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution valeurs, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>Vue d’ensemble du protocole 1,3 (synopsis)

Un **service d’indexation** de contenu permet d’organiser efficacement les fonctionnalités extraites d’une collection de documents. Le protocole CISP (Content Indexing Service Protocol) permet à un client de communiquer avec un serveur hébergeant un service d’indexation pour émettre des requêtes et permettre à un administrateur de gérer le serveur d’indexation.

Lors du traitement de fichiers, un service d’indexation analyse un ensemble de documents et réorganise leur contenu de telle sorte que les **Propriétés** de ces documents peuvent être retournées efficacement en réponse aux requêtes. Une collection de documents qui peuvent être interrogés comprend un **catalogue** . Un catalogue peut contenir un **index** (pour une référence rapide à du texte) et un **cache de propriétés** (pour une récupération rapide des valeurs de propriété).

Conceptuellement, un catalogue se compose d’une « table » logique de propriétés avec le texte ou la valeur et les paramètres régionaux correspondants stockés dans les **colonnes** de la table. Chaque « ligne » de la table correspond à un document distinct dans l’étendue du catalogue et chaque « colonne » de la table correspond à une propriété.

Les tâches spécifiques effectuées par CISP sont regroupées en deux zones fonctionnelles :

-   Administration à distance des catalogues de service d’indexation,
-   Interrogation à distance des catalogues de service d’indexation.

### <a name="131-remote-administration-tasks"></a>1.3.1 tâches d’administration à distance

CISP active les tâches de gestion du catalogue du service d’indexation suivantes à partir d’un client :

-   Interrogez l’état actuel d’un catalogue du service d’indexation sur le serveur.
-   Mettre à jour l’état d’un catalogue de services d’indexation.
-   Lancez le processus d’indexation pour un ensemble de fichiers particulier.
-   Initiez l’optimisation d’un index afin d’améliorer les performances des requêtes.

Toutes les tâches d’administration à distance suivent un modèle de requête/réponse simple. Aucun État n’est conservé sur le client pour tout appel d’administration et les appels administratifs peuvent être effectués dans n’importe quel ordre.

### <a name="132-remote-querying"></a>1.3.2 interrogation à distance

CISP permet aux clients d’effectuer des requêtes de recherche sur un serveur distant qui héberge un service d’indexation.

L’envoi d’une requête de recherche est un processus à plusieurs étapes initié par le client. Les étapes sont les suivantes :

1.  Le client demande une connexion à un serveur qui héberge un service d’indexation.
2.  Le client envoie les paramètres pour la requête de recherche, notamment :
    -   **Restrictions** permettant de spécifier les documents à inclure et/ou à exclure des résultats de la recherche.
    -   Ordre dans lequel les résultats de la recherche doivent être retournés.
    -   Colonnes à retourner dans le jeu de résultats.
    -   Nombre maximal de **lignes** qui doivent être retournées pour la requête.
    -   Durée maximale d’exécution de la requête.

        Une fois que le serveur a accepté la demande de lancement de la requête du client, le client peut demander des informations d’État sur la requête, mais cette étape n’est pas obligatoire.

3.  Le client spécifie ensuite les propriétés que le serveur doit inclure dans les résultats de la recherche.
4.  Le client demande un jeu de résultats sur le serveur, et le serveur répond en envoyant au client les valeurs de propriété des fichiers qui ont été inclus dans les résultats pour la requête de recherche du client. Si la valeur d’une propriété est trop grande pour tenir dans une seule mémoire tampon de réponse, le serveur n’envoie pas la propriété, mais définit plutôt l’état de la propriété sur différé. Le client demande ensuite la valeur de propriété séparément à l’aide d’une série de demandes pour les segments successifs de la valeur, puis reprend la demande d’autres valeurs.
5.  Une fois que le client a terminé la requête de recherche et n’a plus besoin de résultats supplémentaires, le client contacte le serveur pour libérer la requête.
6.  Une fois la requête lancée par le serveur, le client peut envoyer une demande de déconnexion du serveur. La connexion est ensuite fermée. Le client peut également émettre une autre requête et répéter la séquence à partir de l’étape 2.

Windows comportement : ce protocole est implémenté sur Windows 2000, Windows XP, Windows Server 2003 et Windows Vista.

### <a name="14-relationship-to-other-protocols"></a>1.4 Relation aux autres protocoles

Le CISP s’appuie sur le \[ protocole SMB MS-SMB \] pour le transport des messages. Aucun autre protocole ne dépend directement du protocole du service d’indexation de contenu.

*Windows Comportement : les applications interagissent généralement avec un wrapper d’interface OLE DB \[ MSDN-OLEDB \] (par exemple, un client de protocole) et pas directement avec le protocole.*

### <a name="15-prerequisites-and-preconditions"></a>1,5 conditions préalables et conditions préalables

Il est supposé que le client a obtenu le nom du serveur et un nom de catalogue avant l’appel de ce protocole. Le mode de fonctionnement d’un client est en dehors de la portée de cette spécification.

Il est également supposé que le client et le serveur ont une association de sécurité utilisable avec les canaux nommés \[ MS-SMB \] .

### <a name="16-applicability-statement"></a>1.6 Instruction d’applicabilité

CISP est conçu pour l’interrogation et la gestion des catalogues sur un serveur distant à partir d’un client. CISP est déconseillé sur Windows Vista.

### <a name="17-versioning-and-capability-negotiation"></a>1.7 Contrôle de version et négociation de capacité

Ce protocole n’a pas de mécanisme de contrôle de version ou de négociation de fonctionnalité.

### <a name="18-vendor-extensible-fields"></a>1.8 Champs extensibles de fournisseur

Ce protocole utilise des HRESULT qui sont extensibles par le fournisseur. Les fournisseurs sont libres de choisir leurs propres valeurs pour ce champ, tant que le bit C (0x20000000) est défini comme indiqué dans la section 4.1.1 de \[ ms-sys \] , indiquant qu’il s’agit d’un code client.

Ce protocole utilise également les valeurs NTSTATUS extraites de l’espace de nombre NTSTATUS défini dans \[ ms-sys \] . Les fournisseurs doivent réutiliser ces valeurs avec leur signification indiquée. Le choix d’une autre valeur exécute le risque d’une collision dans le futur.

*Windows comportement : Windows utilise uniquement les valeurs spécifiées dans la Section 4.1.3 de \[ MS-SYS \] .*

### <a name="181-property-ids"></a>ID de propriété 1.8.1

Les propriétés sont représentées par des ID connus sous le nom d’ID de propriété. Chaque propriété doit avoir un identificateur global unique. Cet identificateur se compose d’un **GUID** qui représente une collection de propriétés appelée un jeu de propriétés, plus une chaîne ou un entier 32 bits pour identifier la propriété dans le jeu. Si la forme entière de ID est utilisée, les valeurs 0x00000000, 0xFFFFFFFF et 0xFFFFFFFE sont considérées comme non valides.

Les fournisseurs peuvent garantir que leurs propriétés sont définies de manière unique en les plaçant dans un jeu de propriétés défini par leur propre GUID.

### <a name="19-standards-assignments"></a>1.9 Affectations de normes

Ce protocole n’a aucune attribution de normes, mais uniquement les affectations privées effectuées par Microsoft à l’aide de procédures d’allocation spécifiées dans d’autres protocoles.

Microsoft a alloué ce protocole à un canal nommé comme spécifié dans \[ MS-SMB \] . L’attribution est :



| Paramètre | Valeur             | Informations de référence  |
|-----------|-------------------|------------|
| Nom du canal | \\canal d' \\ intégration de \_ SKADS | \[MS-SMB\] |



 

## <a name="2-messages"></a>2 Messages

-   [2.1 Transport](#21-transport)
-   [2.2 Syntaxe de message](#22-message-syntax)

### <a name="21-transport"></a>2.1 Transport

Tous les messages doivent être transportés à l’aide d’un canal nommé, tel que spécifié dans \[ MS-SMB \] . Le nom de canal suivant est utilisé :

-   \\canal d' \\ intégration de \_ SKADS

Ce protocole utilise le protocole de canal nommé SMB sous-jacent pour récupérer l’identité de l’appelant qui a établi la connexion comme indiqué dans la section 2.2.8 de \[ MS-SMB \] ; le client doit définir l’identification de sécurité \_ en tant que ImpersonationLevel dans la demande pour ouvrir le canal nommé.

### <a name="22-message-syntax"></a>2.2 Syntaxe de message

Plusieurs structures et messages dans les sections suivantes font référence aux descripteurs de chapitres ou de signets. Un descripteur est une structure opaque de 32 bits qui identifie de façon unique un chapitre ou un signet. En règle générale, les applications clientes reçoivent des valeurs de handle via des appels de méthode ; Toutefois, il existe plusieurs valeurs connues qui n’ont pas besoin d’être obtenues à partir d’un serveur, ce qui signifie qu’elles sont spécifiées dans le tableau suivant :



| Valeur                         | Signification                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| DB \_ null \_ HCHAPTER 0x00000000 | Descripteur de chapitre de l’ensemble de lignes non chapitre, contenant tous les résultats de la requête.    |
| DBBMK \_ premier 0x00000001       | Handle de signet vers un signet qui identifie la première ligne dans l’ensemble de lignes. |
| DBBMK \_ dernier 0x00000002        | Handle de signet vers un signet qui identifie la dernière ligne de l’ensemble de lignes.  |



 

### <a name="221-structures"></a>2.2.1 structures

Cette section détaille les structures de données qui sont définies et utilisées par CISP.

Tous les entiers signés à 2, 4 et 8 octets et non signés dans les structures suivantes doivent être transférés dans l’ordre d’octet avec primauté des octets de poids faible (Little-endian).

Le tableau suivant récapitule les structures de données définies dans cette section.



| Structure                    | Description                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| CBaseStorageVariant          | Contient la valeur sur laquelle effectuer une opération de correspondance pour une propriété spécifiée dans une structure CPropertyRestriction. |
| SAFEARRAY, SAFEARRAY2        | Contient un tableau multidimensionnel.                                                                                     |
| SAFEARRAYBOUND               | Représente les limites d’une dimension d’un tableau spécifié dans une structure SAFEARRAY.                                  |
| CFullPropSpec                | Contient une spécification de propriété.                                                                                     |
| CContentRestriction          | Contient une chaîne à faire correspondre pour une valeur de propriété dans le cache de propriétés.                                                 |
| CKey                         | Contient une valeur de propriété.                                                                                             |
| CInternalPropertyRestriction | Contient une valeur de propriété à associer à une opération.                                                                  |
| CNatLanguageRestriction      | Contient une correspondance de requête en langage naturel pour une propriété.                                                                |
| CNodeRestriction             | Contient un tableau de nœuds d’arborescence de commandes spécifiant les restrictions pour une requête.                                       |
| COccRestriction              | Contient l’emplacement d’un mot dans une expression.                                                                           |
| CPropertyRestriction         | Contient une valeur de propriété à associer à une opération.                                                                  |
| CRangeRestriction            | Contient une restriction sur une plage de valeurs.                                                                           |
| CScopeRestriction            | Contient une restriction sur les fichiers à rechercher.                                                                    |
| CSort                        | Identifie une colonne à trier.                                                                                           |
| CSynRestriction              | Contient un mot ou ses synonymes pour une expression de requête.                                                                    |
| CVectorRestriction           | Contient une opération pondérée sur un nœud d’arborescence de commandes.                                                               |
| CWordRestriction             | Contient un mot pour une expression de requête.                                                                                    |
| CRestriction                 | Contient un nœud d’une arborescence de commandes de requête.                                                                               |
| CColumnSet                   | Indique le nombre de colonnes à retourner.                                                                             |
| CCategorizationSet           | Contient des informations sur le regroupement d’un ensemble de résultats de requête.                                                     |
| CCategorizationSpec          | Contient une définition des catégories dans lesquelles les résultats de la requête seront catégorisés.                                      |
| CDbColId                     | Contient une colonne.                                                                                                     |
| CDbProp                      | Contient une propriété.                                                                                                   |
| CDbPropSet                   | Contient un ensemble de propriétés.                                                                                          |
| CPidMapper                   | Contient un tableau d’ID de propriété spécifiant les propriétés à retourner dans un ensemble de lignes.                                     |
| CRowSeekAt                   | Contient le décalage à partir duquel récupérer des lignes dans un message CPMGetRowsIn                                                |
| CRowSeekAtRatio              | Identifie le point à partir duquel commencer la récupération d’un message CPMGetRowsIn.                                           |
| CRowSeekByBookmark           | Identifie les signets à partir desquels récupérer des lignes pour un message CPMGetRowsIn.                                       |
| CRowSeekNext                 | Contient le nombre de lignes à ignorer dans un message CPMGetRowsIn.                                                         |
| CRowsetProperties            | Contient les informations de configuration d’une requête.                                                                    |
| CSortSet                     | Contient l’ordre de tri d’une requête.                                                                                   |
| CTableColumn                 | Contient une colonne pour le message CPMSetBindings.                                                                      |
| SERIALIZEDPROPERTYVALUE      | Contient une valeur sérialisée.                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>2.2.1.1 CBaseStorageVariant

La structure CBaseStorageVariant contient la valeur sur laquelle effectuer une opération de correspondance pour une propriété spécifiée dans la structure CPropertyRestriction.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

vData1

vData2

vValue (variable)



 

**vType**: indicateur de type indiquant le type de vValue. Il doit s’agir de l’une des valeurs VARENUM spécifiées dans le tableau suivant.



| Valeur                 | Signification                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ vide (0x0000)    | vValue n’est pas présent.                                                                                                               |
| VT \_ null (0x0001)     | vValue n’est pas présent.                                                                                                               |
| VT \_ I1 (0x0010)       | Entier signé sur 1 octet.                                                                                                             |
| VT \_ UI1 (0x0011)      | Entier non signé sur 1 octet.                                                                                                           |
| VT \_ I2 (0x0002)       | Entier signé sur 2 octets.                                                                                                             |
| VT \_ UI2 (0x0012)      | Entier non signé sur 2 octets.                                                                                                           |
| VT \_ bool (0x000B)     | Valeur booléenne ; entier sur 2 octets qui contient 0x0000 (FALSe) ou 0xFFFF (TRUE).                                                        |
| VT \_ I4 (0x0003)       | Entier signé sur 4 octets.                                                                                                             |
| VT \_ UI4 (0x0013)      | Entier non signé sur 4 octets.                                                                                                           |
| VT \_ R4 (0x0004)       | Nombre à virgule flottante IEEE 32 bits, tel que défini dans \[ IEEE754 \] .                                                                     |
| VT \_ int (0x0016)      | Entier signé sur 4 octets.                                                                                                             |
| VT \_ uint (0x0017)     | Entier non signé sur 4 octets.                                                                                                           |
| \_Erreur VT (0x000A)    | Entier non signé de 4 octets contenant un HRESULT, tel que spécifié dans \[ ms-sys \] .                                                         |
| 0x0014 VT (en anglais \_ )       | Entier signé de 8 octets.                                                                                                            |
| VT \_ UI8 (0x0015)      | Entier non signé sur 8 octets.                                                                                                          |
| VT \_ R8 (0x0005)       | Nombre à virgule flottante IEEE 64 bits tel que défini dans \[ IEEE754 \] .                                                                      |
| VT \_ CY (0x0006)       | Entier de complément à deux octets (mis à l’échelle par 10 000).                                                                               |
| \_Date VT (0x0007)     | Nombre à virgule flottante 64 bits représentant le nombre de jours écoulés depuis 00:00:00 le 31 décembre 1899 (temps universel coordonné).     |
| VT \_ FILETIME (0x0040) | Entier 64 bits représentant le nombre d’intervalles de 100 nanosecondes depuis 00:00:00 le 1er janvier 1601 (heure universelle coordonnée). |
| VT \_ décimale (0x000E)  | Structure DÉCIMALe telle que spécifiée dans la section 2.2.1.1.1.1.                                                                             |
| \_CLSID VT (0x0048)    | Valeur binaire de 16 octets contenant un GUID.                                                                                            |
| \_Objet BLOB VT (0x0041)     | Nombre entier non signé de 4 octets d’octets dans l’objet BLOB, suivi de beaucoup d’octets de données.                                           |
| VT \_ BSTR (0x0008)     | Nombre entier d’octets non signés sur 4 octets dans la chaîne, suivi d’une chaîne, comme indiqué ci-dessous sous vValue.                       |
| VT \_ LPSTR (0x001E)    | Chaîne ANSI terminée par le caractère null.                                                                                                       |
| VT \_ LPWStr (0x001F)   | Chaîne Unicode Unicode terminée par le caractère null \[ \] .                                                                                        |
| \_Variante VT (0x000c)  | CBaseStorageVariant. DOIT être combiné avec un modificateur de type de \_ tableau VT ou de \_ vecteur VT.                                               |



 

Le tableau suivant spécifie les modificateurs de type pour vType. Les modificateurs de type peuvent être binaires avec vType, pour modifier la signification de vValue afin d’indiquer qu’il s’agit de l’un des deux types de tableau possibles.



| Valeur               | Signification                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Vecteur VT (0x1000) | Si l’indicateur de type est combiné avec \_ un vecteur VT à l’aide d’un opérateur or, vValue est un tableau compté des valeurs du type indiqué. Pour plus d’informations, consultez la section 2.2.1.1.1.2. <br/> Ce modificateur de type ne doit pas être combiné avec les types suivants : VT \_ int, VT \_ uint, VT \_ Decimal, VT \_ BLOB \_ , \_ objet BLOB VT.<br/>                                    |
| \_Tableau VT (0x2000)  | Si l’indicateur de type est combiné avec \_ un tableau VT par un opérateur or, la valeur est un SafeArray (comme spécifié dans la section 2.2.1.1.1.3) qui contient les valeurs du type indiqué. <br/> Ce modificateur de type ne doit pas être combiné avec les types suivants : VT \_ I8, VT \_ UI8, VT \_ fileTime, VT \_ CLSID, \_ objet BLOB VT, \_ objet BLOB VT \_ , VT \_ LPSTR, VT \_ LPWStr. <br/> |



 

**vData1**: lorsque vType est de type VT \_ Decimal, la valeur de ce champ est spécifiée en tant que champ Scale dans la section 2.2.1.1.1.1. Pour tous les autres vTypes, la valeur doit être égale à 0x00.

**vData2**: lorsque vType est de type VT \_ Decimal, la valeur de ce champ est spécifiée comme champ de signe dans la section 2.2.1.1.1.1. Pour tous les autres vTypes, la valeur doit être égale à 0x00.

**vValue**: valeur de l’opération de correspondance. La syntaxe doit être indiquée dans le champ vType.

Le tableau suivant récapitule les tailles du champ vValue, selon le champ vType pour les types de données de longueur fixe. La taille est en octets.



| vType                                                   | Taille |
|---------------------------------------------------------|------|
| VT \_ I1, VT, \_ UI1                                        | 1    |
| VT \_ I2, VT \_ UI2, VT \_ bool                               | 2    |
| VT \_ i4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, \_ erreur VT   | 4    |
| VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ ca, VT \_ date, VT \_ fileTime | 8    |
| VT \_ décimal, \_ CLSID VT                                  | 16   |



 

Si vType a \_ la valeur BLOB VT, VT \_ BSTR ou VT \_ LPSTR, la structure de vValue est spécifiée dans le diagramme suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbSize

blobData (variable, facultative)



 

**cbSize**: entier 32 bits non signé, indiquant la taille du champ blobData en octets. Si vType est défini sur VT \_ BSTR ou VT \_ LPSTR, cbSize doit avoir la valeur 0x00000000 lorsque la chaîne représentée est une chaîne vide.

**blobData**: doit avoir une longueur de cbSize en octets.

Pour vType ayant la valeur d' \_ objet BLOB VT, ce champ est opaque Binary BLOB Data.

Pour vType défini sur VT \_ BSTR, ce champ est un jeu de caractères dans un jeu de caractères OEM sélectionné. Le client et le serveur doivent être configurés pour avoir des jeux de caractères interopérables (hors bande du protocole). Il n’est pas nécessaire qu’elle se termine par un caractère null.

Pour vType défini sur VT \_ LPSTR, ce champ est une chaîne de caractères se terminant par un caractère NULL dans un jeu de caractères OEM sélectionné. Le client et le serveur doivent être configurés pour avoir des jeux de caractères interopérables (hors bande du protocole).

Si vType est défini sur VT \_ LPWStr, la structure de vValue est spécifiée dans le diagramme suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

ccLen

String (variable, facultative)



 

**ccLen**: entier non signé 32 bits, indiquant la taille du champ de chaîne en caractères Unicode. DOIT être défini sur 0x00000000 pour une chaîne vide.

**chaîne**: chaîne Unicode terminée par le caractère null.

### <a name="22111-cbasestoragevariant-structures"></a>Structures 2.2.1.1.1 CBaseStorageVariant

Les structures suivantes sont utilisées dans la structure CBaseStorageVariant.

### <a name="221111-decimal"></a>2.2.1.1.1.1 DÉCIMAL

Le nombre décimal est utilisé pour représenter une valeur numérique exacte avec une précision fixe et une échelle fixe.

Quand vType est défini sur VT \_ Decimal (0x0000E), les champs vData1 et vData2 de CBASESTORAGEVARIANT doivent être interprétés comme suit :

**vData1**: nombre de chiffres à droite de la virgule décimale. DOIT être compris entre 0 et 28.

**vData2**: signe de la valeur numérique. Défini sur 0x00 si positif, 0x80 si négatif.

Le format du champ vValue est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Hi32

Lo32

Mid32



 

**Hi32**: 32 bits les plus élevés de l’entier 96 bits.

**Lo32**: 32 bits de poids faible de l’entier 96 bits.

**Mid32**: bits 32 au milieu de l’entier 96 bits.

### <a name="221112-vt_vector"></a>vecteur VT 2.2.1.1.1.2 \_

Le \_ vecteur VT est utilisé pour passer des tableaux unidimensionnels.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vVectorElements

vVectorData



 

**vVectorElements**: entier non signé 32 bits, indiquant le nombre d’éléments contenus dans le champ vVectorData.

**vVectorData**: tableau d’éléments qui ont un type indiqué par vType avec le bit 0x1000 effacé. La taille d’un élément de longueur fixe individuel peut être obtenue à partir de la table de type de données de longueur fixe, comme indiqué dans la section 2.2.1.1. La longueur de ce champ, en octets, peut être calculée en multipliant vVectorElements par la taille d’un élément individuel.

Pour les types de données de longueur variable, vVectorData contient une séquence de types simples marshalés consécutivement, où le type est indiqué par vType avec le bit 0x1000 effacé. Cela comprend un cas spécial indiqué par la \_ variante VT du tableau VTYPE VT \| \_ (c’est-à-dire, 0x100C).

Les éléments du champ vVectorData doivent être séparés par 0 à 3 octets de remplissage, de sorte que chaque élément commence à un offset qui est un multiple de 4 octets à partir du début du message qui contient ce tableau. Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire. Le contenu des octets de remplissage doit être ignoré par le récepteur.

Pour un vType défini sur une \_ variante VT du tableau VT \| \_ , le type des éléments de cette séquence est CBaseStorageVariant.

### <a name="221113-safearray"></a>2.2.1.1.1.3 SAFEARRAY

SAFEARRAY est utilisé pour passer des tableaux multidimensionnels. La structure contient des informations sur la taille du tableau ainsi que les données du tableau.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

fFeatures

cbElements

Rgsabound (variable)

vData (variable)



 

**cDims**: entier 16 bits non signé indiquant le nombre de dimensions du tableau multidimensionnel.

**fFeatures**: un champ de bits de 16 bits. Les valeurs représentent les fonctionnalités définies par les applications de couche supérieure et doivent être ignorées.

**cbElements**: entier non signé 32 bits spécifiant la taille de chaque élément du tableau.

**Rgsabound**: tableau qui contient une structure SAFEARRAYBOUND, comme spécifié dans la section 2.2.1.1.1.4, par dimension dans le SAFEARRAY. Ce tableau a la dimension la plus à gauche et la dimension la plus à droite en dernier.

**vdata**: vecteur d’éléments marshalés d’un type particulier, indiqué par le VType du CBaseStorageVariant conteneur, avec le bit 0x2000 effacé.

vData est marshalé de la même façon \_ que le vecteur VT, comme spécifié dans la section 2.2.1.1.1.2, avec la différence selon laquelle le nombre d’éléments n’est pas stocké devant le vecteur. Au lieu de cela, le nombre d’éléments est calculé en multipliant la valeur cElements par toutes les limites de tableau sécurisées indiquées dans le champ Rgsabound. Les éléments sont stockés dans un vecteur dans l’ordre des dimensions, en commençant par la dimension la plus à droite.

Le diagramme suivant représente visuellement un exemple de tableau à deux dimensions. La première dimension a un cElements égal à 4 (représenté horizontalement) et lLbound égal à 0, et la deuxième dimension a cElements égal à 2 (représenté verticalement) et lLbound égal à 0.

:::row:::
    :::column:::
        0x00000001
    :::column-end:::
    :::column:::
        0x00000002
    :::column-end:::
    :::column:::
        0x00000003
    :::column-end:::
    :::column:::
        0x00000005
    :::column-end:::
:::row-end:::

:: Row :::
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

À l’aide du diagramme ci-dessus, vData contient la séquence suivante : 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (en commençant par parcourir la dimension la plus à droite, puis en incrémentant la dimension suivante). Le Rgsabound précédent (qui enregistre cElements et LBound) est : 0x00000004, 0x00000000, 0x00000002, 0x00000000.

### <a name="221114-safearraybound"></a>2.2.1.1.1.4 SAFEARRAYBOUND

La structure SAFEARRAYBOUND représente les limites d’une dimension d’un SAFEARRAY ou d’un SAFEARRAY2. Son format est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cElements

lLbound



 

**cElements**: entier non signé 32 bits spécifiant le nombre d’éléments dans la dimension.

**lLbound**: entier non signé 32 bits spécifiant la limite inférieure de la dimension.

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 est utilisé pour passer des tableaux multidimensionnels dans SERIALIZEDPROPERTYVALUE. La structure contient des informations sur les limites ainsi que les données.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

Rgsabound (variable)

vData (variable)



 

**cDims**: entier non signé 32 bits, indiquant le nombre de dimensions du SAFEARRAY2.

**Rgsabound**: tableau qui contient une structure SAFEARRAYBOUND, comme spécifié dans la section 2.2.1.1.1.4 par dimension dans le SAFEARRAY2. Ce tableau a la dimension la plus à gauche et la dimension la plus à droite en dernier.

**vdata**: vecteur d’éléments marshalés d’un type particulier, indiqué par le DWTYPE du SERIALIZEDPROPERTYVALUE conteneur, avec le bit 0x2000 effacé. Le format de vData est le même que celui spécifié pour le champ vData de SAFEARRAY dans la section 2.2.1.1.1.3.

### <a name="2212-cfullpropspec"></a>2.2.1.2 CFullPropSpec

La structure CFullPropSpec contient un GUID de jeu de propriétés et un identificateur de propriété pour identifier la propriété de manière unique.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_guidPropSet

...

...

...

ulKind

PrSpec

Nom de la propriété (variable)



 

**\_ GUIDPROPSET**: GUID du jeu de propriétés auquel appartient la propriété.

**ulKind**: entier non signé 32 bits. L’une des valeurs suivantes, qui indique le contenu de PrSpec.



| Valeur                                            | Signification                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| PRSPEC \_ LPWStr<br/> 0x00000000<br/> | Le champ PrSpec spécifie le nombre de caractères non NULL dans le champ nom de la propriété. |
| PRSPEC \_ propid<br/> 0x00000001<br/>  | Le champ PrSpec spécifie l’ID de propriété (PROPID).                                     |



 

**PrSpec**: entier non signé 32 bits avec une signification comme indiqué par le champ ulKind.

**Nom** de la propriété : si ulKind a la valeur PRSPEC \_ propId, ce champ ne doit pas être présent. Si ulKind a la valeur PRSPEC \_ LPWStr, ce champ doit contenir un tableau ne respectant pas la casse des caractères Unicode non null PRSPEC, contenant le nom de la propriété.

### <a name="2213-ccontentrestriction"></a>2.2.1.3 CContentRestriction

La structure CContentRestriction contient une chaîne à faire correspondre pour une propriété dans le cache de propriétés.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Property (variable)

...

Padding1 (variable)

Cc

\_pwcsPhrase (variable)

...

Padding2 (variable)

lcid

\_ulGenerateMethod



 

**\_ Property**: une structure CFullPropSpec, comme indiqué dans la section 2.2.1.2. Ce champ indique la propriété sur laquelle effectuer une opération de correspondance.

**Padding1**: ce champ doit avoir une longueur comprise entre 0 et 3 octets. La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure. Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire. Le contenu de ce champ doit être ignoré par le récepteur.

**CC**: entier non signé 32 bits, spécifiant le nombre de caractères dans le \_ champ pwcsPhrase.

**\_ pwcsPhrase**: chaîne Unicode qui se termine par un caractère non null représentant le mot ou l’expression à mettre en correspondance pour la propriété. Ce champ ne doit pas être vide. Le champ CC contient la longueur de la chaîne.

**Padding2**: ce champ doit avoir une longueur comprise entre 0 et 3 octets. La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure. Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire. Le contenu de ce champ doit être ignoré par le récepteur.

**LCID**: entier non signé 32 bits indiquant les paramètres régionaux de \_ pwcsPhrase, comme indiqué dans \[ MS-GPSI \] annexe A.

**\_ ulGenerateMethod**: entier non signé 32 bits, spécifiant la méthode à utiliser lors de la génération de formes de mots secondaires



| Valeur                                                       | Signification                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GÉNÉRATION \_ exacte de la méthode \_<br/> 0x00000000<br/>    | Correspondance exacte.                                                                                                                                                                                                                                                                                      |
| GÉNÉRER \_ le \_ préfixe de méthode<br/> 0x00000001 <br/>  | Correspondance du préfixe.                                                                                                                                                                                                                                                                                     |
| GENERATE, \_ méthode \_ INFLECT <br/> 0x00000002<br/> | Correspond aux fléchies d’un mot. Une inflexion d’un mot est une variante du mot racine dans la même partie de la parole qui a été modifiée selon les règles linguistiques d’une langue donnée. Par exemple, les formes fléchies du verbe « natation » en anglais incluent « natation », « natation », « natation » et « SWAM ». |



 

### <a name="2214-ckey"></a>2.2.1.4 CKey

La structure CKey contient une valeur de propriété.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PROPID

Libéré

buf (variable)



 

**Propid**: entier non signé 32 bits représentant l’ID de propriété comme indiqué dans la section 1.8.1. Les valeurs connues sont les suivantes :



| Valeur      | Signification                                                 |
|------------|---------------------------------------------------------|
| 0xFFFFFFFF | Représente un ID de propriété non valide et ne doit pas être utilisé. |
| 0xFFFFFFFE | Représente un ID de propriété non valide et ne doit pas être utilisé. |
| 0x00000000 | Représente un ID de propriété.                             |



 

**CB**: entier non signé 32 bits contenant la longueur de buf, en octets.

**buf**: séquence d’octets représentant la valeur de la propriété.

### <a name="2215-cinternalpropertyrestriction"></a>2.2.1.5 CInternalPropertyRestriction

La structure CInternalPropertyRestriction contient une valeur de propriété à associer à une opération.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_RelOp

\_ELECTRIQUE

\_prval (variable)

restrictionPresent

nextRestriction (variable)



 

**\_ RelOp**: entier 32 bits spécifiant la relation à exécuter sur la propriété. Il doit s’agir de l’une des valeurs suivantes :



| Valeur                 | Signification                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | Comparaison d’infériorité.                                                                                           |
| PRLE 0x00000001       | Comparaison d’infériorité ou d’égalité.                                                                               |
| PRGT 0x00000002       | Comparaison plus grande que.                                                                                        |
| PRGE 0x00000003       | Comparaison supérieur ou égal à.                                                                            |
| PREQ 0x00000004       | Comparaison d’égalité.                                                                                           |
| PRNE 0x00000005       | Comparaison inégale.                                                                                           |
| PRRE 0x00000006       | Comparaison d’expressions régulières.                                                                                  |
| PRAllBits 0x00000007  | Opérateur de bits AND qui retourne l’opérande de droite.                                                                     |
| PRSomeBits 0x00000008 | Opérateur de bits AND qui retourne une valeur différente de zéro.                                                                       |
| PRAll 0x00000100      | L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et n’a la valeur true que si l’opération a la valeur true pour toutes les lignes. |
| PRAny 0x00000200      | L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et a la valeur true si l’opération a la valeur true pour une ligne quelconque.       |



 

**\_ PID**: entier non signé 32 bits représentant l’ID de propriété (consultez PROPID dans la section 2.2.1.4).

**\_ Prval**: CBaseStorageVariant contenant la valeur à associer à la propriété.

**restrictionPresent**: valeur d’octet indiquant si le champ nextRestriction est présent. DOIT être défini sur 0x00 ou 0x01. Si cette valeur est définie sur 0x01, restrictionPresent indique que le champ nextRestriction est présent. Si la valeur est 0x00, restrictionPresent indique que le champ nextRestriction n’est pas présent.

**nextRestriction**: structure CRestriction, comme spécifié dans la section 2.2.1.16, en spécifiant une restriction supplémentaire.

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 CNatLanguageRestriction

La structure CNatLanguageRestriction contient une correspondance de **requête en langage naturel** pour une propriété.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Property (variable)

...

\_remplissage \_ de CC (variable)

Cc

\_pwcsPhrase (variable)

...

\_\_LCID de remplissage (variable)

Lcid



 

**\_ Property**: une structure CFullPropSpec, comme indiqué dans la section 2.2.1.3. Ce champ indique la propriété sur laquelle effectuer l’opération de correspondance.

**\_ remplissage de \_ CC**: ce champ doit avoir une longueur comprise entre 0 et 3 octets. La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure. Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire. Le contenu de ce champ doit être ignoré par le récepteur.

**CC**: entier non signé 32 bits. Nombre de caractères dans le \_ champ pwcsPhrase.

**\_ pwcsPhrase**: chaîne Unicode qui se termine par un caractère non null représentant le mot ou l’expression à mettre en correspondance pour la propriété. NE doit pas être vide. Le champ CC contient la longueur de la chaîne.

**\_ \_ LCID de remplissage**: ce champ doit avoir une longueur comprise entre 0 et 3 octets. La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure. Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire. Le contenu de ce champ doit être ignoré par le récepteur.

**LCID**: entier non signé 32 bits indiquant les paramètres régionaux de \_ pwcsPhrase, comme spécifié dans \[ MS-GPSI \] annexe A.

### <a name="2217-cnoderestriction"></a>2.2.1.7 CNodeRestriction

La structure CNodeRestriction contient un tableau de nœuds d' **arborescence de commandes** qui spécifient les restrictions pour la requête.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cNode

\_paNode (variable)



 

**\_ CNode**: entier non signé 32 bits spécifiant le nombre de structures CRestriction contenues dans le \_ champ paNode.

**\_ paNode**: tableau de structures CRestriction. Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient ce tableau. Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire. Le contenu des octets de remplissage doit être ignoré par le récepteur.

### <a name="2218-coccrestriction"></a>2.2.1.8 COccRestriction

La structure COccRestriction contient l’emplacement d’un mot dans une expression.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ETag

\_cPrevNoiseWords

\_cNextNoiseWords



 

**\_ ETag**: entier non signé 32 bits spécifiant le décalage du mot dans une chaîne de requête, en unités de mots. Un mot, tel qu’il est utilisé dans cette spécification, est une unité de langue dans tous les paramètres régionaux qui impliquent la signification.

**\_ cPrevNoiseWords**: entier non signé 32 bits contenant le nombre de **mots parasites** qui se produisent entre ce mot et le mot précédent dans l’expression.

**\_ cNextNoiseWords**: entier non signé 32 bits contenant le nombre de mots parasites qui se produisent entre ce mot et le mot suivant dans l’expression.

### <a name="2219-cpropertyrestriction"></a>2.2.1.9 CPropertyRestriction

La structure CPropertyRestriction contient une valeur de propriété à associer à une opération.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_RelOp

\_Property (variable)

\_prval (variable)



 

**\_ RelOp**: entier non signé 32 bits spécifiant la relation à exécuter sur la propriété. DOIT avoir l’une des valeurs suivantes.



| Valeur                 | Signification                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | Comparaison d’infériorité.                                                                                           |
| PRLE 0x00000001       | Comparaison d’infériorité ou d’égalité.                                                                               |
| PRGT 0x00000002       | Comparaison plus grande que.                                                                                        |
| PRGE 0x00000003       | Comparaison supérieur ou égal à.                                                                            |
| PREQ 0x00000004       | Comparaison d’égalité.                                                                                           |
| PRNE 0x00000005       | Comparaison inégale.                                                                                           |
| PRRE 0x00000006       | Comparaison d’expressions régulières.                                                                                  |
| PRAllBits 0x00000007  | Opérateur de bits AND qui retourne l’opérande de droite.                                                                     |
| PRSomeBits 0x00000008 | Opérateur de bits AND qui retourne une valeur différente de zéro.                                                                       |
| PRAll 0x00000100      | L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et n’a la valeur true que si l’opération a la valeur true pour toutes les lignes. |
| PRAny 0x00000200      | L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et a la valeur true si l’opération a la valeur true pour une ligne quelconque.       |



 

**\_ Propriété**: une structure CFullPropSpec, comme spécifié dans la section 2.2.1.2, indiquant la propriété sur laquelle effectuer une opération de correspondance.

**\_ prval**: structure CBaseStorageVariant, comme indiqué dans la section 2.2.1.1, contenant la valeur à associer à la propriété.

### <a name="22110-crangerestriction"></a>2.2.1.10 CRangeRestriction

La structure CRangeRestriction contient une restriction sur une plage de valeurs.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_keystart (variable)

\_keyEnd (variable)



 

**\_ keystart**: une structure CKey, comme spécifié dans la section 2.2.1.4, contenant le début de la plage.

**\_ keyEnd**: structure CKey contenant la fin de la plage.

### <a name="22111-cscoperestriction"></a>2.2.1.11 CScopeRestriction

La structure CScopeRestriction contient une restriction sur les fichiers à rechercher.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CcLowerPath

\_lowerPath (variable)

...

\_Padding (variable)

\_base

\_fRecursive

\_fVirtual



 

**CcLowerPath**: entier non signé 32 bits contenant le nombre de caractères Unicode dans le \_ champ lowerPath.

**\_ lowerPath**: chaîne Unicode qui se termine par un caractère non null qui représente le **chemin d’accès** auquel la requête doit être restreinte. Le champ CcLowerPath contient la longueur de la chaîne.

**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets. La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure. Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire. Le contenu de ce champ doit être ignoré par le récepteur.

**\_ Length**: entier non signé 32 bits contenant la longueur de \_ LowerPath, en caractères Unicode. Il doit s’agir de la même valeur que CcLowerPath.

**\_ fRecursive**: entier non signé 32 bits. DOIT être défini sur 0x00000001 ou 0x00000000. Si la valeur est définie sur 0x00000001, le serveur doit examiner de manière récursive tous les sous-répertoires du chemin d’accès. Si la valeur est 0x00000000, le serveur n’examine pas les sous-répertoires.

**\_ fVirtual**: entier non signé 32 bits. DOIT être défini sur 0x00000001 ou 0x00000000. Si la valeur est 0x00000001, \_ lowerPath est un chemin d’accès virtuel (le Uniform Resource Locator (URL) associé à un répertoire physique sur le système de fichiers) pour un site Web. Si la valeur est 0x00000000, \_ lowerPath est un chemin d’accès au système de fichiers.

### <a name="22112-csort"></a>2.2.1.12 CSort

La structure CSort identifie une colonne à trier.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

pidColumn

Valeur dwOrd

locale



 

**pidColumn**: entier non signé 32 bits. Numéro de la colonne par laquelle Trier.

**DWORD**: entier non signé 32 bits. DOIT avoir l’une des valeurs suivantes, en spécifiant comment trier en fonction de la colonne.



| Valeur                        | Signification                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| REQUÊTE \_ SORTASCEND 0x00000000 | Les lignes doivent être triées dans l’ordre croissant en fonction des valeurs de la colonne spécifiée.  |
| REQUÊTE \_ descendante 0x00000001    | Les lignes doivent être triées dans l’ordre décroissant en fonction des valeurs de la colonne spécifiée. |



 

**paramètres régionaux**: entier non signé 32 bits indiquant les paramètres régionaux, tels que spécifiés dans \[ MS-GPSI \] annexe A, de la colonne.

### <a name="22113-csynrestriction"></a>2.2.1.13 CSynRestriction

La structure CSynRestriction contient un mot ou ses synonymes pour une expression de requête.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Restriction

...

...

cKey

\_keyarray (variable)

\_isRange



 

**Restriction**: structure COccRestriction spécifiant l’emplacement du mot.

**CKEY**: entier non signé 32 bits spécifiant le nombre d’éléments dans le tableau de \_ tableaux de la matrice.

**\_ keyarray**: tableau de structures CKey spécifiant un mot et ses synonymes.

**\_ isRange**: si la valeur est 0x01, les clés sont des préfixes à faire correspondre. Si la valeur est 0x00, les clés sont des valeurs exactes à mettre en correspondance. \_isRange ne doit avoir aucune autre valeur.

### <a name="22114-cvectorrestriction"></a>2.2.1.14 CVectorRestriction

La structure CVectorRestriction contient une opération pondérée sur un nœud d’arborescence de commandes.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_PRES (variable)

...

\_Padding (variable)

\_ulRankMethod



 

**\_ pres**: arborescence de commandes CNodeRestriction sur laquelle un classement ou une opération doit être effectué.

**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets. La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure. Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire. Le contenu de ce champ doit être ignoré par le récepteur.

**\_ ulRankMethod**: entier non signé 32 bits spécifiant un algorithme de classement. DOIT être défini sur l’une des valeurs suivantes.



| Valeur                            | Signification                                       |
|----------------------------------|-----------------------------------------------|
| Rang de vecteur \_ \_ min 0x00000000     | Utilisez l’algorithme minimal \[ Salton \] .             |
| Nombre maximal de VECTEURs \_ \_ 0x00000001     | Utilisez le nombre maximal d’algorithmes \[ Salton \] .             |
| VECTOR de \_ classement \_ interne 0x00000002   | Utilisez l’algorithme de produit interne \[ Salton \] .       |
| \_0x00000003 de rang de vecteurs \_    | Utiliser l’algorithme de coefficient \[ Salton \] .    |
| Classement de vecteur \_ \_ Jaccard 0x00000004 | Utilisez l’algorithme de coefficient Jaccard \[ Salton \] . |



 

### <a name="22115-cwordrestriction"></a>2.2.1.15 CWordRestriction

La structure CWordRestriction contient un mot pour une expression de requête.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

restriction

...

...

\_clé (variable)

\_isRange



 

**restriction**: structure COccRestriction spécifiant l’emplacement du mot.

**\_ clé**: une structure CKey spécifiant un mot.

**\_ isRange**: si la valeur est 0x01, la clé est un préfixe à faire correspondre. Si la valeur est 0x00, la clé est une valeur exacte à mettre en correspondance. \_isRange ne doit pas être défini sur une autre valeur.

### <a name="22116-crestriction"></a>2.2.1.16 CRestriction

La structure CRestriction contient un nœud d’une arborescence de commandes de requête.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ulType

Poids

Restriction



 

**\_ ulType**: entier non signé 32 bits indiquant le type de restriction utilisé pour le nœud de l’arborescence de commandes. DOIT être défini sur l’une des valeurs suivantes.



| Valeur                    | Signification                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| RTNone 0x00000000        | Le nœud représente un mot parasite dans une requête de vecteur.                                         |
| RTAnd 0x00000001         | Le nœud contient un CNodeRestriction sur lequel une opération logique AND doit être effectuée. |
| RTOr 0x00000002          | Le nœud contient un CNodeRestriction sur lequel une opération OR logique doit être effectuée.  |
| RTNot 0x00000003         | Le nœud contient un CRestriction sur lequel une opération NOT doit être effectuée.             |
| RTContent 0x00000004     | Le nœud contient un CContentRestriction.                                                    |
| RTProperty 0x00000005    | Le nœud contient un CPropertyRestriction.                                                   |
| RTProximity 0x00000006   | Le nœud contient un CNodeRestriction sur lequel un classement de proximité doit être effectué,     |
| RTVector 0x00000007      | Le nœud contient un CVectorRestriction.                                                     |
| RTNatLanguage 0x00000008 | Le nœud contient un CNatLanguageRestriction.                                                |
| RTScope 0x00000009       | Le nœud contient un CScopeRestriction.                                                      |
| PRAny 0xFFFFFFFA         | Le nœud contient un CInternalPropertyRestriction.                                           |
| RTRange 0xFFFFFFFC       | Le nœud contient un CRangeRestriction.                                                      |
| RTPhrase 0xFFFFFFFD      | Le nœud contient un CNodeRestriction sur lequel une expression de correspondance doit être effectuée.          |
| RTSynonym 0xFFFFFFFE     | Le nœud contient un CSynRestriction.                                                        |
| RTWord 0xFFFFFFFF        | Le nœud contient un CWordRestriction.                                                       |



 

**Weight**: entier non signé 32 bits représentant le poids du nœud. Weight indique l’importance du nœud par rapport aux autres nœuds de l’arborescence de commandes de requête. Les valeurs de pondération supérieure sont plus importantes.

**Restriction**: type de restriction pour le nœud de l’arborescence de commandes. La syntaxe doit être la même que celle indiquée par le \_ champ ulType.

### <a name="22117-ccolumnset"></a>2.2.1.17 CColumnSet

La structure CColumnSet spécifie les numéros de colonne à retourner. Cette structure est toujours utilisée en référence à une structure CPidMapper spécifique (section 2.2.1.23).



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

index (variable)



 

**Count**: entier non signé 32 bits spécifiant le nombre d’éléments dans le tableau d’index.

**index**: tableau d’entiers non signés de 4 octets représentant les index de base zéro dans le tableau aPropSpec de la structure CPidMapper correspondante.

### <a name="22118-ccategorizationset"></a>2.2.1.18 CCategorizationSet

La structure CCategorizationSet contient des informations sur le regroupement d’un jeu de résultats de requête.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

catégories (variable)



 

**Count**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau des catégories.

**categories**: tableau de structures CCategorizationSpec spécifiant le regroupement de la requête.

### <a name="22119-ccategorizationspec"></a>2.2.1.19 CCategorizationSpec

La structure CCategorizationSpec contient un regroupement pour un jeu de résultats de requête.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_csColumns (variable)

\_ulCategType



 

**\_ csColumns**: structure CColumnSet indiquant les colonnes selon lesquelles regrouper la requête.

**\_ ulCategType**: entier non signé 32 bits. DOIT être défini sur 0x00000000.

### <a name="22120-cdbcolid"></a>2.2.1.20 CDbColId

La structure CDbColId contient une colonne.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

eKind

GUID

...

...

...

ulId

vString (variable)



 

**eKind**: doit être défini sur l’une des valeurs ci-dessous qui indique le contenu de GUID et vValue.



| Valeur                            | Signification                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| \_Nom GUID \_ 0x00000000 DBKIND    | vString contient un nom de propriété.                                                                               |
| \_GUID DBKIND \_ propid 0x00000001  | ulId contient un entier de 4 octets indiquant l’ID de propriété.                                                      |
| Nom de DBKIND \_ PGUID \_ 0x00000003   | vString contient un nom de propriété. Cette valeur doit être traitée de la même façon que le \_ nom GUID DBKIND \_ .                    |
| DBKIND \_ PGUID \_ propid 0x00000004 | ulId contient un entier de 4 octets indiquant l’ID de propriété. Cette valeur doit être identique à DBKIND \_ GUID \_ propid. |



 

**GUID**: le GUID de la propriété.

**ulId**: si EKIND est DBKIND \_ GUID \_ propid ou DBKIND \_ PGUID \_ propId, ce champ contient un entier non signé, en spécifiant l’ID de propriété. Si eKind est \_ \_ un nom GUID DBKIND ou \_ \_ un nom DBKIND PGUID, ce champ contient un entier non signé spécifiant le nombre de caractères Unicode contenus dans le champ vString.

**vString**: chaîne Unicode qui se termine par un caractère non null représentant le nom de la propriété. Elle doit être omise sauf si le champ eKind est défini sur DBKIND \_ GUID \_ Name ou DBKIND \_ PGUID \_ Name.

### <a name="22121-cdbprop"></a>2.2.1.21 CDbProp

La structure CDbProp contient une propriété.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

DBPROPID

DBPROPOPTIONS

DBPROPSTATUS

colid (variable)

vValue (variable)



 

**DBPROPID**: entier non signé 32 bits indiquant l’ID de propriété.

**DBPROPOPTIONS** : doit être défini sur 0x00000000.

**DBPROPSTATUS**: doit être défini sur 0x00000000.

**colid**: une structure CDbColId, comme indiqué dans la section 2.2.1.20, indiquant la colonne à laquelle la propriété s’applique.

**vValue**: CBaseStorageVariant contenant la valeur de la propriété.

### <a name="221211-properties"></a>Propriétés 2.2.1.21.1

Cette section détaille les propriétés utilisées par CISP. Ces propriétés sont regroupées en trois jeux de propriétés, ident 2.2.1.21.1 ified dans le champ guidPropertySet de la structure CDbPropSet (section 2.2.1.22).

Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés DBPROPSET FSCIFRMWRK \_ ext.



| Valeur                                  | Signification                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Nom de \_ catalogue ci DBPROP \_ 0x00000002   | Spécifie le nom du catalogue ou des catalogues à interroger. La valeur doit être un \_ LPWStr VT ou un \_ LPWStr VT Vector \| VT \_                                   |
| DBPROP \_ ci \_ inclut des \_ étendues 0x00000003 | Spécifie un ou plusieurs chemins d’accès à inclure dans la requête. La valeur doit être un \_ LPWStr VT ou un \_ LPWStr VT Vector \| VT \_ .                                 |
| Indicateurs d’étendue de l’élément de configuration DBPROP \_ \_ \_ 0x00000004    | Spécifie comment les chemins d’accès spécifiés par la \_ propriété DBPROP ci \_ include \_ scope doivent être traités. La valeur doit être un \_ I4 VT ou un \_ vecteur VT VT \| \_ I4. |
| DBPROP \_ \_ type de requête ci \_ 0x00000007     | Spécifie le type de requête. CDbColId doit être défini sur DB \_ NULLID.                                                                               |



 

Le tableau suivant répertorie les indicateurs pour la \_ propriété indicateurs d’étendue d’DBPROP ci \_ \_ :



| Valeur                     | Signification                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REQUÊTE \_ complète 0x01          | Si cette valeur est définie, cela indique que les fichiers dans le répertoire d’étendue et tous les sous-répertoires sont inclus dans les résultats. Si cette case est désactivée, seuls les fichiers du répertoire d’étendue sont inclus dans les résultats. NE doit pas être combiné avec une requête \_ profonde. |
| \_ \_ Chemin d’accès virtuel de requête 0x02 | S’il est défini, indique que l’étendue est un chemin d’accès virtuel. Si cette case est désactivée, cela indique que l’étendue est un répertoire physique.                                                                                                         |



 

Le tableau suivant répertorie les types de requêtes pour \_ la \_ propriété type de requête DBPROP ci \_ :



| Valeur                     | Signification                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| CiNormal 0x00000000       | Requête normale.                                                                                                   |
| CiVirtualRoots 0x00000001 | La requête demande une liste des racines virtuelles du catalogue. Cette valeur requiert des privilèges d’administrateur. |
| CiProperties 0x00000003   | La requête demande une liste de toutes les propriétés prises en charge par le service d’indexation.                            |
| CiAdminOp 0x00000004      | La requête est une opération d’administration. Cette valeur requiert des privilèges d’administrateur.                           |



 

Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés QUERYEXT DBPROPSET.



| Valeur                                      | Signification                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ USECONTENTINDEX 0x00000002         | Spécifie la manière dont le service d’indexation gère les requêtes lentes. La valeur doit être un \_ booléen VT. Si la valeur est TRUE, le serveur est autorisé à faire échouer ces requêtes.                                                                                    |
| DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003 | Indique si le service d’indexation doit effectuer la suppression des résultats. Si la valeur est TRUE, le serveur doit envisager d’effectuer une suppression des résultats de manière à optimiser le temps de réponse pour le client. La valeur doit être un \_ booléen VT.             |
| DBPROP \_ USEEXTENDEDDBTYPES 0x00000004      | Indique si le client prend en charge les \_ types de données vectorielles VT. Si la valeur est TRUE, le client prend en charge VT \_ Vector ; si la valeur est false, le serveur doit convertir les \_ types de données de Vector VT en \_ types de données de tableau VT.  La valeur doit être un \_ booléen VT. |
| DBPROP \_ FIRSTROWS 0x00000007               | Indique que les lignes correspondent à retourner. Si la valeur est TRUE, le serveur doit retourner le premier ensemble de lignes correspondantes. Si la valeur est FALSe, les lignes les plus pertinentes doivent être retournées. La valeur doit être un \_ booléen VT.                                             |



 

Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés DBPROPSET CIFRMWRKCORE \_ ext.



| Valeur/DBPROPID                 | Signification                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| \_Ordinateur DBPROP 0x00000002       | Spécifie le nom du ou des ordinateurs sur lesquels une requête doit être traitée. La valeur doit être VT \_ BSTR ou VT \_ array \| VT \_ BSTR. |
| DBPROP \_ client \_ CLSID 0x00000003 | Spécifie une constante de connexion pour le service d’indexation. La valeur doit être un \_ CLSID VT contenant 0x2A4880706FD911D0A80800A0C906241A.  |



 

### <a name="22122-cdbpropset"></a>2.2.1.22 CDbPropSet

La structure CDbPropSet contient un jeu de propriétés. Notez que le premier champ est de taille fixe, mais peut ne pas être aligné sur un décalage qui est un multiple de 4 octets à partir du début du message contenant cette structure. Toutefois, le champ cProperties est aligné en tant que tel, et le format est donc représenté comme suit :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

guidPropertySet

...

...

...

...

\_Padding (variable)

cProperties

aProps (variable)



 

**guidPropertySet**: GUID identifiant le jeu de propriétés. DOIT être défini sur la forme binaire correspondant à l’une des valeurs suivantes (affichées sous forme de représentation sous forme de chaîne), identifiant le jeu de propriétés des propriétés contenues dans le champ aProps.



| Valeur/GUID                                                                              | Nom                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET \_ FSCIFRMWRK \_ ext<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | Jeu de propriétés de l’infrastructure d’index de contenu du système de fichiers |
| DBPROPSET \_ QUERYEXT<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | Jeu de propriétés d’extension de requête                     |
| DBPROPSET \_ CIFRMWRKCORE \_ ext<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | Jeu de propriétés principales de l’infrastructure d’index de contenu        |



 

**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets. La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure. Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire. Le contenu de ce champ doit être ignoré par le récepteur.

**cProperties**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau aProps.

**aProps**: tableau de structures CDbProp, tel que spécifié dans la section 0, contenant les propriétés. Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient ce tableau. Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire. Le contenu des octets de remplissage doit être ignoré par le récepteur.

### <a name="22123-cpidmapper"></a>2.2.1.23 CPidMapper

La structure CPidMapper contient un tableau d’ID de propriété spécifiant les propriétés à retourner dans un ensemble de lignes.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

aPropSpec

... variable



 

**Count**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau aPropSpec.

**aPropSpec**: tableau de structures CFullPropSpec indiquant les propriétés à retourner. Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message. Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.

### <a name="22124-crowseekat"></a>2.2.1.24 CRowSeekAt

La structure CRowSeekAt contient le décalage à partir duquel récupérer des lignes dans un message CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cskip

\_bmkOffset



 

**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.

**\_ cskip**: entier non signé 32 bits contenant le nombre de lignes à ignorer dans l’ensemble de lignes.

**\_ bmkOffset**: valeur 32 bits représentant le handle du **signet** indiquant la position de départ à partir de laquelle ignorer le nombre de lignes spécifié dans \_ cskip, avant de commencer la récupération.

### <a name="22125-crowseekatratio"></a>2.2.1.25 CRowSeekAtRatio

La structure CRowSeekAtRatio identifie le point à partir duquel commencer la récupération d’un message CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_ulNumerator

\_ulDenominator



 

**CiTblChapt**: entier non signé 32 bits indiquant le chapitre de l’ensemble de lignes à partir duquel récupérer des lignes.

**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.

**\_ ulNumerator**: entier 32 bits non signé représentant le numérateur du rapport entre les lignes du chapitre et le début de la récupération.

**\_ ulDenominator**: entier 32 bits non signé représentant le dénominateur du rapport entre les lignes du chapitre et le début de la récupération. DOIT être supérieur à zéro.

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 CRowSeekByBookmark

La structure CRowSeekByBookmark identifie les signets à partir desquels commencer la récupération de lignes pour un message CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cBookmarks

\_maxRet

\_cValidRet

\_aBookmarks (variable)

\_ascRet (variable)



 

**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.

**\_ cBookmarks**: entier 32 bits non signé représentant le nombre d’éléments dans le \_ tableau aBookmarks.

**\_ maxRet**: entier 32 bits non signé représentant le nombre d’éléments dans le \_ tableau ascRet.

**\_ cValidRet**: entier non signé 32 bits représentant le nombre d’éléments dans le \_ tableau ascRet qui sont valides. Des éléments valides ont été définis dans le tableau, alors que les éléments non valides ne sont pas définis.

**\_ aBookmarks**: tableau de handles de signet (chacun représenté par 4 octets), obtenu à partir d’un message CPMGetRowsOut.

**\_ ascRet**: tableau de valeurs HRESULT. Lorsque le CRowSeekByBookMark est envoyé dans le cadre de la demande CPMGetRowsIn, le nombre d’entrées dans le tableau doit être égal à \_ cBookMarks. Lorsqu’il est envoyé par le client, les valeurs doivent être égales à zéro, et le serveur doit ignorer le contenu du tableau. Lorsqu’il est envoyé par le serveur (dans le cadre du message CPMGetRowsOut), les valeurs du tableau indiquent l’état du résultat pour chaque extraction de ligne.

### <a name="22127-crowseeknext"></a>2.2.1.27 CRowSeekNext

La structure CRowSeekNext contient le nombre de lignes à ignorer dans un message CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_cskip



 

**CiTblChapt**: entier 32 bits non signé spécifiant le chapitre de l’ensemble de lignes à partir duquel récupérer des lignes.

**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.

**\_ cskip**: entier 32 bits non signé représentant le nombre de lignes à ignorer dans l’ensemble de lignes.

### <a name="22128-crowsetproperties"></a>2.2.1.28 CRowsetProperties

La structure CRowsetProperties contient des informations de configuration pour une requête.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_uBooleanOptions

\_ulMaxOpenRows

\_ulMemoryUsage

\_cMaxResults

\_cCmdTimeout



 

**\_ uBooleanOptions**: les 3 bits les moins significatifs de ce champ doivent contenir l’une des trois valeurs suivantes :



| Valeur                  | Signification                                                             |
|------------------------|---------------------------------------------------------------------|
| eSequential 0x00000001 | Le curseur peut être déplacé uniquement vers l’avant.                              |
| eLocatable 0x00000003  | Le curseur peut être déplacé vers n’importe quelle position.                            |
| eScrollable 0x00000007 | Le curseur peut être déplacé vers n’importe quelle position et extraction dans n’importe quelle direction. |



 

Les bits restants peuvent être clairs ou définis sur une combinaison des valeurs suivantes logiquement ou ensemble :



| Valeur                     | Signification                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| eAsynchronous 0x00000008  | Le client n’attend pas la fin de l’exécution.                                                          |
| eFirstRows 0x00000080     | Retourne les premières lignes rencontrées, pas les meilleures correspondances.                                                    |
| eHoldRows 0x00000200      | Le serveur ne doit pas ignorer les lignes tant que le client n’est pas terminé par une requête.                                     |
| eChaptered 0x00000800     | L’ensemble de lignes prend en charge les chapitres.                                                                               |
| eUseCI 0x00001000         | Répondez uniquement à la requête à partir de l’index, et non du système de fichiers.                                                  |
| eDeferTrimming 0x00002000 | Le service d’indexation doit envisager d’optimiser le temps de réponse du client lors de la suppression des résultats. |



 

**\_ ulMaxOpenRows**: entier non signé 32 bits. Doit être défini sur 0x00000000. Non utilisé et doit être ignoré.

**\_ ulMemoryUsage**: entier non signé 32 bits. Doit être défini sur 0x00000000. Non utilisé et doit être ignoré.

**\_ cMaxResults**: entier non signé 32 bits spécifiant le nombre maximal de lignes à retourner pour la requête.

**\_ cCmdTimeout**: entier non signé 32 bits, qui spécifie le nombre de secondes au terme duquel une requête expire et se termine automatiquement, en comptant à partir du moment où la requête commence à s’exécuter sur le serveur. La valeur 0x00000000 signifie que la requête n’expire pas.

### <a name="22129-crowvariant"></a>2.2.1.29 CRowVariant

La structure CRowVariant contient la partie de taille fixe d’un type de données de longueur variable stockée dans le message CPMGetRowsOut.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

Reserved1

reserved2

Offset (facultatif)



 

**vType**: indicateur de type indiquant le type de vValue. Il doit s’agir de l’une des valeurs VARENUM spécifiées dans la section 2.2.1.1.

**Reserved1**: non utilisé. La valeur peut être définie sur n’importe quelle valeur arbitraire et doit être ignorée lors de la réception.

**Reserved2**: non utilisé. La valeur peut être définie sur n’importe quelle valeur arbitraire et doit être ignorée lors de la réception.

**Offset**: décalage des données de longueur variable (par exemple, une chaîne).  Il doit s’agir d’une valeur 32 bits (4 octets de long) si les décalages 32 bits sont utilisés (conformément aux règles de la section 2.2.3.16) ou d’une valeur de 64 octets (8 octets de long) si les décalages de 64 bits sont utilisés.

### <a name="22130-csortset"></a>2.2.1.30 CSortSet

La structure CSortSet contient l’ordre de tri de la requête.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Count

sortArray (variable)



 

**Count**: entier non signé 32 bits spécifiant le nombre d’éléments dans sortArray.

**sortArray**: tableau de structures CSort décrivant l’ordre dans lequel trier les résultats de la requête. Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message. Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.

### <a name="22131-ctablecolumn"></a>2.2.1.31 CTableColumn

La structure CTableColumn contient une colonne d’un message CPMSetBindingsIn



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PropSpec

... variable

vType

ValueUsed

\_padding1 (facultatif)

ValueOffset (facultatif)

Value (facultatif)

StatusUsed

\_padding2 (facultatif)

StatusOffset (facultatif)

LengthUsed

\_padding3 (facultatif)

LengthOffset (facultatif)



 

**PropSpec**: structure CFullPropSpec telle que spécifiée dans la section 2.2.1.3.

**vType**: spécifie le type de valeur de données contenu dans la colonne. Consultez le champ vType de la section 2.2.1.1 pour obtenir la liste des valeurs de ce champ.

**ValueUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00. Si la valeur est 0x01, la colonne est transférée dans la ligne de taille fixe. Si la valeur est 0x00, la valeur de la colonne est transférée dans la section de longueur variable à la fin de la mémoire tampon.

**\_ padding1**: un champ d’un octet qui doit être inséré avant ValueOffset si, sans lui, ValueOffset ne commence pas à un décalage pair à partir du début du message. La valeur de cet octet est arbitraire et doit être ignorée. Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.

**ValueOffset**: entier non signé de 2 octets spécifiant le décalage de la valeur de colonne dans la ligne. Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.

**Value**: entier non signé de 2 octets spécifiant la taille de la colonne en octets. Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.

**StatusUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00. Si la valeur est 0x01, l’état de la colonne est transféré dans la ligne. Si 0x00, l’état de la colonne n’est pas transféré dans la ligne.

**\_ padding2**: un champ d’un octet qui doit être inséré avant StatusOffset si, sans lui, le champ StatusOffset ne commence pas à un décalage pair à partir du début du message. La valeur de cet octet est arbitraire et doit être ignorée. Si StatusUsed a la valeur 0x00, ce champ ne doit pas être présent.

**StatusOffset**: entier non signé de 2 octets spécifiant le décalage de l’état de la colonne dans la ligne. Si StatusUsed a la valeur 0x00, ce champ ne doit pas être présent.

**LengthUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00. Si la valeur est 0x01, la longueur de la colonne est transférée dans la ligne. Si 0x00, la longueur de la colonne ne doit pas être transférée dans la ligne.

**\_ padding3**: un champ d’un octet qui doit être inséré avant LengthOffset si, sans lui, LengthOffset ne commence pas à un décalage pair à partir du début d’un message. La valeur de cet octet est arbitraire et doit être ignorée. Si LengthUsed a la valeur 0x00, ce champ ne doit pas être présent.

**LengthOffset**: entier non signé de 2 octets spécifiant le décalage de la longueur de colonne dans la ligne. Si LengthUsed a la valeur 0x00, ce champ ne doit pas être présent.

### <a name="22132-serializedpropertyvalue"></a>2.2.1.32 SERIALIZEDPROPERTYVALUE

La structure SERIALIZEDPROPERTYVALUE contient une valeur sérialisée.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

dwType

RGB (variable)



 

**dwType**: l’un des types variant, défini dans la section 2.2.1.1, qui peut être combiné avec des modificateurs de type Variant. Pour tous les types variant, à l’exception de ceux associés à VT \_ Array, SERIALIZEDPROPERTYVALUE a la même disposition que CBaseStorageVariant, comme indiqué dans la section 2.2.1.1. Si le type Variant est combiné avec le \_ modificateur de type tableau VT, SAFEARRAY2, spécifié dans la section 2.2.1.2.1.1, est utilisé à la place de SAFEARRAY dans le champ vValue de CBaseStorageVariant.

**RGB**: valeur sérialisée. Consultez les détails de la sérialisation pour vValue dans 2.2.1.1.

### <a name="222-message-headers"></a>2.2.2 en-têtes de message

Tous les messages du protocole de service d’indexation de contenu ont un en-tête de 16 octets.

Vous trouverez ci-dessous un diagramme montrant le format d’en-tête de message du protocole du service d’indexation de contenu.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_fragment

\_statu

\_ulChecksum

\_ulReserved2



 

\_**MSG**: entier 32 bits qui identifie le type de message suivant l’en-tête. Le tableau suivant répertorie les messages du protocole du service d’indexation de contenu et les valeurs entières spécifiées pour chaque message. Comme indiqué dans le tableau, certaines valeurs identifient 2 messages dans la table. Dans ces instances, le message qui suit l’en-tête peut être identifié par la direction du message. Si la direction est client à serveur, le message avec « in » ajouté au nom du message est indiqué. Si la direction est de serveur à client, le message « out » ajouté au nom du message est indiqué.



| Valeur      | Signification                                                     |
|------------|-------------------------------------------------------------|
| 0x000000C8 | CPMConnectIn ou CPMConnectOut                               |
| 0x000000C9 | CPMDisconnect                                               |
| 0x000000CA | CPMCreateQueryIn ou CPMCreateQueryOut                       |
| 0x000000CB | CPMFreeCursorIn ou CPMFreeCursorOut                         |
| 0x000000CC | CPMGetRowsIn ou CPMGetRowsOut                               |
| 0x000000CD | CPMRatioFinishedIn ou CPMRatioFinishedOut                   |
| 0x000000CE | CPMCompareBmkIn ou CPMCompareBmkOut                         |
| 0x000000CF | CPMGetApproximatePositionIn ou CPMGetApproximatePositionOut |
| 0x000000D0 | CPMSetBindingsIn                                            |
| Stop | CPMGetNotify                                                |
| 0x000000D2 | CPMSendNotifyOut                                            |
| 0x000000D7 | CPMGetQueryStatusIn ou CPMGetQueryStatusOut                 |
| 0x000000D9 | CPMCiStateInOut                                             |
| 0x000000E1 | CPMForceMergeIn                                             |
| 0x000000E4 | CPMFetchValueIn ou CPMFetchValueOut                         |
| 0x000000E6 | CPMUpdateDocumentsIn                                        |
| 0x000000E7 | CPMGetQueryStatusExIn ou PMGetQueryStatusExOut              |
| 0x000000E8 | CPMRestartPositionIn                                        |
| 0x000000E9 | CPMStopAsynchIn                                             |
| 0x000000EC | CPMSetCatStateIn ou CPMSetCatStateOut                       |



 

\_**État**: HRESULT \[ ms-sys \] , indiquant l’état de l’opération demandée.

\* *

*Windows Comportement : le client définit toujours le \_ champ d’État sur 0x00000000.*

**\_ ulChecksum**: le \_ ulChecksum doit être calculé comme indiqué dans la section 3.2.4 pour les messages suivants :

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMSetBindingsIn
-   CPMGetRowsIn
-   CPMFetchValueIn

Pour tous les autres messages, \_ ULCHECKSUM doit avoir la valeur 0x00000000. Un client doit ignorer le \_ champ ulChecksum.

**\_ ulReserved2**: doit être défini sur 0 et ignoré par le récepteur.

### <a name="223-messages"></a>2.2.3 messages

### <a name="2231-cpmcistateinout"></a>2.2.3.1 CPMCiStateInOut

Le message CPMCiStateInOut contient des informations sur l’état du service d’indexation. Le format du message CPMCiStateInOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbStruct

cWordList

cPersistentIndex

cQueries

cDocuments

cFreshTest

dwMergeProgress

Immobilier

cFilteredDocuments

cTotalDocuments

cPendingScans

dwIndexSize

cUniqueKeys

cSecQDocuments

dwPropCacheSize



 

**cbStruct**: entier non signé 32 bits. Taille en octets de ce message (à l’exception de l’en-tête commun). DOIT être défini sur 0x0000003C.

**cWordList**: entier non signé 32 bits indiquant le nombre d’index initiaux créés pour les documents récemment indexés.

**cPersistentIndex**: entier non signé 32 bits indiquant le nombre d’index persistants.

**cQueries**: entier non signé 32 bits indiquant un certain nombre de requêtes en cours d’exécution.

**cDocuments**: entier non signé 32 bits indiquant le nombre total de documents en attente d’indexation.

**cFreshTest**: entier non signé 32 bits indiquant le nombre de documents uniques avec les informations des index qui ne sont pas entièrement optimisés pour les performances.

**dwMergeProgress**: entier 32 bits non signé spécifiant le pourcentage d’achèvement de l’optimisation complète actuelle des index, si l’optimisation est actuellement en cours. DOIT être inférieur ou égal à 100.

**patrimoine**: état de l’indexation du contenu comme indiqué par une ou plusieurs des \_ constantes d’état ci \_ \* définies dans le tableau ci-dessous.



| Valeur                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| État de l’instantané de l' \_ état ci \_ \_ 0x00000001           | Le service d’indexation est en train d’optimiser certains des index afin de réduire l’utilisation de la mémoire et d’améliorer les performances des requêtes.                                                                                                                                                                                                                                                                                                                                                                |
| \_Fusion du maître d’état ci \_ \_ 0x00000002           | Le service d’indexation est en cours d’optimisation complète pour tous les index.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Analyse du contenu de l' \_ état ci \_ \_ \_ requise 0x00000004 | Certains documents de l’index ont changé et le service d’indexation doit déterminer ceux qui ont été ajoutés, modifiés ou supprimés.                                                                                                                                                                                                                                                                                                                                                              |
| État de l' \_ \_ opération de fusion recuite d’état ci \_        | Le service d’indexation est en train d’optimiser les index afin de réduire l’utilisation de la mémoire et d’améliorer les performances des requêtes. Ce processus est plus complet que celui identifié par la valeur de \_ fusion de cliché instantané d’état ci \_ \_ , mais il n’est pas aussi complet que spécifié par la \_ valeur de fusion du maître d’état ci \_ \_ . Ces optimisations sont spécifiques à l’implémentation, car elles dépendent de la façon dont les données sont stockées en interne. les optimisations n’affectent pas le protocole de la même façon que le temps de réponse. |
| \_Analyse d’état ci \_ 0x00000010                | Le service d’indexation examine un répertoire ou un ensemble de répertoires pour déterminer si des fichiers ont été ajoutés, supprimés ou mis à jour depuis la dernière indexation du répertoire.                                                                                                                                                                                                                                                                                                                 |
| RÉCUPÉRATION de l’état de l’élément de configuration \_ \_ 0x00000020              | Le service démarre à partir du dernier état enregistré et est en cours de récupération.                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_ \_ Mémoire insuffisante de l’état ci \_ 0x00000080             | La majeure partie de la mémoire virtuelle du serveur est en cours d’utilisation.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_ \_ \_ 0x00000100 e/s haute d’état de l’élément de configuration                | Le niveau d’activité d’entrée/sortie (e/s) sur le serveur est relativement élevé.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 0x00000200 de la \_ fusion principale de l’état ci \_ \_ \_ suspendu   | Le processus d’optimisation complète de tous les index en cours a été suspendu. Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.                                                                                                                                                                                                                                                                                                                                  |
| État de l’élément de configuration \_ \_ en lecture \_ seule 0x00000400              | La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue. Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.                                                                                                                                                                                                                                                                                                                               |
| \_0x00000800 de \_ batterie \_ d’état de l’élément de configuration          | La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue pour économiser la durée de vie de la batterie, tout en répondant aux requêtes. Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.                                                                                                                                                                                                                                                                 |
| État de l' \_ \_ utilisateur \_ actif 0x00001000            | La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue en raison d’une activité élevée par l’utilisateur (clavier ou souris), mais elle répond toujours aux requêtes. Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.                                                                                                                                                                                                                                         |
| État de l’élément de configuration à \_ \_ partir de 0x00002000                | Le service est en cours de démarrage. Les requêtes peuvent être exécutées, mais l’analyse et la notification n’ont pas encore été activées. Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.                                                                                                                                                                                                                                                                                                                   |
| État de l’élément de configuration \_ \_ \_ USN lecture USN 0x00004000           | Le service n’a pas lu le journal conservé par le système de fichiers pour effectuer le suivi des modifications apportées aux fichiers ou aux répertoires d’un volume, de sorte que l’index ne soit peut-être pas à jour.                                                                                                                                                                                                                                                                                                                                  |



 

**cFilteredDocuments**: entier non signé 32 bits indiquant le nombre de documents indexés depuis le début de l’indexation du contenu.

**cTotalDocuments**: entier non signé 32 bits indiquant le nombre total de documents dans le système.

**cPendingScans**: entier non signé 32 bits indiquant le nombre d’opérations d’indexation de haut niveau en attente. La signification de cette valeur est spécifique au fournisseur, mais des nombres plus élevés sont supposés indiquer qu’un plus grand nombre d’index est conservé.

*comportement de Windows*: cette valeur est généralement zéro, sauf immédiatement après le démarrage de l’indexation ou après un dépassement de la file d’attente de notification.

**dwIndexSize**: entier non signé 32 bits indiquant la taille, en mégaoctets, de l’index (à l’exception du cache de propriété).

**cUniqueKeys**: entier non signé 32 bits indiquant le nombre approximatif de clés uniques dans le catalogue.

**cSecQDocuments**: entier non signé 32 bits indiquant le nombre de documents que le service d’indexation réessaiera d’indexer en raison d’un échec lors de la tentative d’indexation initiale.

**dwPropCacheSize**: entier non signé 32 bits indiquant la taille, en mégaoctets, du cache de propriétés.

### <a name="2232-cpmsetcatstatein"></a>2.2.3.2 CPMSetCatStateIn

Le message CPMSetCatStateIn définit l’état d’un catalogue. Le format du message CPMSetCatStateIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID

\_dwNewState

\_CatName (variable, facultative)



 

**\_ partid**: doit avoir la valeur 0x00000001.

**\_ dwNewState**: doit être défini sur l’une des valeurs suivantes, indiquant le nouvel État du catalogue.



| Valeur                         | Signification                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CICAT \_ arrêté 0x00000001     | Le catalogue est arrêté. Cet État signifie qu’aucun nouveau fichier ne doit être indexé et qu’aucune requête de recherche ne doit être traitée.                                                     |
| CICAT \_ ReadOnly 0x00000002    | Le catalogue est en lecture seule. Aucun nouveau fichier ne doit être indexé.                                                                                                               |
| CICAT, en \_ écriture, 0x00000004    | Le catalogue est accessible en écriture. Les nouveaux fichiers peuvent être indexés et les requêtes de recherche doivent être traitées.                                                                              |
| CICAT \_ pas de \_ requête 0x00000008   | Le catalogue n’est pas disponible pour l’interrogation.                                                                                                                              |
| CICAT \_ obtient l' \_ État 0x00000010  | L’état du catalogue ne doit pas être modifié, récupéré uniquement.                                                                                                          |
| CICAT \_ tous les \_ 0x00000020 ouverts | Une vérification pour voir si tous les catalogues ont été démarrés. Si c’est le cas, le \_ champ dwOldState envoyé dans le CPMSetCatStateOut répondre à ce message est signalé comme étant différent de zéro. |



 

**\_ CatName**: nom du catalogue dont l’État doit être modifié. Le nom doit être une chaîne Unicode terminée par le caractère null. Ce champ doit être omis si \_ dwNewState a la valeur CICAT \_ All \_ Opened.

### <a name="2233-cpmsetcatstateout"></a>2.2.3.3 CPMSetCatStateOut

Le message CPMSetCatStateOut est une réponse à un message CPMSetCatStateIn avec l’ancien état du catalogue. Le format du message CPMSetCatStateOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwOldState



 

**\_ dwOldState**: l’une des valeurs suivantes, indiquant l’ancien état du catalogue.



| Valeur                       | Signification                                    |
|-----------------------------|--------------------------------------------|
| CICAT \_ arrêté 0x00000001   | Le catalogue est arrêté.                    |
| CICAT \_ ReadOnly 0x00000002  | Le catalogue est en lecture seule.                  |
| CICAT, en \_ écriture, 0x00000004  | Le catalogue est accessible en écriture.                   |
| CICAT \_ pas de \_ requête 0x00000008 | Le catalogue n’est pas disponible pour l’interrogation. |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 CPMUpdateDocumentsIn

Le message CPMUpdateDocumentsIn indique au serveur d’indexer le chemin d’accès spécifié.

Le serveur répondra avec l’en-tête de message du message CPMUpdateDocumentsOut, avec les résultats de la requête contenus dans le \_ champ État de l’en-tête de message.

Le format du message CPMUpdateDocumentsIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_indicateur (facultatif)

\_fRootPath (facultatif)

RootPath (variable, facultative)



 

**\_ indicateur**: type de mise à jour à effectuer. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur. Ce champ doit être défini sur l’une des valeurs suivantes :



| Valeur                  | Signification                                   |
|------------------------|-------------------------------------------|
| UPD \_ INCREM 0x00000000 | Une mise à jour incrémentielle doit être effectuée. |
| UPD \_ complet 0x00000001   | Une mise à jour complète doit être effectuée.         |
| UPD \_ init 0x00000002   | Une nouvelle initialisation doit être effectuée.  |



 

**\_ fRootPath**: valeur booléenne indiquant si le champ RootPath spécifie un chemin d’accès sur lequel effectuer la mise à jour. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur. Ce champ doit avoir la valeur 0x00000001 ou 0x00000000. Si la valeur est définie sur 0x00000001, un chemin d’accès sur lequel effectuer la mise à jour est inclus dans RootPath. Si la valeur est 0x00000000, la mise à jour doit être effectuée sur tous les chemins d’accès indexés.

**RootPath**: nom du chemin d’accès à mettre à jour. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur. Le nom doit être une chaîne Unicode terminée par le caractère null. Ce champ doit être omis si \_ fRootPath a la valeur 0x00000000.

### <a name="2235-cpmforcemergein"></a>2.2.3.5 CPMForceMergeIn

Le message CPMForceMergeIn demande à un serveur d’effectuer les opérations de maintenance nécessaires pour améliorer les performances des requêtes. Le serveur répondra avec l’en-tête du message CPMForceMergeIn, avec les résultats de la requête contenus dans le \_ champ État.

Le format du message CPMForceMergeIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partId (facultatif)



 

**\_ partid**: ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur. Quand ce champ est présent, il doit avoir la valeur 0x00000001.

### <a name="2236-cpmconnectin"></a>2.2.3.6 CPMConnectIn

Le message CPMConnectIn commence une session entre le client et le serveur.

Le format du message CPMConnectIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_iClientVersion

\_fClientIsRemote

\_cbBlob1

\_cbBlob2

\_remplissage

...

...

MachineName

... variable

UserName

... variable

\_paddingcPropSets (facultatif, variable)

cPropSets

PropertySet1 (variable)

PropertySet2 (variable)

\_paddingExtPropset (facultatif, variable)

cExtPropSet

aPropertySets (variable)



 

**\_ iClientVersion**: entier 32 bits qui indique si le serveur doit valider la valeur de somme de contrôle spécifiée dans le \_ champ ulChecksum des en-têtes de message pour les messages envoyés par le client. Si le \_ champ iClientVersion est défini sur 0x00000008 ou une version ultérieure, le serveur doit valider la \_ valeur du champ ulChecksum pour les messages suivants :

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMFetchValueIn
-   CPMGetRowsIn
-   CPMSetBindingsIn

Pour plus d’informations sur la façon dont le serveur valide la valeur spécifiée par le client dans le champ ulChecksum pour les messages listés ci-dessus, consultez la section 3.2.5.

Si la valeur est supérieure à 0x00000008, le client est supposé être en charge de la gestion des décalages 64 bits dans les messages CPMGetRowsOut. Pour plus d’informations, consultez la section 2.2.3.16.

*Windows comportement : sur les clients Windows, iClientVersion est défini comme suit*:



| Valeur      | Signification                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | le système d’exploitation Client est Windows 2000.                                           |
| 0x00000008 | le système d’exploitation Client est 32 bits Windows XP ou 32 bits Windows Server 2003. |
| 0x00010008 | le système d’exploitation Client est 64 bits Windows XP ou 64 bits Windows Server 2003. |



 

\_**fClientIsRemote**: valeur booléenne indiquant si le client s’exécute sur un ordinateur différent du serveur. DOIT être défini sur 0x00000001.

\_**cbBlob1**: entier non signé 32 bits indiquant la taille en octets des champs CPropSet, PropertySet1 et PropertySet2, combinée.

\_**cbBlob2**: entier non signé 32 bits indiquant la taille en octets des champs CExPropSet et aPropertySet, combinée.

\_**remplissage**: 12 octets de remplissage qui peuvent contenir des valeurs arbitraires et doivent être ignorés.

**MachineName**: nom de l’ordinateur du client. La chaîne de nom doit être un tableau de moins de 512 caractères Unicode se terminant par un caractère null, y compris la marque de fin NULL.

**Username**: chaîne qui représente le nom d’utilisateur de la personne qui exécute l’application qui a appelé ce protocole. La chaîne de nom doit être un tableau de moins de 512 caractères Unicode se terminant par un caractère null en cas de concaténation avec MachineName.

**\_ paddingcPropSets**: ce champ doit avoir une longueur de 0 à 7 octets. Le nombre d’octets doit être le nombre requis pour que l’offset d’octet du champ cPropSets à partir du début du message qui contient cette structure soit un multiple de 8. La valeur des octets peut être n’importe quelle valeur arbitraire et doit être ignorée par le récepteur.

**cPropSets**: entier non signé 32 bits indiquant le nombre de structures CDbPropSet qui suivent ce champ. Cette valeur doit être définie sur 0x0000002.

**PropertySet1**: structure CDbPropSet avec GUIDPROPERTYSET contenant DBPROPSET \_ FSCIFRMWRK \_ ext (voir la section 2.2.1.22).

**PropertySet2**: structure CDbPropSet avec GUIDPROPERTYSET contenant DBPROPSET \_ CIFRMWRKCORE \_ ext (voir la section 2.2.1.22).

\_**PaddingExtPropset**: ce champ doit avoir une longueur de 0 à 7 octets. Le nombre d’octets doit être le nombre requis pour que l’offset d’octet du champ cExtPropSets à partir du début du message qui contient cette structure soit un multiple de 8. La valeur des octets peut être n’importe quelle valeur arbitraire et doit être ignorée par le récepteur.

**cExtPropSet**: entier non signé 32 bits indiquant le nombre de structures CDbPropSet qui suivent ce champ.

**aPropertySets**: tableau de structures CDbPropSet spécifiant d’autres propriétés. Le nombre d’éléments de ce tableau doit être égal à cExtPropSet.

### <a name="2237-cpmconnectout"></a>2.2.3.7 CPMConnectOut

Le message CPMConnectOut contient une réponse à un message CPMConnectIn.

Le format du message CPMConnectOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_serverVersion

\_réservé (variable)



 

**\_ ServerVersion**:

Entier 32 bits, indiquant si le serveur peut prendre en charge les décalages 64 bits *.* Pour plus d’informations, consultez la section 2.2.3.16.



| Valeur      | Signification                                 |
|------------|-----------------------------------------|
| 0x00000007 | Le serveur peut uniquement envoyer des décalages 32 bits. |
| 0x00010007 | Le serveur peut envoyer des décalages 32 ou 64 bits.   |



 

**\_ réservé**: réservé. Le serveur peut envoyer un nombre arbitraire de valeurs arbitraires et le client doit ignorer ces valeurs, le cas échéant.

### <a name="2238-cpmcreatequeryin"></a>2.2.3.8 CPMCreateQueryIn

Le message CPMCreateQueryIn crée une nouvelle requête. Le format du message CPMCreateQueryIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Taille

CColumnSetPresent

ColumnSet (facultatif)

... variable

CRestrictionPresent.

Restriction (facultatif)

... variable

CSortSetPresent

SortSet (facultatif)

... variable

CCategorizationSetPresent

CategorizationSet (facultatif)

... variable

RowSetProperties

...

...

...

...

PidMapper (variable)



 

**Size**: entier non signé 32 bits indiquant le nombre d’octets entre le début de ce champ et la fin du message.

**CColumnSetPresent**: champ d’octets indiquant si le champ ColumnSet est présent. Ce champ doit être défini sur 0x01 ou 0x00. Si la valeur est définie sur 0x01, le champ CColumnSet doit être présent. Si la valeur est 0x00, elle doit être absente.

**ColumnSet**: structure CColumnSet contenant les numéros de colonne dans lesquels les propriétés de CPidMapper doivent être retournées.

**CRestrictionPresent**: champ d’octets indiquant si le champ de restriction est présent. Si vous définissez une valeur différente de zéro, le champ de restriction doit être présent. Si la valeur est 0x00, la restriction doit être absente.

**Restriction**: structure CRestriction contenant l’arborescence de commandes de la requête.

**CSortSetPresent**: champ d’octets indiquant si le champ SortSet est présent. Si vous définissez une valeur différente de zéro, le champ SortSet doit être présent. Si la valeur est 0x00, SortSet doit être absent.

**SortSet**: structure CSortSet indiquant l’ordre de tri de la requête.

**CCategorizationSetPresent**: champ d’octets indiquant si le champ CCategorizationSet est présent. Si vous définissez une valeur différente de zéro, le champ CCategorizationSet doit être présent. Si la valeur est 0x00, CCategorizationSet doit être absent.

**CCategorizationSet**: structure CCategorizationSet qui contient les groupes de la requête.

**RowSetProperties**: structure CRowsetProperties fournissant des informations de configuration pour la requête.

**PidMapper**: structure CPidMapper contenant les propriétés à retourner dans un ensemble de lignes.

### <a name="2239-cpmcreatequeryout"></a>2.2.3.9 CPMCreateQueryOut

Le message CPMCreateQueryOut contient une réponse à un message CPMCreateQueryIn.

Le format du message CPMCreateQueryOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_fTrueSequential

\_fWorkIdUnique

aCursors



 

**\_ fTrueSequential**: valeur booléenne informatif indiquant si la requête peut être supposée fournir des résultats plus rapidement. Lorsqu’il est défini sur 0x00000001 pour la requête fournie dans CPMCreateQueryIn, le serveur peut utiliser l’index de telle sorte que les résultats de la requête seront probablement remis plus rapidement. Lorsque la valeur est 0x00000000, il y a une latence plus importante dans la transmission des résultats de la requête. Ne doit pas être défini sur une autre valeur.

**\_ fWorkIdUnique**: valeur booléenne indiquant si les identificateurs de document pointés par les curseurs sont uniques dans tous les résultats de la requête. Si la valeur est 0x00000001, les identificateurs sont uniques. Si la valeur est 0x00000000, elles sont uniques uniquement dans l’ensemble de lignes.

**aCursors**: tableau d’entiers non signés 32 bits représentant les handles des curseurs, avec le nombre d’éléments égal au nombre de catégories dans le champ CategorizationSet du message CPMCreateQueryIn.

### <a name="22310-cpmgetquerystatusin"></a>2.2.3.10 CPMGetQueryStatusIn

Le message CPMGetQueryStatusIn demande l’état d’une requête. Le format du message CPMGetQueryStatusIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor**: entier non signé 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les informations d’État doivent être récupérées.

### <a name="22311-cpmgetquerystatusout"></a>2.2.3.11 CPMGetQueryStatusOut

Le message CPMGetQueryStatusOut répond à un message CPMGetQueryStatusIn avec l’état de la requête. Le format du message CPMGetQueryStatusOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Statut



 

**\_ État**: masque de sous-masque des valeurs définies dans les tableaux ci-dessous, qui décrit la requête.

Le tableau suivant répertorie les \_ \* valeurs stat obtenues en effectuant une opération and au niveau du bit sur \_ Status avec 0x00000007. Le résultat doit être l’un des suivants :



| Constante                 | Signification                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| STAT \_ occupées 0x00000000    | La requête asynchrone est toujours en cours d’exécution.                                          |
| \_Erreur stat 0x00000001   | La requête est dans un état d’erreur.                                                   |
| STATISTIQUES \_ terminées 0x00000002    | La requête est terminée.                                                            |
| STATISTIQUES d' \_ actualisation 0x00000003 | La requête est terminée, mais les mises à jour entraînent des calculs de requête supplémentaires. |



 

Le tableau suivant répertorie les bits STAT supplémentaires \_ \* qui peuvent être définis indépendamment.



| Constante                                    | Signification                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| \_Mots parasites statistiques \_ 0x00000010               | Les mots parasites ont été remplacés par des caractères génériques dans la requête de contenu.                                                              |
| \_Contenu stat \_ obsolète \_ \_     | Les résultats de la requête sont peut-être incorrects, car la requête impliquait des fichiers modifiés, mais non indexés.                             |
| Actualisation des statistiques \_ \_ 0x00000040 incomplète        | Les résultats de la requête sont peut-être incorrects, car la requête impliquait la modification et la réindexation des fichiers dont le contenu n’était pas inclus. |
| \_Requête de contenu stat \_ \_ incomplète 0x00000080 | La requête de contenu était trop complexe pour être exécutée ou une énumération requise au lieu d’utiliser l’index de contenu.                          |
| Limite de durée des statistiques \_ \_ \_ dépassée 0x00000100      | Les résultats de la requête sont peut-être incorrects, car la durée d’exécution de la requête a atteint le délai maximal autorisé.                    |



 

### <a name="22312-cpmgetquerystatusexin"></a>2.2.3.12 CPMGetQueryStatusExIn

Le message CPMGetQueryStatusExIn demande l’état d’une requête et des informations supplémentaires, telles que le nombre de documents qui ont été indexés, le nombre de documents restant à indexer, etc. Le format du message CPMGetQueryStatusExIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_bmk



 

**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les informations d’État doivent être récupérées.

**\_ BMK**: valeur 32 bits indiquant le descripteur d’un signet dont la position doit être récupérée.

### <a name="22313-cpmgetquerystatusexout"></a>2.2.3.13 CPMGetQueryStatusExOut

Le message CPMGetQueryStatusExOut répond à un message CPMGetQueryStatusExIn avec l’état de la requête et d’autres informations d’État, comme indiqué dans le diagramme ci-dessous. Le format du message CPMGetQueryStatusExOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Statut

\_cFilteredDocuments

\_cDocumentsToFilter

\_dwRatioFinishedDenominator

\_dwRatioFinishedNumerator

\_iRowBmk

\_cRowsTotal



 

**\_ État**: l’une des statistiques \_ \* valeurs spécifiées dans la section 2.2.3.11.

**\_ cFilteredDocuments**: entier non signé 32 bits indiquant le nombre de documents qui ont été indexés

**\_ cDocumentsToFilter**: entier non signé 32 bits indiquant le nombre de documents restant à indexer.

**\_ dwRatioFinishedDenominator**: entier non signé 32 bits indiquant le dénominateur du rapport de documents dont la requête a terminé le traitement.

**\_ dwRatioFinishedNumerator**: entier non signé 32 bits indiquant le numérateur du rapport de documents dont la requête a terminé le traitement.

**\_ iRowBmk**: entier non signé 32 bits indiquant la position approximative du signet dans l’ensemble de lignes en termes de lignes.

**\_ cRowsTotal**: entier non signé 32 bits spécifiant le nombre total de lignes dans l’ensemble de lignes.

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 CPMSetBindingsIn

Le message CPMSetBindingsIn demande la liaison de colonnes à un ensemble de lignes. Le serveur répond au message de requête CPMSetBindingsIn à l’aide de la section d’en-tête du message CPMBindingsIn avec les résultats de la requête contenue dans le \_ champ État. Le format du message CPMSetBindingsIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (facultatif)

\_cbRow (facultatif)

\_cbBindingDesc (facultatif)

\_factice (facultatif)

cColumns (facultatif)

aColumns (variable, facultative)



 

**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut qui identifie la ligne pour laquelle définir des liaisons. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.

**\_ cbRow**: entier non signé 32 bits indiquant la taille, en octets, d’une ligne. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.

**\_ cbBindingDesc**: entier non signé 32 bits indiquant la longueur, en octets, des champs qui suivent le \_ champ factice. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.

**\_ factice**: ce champ n’est pas utilisé et doit être ignoré. Il peut être défini sur n’importe quelle valeur arbitraire. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.

**CColumns**: entier non signé 32 bits indiquant le nombre d’éléments dans le tableau aColumns. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.

**aColumns**: tableau des structures CTableColumn décrivant les colonnes d’une ligne dans l’ensemble de lignes. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur. Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message. Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.

### <a name="22315-cpmgetrowsin"></a>2.2.3.15 CPMGetRowsIn

Le message CPMGetRowsIn demande des lignes d’une requête. Le format du message CPMGetRowsIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_cRowsToTransfer

\_cbRowWidth

\_cbSeek

\_cbReserved

\_cbReadBuffer

\_ulClientBase

\_fBwdFetch

eType

\_chap

SeekDescription

...

... variable



 

**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les lignes doivent être récupérées.

**\_ cRowsToTransfer**: entier non signé 32 bits indiquant le nombre maximal de lignes que le client souhaite recevoir en réponse à ce message.

**\_ cbRowWidth**: entier non signé 32 bits indiquant la longueur d’une ligne, en octets.

**\_ cbSeek**: entier non signé 32 bits indiquant la taille du message commençant par ETYPE.

**\_ cbReserved**: entier non signé 32 bits indiquant la taille, en octets, d’un message CPMGetRowsOut (sans les champs Rows et SeekDescriptions). Cette valeur dans ce champ est ajoutée à la valeur du \_ champ cbSeek, puis doit être utilisée pour calculer le décalage du champ Rows dans le message CPMGetRowsOut.

**\_ cbReadBuffer**: entier non signé 32 bits qui doit être défini sur la valeur maximale de la valeur de \_ cbRowWidth ou 1000 fois la valeur de \_ cRowsToTransfer, arrondie au multiple de 512 octets le plus proche. La valeur ne doit pas dépasser 0x00004000.

**\_ ulClientBase**: entier non signé 32 bits indiquant la valeur de base à utiliser pour les calculs de pointeur dans la mémoire tampon de ligne. Si des décalages 64 bits sont utilisés, le champ Reserved2 de l’en-tête de message est utilisé comme les 32 bits supérieurs et \_ ulClientBase en tant que 32 bits inférieur d’une valeur de 64 bits. Pour plus d’informations, consultez la section 2.2.3.16.

**\_ fBwdFetch**: entier non signé 32 bits indiquant l’ordre dans lequel les lignes sont extraites. Si la valeur est définie sur 0x00000001, les lignes doivent être extraites dans l’ordre inverse. Si la valeur est 0x00000000, les lignes doivent être extraites dans l’ordre de transmission. NE doit avoir aucune autre valeur.

**ETYPE**: entier non signé 32 bits contenant l’une des valeurs suivantes pour indiquer le type d’opération à effectuer.



| Valeur                         | Signification                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowSeekNext 0x00000001       | SeekDescription contient une structure CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contient une structure CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contient une structure CRowSeekAtRatio.    |
| eRowSeekByBookmark 0x00000004 | SeekDescription contient une structure CRowSeekByBookmark. |



 

**\_ Chapt**: valeur 32 bits représentant le descripteur du chapitre de l’ensemble de lignes.

**SeekDescription**: ce champ doit contenir une structure du type indiqué par la valeur ETYPE.

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 CPMGetRowsOut

Le message CPMGetRowsOut répond à un message CPMGetRowsIn avec les lignes d’une requête. Les serveurs doivent mettre en forme des décalages avec les types de données de longueur variable dans le champ Rows comme suit :

-   Le client a indiqué qu’il s’agissait d’un système 32 bits (0x00000008 ou moins dans le champ iClientVersion de CPMConnectIn) : les décalages sont des entiers 32 bits.
-   Le client a indiqué qu’il s’agissait d’un système 64 bits ( \_ iClientVersion > 0x00000008 dans CPMConnectIn) et que le serveur indiquait qu’il s’agissait d’un système 32 bits ( \_ ServerVersion défini sur 0X00000007 dans CPMConnectOut) : les décalages sont des entiers de 32 bits
-   Le client a indiqué qu’il s’agissait d’un système 64 bits ( \_ iClientVersion > 0x00000008 dans CPMConnectIn) et que le serveur indiquait qu’il s’agissait d’un système 64 bits ( \_ ServerVersion défini sur 0X00010007 dans CPMConnectOut) : les décalages sont des entiers de 64 bits

Le format du message CPMGetRowsOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cRowsReturned

eType

\_chap

SeekDescription (facultatif, variable)

...

...

paddingRows (facultatif, variable)

Lignes



 

**\_ cRowsReturned**: entier non signé 32 bits indiquant le nombre de lignes retournées dans les lignes.

**ETYPE**: entier non signé 32 bits contenant l’une des valeurs suivantes pour indiquer le type d’opération rowseek à effectuer



| Valeur                         | Signification                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowsSeekNone 0x00000000      | Aucun SeekDescription, ignorer le champ SeekDescription.        |
| eRowSeekNext 0x00000001       | SeekDescription contient une structure CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contient une structure CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contient une structure CRowSeekAtRatio.    |
| eRowSeekByBookmark 0x00000004 | SeekDescription contient une structure CRowSeekByBookmark. |



 

**\_ Chapt**: valeur 32 bits représentant le descripteur du chapitre de l’ensemble de lignes.

**SeekDescription**: ce champ doit contenir une structure du type indiqué par le champ ETYPE.

**paddingRows**: ce champ doit avoir une longueur suffisante (de 0 à \_ cbReserved octets) pour remplir le champ de lignes à \_ cbReserved offset à partir du début d’un message, où \_ cbReserved est la valeur dans le message CPMGetRowsIn. Les octets de remplissage utilisés dans ce champ peuvent être n’importe quelle valeur arbitraire. Ce champ doit être ignoré par le récepteur.

**Lignes**: données de ligne, est mise en forme comme stipulé par les informations de colonne dans le message CPMSetBindingsIn le plus récent. Les lignes doivent être stockées dans l’ordre de transfert (par exemple, ligne 1 avant la ligne 2).

Les colonnes de taille fixe doivent être stockées aux décalages spécifiés par le message CPMSetBindingsIn le plus récent.

Les colonnes de taille variable (par exemple, les chaînes) doivent être stockées comme suit :

-   Les données de la variable proprement dite (par exemple, la chaîne) sont stockées vers la fin de la mémoire tampon dans l’ordre décroissant (par exemple, la collection de toutes les données de variable pour la ligne 1 est à la fin, ligne 2 la plus proche, etc.).
-   La zone de taille fixe (au début de la mémoire tampon de ligne) doit contenir un CRowVariant pour chaque colonne, stockée au décalage spécifié dans le message CPMSetBindingsIn le plus récent. vType doit contenir le type de données (par ex \_ ., VT LPWSTR). Si, comme déterminé par les règles au début de la section de cette section, les décalages 32 bits sont utilisés, alors le champ offset dans CRowVariant doit contenir une valeur 32 bits qui correspond au décalage des données variables à partir du début du message CPMGetRowsOut, plus la valeur de \_ ulClientBase spécifiée dans le message CPMGetRowsIn le plus récent. Si des décalages 64 bits sont utilisés, le champ de décalage dans CRowVariant doit contenir une valeur 64 bits qui correspond au décalage du début du message CPMGetRowsOut, ajouté à une valeur de 64 bits composée à l’aide de \_ ulClientBase comme 32 bits et ulReserved2 de poids \_ fort (32 bits).

Par exemple, si le message CPMSetBindingsIn spécifiant deux colonnes-Size (VT \_ I4) et title (VT \_ LPWStr)-et \_ ulClientBase de CPMGetRowsIn a été 0x10000, deux lignes s’affichent comme suit. La section marquée en gris est la partie de longueur fixe de la mémoire tampon.

![exemple de message cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a>2.2.3.17 CPMRatioFinishedIn

Le message CPMRatioFinishedIn demande le pourcentage d’achèvement d’une requête. Le format du message CPMRatioFinishedIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_fQuick



 

**\_ hCursor**: descripteur du message CPMCreateQueryOut identifiant la requête pour laquelle des informations de saisie semi-automatique doivent être demandées.

**\_ fQuick**: doit être défini sur 0x00000001. Inutilisé et doit être ignoré par le serveur.

### <a name="22318-cpmratiofinishedout"></a>2.2.3.18 CPMRatioFinishedOut

Le message CPMRatioFinishedOut répond à un message CPMRatioFinishedIn avec le ratio d’achèvement d’une requête. Le format du message CPMRatioFinishedOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ ulNumerator

\_ulDenominator

\_cRows

\_fNewRows



 

**\_ ulNumerator**: entier non signé 32 bits indiquant le numérateur du rapport d’achèvement en termes de lignes.

**\_ ulDenominator**: entier non signé 32 bits indiquant le dénominateur du rapport d’achèvement en termes de lignes. DOIT être supérieur à zéro.

**\_ Crows**: entier non signé 32 bits indiquant le nombre total de lignes de la requête.

**\_ fNewRows**: valeur booléenne indiquant si de nouvelles lignes sont disponibles. La valeur 0x00000001 indique que les nouvelles lignes sont disponibles dans l’ensemble de lignes. La valeur 0x00000000 indique que l’ensemble de lignes ne contient pas de nouvelles lignes. Ce champ ne doit avoir aucune autre valeur.

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 CPMFetchValueIn

Le message CPMFetchValueIn demande une valeur de propriété qui était trop grande pour être renvoyée dans un ensemble de lignes. Comme indiqué dans la section 3.2.4.2.5, ce message est envoyé à plusieurs reprises pour récupérer tous les octets de la propriété, en mettant à jour \_ cbSoFar pour chacun, jusqu’à ce que le \_ champ fMoreExists du message CPMFetchValueOut soit défini sur **false**.

Le format du message CPMFetchValueIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_wid

\_cbSoFar

\_cbPropSpec

\_cbChunk

PropSpec (variable)

...

\_Padding (variable)



 

**\_ wid**: entier non signé 32 bits contenant des informations sur l’ID de document identifiant le document pour lequel une propriété doit être extraite.

**\_ cbSoFar**: entier non signé 32 bits contenant le nombre d’octets transférés précédemment pour cette propriété. DOIT être défini sur 0x00000000 dans le premier message.

**\_ cbPropSpec**: entier non signé 32 bits contenant la taille du champ PropSpec, en octets.

**\_ cbChunk**: entier non signé 32 bits contenant le nombre maximal d’octets que l’expéditeur peut accepter dans un message CPMFetchValueOut.

*Windows Comportement : ce champ est défini sur 0x00004000 pour toutes les versions de Windows.*

**PropSpec**: structure CFullPropSpec spécifiant la propriété à récupérer.

**\_ remplissage**: ce champ doit avoir la longueur nécessaire (de 0 à 3 octets) pour remplir le message sur un multiple de 4 octets. La valeur des octets de remplissage peut être n’importe quelle valeur arbitraire. Ce champ doit être ignoré par le récepteur.

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 CPMFetchValueOut

Le message CPMFetchValueOut répond à un message CPMFetchValueIn avec une valeur de propriété d’une requête précédente. Comme indiqué dans la section 3.1.5.2.8, ce message est envoyé après chaque message CPMFetchValueIn jusqu’à ce que tous les octets de la propriété soient transférés.

Le format du message CPMFetchValueOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cbValue

\_fMoreExists

\_fValueExists

vType

vValue (variable)



 

**\_ cbValue**: entier non signé 32 bits contenant la taille totale, en octets, dans vValue.

**\_ fMoreExists**: valeur booléenne indiquant si des messages CPMFetchValueOut supplémentaires sont disponibles. S’il est défini sur 0x00000001, il y a des messages CPMFetchValueOut supplémentaires. Si la valeur est 0x00000000, aucun message CPMFetchValueOut supplémentaire n’est disponible.

**\_ fValueExists**: valeur booléenne indiquant s’il existe une valeur pour la propriété. Si la valeur est définie sur 0x00000001, il existe une valeur pour la propriété. Si la valeur est 0x00000000, la valeur de la propriété n’existe pas.

**vType**: une valeur de l’énumération VarEnum, consultez la section 2.2.1.1 pour plus d’informations, décrivant le type de la propriété.

**vValue**: partie d’un tableau d’octets contenant une structure SERIALIZEDPROPERTYVALUE telle que spécifiée dans la section 2.2.1.32, où l’offset du début de la partie est la valeur de \_ cbSoFar dans CPMFetchValueIn. La longueur de la partie, indiquée par le \_ champ cbValue, doit être égale à la valeur de \_ CbChunk dans CPMFetchValueIn si \_ fMoreExists est défini sur 0x00000001 et doit être inférieur ou égal à la valeur de cbChunk dans le \_ cas contraire.

### <a name="22321-cpmgetnotify"></a>2.2.3.21 CPMGetNotify

Le message CPMGetNotify demande que le client souhaite être averti des modifications de l’ensemble de lignes.

Le message ne doit pas inclure un corps ; seul l’en-tête de message, tel que spécifié dans la section 2.2.2, doit être envoyé.

### <a name="22322-cpmsendnotifyout"></a>2.2.3.22 CPMSendNotifyOut

Le message CPMSendNotifyOut avertit le client qu’une modification a été apportée aux résultats d’une requête.

Ce message est envoyé uniquement lorsqu’une modification se produit. Le format du message CPMSendNotifyOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_watchNotify



 

**\_ watchNotify**: modification de la requête. Il doit s’agir de l’une des valeurs suivantes :



| Valeur                                     | Signification                                             |
|-------------------------------------------|-----------------------------------------------------|
| DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001     | Le nombre de lignes dans l’ensemble de lignes de requête a changé. |
| DBWATCHNOTIFY \_ QUERYDONE 0x00000002       | La requête est terminée.                            |
| DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003 | La requête a été réexécutée.                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a>2.2.3.23 CPMGetApproximatePositionIn

Le message CPMGetApproximatePositionIn demande la position approximative d’un signet dans un chapitre. Le format du message CPMGetApproximatePositionIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chap

\_bmk



 

**\_ hCursor**: valeur 32 bits représentant le curseur de requête obtenu à partir de CPMCreateQueryOut pour l’ensemble de lignes contenant le signet.

**\_ Chapt**: valeur 32 bits représentant le handle du chapitre contenant le signet.

**\_ BMK**: valeur 32 bits représentant le handle du signet pour lequel récupérer la position approximative.

### <a name="22324-cpmgetapproximatepositionout"></a>2.2.3.24 CPMGetApproximatePositionOut

Le message CPMGetApproximatePositionOut répond à un message CPMGetApproximatePositionIn décrivant la position approximative du signet dans le chapitre. Le format du message CPMGetApproximatePositionOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_numerator

\_denominator



 

**\_ numérateur**: entier non signé 32 bits contenant le numéro de ligne du signet dans l’ensemble de lignes. En l’absence de lignes, ce champ doit avoir la valeur 0x00000000.

**\_ dénominateur**: entier non signé 32 bits contenant le nombre de lignes dans l’ensemble de lignes.

### <a name="22325-cpmcomparebmkin"></a>2.2.3.25 CPMCompareBmkIn

Le message CPMCompareBmkIn demande une comparaison de deux signets dans un chapitre.

Le format du message CPMCompareBmkIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chap

\_bmkFirst

\_bmkSecond



 

\_**hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut pour l’ensemble de lignes contenant les signets.

\_**Chapt**: valeur de 32 bits représentant le descripteur du chapitre contenant les signets à comparer.

\_**bmkFirst**: valeur 32 bits représentant le handle du premier signet à comparer.

\_**bmkSecond**: valeur 32 bits représentant le handle du deuxième signet à comparer.

### <a name="22326-cpmcomparebmkout"></a>2.2.3.26 CPMCompareBmkOut

Le message CPMCompareBmkOut répond à un message CPMCompareBmkIn avec la comparaison des deux signets du chapitre. Le format du message CPMCompareBmkOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwComparison



 

\_**dwComparison**: l’une des valeurs suivantes, indiquant les positions relatives des deux signets dans le chapitre.



| Valeur                               | Signification                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DBCOMPARE \_ lt 0x00000000            | Le premier signet est positionné avant le deuxième.               |
| DBCOMPARE \_ EQ 0x00000001            | Le premier signet a la même position que le second.           |
| DBCOMPARE \_ gt 0x00000002            | Le premier signet est positionné après le deuxième.                |
| DBCOMPARE ne \_ 0x00000003            | Le premier signet n’a pas la même position que le second. |
| DBCOMPARE \_ NOTCOMPARABLE 0x00000004 | Le premier signet n’est pas comparable au second.               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 CPMRestartPositionIn

Le message CPMRestartPositionIn déplace la position d’extraction d’un curseur vers le début du chapitre. Comme indiqué dans la section 3.1.5.2.12, le serveur répondra en utilisant le même message, avec les résultats de la requête contenus dans le \_ champ Status de l’en-tête CISP.

Le format du message CPMRestartPositionIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (facultatif)

\_Chapt (facultatif)



 

**\_ hCursor**: valeur 32 bits représentant le descripteur, obtenue à partir d’un message CPMCreateQueryOut, qui identifie la requête pour laquelle la position doit être redémarrée. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.

**\_ Chapt**: valeur 32 bits représentant le descripteur d’un chapitre à partir duquel récupérer des lignes. Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.

### <a name="22328-cpmfreecursorin"></a>2.2.3.28 CPMFreeCursorIn

Le message CPMFreeCursorIn demande la libération d’un curseur. Le format du message CPMFreeCursorIn qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor**: valeur 32 bits représentant le handle du curseur du message CPMCreateQueryOut à libérer.

### <a name="22329-cpmfreecursorout"></a>2.2.3.29 CPMFreeCursorOut

Le message CPMFreeCursorOut répond à un message CPMFreeCursorIn avec les résultats de la libération d’un curseur. Le format du message CPMFreeCursorOut qui suit l’en-tête est le suivant :



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cCursorsRemaining



 

**\_ cCursorsRemaining**: entier non signé 32 bits indiquant le nombre de curseurs encore utilisés pour la requête.

### <a name="22330-cpmdisconnect"></a>2.2.3.30 CPMDisconnect

Le message CPMDisconnect met fin à la connexion avec le serveur

Le message ne doit pas inclure un corps ; seul l’en-tête de message, tel que spécifié dans la section 2.2.2, doit être envoyé.

### <a name="224-errors"></a>Erreurs 2.2.4

Tous les messages du protocole de service d’indexation de contenu doivent retourner 0x00000000 en cas de réussite ; dans le cas contraire, ils retournent un code d’erreur non nul 32 bits qui peut être un HRESULT ou une valeur NTSTATUS (voir la section 1,8). Si une mémoire tampon est trop petite pour contenir un résultat, un code d’état de \_ l’État ressources insuffisantes \_ (0XC0000009A) doit être retourné et l’opération ayant échoué doit être retentée avec une mémoire tampon plus grande.

Toutes les autres valeurs d’erreur doivent être traitées de la même façon.

(Notez que actuellement, les espaces de numérotation HRESULT et NTSTATUS ne se chevauchent pas, à l’exception des valeurs de signification identique, mais même s’ils étaient des conflits à l’avenir, cela ne provoque aucun problème de protocole tant que la valeur de l’état \_ Les ressources insuffisantes \_ restent uniques, car toutes les autres valeurs d’erreur sont traitées de la même façon.)

## <a name="3-protocol-details"></a>3 Détails du protocole

-   [Détails du serveur 3,1](#31-server-details)
-   [Détails du client 3,2](#32-client-details)

Les demandes de message CISP pour l’interrogation à distance des catalogues du service d’indexation ne nécessitent pas de séquence particulière. Il est recommandé que la couche supérieure adhère à une séquence de messages significative, comme pour les messages reçus à partir de cette séquence ou avec des données non valides, le serveur répond avec une erreur. Certains messages dépendent également de la couche supérieure qui fournit des données valides qui ont été reçues dans les messages précédemment dans la séquence.

Une séquence de message standard pour une requête simple à partir d’un client vers un ordinateur distant est illustrée dans le diagramme suivant.

![séquence de message pour une requête simple](images/protocoldetails.jpg)

Les messages représentés dans le diagramme précédent représentent un sous-ensemble de tous les messages CISP utilisés pour l’interrogation d’un catalogue du service d’indexation à distance.

### <a name="31-server-details"></a>Détails du serveur 3,1

### <a name="311-abstract-data-model"></a>3.1.1 Modèle de données abstraites

La section suivante spécifie les données et l’état géré par le serveur CISP. Les données fournies ici sont pour faciliter l’explication du comportement du protocole. Cette section ne stipule pas que les implémentations adhèrent à ce modèle tant que leur comportement externe est cohérent avec celui décrit dans ce document.

Un service d’indexation qui implémente CISP doit conserver les éléments de données abstraits suivants :

-   Liste des clients connectés au serveur
-   Informations sur chaque client, notamment :
-   -   Version du client (comme indiqué dans le message CPMConnectIn spécifié dans la section 2.2.3.6)
    -   Catalogue associé au client (par un message CPMConnectIn)
    -   Propriétés client supplémentaires comme indiqué dans la section 2.2.1.21.1.
    -   Requête de recherche du client
    -   Liste des handles de curseur pour la requête et la position dans le jeu de résultats pour chaque descripteur.
    -   Ensemble actuel de liaisons
    -   État actuel de la requête qui comprend (pour chaque curseur) :
    -   -   Nombre de lignes dans le résultat de la requête
        -   Numérateur et dénominateur de la saisie semi-automatique des requêtes
        -   Nombre de lignes indiqué par le message CPMRatioFinishedOut le plus récent pour ce curseur
        -   Si la requête est analysée par le serveur pour les modifications des résultats de la requête et si elle est analysée, ce qui a changé dans les résultats de la requête depuis son dernier rapport au client par CPMSendNotifyOut
        -   Liste des descripteurs de chapitres, servis par cette requête à un client.
        -   Liste de handles de signet pour chaque curseur, servie par cette requête à un client.

-   État actuel du service d’indexation, qui peut être « non initialisé », « en cours d’exécution » ou « arrêt en cours ». Notez que la plupart du serveur de temps est dans l’État « en cours d’exécution ». Voici le diagramme d’ordinateur d’État pour le serveur :

    ![diagramme d’ordinateur d’État du serveur de service d’indexation](images/abstractdatamodel.jpg)

-   Informations par catalogue : nombre de documents indexés, taille de l’index, nombre de clés uniques, etc. (voir la section 2.2.3.1 pour obtenir la liste complète), State (qui correspond aux valeurs de dwNewState dans la section 2.2.3.2).
-   Pour chaque langue prise en charge, une base de données de variantes Word, comme indiqué dans la section 2.2.1.3.

### <a name="312-timers"></a>3.1.2 Minuteurs

Aucun minuteur de protocole n’est requis.

### <a name="313-initialization"></a>3.1.3 Initialisation

Lors de l’initialisation, le serveur doit définir son état sur « non initialisé » et commencer à écouter les messages sur le canal nommé spécifié dans la section 1,9. Une fois l’initialisation interne effectuée, elle doit passer à l’État « en cours d’exécution ».

### <a name="314-higher-layer-triggered-events"></a>3.1.4 Événements déclenchés de niveau supérieur

Aucun.

### <a name="315-message-processing-and-sequencing-rules"></a>Règles de traitement et de séquencement des messages 3.1.5

À chaque fois qu’une erreur se produit lors du traitement d’un message envoyé par un client, le serveur doit signaler une erreur au client comme suit :

-   Arrêter le traitement du message envoyé par le client
-   Répondre avec l’en-tête de message (uniquement) du message envoyé par le client, en conservant le \_ champ MSG intact.
-   Définissez le \_ champ État sur la valeur du code d’erreur.

Lorsqu’un message arrive, le serveur doit vérifier la \_ valeur du champ MSG pour déterminer s’il s’agit d’un type connu (voir la section 2.2.2). Si le type n’est pas connu, il doit signaler un état d' \_ erreur de paramètre non valide \_ (0xC000000D).

Le serveur doit ensuite valider la \_ valeur du champ ulChecksum si le type de message est l’un des éléments suivants :

-   CPMConnectIn (0x000000C8)
-   CPMCreateQueryIn (0x000000CA)
-   CPMSetBindingsIn (0x000000D0)
-   CPMGetRowsIn (0x000000CC)
-   CPMFetchValueIn (0x000000E4)

Pour valider la \_ valeur du champ ulChecksum, le serveur doit vérifier la valeur spécifiée par le client dans le \_ champ iClientVersion du message CPMConnectIn.

Si le \_ champ iClientVersion n’a pas la valeur 0x00000008 et que le \_ champ ulChecksum n’a pas la valeur 0x00000000, le serveur doit signaler une \_ erreur de paramètre non valide d’état \_ (0xC000000D). Le serveur ne doit pas valider le \_ champ ulChecksum pour les clients \_ . le champ iClientVersion a une valeur inférieure à 0x00000008.

Si la \_ valeur du champ iClientVersionfield est 0x00000008 ou supérieure, le serveur doit vérifier que le \_ champ ulChecksum a été calculé comme indiqué dans la section 3.2.4. Si la \_ valeur ulChecksum n’est pas valide, le serveur doit signaler une \_ erreur de paramètre non valide d’état \_ (0xC000000D).

Ensuite, le serveur vérifie l’État dans lequel il se trouve. Si son état est « non initialisé », le serveur doit signaler une \_ erreur d’E/t \_ non \_ initialisée (0x8004180B). Si l’État est « arrêt en cours », le serveur doit signaler une \_ erreur d’arrêt de l’E/ \_ 0X80041812 (ci).

Une fois qu’un en-tête a été déterminé comme étant valide et que le serveur est en état d’exécution, un traitement spécifique des messages doit être effectué comme indiqué dans les sous-sections ci-dessous.

### <a name="3151-remote-indexing-service-catalog-management"></a>Gestion du catalogue du service d’indexation à distance 3.1.5.1

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 recevant une demande CPMCiStateInOut

Lorsque le serveur reçoit une demande de message CPMCIStateInOut du client, le serveur doit d’abord vérifier si le client figure dans une liste de clients connectés. Si le client ne figure pas dans la liste, le serveur doit signaler une erreur de paramètre d’état \_ non valide \_ (0xC000000D). Dans le cas contraire, il doit répondre au client avec un message CPMCIStateInOut, en le remplissant avec les informations relatives au catalogue associé du client, comme indiqué dans la section 2.2.3.1.

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 recevant une demande CPMSetCatStateIn

Lorsque le serveur reçoit une demande de message CPMSetCatStateIn du client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez que le client dispose d’un accès administratif. Si le client ne dispose pas d’un accès administrateur, le serveur doit signaler une erreur d’état \_ accès \_ refusé (0xc0000022).
-   Si \_ dwNewState n’est pas égal à CICAT \_ All \_ Opened, modifiez l’état du catalogue spécifié dans le champ CatName comme spécifié par le \_ champ dwNewState. Pour plus d’informations, consultez la section 2.2.3.2. Si le serveur ne trouve pas de catalogue avec le nom spécifié dans le champ CatName, le serveur doit retourner une \_ erreur de paramètre non valide de l’état \_ (0xC000000D).
-   Répondez au client avec un message CPMSetCatStateOut, où \_ DWOLDSTATE doit être défini à l’état précédent du catalogue. Si \_ dwNewState est égal à CICAT \_ All \_ Opened, le serveur doit vérifier l’état de tous les catalogues et, s’ils sont tous démarrés, il doit définir \_ dwOldState sur 0x00000001 et, sinon, définir \_ dwOldState sur 0x00000000.

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 recevant une demande CPMUpdateDocumentsIn

Lorsque le serveur reçoit une demande de message CPMUpdateDocumentsIn, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client figure dans une liste de clients connectés (auxquels est associé un catalogue). Si le client ne figure pas dans la liste, le serveur doit signaler une erreur de paramètre d’état \_ non valide \_ (0xC000000D).
-   Vérifiez que le client dispose d’un accès administratif. Si le client ne dispose pas d’un accès administratif au serveur, le serveur doit signaler une \_ erreur d’accès \_ refusé (0xc0000022).
-   Commencez le processus d’indexation du chemin d’accès spécifié par le client, en procédant à une analyse complète ou incrémentielle, en fonction de la valeur du \_ champ d’indicateur dans le message CPMUpdateDocumentsIn. Si le chemin d’accès n’était pas déjà indexé, il doit être ajouté à la collection d’emplacements indexés et une analyse complète est effectuée. Si une valeur non conforme du \_ champ indicateur est spécifiée, le serveur doit agir comme si \_ Flag était défini sur UPD \_ Init et effectuer une analyse complète. Cette opération doit être effectuée dans le catalogue associé au client.
-   Répondez au client avec l’en-tête de message pour CPMUpdateDocumentsIn et définissez le \_ champ Status sur les résultats de la demande.

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 recevant une demande CPMForceMergeIn

Lorsque le serveur reçoit une demande de message CPMForceMergeIn, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client figure dans une liste de clients connectés (auxquels est associé un catalogue). Si le client ne figure pas dans la liste, le serveur doit signaler un état d' \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez que le client dispose d’un accès administratif. Si le client ne dispose pas d’un accès administrateur, le serveur doit signaler une erreur d’état \_ accès \_ refusé (0xc0000022).
-   Commencez tout processus de maintenance nécessaire pour améliorer les performances des requêtes sur un catalogue, associées au client.
-   Répondez au client avec un en-tête de message pour CPMForceMergeIn et définissez le \_ champ Status sur les résultats de la demande.

Notez que le processus de maintenance est asynchrone et peut continuer une fois que le client a reçu le message de réponse. Ce processus n’affecte pas directement le protocole de quelque façon que ce soit (autre que le temps de réponse).

### <a name="3152-remote-indexing-service-querying"></a>interrogation du service d’indexation à distance 3.1.5.2

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 recevant une demande CPMConnectIn

Lorsque le serveur reçoit une requête CPMConnectIn à partir d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client figure dans la liste des clients connectés. Si c’est le cas, le serveur doit signaler une \_ erreur de \_ paramètre non valide (0xC000000D).
-   Vérifie si le catalogue spécifié existe et s’il n’est pas à l’état arrêté. Si ce n’est pas le cas, le serveur doit disposer d’une erreur de l’état d' \_ \_ absence du \_ catalogue (0x8004181D) du rapport ci.
-   Ajoutez le client à la liste des clients connectés.
-   Associez le catalogue au client.
-   Stockez les informations transmises dans le message CPMConnectIn (telles que le nom du catalogue, la version du client, etc.) dans l’état du client.
-   Répondez au client avec un message CPMConnectOut.

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 recevant une demande CPMCreateQueryIn

Lorsque le serveur reçoit une demande de message CPMCreateQueryIn d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client figure dans la liste des clients connectés. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si une requête est déjà associée au client. Si c’est le cas, le serveur doit signaler une \_ erreur de \_ paramètre non valide (0xC000000D).
-   Vérifiez si le catalogue associé au client est dans l’État, ce qui permet le traitement de la requête (CICAT \_ ReadOnly ou CICAT \_ accessible en écriture). Si ce n’est pas le cas, le serveur doit signaler une \_ erreur requête S \_ aucune \_ requête (0x8004160C).
-   Analysez l’ensemble de restrictions, les ordres de tri et les regroupements spécifiés dans la requête. Si le serveur rencontre une erreur, il doit signaler une erreur appropriée. Si cette étape échoue pour une autre raison, le serveur doit signaler l’erreur rencontrée. Pour plus d’informations sur les erreurs de requête du service d’indexation, consultez \[ MSDN-QUERYERR \] .
-   Enregistrez la requête de recherche dans l’état du client.
-   Effectuez les préparatifs nécessaires pour servir les lignes à un client et associez la requête aux handles de curseur appropriés (en fonction des informations transmises dans le message CPMCreateQueryIn).
-   Ajoutez ces handles à la liste des handles de curseurs du client et initialisez les listes de handles de chapitre et de signets.
-   Initialise la liste des descripteurs de chapitre pour chaque curseur de cette requête sur DB \_ null \_ HCHAPTER
-   Initialisez la liste des descripteurs de signet pour chaque curseur de cette requête sur un ensemble de DBBMK \_ et de DBBMK en \_ dernier.
-   Marquez la requête comme non surveillée pour les modifications.
-   Initialisez le nombre de lignes sur le nombre de lignes actuellement calculé (ce qui peut être 0 si la requête n’a pas commencé à s’exécuter ou un nombre si la requête est en cours d’exécution) et initialisez le numérateur et le dénominateur de la saisie semi-automatique des requêtes.
-   Répondez au client avec un message CPMCreateQueryOut.

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 recevant une demande CPMGetQueryStatusIn

Lorsque le serveur reçoit une demande de message CPMGetQueryStatusIn d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client est associé à une requête. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur se trouve dans une liste de handles de curseur du client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Préparez un message CPMGetQueryStatusOut. Le serveur doit récupérer l’état actuel de la requête et le définir dans le \_ champ QStatus (consultez 2.2.3.11 pour connaître les valeurs possibles). Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.
-   Répondez au client avec le message CPMGetQueryStatusOut.

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 recevant une demande CPMGetQueryStatusExIn

Lorsque le serveur reçoit une demande de message CPMGetQueryStatusExIn d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si une requête est associée au client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur réussi figure dans une liste de handles de curseur du client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Préparez un message CPMGetQueryStatusExOut. Le serveur doit récupérer l’état de la requête actuelle et la progression de la requête et définir QStatus (consultez 2.2.3.11 pour connaître les valeurs possibles), \_ dwRatioFinishedDenominator et \_ dwRatioFinishedNumerator respectivement. Il doit ensuite définir le nombre de lignes dans les résultats de la requête sur \_ cRowsTotal. Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.
-   Récupérez des informations sur le catalogue du client et remplissez \_ cFilteredDocuments et \_ cDocumentsToFilter. Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.
-   Récupérez la position du signet indiquée par la poignée dans le \_ champ BMK, puis remplissez le \_ champ iRowBmk restant dans le message CPMGetQueryStatusExOut. Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.
-   Répondez au client avec le message CPMGetQueryStatusExOut.

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 recevant une demande CPMRatioFinishedIn

Lorsque le serveur reçoit une demande de message CPMRatioFinishedIn d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client est associé à une requête. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Préparez un message CPMRatioFinishedOut. Le serveur doit récupérer l’état de la requête du client et remplir les \_ champs ulNumerator, \_ ulDenominator et \_ Crows. Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.
-   Si \_ Crows est égal au dernier nombre de lignes signalées pour cette requête, définissez \_ fNewRows sur 0x00000000. sinon, affectez-lui la valeur 0x00000001.
-   Met à jour le dernier nombre de lignes signalées pour cette requête à la valeur de \_ Crows.
-   Répondez au client avec le message CPMRatioFinishedOut.

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 recevant une demande CPMSetBindingsIn

Lorsque le serveur reçoit une demande de message CPMSetBindingsIn d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si une requête est associée au client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Vérifiez que les informations de liaison sont valides (c’est-à-dire que la colonne spécifie au moins la valeur, la longueur ou l’État à renvoyer ; aucun chevauchement des liaisons pour la valeur, la longueur ou l’État ; et la valeur, la longueur et l’État s’ajustent à la taille de ligne spécifiée) et si aucune erreur de base de données \_ \_ BADBINDINFO (0x80040E08) n’est signalée
-   Enregistrez les informations de liaison associées aux colonnes spécifiées dans le champ aColumns. Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.
-   Répondez au client avec un en-tête de message (uniquement) avec \_ MSG défini sur CPMSetBindingsIn et \_ Status défini sur les résultats de la liaison spécifiée.

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 recevant une demande CPMGetRowsIn

Lorsque le serveur reçoit une demande de message CPMGetRowsIn d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client est associé à une requête. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur passé est dans athelist des handles de curseur du client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Vérifiez si le client dispose d’un ensemble de liaisons en cours. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Préparez un message CPMGetRowsOut. Le serveur doit positionner le curseur dans les résultats de la requête comme indiqué par la description de la recherche. Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.
-   Récupérez autant de lignes que vous le configurez dans une mémoire tampon, dont la taille est indiquée par \_ cbReadBuffer, mais pas plus que ce qui est indiqué par \_ cRowsToTransfer. Lors de l’extraction de lignes, le serveur doit comparer le type de valeur de propriété de chaque colonne sélectionnée au type spécifié dans le jeu de liaisons actuel du client (section 3.1.1). Si le type de la liaison n’est pas de type VT \_ , le serveur doit tenter de convertir la valeur de la propriété de la colonne en ce type. Sinon, si l' \_ indicateur DBPROP USEEXTENDEDDBTYPES est défini dans le jeu de propriétés DBPROPSET QUERYEXT du client \_ , ou si la valeur de la propriété de la colonne n’est pas un \_ type de vecteur VT, la valeur de la propriété doit être retournée dans son type normal. Si aucune de ces conditions n’est respectée (c’est-à-dire que le serveur a un \_ type de vecteur VT et que le client ne prend pas en charge VT \_ Vector), le serveur doit tenter de le convertir en un \_ type de tableau VT comme suit : les \_ éléments VT I8, VT \_ UI8, VT \_ fileTime et VT \_ CLSID du tableau ne peuvent pas être convertis et échouent à la place ; \_ \_ Les éléments de tableau VT LPSTR et VT LPWStr doivent être convertis en \_ BSTR BSTR ; les éléments de tableau de tous les autres types doivent rester inchangés. Enfin, si les colonnes de ligne contiennent des handles de chapitre ou de signet, le serveur doit mettre à jour les listes correspondantes. Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.
-   Stockez le nombre réel de lignes extraites dans \_ cRowsReturned.
-   Copiez la description de recherche et le champ de chapitre de CPMGetRowsIn dans un message CPMGetRowsOut à envoyer.
-   Stockez les lignes extraites dans le champ Rows (voir la remarque sur l’octet d’état ci-dessous et la section 2.2.3.16 dans la structure du champ Rows).
-   Répondez au client avec le message CPMGetRowsOut.

Remarque sur le champ octet d’État :

Si StatusUsed est défini sur 0x01 dans le CTableColumn du message CPMSetBindingIn pour la colonne, le serveur doit définir l’octet d’État (qui se trouve à StatusOffset à partir du début de la ligne) pour cette colonne à l’une des valeurs suivantes :



| Valeur | Signification        |
|-------|----------------|
| 0x00  | StatusOK       |
| 0x01  | StatusDeferred |
| 0x02  | StatusNull     |



 

Si la valeur de propriété est absente pour cette ligne, le serveur doit définir l’octet d’État sur StatusNull. Si la valeur est trop grande pour être transférée dans le message CPMGetRowsOut, le serveur doit définir l’octet d’État sur StatusDeferred. Dans le cas contraire, le serveur doit définir l’octet d’État sur StatusOK.

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 recevant une demande CPMFetchValueIn

Lorsque le serveur reçoit une demande de message CPMFetchValueIn d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client est associé à une requête. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Préparez un message CPMFetchValueOut. Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.
-   Recherchez le document indiqué par le \_ champ wid et vérifiez si l’ID de propriété de ce document (ultérieurement appelé « valeur de propriété ») indiqué par la structure PropSpec est disponible pour ce client. Si cette valeur n’est pas disponible, le serveur doit définir \_ fValueExists sur 0x00000000 et, sinon, définir \_ fValueExists sur 0x00000001. Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.
-   Si \_ fValueExists est égal à 0x00000001, le serveur doit effectuer les opérations suivantes :
-   -   Sérialisez la valeur de la propriété dans une structure SERIALIZEDPROPERTYVALUE et copiez-la, en commençant par l' \_ offset cbSoFar, au maximum \_ cbChunk octets (mais sans dépasser la fin de la propriété sérialisée) dans le champ vValue. Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.
    -   Définissez \_ cbValue sur le nombre d’octets copiés à l’étape précédente.
    -   Définissez vType sur le type de propriété de la valeur de propriété.
    -   Si la longueur de la propriété sérialisée est supérieure à \_ cbSoFar ajoutée à \_ cbValue, affectez à fMoreExists la valeur \_ 0x00000001. sinon, affectez-lui la valeur 0x00000000.

-   Répondre au client avec le message CPMFetchValueOut

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 recevant une demande CPMGetNotify

Lorsque le serveur reçoit un message CPMGetNotify d’un client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si le client est associé à une requête. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Si aucune modification n’a été apportée dans le jeu de résultats de la requête depuis le dernier message CPMSendNotifyOut pour ce client, ou si la requête n’est pas actuellement surveillée pour les modifications dans le jeu de résultats, le serveur doit répondre avec le message CPMGetNotify et commencer à analyser la requête pour rechercher les modifications dans le jeu de résultats. Si, par la suite, une modification est apportée au jeu de résultats de la requête, le serveur doit envoyer un seul message CPMSendNotifyOut au client et doit spécifier la modification dans le \_ champ watchNotify.
-   Si des modifications ont été apportées au jeu de résultats de la requête depuis le dernier message CPMSendNotifyOut, le serveur doit répondre avec CPMSendNotifyOut et doit spécifier la modification dans le \_ champ watchNotify. Notez que, dans le cas de nombreuses modifications des résultats de la requête, DBWATCHNOTIFY \_ ROWSCHANGED prend la priorité (c’est-à-dire, si la requête a été exécutée, réexécutée et que le nombre de lignes modifiées et la requête a été effectué à nouveau, l’événement signalé est DBWATCHNOTIFY \_ ROWSCHANGED).

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 recevant une demande CPMGetApproximatePositionIn

Lorsque le serveur reçoit une demande de message CPMGetApproximatePositionIn du client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si une requête est associée au client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur, le handle de chapitre et le handle de signet passés se trouvent dans les listes correspondantes. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Recherchez une ligne qui est associée au handle de signet dans les résultats de la requête et déterminez approximativement la position de la ligne dans l’ensemble de lignes, référencée par le handle de chapitre, et déterminez le numérateur et le dénominateur de la position. Notez que lorsque le descripteur de chapitre est DB \_ null \_ HCHAPTER, le chapitre correspondant est l’ensemble de lignes principal de la requête. Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.
-   Répondez au client avec un message CPMFetchValueOut.

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 recevant une demande CPMCompareBmkIn

Lorsque le serveur reçoit une demande de message CPMCompareBmkIn du client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si une requête est associée au client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur, le handle de chapitre et les handles de signet réussis se trouvent dans les listes correspondantes. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Préparez un message CPMCompareBmkOut.
-   Si les poignées de signet sont égales, \_ DWCOMPARISON doit avoir la valeur DBCOMPARE \_ EQ.
-   Sinon, si l’un des descripteurs de signets est DBBMK \_ First ou DBBMK \_ Last, \_ dwComparison doit être défini sur DBCOMPARE ne \_ .
-   Dans le cas contraire, le serveur doit effectuer les opérations suivantes :
-   -   Rechercher les lignes référencées par chaque handle de signet dans les résultats de la requête
    -   Si l’une des lignes n’est pas dans le chapitre indiqué par le descripteur de chapitre dans CPMCompareBmkIn, \_ DWCOMPARISON doit être défini sur DBCOMPARE \_ NOTCOMPARABLE.
    -   Dans le cas contraire, lorsque les deux lignes se trouvent dans le même chapitre, le serveur doit arrondir la position de ces lignes dans l’ensemble de lignes référencé par le handle de ce chapitre. Il doit ensuite comparer les valeurs de position et définir \_ dwComparison sur DBCOMPARE \_ lt si la position de la première ligne est inférieure à la position de la deuxième ligne ; sinon, \_ dwComparison doit être défini sur DBCOMPARE \_ gt.

-   Répondez au client avec un message CPMCompareBmkOut rempli.

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 recevant une demande CPMRestartPositionIn

Lorsque le serveur reçoit la demande de message CPMRestartPositionIn du client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si une requête est associée au client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur et le descripteur de chapitre sont dans les listes correspondantes. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Placez le curseur au début du chapitre, identifié par le handle de chapitre. Notez que lorsque le descripteur de chapitre est DB \_ null \_ HCHAPTER, le chapitre correspondant est l’ensemble de lignes principal de la requête. Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.
-   Répondez au client avec un message CPMRestartPositionIn.

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 recevant une demande CPMFreeCursorIn

Lorsque le serveur reçoit une demande de message CPMFreeCursorIn du client, le serveur doit effectuer les opérations suivantes :

-   Vérifiez si une requête est associée au client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).
-   Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client. Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).
-   Libérer le curseur et les ressources associées (voir la section 3.1.1 pour obtenir la liste complète) pour ce handle de curseur.
-   Supprimez le curseur de la liste des curseurs pour ce client.
-   Répondez avec un message CPMFreeCursorOut, en définissant le \_ champ cCursorsRemaining avec le nombre de curseurs restants. dans la liste de ce client.
-   S’il n’y a plus de curseurs pour ce client, le serveur doit libérer la requête et les ressources associées (voir la section 3.1.1).

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 recevant une demande CPMDisconnect

Lorsque le serveur reçoit une demande de message CPMDisconnect du client, le serveur doit supprimer le client de la liste des clients connectés et libérer toutes les ressources associées au client.

### <a name="316-timer-events"></a>Événements de minuterie 3.1.6

Aucun.

### <a name="317-other-local-events"></a>3.1.7 autres événements locaux

Quand le serveur est arrêté, il doit d’abord passer à l’état « arrêt ». Il doit ensuite arrêter d’écouter le canal, effectuer d’autres tâches d’arrêt spécifiques à l’implémentation, puis passer à l’état « arrêté ».

### <a name="32-client-details"></a>Détails du client 3,2

### <a name="321-abstract-data-model"></a>3.2.1 modèle de données abstraites

La section suivante spécifie les données et l’état géré par le client du protocole du service d’indexation de contenu. Les données fournies sont pour faciliter l’explication du comportement du protocole. Cette section ne stipule pas que les implémentations adhèrent à ce modèle tant que leur comportement externe est cohérent avec celui décrit dans ce document.

Un client a l’État abstrait suivant :

-   **Dernier message envoyé**: copie du dernier message envoyé au serveur.
-   **Valeur de propriété actuelle**: valeur partielle d’une propriété « différée », qui est en cours de récupération.
-   **Octets actuels reçus**: nombre d’octets reçus pour la valeur de propriété actuelle jusqu’à présent.
-   **État de la connexion de canal nommé**: une connexion au serveur

### <a name="322-timers"></a>les minuteurs 3.2.2

Aucun minuteur de protocole n’est requis.

### <a name="323-initialization"></a>3.2.3 initialisation

Aucune action n’est effectuée tant qu’une demande de couche supérieure n’a pas été reçue.

### <a name="324-higher-layer-triggered-events"></a>3.2.4 Higher-Layer événements déclenchés

Lorsqu’une demande est reçue à partir d’une couche supérieure, le client doit créer une connexion de canal nommé au serveur, à l’aide des détails spécifiés dans la section 2,1. Si ce n’est pas le cas, la demande de couche supérieure doit être en échec. Autrement dit, en cas de défaillance de la connexion, il incombe au niveau supérieur de réessayer si vous le souhaitez.

Un en-tête doit être préalablement associé à des champs définis comme indiqué dans la section 2.2.2.

Pour les messages spécifiés comme nécessitant une somme de contrôle différente de zéro, la \_ valeur ULCHECKSUM doit être calculée comme suit :

1.  Le contenu du message après que le \_ champ ulReserved2 de l’en-tête de message doit être interprété comme une séquence d’entiers 32 bits. Le client doit calculer la somme des valeurs numériques fournies par ces entiers.
2.  Calcule l’opération de bits XOR de cette valeur avec 0x59533959.
3.  Soustrait la valeur donnée par \_ MSG de la valeur qui résulte de l’opération de bits XOR.

### <a name="3241-remote-indexing-service-catalog-management"></a>Gestion du catalogue du service d’indexation à distance 3.2.4.1

Chaque message est déclenché par une demande de la couche supérieure. Aucune séquence de message n’est appliquée par le client pour les demandes de message CISP pour la gestion à distance des catalogues, mais (à l’exception d’un message CPMSetCatStateIn) le serveur répondra uniquement avec succès si le client s’est connecté précédemment au moyen d’un message CPMConnectIn.

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 envoyant une demande CPMCiStateInOut

En règle générale, la couche supérieure demande au client de protocole d’envoyer un message CPMCiStateInOut lorsqu’il a besoin d’informations sur les services d’indexation sur le serveur.

Lorsque vous demandez à envoyer ce message, le client doit effectuer les opérations suivantes :

-   Envoyez un message CPMCiStateInOut tel que spécifié dans la section 2.2.3.1 au serveur.
-   Attendez de recevoir le message CPMCiStateInOut du serveur, en ignorant silencieusement tous les autres messages.
-   Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, la structure d’information pour revenir à la couche supérieure.

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 envoyant une demande CPMSetCatStateIn

En règle générale, la couche supérieure demande au client de protocole d’envoyer un message CPMSetCatStateIn lorsqu’il a besoin d’informations sur un catalogue ou sur tous les catalogues. Pour ce message, la couche supérieure doit fournir au client de protocole une valeur pour \_ dwNewState et, si nécessaire, le nom du catalogue.

Lorsque vous demandez à envoyer ce message, le client doit effectuer les opérations suivantes :

-   Envoi d’un message CPMSetCatStateIn tel que spécifié dans 2.2.3.2 au serveur.
-   Attendez de recevoir un message CPMSetCatStateOut du serveur, en ignorant silencieusement tous les autres messages.
-   Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, \_ redwOldState à la couche supérieure.

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 envoyant une demande CPMUpdateDocumentsIn

En général, la couche supérieure demande à envoyer ce message lorsqu’il doit mettre à jour des documents dans un chemin d’accès existant ou ajouter un nouveau chemin d’accès de fichier à l’index. La couche supérieure est donc de fournir le chemin d’accès et le type d’une analyse, qui est spécifiée comme dans la section 2.2.3.4 où une mise à jour incrémentielle ou complète est destinée à des chemins d’accès existants, et l’initialisation de nouvelles est destinée aux nouveaux chemins d’accès.

Pour répondre à la demande de couche supérieure, le client doit effectuer les opérations suivantes :

-   Envoyez un message CPMUpdateDocumentsIn tel que spécifié dans la section 2.2.3.4 au serveur.
-   Attendez de recevoir le message CPMUpdateDocumentsIn du serveur, en ignorant silencieusement tous les autres messages.
-   Signalez la valeur du \_ champ d’état de la réponse à la couche supérieure.

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 envoyant une demande CPMForceMergeIn

En règle générale, la couche supérieure demande à envoyer ce message lorsqu’il est nécessaire d’améliorer les performances des requêtes ou qu’elle fait partie de la maintenance planifiée du service d’indexation.

Afin de servir la couche supérieure, le client doit effectuer les opérations suivantes :

-   Envoie le message CPMForceMergeIn tel que spécifié par la section 2.2.3.5 au serveur.
-   Attente de réception d’un message CPMUpdateDocumentsIn à partir du serveur, en ignorant silencieusement tous les autres messages.
-   Signalez la valeur du \_ champ d’état de la réponse à la couche supérieure.

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>Messages de requête du catalogue du service d’indexation à distance 3.2.4.2

À l’exception de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, il existe une relation un-à-un entre les messages CISP et les demandes de couche supérieures. Pour les deux exceptions mentionnées ci-dessus, il peut y avoir plusieurs messages générés par le client pour répondre aux exigences de taille, ou pour récupérer une propriété complète. La couche supérieure effectue généralement le suivi de toutes les informations spécifiques à la requête (telles que les handles de curseur ouverts, les valeurs autorisées pour les descripteurs de signet et de chapitre, les valeurs wid pour les valeurs de propriété différées, etc.) et effectue également le suivi si le client est dans un état connecté, mais cela n’est pas appliqué par le client.

À des fins d’illustration, la partie cliente du diagramme de la section 3 illustre cette séquence pour une requête de service d’indexation simple.

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 envoyant une demande CPMConnectIn

Ce message est généralement la toute première requête de la couche supérieure (comme si le client n’est pas connecté, le serveur échouera la plupart des messages avec l’exception de CPMSetCatStateIn). Le niveau supérieur fournit au client de protocole les informations nécessaires pour se connecter.

Afin de servir la couche supérieure, le client doit effectuer les opérations suivantes :

-   Renseignez le message à l’aide des informations fournies par le client de couche supérieure (voir la section 2.2.3.6) dans \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 et aPropertySet.
-   Définissez \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet et cExtPropSet comme spécifié dans 2.2.3.6.
-   Définissez la somme de contrôle dans le \_ champ ulChecksum.
-   Envoyez le message CPMConnectIn au serveur.
-   Attente de réception d’un message CPMConnectOut à partir du serveur, en ignorant silencieusement tous les autres messages.
-   Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, \_ restaurez la couche supérieure.

À des fins d’information, il est prévu que les couches supérieures effectuent généralement les actions suivantes lors de la connexion réussie, mais elles ne sont pas appliquées par le client CISP :

-   Utiliser les messages de gestion du catalogue du service d’indexation à distance pour les tâches d’administration
-   Utilisez une demande CPMCreateQueryIn pour créer une requête de recherche dans le but de récupérer les résultats du catalogue.

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 envoyant une demande CPMCreateQueryIn

La couche supérieure fournit généralement des informations pour la création de la requête une fois que le client de protocole est connecté. La couche supérieure fournit au client un ensemble de restrictions, un jeu de colonnes, des règles d’ordre de tri et un ensemble de catégorisation (chacune d’elles peut être omise), des propriétés d’ensemble de lignes et la structure du mappeur d’ID de propriété.

Lorsque cette demande est reçue à partir d’une couche supérieure, le client doit effectuer les opérations suivantes :

-   Préparez un CPMCreateQueryOut comme suit.
-   -   Si un jeu de colonnes est présent, définissez CColumnsSetPreset sur 0x01 et remplissez le champ ColumnsSet.
    -   Si des restrictions sont présentes, définissez CRestrictionPresent sur 0x01 et remplissez le champ restriction.
    -   Si un ensemble de tris est présent, renseignez le champ SortSet.
    -   Si un ensemble de catégorisations est présent, définissez CSortSetPresent sur 0x01 et remplissez le champ CategorizationSet.
    -   Définir le reste des champs comme indiqué dans 2.2.3.8

-   Calculez \_ le champ ulCheckSum dans l’en-tête.
-   Envoyez le message CPMCreateQueryIn au serveur.
-   Attendez de recevoir le message CPMCreateQueryOut (voir les détails dans la section 3.2.5.1.1), en ignorant silencieusement tous les autres messages.
-   Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, le tableau de handles de curseur et les valeurs booléennes informatifs (comme spécifié dans 2.2.3.9) à la couche supérieure.

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 envoyant une demande CPMSetBindingsIn

En règle générale, la couche supérieure définit des liaisons pour chaque colonne à retourner dans les lignes lorsqu’elle a déjà un handle de curseur valide (après avoir reçu avec succès CPMCreateQueryOut, consultez la section 3.2.5.1.1). Le plus élevé est supposé fournir un tableau de structures CTableColumn, comme indiqué dans la section 2.2.4.31, pour le champ aColumns et un handle de curseur valide.

Lorsque cette demande est reçue de la couche supérieure, le client doit effectuer les opérations suivantes :

-   Calculez le nombre de structures CTableColumn dans le tableau aColumns et définissez le champ cColumns sur cette valeur.
-   Calculez la taille totale en octets des champs cColumns et aColumns, puis affectez la \_ valeur au champ cbBindingDesc.
-   Définissez les champs spécifiés dans le message CPMSetBindingsIn sur les valeurs fournies par la couche d’application supérieure. Définissez le \_ champ ulChecksum sur la valeur calculée comme indiqué dans la section 3.2.5.
-   Envoyez le message CPMSetBindignsIn terminé au serveur.
-   Attendez de recevoir un message CPMSetBindingsIn du serveur, en ignorant les autres messages.
-   Indiquez l’état du \_ champ État de la réponse à la couche supérieure.

À des fins d’information, il est prévu que les couches supérieures demandent généralement à un client d’envoyer un message CPMGetRowsIn, mais cela n’est pas appliqué par le protocole de service d’indexation de contenu.

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 envoyant une demande CPMGetRowsIn

Lorsque la couche supérieure est sur le point de recevoir des informations sur les lignes, elle fournit au client de protocole un pointeur et un handle de chapitre valides et donne une description de recherche appropriée. En règle générale, une couche supérieure est censée le faire lorsqu’elle a un handle de curseur et/ou de chapitre valide et que les liaisons ont été définies avec un message CPMSetBindingsIn. Pour accéder à l’ensemble de lignes dans un chapitre, la couche supérieure est d’utiliser le descripteur de chapitre reçu du serveur dans un message CPMGetRowsOut précédent.

Lorsque cette demande est reçue de la couche supérieure, le client doit effectuer les opérations suivantes :

-   Déterminez la valeur de l’entier non signé à spécifier pour le \_ champ cbReadBuffer. Pour déterminer cette valeur, le client doit prendre la valeur maximale de ce qui suit :
-   -   1000 fois la valeur du champ c \_ RowsToTransfer.
    -   Valeur de \_ cbRowWidth, arrondie au multiple de 512 octets le plus proche.
    -   Prenez la valeur la plus élevée de ces deux valeurs, jusqu’à la limite de 16 Ko.
    -   Dans les cas où une seule ligne est supérieure à 16 Ko, le serveur ne peut pas retourner les résultats de cette requête.

Spécifiez une base de client pour les données de ligne de taille variable dans l’espace d’adressage du client dans le \_ champ ulClientBase.

*Windows Comportement : pour un client 32 bits communiquant avec un serveur 32 bits, ou un client 64 bits parlant à un serveur 64 bits, cette valeur est définie sur une adresse mémoire de la mémoire tampon de réception dans le processus d’application. Cela permet aux pointeurs, qui sont reçus dans le champ de lignes de CPMGetRowsOut d’être des pointeurs de mémoire corrects dans un processus d’application cliente. Sinon, la valeur est 0x00000000.*

-   Calculez la taille de la description de la recherche et définissez-la dans le \_ champ cbSeek.
-   Définissez la valeur de cbReserved (qui ferait office de décalage pour les lignes de début) à la valeur de \_ cbSeek plus 0x14.
-   Envoi d’un message CPMConnectIn tel que spécifié dans 2.2.3.15 au serveur.

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 envoyant une demande CPMFetchValueIn

Si le client reçoit une réponse CPMGetRowsOut du serveur avec le champ d’état de la colonne défini sur StatusDeferred (0x01), cela signifie que la valeur de propriété n’a pas été incluse dans le champ Rows du message CPMGetRowsOut. Dans ce cas, la couche supérieure demande généralement au client de protocole de récupérer la valeur au moyen du message CPMFetchValueIn et fournit la valeur PropSpec et \_ wid pour une propriété différée, que le client de protocole doit utiliser dans le premier message CPMFetchValueIn.

S’il s’agit du premier message CPMFetchValueIn que le client a envoyé pour demander la propriété spécifiée, le client doit effectuer les opérations suivantes :

-   Définissez tous les champs d’un message comme indiqué dans la section 2.2.3.19.
-   Affectez \_ à cbSoFar la valeur 0x00000000.
-   Définir les octets actuels reçus à 0.
-   Envoyez le message CPMFetchValueIn au serveur.

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 envoyant une demande CPMFreeCursorIn

Une fois que le niveau supérieur n’utilise plus la requête de recherche, il peut libérer les ressources sur le serveur en demandant au client d’envoyer un message CPMFreeCursorIn.

Lorsque cette demande est reçue, le client doit envoyer un message CPMFreeCursorIn tel que spécifié dans 2.2.3.28 au serveur, contenant le descripteur spécifié par la couche supérieure.

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 envoi d’un message CPMDisconnect

Si la couche supérieure n’a plus de requêtes pour le service d’indexation, pour libérer davantage de ressources serveur, l’application peut demander que le client envoie un message CPMDisconnect au serveur. Lorsque cette requête est reçue, le client doit simplement envoyer le message comme demandé. Il n’y a aucune réponse à ce message à partir du serveur.

### <a name="325-message-processing-and-sequencing-rules"></a>3.2.5 traitement des messages et règles de séquencement

Lorsque le client reçoit une réponse de message du serveur, le client doit utiliser le dernier message envoyé pour déterminer si le message reçu du serveur est celui attendu par le client. Tous les messages dont \_ le champ MSG est différent de celui du dernier message d’envoi doivent être ignorés.

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 recevant une réponse CPMCreateQueryOut

Lorsque le client reçoit une réponse de message CPMCreateQueryOut du serveur, le client doit renvoyer l' \_ État et (si l’État est réussi) les valeurs de handle de curseur sont retournées à une couche supérieure. Toutes les actions supplémentaires sont effectuées jusqu’à la couche supérieure.

Comme la couche supérieure est consciente de la structure de la requête, elle devrait toujours s’attendre à ce que le nombre de handles de curseur soit renvoyé dans le message CPMCreateOueryOut. Les handles de curseur sont retournés dans l’ordre suivant : le premier descripteur est l’ensemble de lignes non chapitre, le second est le premier ensemble de lignes chapitre (qui est le regroupement de résultats en fonction de la première catégorie spécifiée dans le champ CategorizationSet du message CPMCreateQueryIn.)

À des fins d’information, il est prévu que les couches supérieures puissent effectuer les actions suivantes, mais elles ne sont pas appliquées par le client CISP :

-   Utilisez CPMSetBindingsIn pour définir des liaisons pour des colonnes individuelles et effectuer toutes les actions suivantes sur le chemin d’accès de la requête
-   Utilisez CPMGetQueryStatusIn pour vérifier la progression de l’exécution d’une requête.
-   Utilisez CPMRatioFinishedIn pour demander le pourcentage d’achèvement de la requête.

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 recevant une réponse CPMGetRowsOut

Lorsque le client reçoit une réponse de message CPMGetRowsOut du serveur, le client doit effectuer les opérations suivantes :

-   Vérifiez si le \_ champ d’État dans l’en-tête indique réussite ou échec.
-   Si la \_ valeur d’État est mémoire tampon d’État insuffisante \_ \_ \_ (0xC0000023), le client doit vérifier l’état du dernier message envoyé. S’il ne contient pas de message CPMGetRowsIn, le message reçu doit être ignoré en mode silencieux. Dans le cas contraire, le client doit envoyer au serveur un nouveau message CPMGetRowsIn avec tous les champs identiques à ceux qui sont stockés, sauf que le \_ CBREADBUFFER doit être augmenté de 512 (mais pas supérieur à 0x4000). Si \_ l’État est \_ \_ trop \_ petit pour le tampon d’État (0xC0000023) et que le dernier message envoyé a déjà un \_ CBREADBUFFER égal au client 0x4000 doit signaler l’erreur au niveau supérieur.
-   Si la \_ valeur d’État est une autre valeur d’erreur, le client doit indiquer l’échec jusqu’à la couche supérieure.
-   Si la \_ valeur d’État indique une réussite, les résultats doivent être indiqués jusqu’à la couche supérieure demandant les informations, et d’autres actions sont effectuées sur la couche supérieure.

À des fins d’information, il est prévu que les couches supérieures effectuent généralement les actions suivantes, mais elles ne sont pas appliquées par le client du protocole du service d’indexation de contenu :

-   Si les valeurs des lignes représentent les ID de document, les poignées de chapitre ou de signet, la couche supérieure les stocke en général pour une utilisation dans des opérations ultérieures qui impliquent des ID de document, des handles de chapitre ou de signet valides.
-   En général, la couche supérieure stocke ou affiche ou utilise les données des valeurs de ligne.
-   Pour les valeurs qui ont été marquées comme couches supérieures différées, la valeur est extraite à l’aide de messages CPMFetchValueIn.
-   La description de la recherche est également retournée à la couche supérieure et peut être réutilisée ou examinée par la couche supérieure.

À des fins d’information, si la couche supérieure a demandé des descripteurs aux chapitres et aux signets qui ont été reçus dans les lignes, elle peut effectuer les opérations suivantes :

-   Utilisez CPMGetQueryStatusExIn pour vérifier la progression de l’exécution d’une requête, ainsi que des informations d’État supplémentaires, telles que le nombre de documents filtrés, les documents restants à filtrer, le rapport entre les documents traités par la requête, le nombre total de lignes dans la requête et la position du signet dans l’ensemble de lignes.
-   Utilisez CPMGetNotify pour demander que le serveur informe le client des modifications de l’ensemble de lignes.
-   Utilisez CPMGetApproximatePositionIn pour demander la position approximative d’un signet dans un chapitre.
-   Utilisez CPMCompareBmkIn pour demander une comparaison de deux signets dans un chapitre.
-   Utilisez CPMRestartPositionIn pour que le serveur modifie l’emplacement du curseur au début de l’ensemble de lignes.

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 recevant une réponse CPMFetchValueOut

Lorsque le client reçoit une réponse de message CPMGetRowsOut du serveur, le client doit effectuer les opérations suivantes :

-   Vérifiez si le \_ champ d’État dans l’en-tête indique réussite ou échec. En cas d’échec, notifiez la couche supérieure. Dans le cas contraire, continuez ci-dessous.
-   Vérifiez \_ fValueExist et, s’il a la valeur 0x00000000, informez la couche supérieure que la valeur est introuvable.
-   Sinon, ajoutez \_ cbValue octets de vValue à la valeur de propriété actuelle.
-   Si \_ \_ fMoreExists a la valeur 0x00000001, incrémentez \_ les octets actuels reçus par \_ cbValue et envoyez un message CPMFetchValueIn au serveur, en définissant \_ CbSoFar sur la valeur des octets actuels reçus, \_ cbPropSpec sur zéro et \_ cbChunk sur la taille de la mémoire tampon souhaitée par la couche supérieure.
-   Si \_ fMoreExists a la valeur 0x00000000, indiquez la valeur de propriété de la valeur de propriété actuelle à la couche supérieure.

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 recevant une réponse CPMFreeCursorOut

Lorsque le client reçoit une réponse de message CPMFreeCursorOut réussie du serveur, le client doit renvoyer la \_ valeur cCursorsRemaining à la couche supérieure.

Les informations suivantes sont fournies à des fins d’information uniquement et ne sont pas appliquées par le client CISP. La couche supérieure est supposée effectuer le suivi des poignées de curseur et ne pas utiliser celles qui ont déjà été libérées. Une fois que le nombre de \_ cCursorsRemaining est égal à 0x00000000, la couche supérieure peut utiliser la connexion pour spécifier une autre requête (à l’aide d’un message CPMCreateQueryIn).

### <a name="326-timer-events"></a>Événements de minuterie 3.2.6

Aucun.

### <a name="327-other-local-events"></a>3.2.7 autres événements locaux

Aucun.

## <a name="4-protocol-examples"></a>4 Exemples de protocoles

-   [4,1 exemple 1](#41-example-1)
-   [4,2 exemple 2](#42-example-2)

### <a name="41-example-1"></a>4,1 exemple 1

Dans l’exemple suivant, nous considérons un scénario dans lequel l’utilisateur JOHN sur l’ordinateur A souhaite obtenir la taille des fichiers qui contiennent le mot « Microsoft » à partir de l’ensemble de documents stockés sur le serveur X dans le système de catalogue. supposons que l’ordinateur a exécute un système d’exploitation 32 bits Windows XP et que l’ordinateur X exécute un système d’exploitation 32 bits Windows Server 2003.

1.  L’utilisateur lance une application de recherche et entre dans la requête de recherche. L’application transmet à son tour la requête de recherche au client du protocole.
2.  Le client de protocole établit une connexion avec le serveur d’indexation X. Le client de protocole utilise le \\ canal de canal nommé \\ ci \_ SKADS pour se connecter au serveur X sur SMB.
3.  Le client de protocole prépare ensuite un message CPMConnectIn avec les valeurs suivantes :

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** a la valeur 0x000000C8, ce qui indique qu’il s’agit d’un message CPMConnectIn.
    -   l' **\_ État** est défini sur 0x00000000.
    -   **\_ ulChecksum** contient la somme de contrôle, calculée comme indiqué dans la section 3.2.4.
    -   **\_ ulReserved2** a la valeur 0x00000000.

    Le corps du message est rempli comme suit :

    -   **\_ iClientVersion** est défini sur 0x00000008, ce qui indique que le serveur doit valider le champ de somme de contrôle.
    -   **\_ fClientIsRemote** a la valeur 0x00000001, ce qui indique que le serveur est un serveur distant.
    -   **\_ cbBlob1** est défini sur la taille, en octets, des champs cPropSet, PropertySet1 et PropertySet2 combinés.
    -   **\_ cbBlob2** a la valeur 0x00000004 (ce qui signifie qu’il n’y a pas de jeux de propriétés supplémentaires).
    -   **MachineName** a pour valeur.
    -   Le **nom d’utilisateur** est défini sur John.
    -   **cPropSets** a la valeur 0x00000002.
    -   Le champ **PropertySet1** est de type CDbPropSet. La structure CDbPropSet comprenant le champ PropertySet1 est remplie comme suit :
        -   Le champ **GuidPropSet** est défini sur A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ ext).
        -   le champ **cProperties** est défini sur 0x00000004.
        -   le champ **aProps** est un tableau de structures CDbProp.

            Pour l' **élément \[ aProps \] 0** :

            -   **PropId** a la valeur 0X00000002 (DBPROP \_ ci \_ nom du catalogue \_ ).
            -   **DBPROPOPTIONS** est défini sur 0x0000000.
            -   **DBPROPSTATUS** a la valeur 0x00000000.
            -   Pour l’élément **colid** :
                -   **eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid)
                -   **GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.
                -   **ulID** a la valeur 0x00000000.
            -   Pour l’élément **vValue** :
                -   **vType** est défini sur 0X001F (VT \_ LPWStr).
                -   **vValue** est défini sur « System », le nom du catalogue souhaité.

            Pour l' **élément \[ aProps \] 1** :

            -   **PropId** est défini sur 0x00000007 ( \_ type de \_ requête DBPROP ci \_ )
            -   **DBPROPOPTIONS** est défini sur 0x0000000.
            -   **DBPROPSTATUS** est défini sur to0x00000000.
            -   Pour l’élément **colid** :
                -   **eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).
                -   **GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.
                -   **ulID** a la valeur 0x00000000.
            -   Pour l’élément **vValue** :
                -   **vType** est défini sur 0X0003 (VT \_ I4).
                -   **vValue** a la valeur 0X00000000 (CiNormal), ce qui signifie qu’il s’agit d’une requête normale.

            Pour l' **élément \[ aProps \] 2** :

            -   **PropId** a la valeur 0x00000004 (indicateurs d’étendue d’DBPROP \_ ci \_ \_ ).
            -   **DBPROPOPTIONS** est défini sur 0x0000000.
            -   **DBPROPSTATUS** a la valeur 0x00000000.
            -   Pour l’élément **colid** :
                -   **eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).
                -   **GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.
                -   **ulID** a la valeur 0x00000000.
            -   Pour l’élément **vValue** :
                -   **vType**: 0X1003 (VT \_ Vector \| VT \_ I4)
                -   **vValue**: 0x00000001/0x00000001 (un élément avec la valeur 1), ce qui signifie que les sous-dossiers de recherche

            Pour l' **élément \[ aProps \] 3** :

            -   **PropId**: 0X00000003 (DBPROP \_ ci \_ include include \_ )
            -   **DBPROPOPTIONS**: 0x0000000
            -   **DBPROPSTATUS**: 0x00000000
            -   Pour l’élément **colid** :
                -   **eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).
                -   **GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.
                -   **ulID** a la valeur 0x00000000
            -   Pour l’élément **vValue** :
                -   **vType** est défini sur 0X101F (VT \_ Vector \| VT \_ LPWStr).
                -   **vValue** est défini sur 0x00000001/0x00000002/" \\ " (un élément avec une chaîne de 2 caractères se terminant par un caractère null), ce qui correspond à l’étendue racine.

    -   Le champ **PropertySet2** est de type CDbPropSet.

        La structure CDbPropSet comprenant le champ PropertySet1 est remplie comme suit :

        -   **GuidPropSet** est défini sur AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ ext).
        -   le champ **cProperties** est défini sur 0x00000001.
        -   Le champ **aProps** est un tableau de structures CDbProp.

            Pour l' **élément \[ aProps \] 0** :

            -   **PropId** a la valeur 0X00000002 (DBPROP \_ machine).
            -   **DBPROPOPTIONS** est défini sur 0x0000000.
            -   **DBPROPSTATUS** a la valeur 0x00000000.
            -   Pour l’élément **colid** :
                -   **eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid),
                -   **GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.
                -   **ulID** a la valeur 0x00000000.
            -   Pour l’élément **vValue** :
                -   **vType**: 0X0008 (VT \_ BSTR)
                -   **vValue**: 0x04/"x" (4 octets/chaîne Unicode terminée par un caractère null), signifiant "X"-nom d’un serveur.

    -   le champ **cExtPropSet** est défini sur 0x00000000.
    -   le tableau **aPropertySets** n’existe pas.
    -   Les différents champs de remplissage sont renseignés en fonction des besoins. Le message est envoyé au serveur.

4.  Le serveur vérifie que le **\_ ulChecksum** est correct, vérifie que l’utilisateur est autorisé à effectuer cette demande et répond avec un message CPMConnectOut.

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** a la valeur 0x000000C8, ce qui indique qu’il s’agit d’un message CPMConnectOut.
    -   l' **\_ État** est défini sur 0X0000000 indiquant la réussite.
    -   **\_ ulChecksum** a la valeur 0.
    -   **\_ ulReserved2** a la valeur 0x00000000.

    Le corps du message est rempli comme suit :

    -   le champ **\_ serverVersion** est défini sur 0x00000007 (32 bits Windows XP ou 32 bits Windows Server 2003).
    -   les champs **\_ réservés** sont remplis avec des données arbitraires.

5.  Le client prépare un message CPMCreateQueryIn.

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** a la valeur 0x000000CA, ce qui indique qu’il s’agit d’un message CPMCreateQueryIn.
    -   l' **\_ État** est défini sur 0x00000000.
    -   **\_ ulChecksum** contient la somme de contrôle calculée d’après 3.2.5.
    -   **\_ ulReserved2** a la valeur 0x00000000.

    Le corps du message est rempli comme suit :

    -   Le champ **taille** est défini sur la taille du reste du message.
    -   Le champ **CColumnSetPresent** est défini sur 0x01.
    -   Le champ **ColumnSet** est de type CColumnSet. La structure CColumnSet comprenant ce champ est définie comme suit :
        -   le champ **\_ Count** a la valeur 0x00000001, indiquant qu’une colonne est retournée.
        -   le tableau d' **index** est 0x00000000 et indique la première entrée dans \_ aPropSpec.
    -   Le champ **CRestrictionPresent** est défini sur 0x01, ce qui indique que le champ de **restriction** est présent.
    -   Le champ de **restriction** est de type CRestriction et a la valeur :
        -   **\_ ulType** est défini sur 0x00000004 (RTContent).
        -   **\_ Weight** a la valeur 0x00000000.
    -   Le reste du champ contient une structure CContentRestriction :
        -   La **\_ propriété** est définie sur GUID B725F130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13 qui représente le corps du document.
        -   **\_ CC** est défini sur 0x00000009.
        -   **\_ pwcsphrase** est défini sur la chaîne « Microsoft ».
        -   **\_ LCID** est défini sur 0x40C (pour l’anglais).
        -   **\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).
    -   **CSortPresent** est défini sur 0x00.
    -   **CCategorizationSetPresent** est défini sur 0x00.
    -   **RowSetProperties** est défini comme suit :
        -   **\_ uBooleanOptions** a la valeur 0x00000001 (Sequential).
        -   **\_ ulMaxOpenRows** a la valeur 0x00000000.
        -   **\_ ulMemoryUsage** a la valeur 0x00000000.
        -   \_**cMaxResults** est défini sur 0x00000100 (retourner au maximum 256 lignes).
        -   **\_ cCmdTimeOut** a la valeur 0x00000000 (jamais timeout).
    -   **PidMapper** a la valeur :
        -   **\_ Count** a la valeur 0x00000001.
        -   **\_ aPropSpec** est défini sur GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0x00000001 (pour PRSPEC \_ PROPID)/0x0000000c qui représente la propriété de taille de fichier Windows.

6.  Le serveur le traite et répond avec un message CPMCreateQueryOut.

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** a la valeur 0x000000CA, ce qui indique qu’il s’agit d’un message CPMCreateQueryOut.
    -   l' **\_ État** est défini sur succès.
    -   **\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).
    -   **\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).

    Le corps du message est rempli comme suit :

    -   **\_ fTrueSeqeuntial** a la valeur 0x00000000, ce qui indique que la requête peut utiliser un index.
    -   **\_ fWorkIdUnique** a la valeur 0x00000001.
    -   Le tableau **aCursors** contient un seul élément, représentant un handle de curseur pour cette requête. La valeur dépend de l’état du serveur. Supposons que la valeur retournée est 0xAAAAAAAA.

7.  Le client émet un message de demande CPMSetBindingsIn pour définir le format d’une ligne.

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** a la valeur 0x000000D0, ce qui indique qu’il s’agit d’un message CPMSetBindingsIn.
    -   l' **\_ État** est défini sur succès.
    -   **\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).
    -   **\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).

    Le corps du message est rempli comme suit :

    -   **\_ hCursor** est défini sur 0xAAAAAAAA.
    -   **\_ cbRow** est défini sur 0x10 (suffisamment grand pour tenir les colonnes).
    -   **\_ cbBindingDesc** est défini sur la taille des champs **\_ CColumns** et **\_ aColumns** combinés.
    -   **\_ CColumns** a la valeur 0x00000001.
    -   le tableau **\_ aColumns** est défini de façon à contenir une structure CTableColumn contenant :
    -   -   **\_ PropSpec** est défini sur GUID b725f130-47ef-101a-a5-f1-02608c9eebac/0x00000001 (pour PRSPEC \_ PROPID)/0x0000000c qui représente la propriété de taille de fichier Windows.
        -   **\_ vType** est défini sur 0x0015 (VT \_ UI8).
        -   **\_ ValueUsed** est défini sur 0x01 (colonne transférée dans la ligne).
        -   **\_ ValueOffset** est défini sur 0x0002 (au début de la ligne).
        -   **\_ Value** est défini sur 0x08 (taille d’un UI8 VT \_ ).
        -   **\_ StatusUsed** est défini sur 0x01.
        -   **\_ StatusOffset** est défini sur 0x0A.
        -   **\_ LengthUsed** est défini sur 0x00.

8.  Le serveur le traite et répond avec un message CPMSetBindingsIn.

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** est défini sur 0x000000D0.
    -   l' **\_ État** est défini sur succès.
    -   **\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).
    -   **\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).

9.  Le client émet un message de demande CPMGetRowsIn. Supposons que le client est prêt à accepter 100 lignes à ce stade et qu’il les souhaite dans l’ordre croissant.

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** a la valeur 0x000000CC, ce qui indique qu’il s’agit d’un message CPMGetRowsIn.
    -   l' **\_ État** est défini sur 0x00000000
    -   **\_ ulChecksum** contient la somme de contrôle calculée en fonction de la section 0.
    -   **\_ ulReserved2** a la valeur 0x00000000.

    Le corps du message est rempli comme suit :

    -   **\_ hCursor** est défini sur 0xAAAAAAAA.
    -   **\_ cRowsToTransfer** est défini sur 0x00000064.
    -   **\_ cRowWidth** est défini sur 0x00000010 (à partir des liaisons).
    -   **\_ cbSeek** est défini sur 0x14, qui est la taille des champs ETYPE, \_ Chapt et CRowSeekNext combinés.
    -   **\_ cbReserved** a la valeur 0x18 (0x14 plus \_ cbSeek).
    -   **\_ cbReadBuffer** est défini sur 0x800 (0x64 \* 0x10 est arrondi au multiple suivant de 0x200).
    -   **\_ ulClientBase** a la valeur 0x00000000.
    -   **\_ fBwdfetch** a la valeur 0x00000000, ce qui indique que les lignes doivent être extraites dans l’ordre de transmission.
    -   **ETYPE** a la valeur 0x0000001, ce qui indique que le client souhaite les lignes suivantes.
    -   **\_ Chapt** a la valeur 0 (pas un résultat chapitre).
    -   **SeekDescription** est défini sur CRowSeekNext. La structure CRowSeekNext contient les valeurs suivantes :
        -   **CiTblChapt** a la valeur 0x00000000.
        -   **\_ hRegion** a la valeur 0x00000000.
        -   **\_ cSkip** a la valeur 0, ce qui indique que le client ne souhaite pas ignorer les lignes.

10. Le serveur le traite et répond avec un message CPMGetRowsOut. Supposons que le serveur a trouvé 100 documents qui contiennent le mot « Microsoft ».

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** a la valeur 0x000000CC, ce qui indique qu’il s’agit d’un message CPMGetRowsOut.
    -   l' **\_ État** est défini sur succès.
    -   **\_ ulChecksum** a la valeur 0x00000000.
    -   **\_ ulReserved2** a la valeur 0x00000000.

    Le corps du message est rempli comme suit :

    -   **\_ CRowsReturned** est défini sur 0x00000064.
    -   **ETYPE** a la valeur 0x00000001.
    -   **\_ Chapt** a la valeur 0x00000000 (pas un résultat chapitre).
    -   **SeekDescription** contient une structure CRowSeekNext, remplie comme suit :
        -   **CiTblChapt** a la valeur 0x00000000.
        -   **\_ hRegion** a la valeur 0x00000000.
        -   **\_ cSkip** a la valeur 0, ce qui indique que le client ne souhaite pas ignorer les lignes.
    -   **Lignes** contient la taille des documents 100 qui contiennent le mot « Microsoft ». Étant donné qu’il s’agit de données de taille fixe, elles sont simplement structurées sous la forme d’une liste d’entiers non signés de 100 à 8 octets.

11. Le client envoie un message CPMDisconnect pour mettre fin à la connexion.

    L’en-tête du message est rempli comme suit :

    -   **\_ MSG** a la valeur 0x000000C9, ce qui indique qu’il s’agit d’un message CPMDisconnect.
    -   l' **\_ État** est défini sur 0x00000000.
    -   **\_ ulChecksum** a la valeur 0x00000000.

12. Le serveur traite le message et supprime tous les États du client.

### <a name="42-example-2"></a>4,2 exemple 2

Dans l’exemple précédent, la requête était assez simple. Prenons maintenant une requête légèrement plus complexe. Supposons que l’utilisateur souhaite récupérer la taille des documents qui contiennent les deux mots suivants : « Microsoft » et « Office ». Cela est spécifié en modifiant le champ de restriction contenu dans le message CPMCreateQueryIn envoyé à l’étape 5 comme suit :

Le champ de **restriction** est de type CRestriction et a la valeur :

-   -   **\_ ulType** est défini sur 0x00000004 (RTAnd).
    -   **\_ Weight** a la valeur 0x00000000.

Le reste du champ contient une structure CNodeRestriction :

-   -   **\_ CNode** a la valeur 0x00000002, ce qui indique qu’il existe deux nœuds dans le tableau paNode.
    -   Le champ **\_ paNode** est un tableau de deux structures CRestriction.

        **\_ paNode \[ 0 \]** contient :

        -   -   **\_ ulType** est défini sur 0x00000004 (RTContent).
            -   **\_ Weight** a la valeur 0x00000000.
            -   Le reste du champ contient une structure CContentRestriction :
                -   La **\_ propriété** est définie sur GUID b725f130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13.
                -   **\_ CC** est défini sur 0x00000009.
                -   **\_ pwcsphrase** est défini sur la chaîne « Microsoft ».
                -   **\_ LCID** est défini sur 0x40C (pour l’anglais).
                -   **\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).

        **\_ paNode \[ 1 \]** contient :

        -   -   **\_ ulType** est défini sur 0x00000004 (RTContent).
            -   **\_ Weight** a la valeur 0x00000000.
            -   Le reste du champ contient une structure CContentRestriction :
                -   La **\_ propriété** est définie sur GUID b725f130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13.
                -   **\_ CC** est défini sur 0x00000006.
                -   **\_ pwcsphrase** est défini sur la chaîne « Office ».
                -   **\_ LCID** est défini sur 0x40C (pour l’anglais).
                -   **\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).

## <a name="5-security"></a>5 Sécurité

### <a name="51-security-considerations-for-implementers"></a>5.1 Considérations relatives à la sécurité pour les implémenteurs

Les implémentations d’indexation qui permettent d’indexer du contenu sécurisé doivent envisager d’utiliser le contexte utilisateur fourni par SMB \[ MS-SMB \] pour supprimer les résultats de recherche et retourner uniquement ceux accessibles à l’appelant.

### <a name="52-index-of-security-parameters"></a>5.2 Index de paramètres de sécurité



| Paramètre de sécurité  | Section |
|---------------------|---------|
| Niveau d'emprunt d'identité | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6 index du comportement spécifique à la version



| Comportement spécifique à la version                                                                         | Section   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| ce protocole est implémenté sur Windows 2000, Windows XP, Windows Server 2003 et Windows Vista. | 1.3.2     | X            | X          | X                   |
| Les applications interagissent généralement avec un wrapper d’interface OLE DB                                  | 1.4       | X            | X          | X                   |
| Valeurs NTSTATUS                                                                                   | 1.8       | X            | X          | X                   |
| Le client définit le \_ champ d’État dans chaque en-tête de message.                                        | 2.2.2     | X            | X          | X                   |
| la valeur de cPendingScans est généralement zéro                                                               | 2.2.3.1   | X            | X          | X                   |
| valeur iClientVersion                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_valeur cbChunk                                                                                   | 2.2.3.19  | X            | X          | X                   |
| adresses mémoire 32 bits et 64 bits                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 





