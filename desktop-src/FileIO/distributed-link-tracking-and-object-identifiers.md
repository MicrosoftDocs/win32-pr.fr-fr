---
description: Le service de suivi de lien distribué permet aux applications clientes de suivre les sources de liens qui ont été déplacées.
ms.assetid: 6f438c72-f23d-4ca4-83bd-fe3bc433ceeb
title: Suivi des liaisons distribuées et identificateurs d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d28e151c21fd5320a41950be7647c1e8e0a88b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106523163"
---
# <a name="distributed-link-tracking-and-object-identifiers"></a>Suivi des liaisons distribuées et identificateurs d’objets

Le stockage d’une référence à un fichier ou à un répertoire à l’aide de son chemin d’accès et de son nom de fichier n’est pas fiable. Si un utilisateur renomme un fichier, il arrête les liens vers le fichier. Si un utilisateur renomme le répertoire, il arrête les liens vers le fichier, ainsi que tous les fichiers et sous-répertoires de l’arborescence de répertoires.

Le **service de suivi de lien distribué** permet aux applications clientes de suivre les sources de liens qui ont été déplacées. Les clients qui s’abonnent au service de suivi des liaisons peuvent préserver l’intégrité de leurs références, et les objets peuvent être suivis d’une manière transparente pour l’utilisateur.

## <a name="object-identifiers"></a>Identificateurs d'objet

Le service de suivi de lien conserve son lien vers un objet à l’aide d’un **identificateur d’objet (ID)**. Un ID d’objet est un attribut facultatif qui identifie de façon unique un fichier ou un répertoire sur un volume.

Un index de tous les ID d’objet est stocké sur le volume. Les opérations de renommage, de sauvegarde et de restauration préservent les ID d’objet. Toutefois, les opérations de copie ne conservent pas les ID d’objet, car cela violerait leur unicité.

Vous pouvez effectuer les opérations suivantes sur les ID d’objet :

-   Création
-   Suppression
-   Requête

Lorsque vous créez un ID d’objet, vous établissez l’identité du fichier dans le service de suivi des liaisons. Inversement, lorsque vous supprimez un ID d’objet, le service de suivi des liaisons arrête de conserver les liens vers le fichier. Pour obtenir la liste des codes de contrôle du système de fichiers qui effectuent des opérations sur les ID d’objet, consultez [codes de contrôle de gestion de fichiers](file-management-control-codes.md).

Le service de suivi de lien distribué effectue le suivi des sources de liens pour les raccourcis de Shell et les liens OLE au sein des volumes de système de fichiers NTFS. Le client Link peut résoudre un lien rompu avec des informations mises à jour sur le nouvel emplacement de la source du lien.

## <a name="link-tracking-features"></a>Fonctionnalités de suivi des liens

Les raccourcis de Shell incluent le suivi de lien heuristique qui utilise un algorithme de recherche d’arborescence pour rechercher une correspondance pour une source de lien déplacée. L’algorithme de recherche est basé sur le dernier chemin d’accès connu du fichier et les informations sur le fichier qui incluent la date de création, la taille du fichier, ainsi que le nom et l’extension du fichier.

La liaison OLE comprend le même suivi de lien heuristique. Windows comprend également le même suivi de lien heuristique avec des améliorations supplémentaires pour la recherche des espaces de noms afin de produire des résultats dans certains scénarios courants. Les améliorations incluent la procédure suivante qui dépend des limites de temps imposées par une application cliente.

**Pour rechercher des espaces de noms**

1.  Recherchez quatre niveaux de répertoires en dessous du dernier répertoire.
2.  Remonter d’un répertoire et répéter les étapes 1 et 2 à trois reprises, ce qui peut générer des résultats si l’objet a été déplacé à proximité.
3.  Rechercher quatre niveaux en dessous de la racine du bureau, ce qui peut donner des résultats si l’objet a été déplacé vers un emplacement sur le même bureau.
4.  Recherchez quatre niveaux en dessous de la racine sur chaque lecteur fixe local.
5.  Répétez les étapes 1-3 sans la limite de quatre répertoires.

> [!Note]  
> Ces modèles de suivi de lien sont transparents pour l’utilisateur final. Toutefois, ils ne produisent pas toujours des résultats positifs et peuvent prendre du temps.

 

Pour plus d’informations sur les raccourcis de l’interpréteur de commandes, consultez [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka).

Pour plus d’informations sur les liaisons OLE, consultez [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink).

Si un lien est créé vers un fichier au format NTFS 3,0 ou version ultérieure et que le fichier est déplacé vers un autre volume avec NTFS 3,0 ou version ultérieure dans le même domaine, le fichier peut être trouvé par le service de suivi, sous réserve de considérations relatives à l’heure. En outre, si le fichier est déplacé en dehors du domaine ou au sein d’un groupe de travail, il est trouvé.

Pour obtenir la version NTFS d’un volume, ouvrez une invite de commandes avec des droits d’accès administrateur et exécutez la commande suivante :

**fsutil fsinfo NTFSInfo** *X * * * :**

où *X* est la lettre de lecteur du volume.

Lorsqu’un lien est créé dans un fichier, le fichier cible est considéré comme la **source** de la liaison et le créateur du lien est le **client de liaison**. Par exemple, si un raccourci de l’interpréteur de commandes est créé pour créer un lien vers un document texte, le document texte est la source du lien et le raccourci de l’interpréteur de commandes est le client de liaison.

Le service de suivi de lien distribué conserve les liens de fichiers pour les situations suivantes qui se produisent dans un domaine :

-   Le fichier source du lien est déplacé d’un volume de système de fichiers NTFS vers un autre au sein du même domaine.
-   Le nom de l’ordinateur qui contient la source du lien est renommé.
-   Les partages réseau sur l’ordinateur source de la liaison sont modifiés.
-   Le volume qui contient le fichier source du lien est déplacé vers un autre ordinateur au sein du même domaine.

Le service de suivi de lien distribué tente également de conserver des liens dans les situations précédentes, même s’ils ne se produisent pas dans un domaine, autrement dit s’ils sont inter-domaines ou au sein d’un groupe de travail. Dans ces situations, les liens peuvent toujours être conservés lorsque le partage réseau sur l’ordinateur source du lien est modifié. Elles peuvent également être conservées quand une source de liaison est déplacée sur un ordinateur. Les liens peuvent généralement être conservés lorsque la source de la liaison est déplacée vers un autre ordinateur, mais cette forme de suivi est moins fiable dans le temps.

## <a name="link-tracking-functionality"></a>Fonctionnalité de suivi des liens

La fonctionnalité de suivi de lien est implémentée principalement sous la forme des deux services système suivants :

-   Client de suivi de liaisons distribuées
-   Serveur de suivi de lien distribué

<dl> <dt>

<span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>Client de suivi de lien distribué
</dt> <dd>

Le client de suivi de lien distribué s’exécute sur tous les ordinateurs et gère les activités de suivi des liaisons pour cet ordinateur. Ces activités incluent la recherche de sources de liens et le traitement des déplacements de source de lien. Lorsqu’une source de lien est déplacée, le service transmet des informations au serveur de suivi de lien distribué qui s’exécute sur les contrôleurs de domaine.

</dd> <dt>

<span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>Serveur de suivi de lien distribué
</dt> <dd>

Le serveur de suivi de lien distribué s’exécute sur chaque contrôleur de domaine dans un domaine. Le service accepte les notifications de déplacement de fichiers et de volumes à partir du service de suivi sur un ordinateur, et permet au client de suivi de liaison distribuée d’interroger l’emplacement actuel d’une source de liaison.

Ce service serveur conserve les informations dans les contrôleurs de domaine sur les volumes et les fichiers qui ont été déplacés. Les informations sur les déplacements ne peuvent pas augmenter au-delà d’une taille spécifique et sont automatiquement supprimées si elles deviennent inutiles.

</dd> </dl>

Les services de suivi de lien sont exposés par les interfaces [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) et [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) . Par conséquent, ils sont utilisés par les raccourcis de l’interpréteur de commandes. Lorsque la méthode [**IShellLink :: Resolve**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) est appelée et que le fichier référent est introuvable, par exemple, lorsque l’utilisateur active un raccourci de l’interpréteur de commandes, le service de suivi est appelé automatiquement pour rechercher le fichier. De même, lorsque l’implémentation de [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) ne peut pas trouver de fichier, par exemple, dans sa méthode [**BindToSource**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) , elle appelle automatiquement sur le service de suivi.

## <a name="link-tracking-limitations"></a>Limitations du suivi des liens

Les services de suivi de lien distribué ne sont disponibles que sur le système de fichiers NTFS et sont disponibles uniquement pour les sources de liens sur NTFS 3,0 ou version ultérieure. Par conséquent, si une source de liaison est déplacée vers un volume de système de fichiers FAT, les informations de suivi sont perdues. En outre, si une source de liaison est déplacée entre le système de fichiers NTFS 3,0 ou version ultérieure, mais que l’ordinateur qui effectue le déplacement exécute une version antérieure de Windows, les informations de suivi de lien sont perdues. Lorsque les informations de suivi de lien sont perdues, aucun dommage n’est fait au fichier source de liaison lui-même, il n’est tout simplement pas suivi par les services de suivi de lien distribué.

Pour obtenir la version NTFS d’un volume, ouvrez une invite de commandes avec des droits d’accès administrateur et exécutez la commande suivante :

**fsutil fsinfo NTFSInfo** *X * * * :**

où *X* est la lettre de lecteur du volume.

Les liens vers des fichiers sur des supports amovibles ne sont pas conservés. En outre, le service de suivi ne reconnaît pas un nouveau volume de système de fichiers NTFS tant que le système n’a pas redémarré. Un nouveau volume peut devenir disponible en raison du repartitionnement, du reformatage d’un volume de système de fichiers FAT dans le système de fichiers NTFS ou de la connexion d’un nouveau lecteur externe.

 

 
