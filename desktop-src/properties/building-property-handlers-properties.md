---
description: Les propriétés sont représentées par des ID connus sous le nom d’identificateurs de propriété (PID).
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Fonctionnement des gestionnaires de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564d6f8bd325e649ff1356869932521d8c1cd885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202241"
---
# <a name="understanding-property-handlers"></a>Fonctionnement des gestionnaires de propriétés

Les propriétés sont représentées par des ID connus sous le nom d’identificateurs de propriété (PID). Chaque propriété doit avoir un identificateur global unique (GUID). Cet identificateur se compose d’un GUID qui représente une collection de propriétés appelée un jeu de propriétés plus une chaîne ou un entier 32 bits pour identifier la propriété dans le jeu. Si la forme entière de ID est utilisée, les valeurs 0x00000000, 0xFFFFFFFF et 0xFFFFFFFE sont considérées comme non valides. Les fournisseurs peuvent garantir que leurs propriétés sont définies de manière unique en les plaçant dans un jeu de propriétés défini par leurs propres GUID.

> [!IMPORTANT]
> Il est essentiel de définir des propriétés avec soin et de façon stratégique pour la première version du schéma. Les modifications apportées aux propriétés personnalisées (telles que la largeur de colonne ou le type de propriété) ne sont pas reflétées dans la base de données après l’inscription d’un schéma. La seule façon de faire en sorte que ces modifications soient reconnues après que le schéma a été inscrit une seule fois sur un système serait de reconstruire l’index, puis d’inscrire le nouveau schéma, ou d’inscrire le schéma, puis de créer une nouvelle propriété (qui se compose d’un nom canonique et d’un type de fichier) pour chaque version de subequent. par exemple `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , et ainsi de suite). Nous vous déconseillons de créer de nouvelles propriétés de cette manière, car plusieurs colonnes superflues peuvent avoir un impact sur les performances du système.

 

Cette rubrique est organisée comme suit :

-   [Métadonnées](#metadata)
    -   [Ouvrir les métadonnées](#open-metadata)
-   [À propos des gestionnaires de propriétés](#about-property-handlers)
-   [Technologie héritée](#legacy-technology)
-   [Rubriques connexes](#related-topics)

## <a name="metadata"></a>Métadonnées

Dans Windows Vista et versions ultérieures, un nouveau système de propriétés basé sur les métadonnées est essentiel à l’Organisation des éléments tels que les fichiers, le courrier électronique et les contacts. Dans ce nouveau système de propriétés, les éléments peuvent être recherchés en fonction de leurs métadonnées, et les utilisateurs peuvent lire ou écrire ces métadonnées. Les métadonnées de ce système sont représentées par un ensemble extensible de *Propriétés* implémentées en tant que paires nom/valeur.

Dans Windows Vista et versions ultérieures, un ensemble complet de propriétés couvre les spécificités des éléments tels que les photos, la musique, les documents, les messages, les contacts et les fichiers. Les éditeurs de logiciels indépendants (ISV) peuvent introduire leurs propres propriétés sur la plateforme si aucune propriété existante ne répond à leurs besoins.

### <a name="open-metadata"></a>Ouvrir les métadonnées

Le système de propriétés dans Windows Vista et les versions ultérieures est un système de métadonnées ouvert. Un format de fichier stocke toute propriété qui lui est assignée et expose cette valeur lorsqu’elle est interrogée, indépendamment de sa pertinence ou de sa signification. Cela permet aux développeurs tiers d’attacher des propriétés supplémentaires au fichier sans qu’il soit nécessaire de modifier le gestionnaire de propriétés associé. Les métadonnées ouvertes sont un concept puissant. Pour plus d’informations sur la prise en charge des métadonnées ouvertes pour un format de fichier XML, consultez « prise en charge des métadonnées ouvertes » dans [initialisation des gestionnaires de propriétés](./building-property-handlers-property-handlers.md).

> [!Note]  
> Les gestionnaires de propriétés sont toujours associés à des types de fichiers spécifiques ; ainsi, si votre format de fichier contient des propriétés qui nécessitent un gestionnaire de propriétés personnalisées, vous devez toujours inscrire une extension de nom de fichier unique pour chaque format de fichier.

 

## <a name="about-property-handlers"></a>À propos des gestionnaires de propriétés

Dans Windows Vista et versions ultérieures, Windows dispose d’un système de propriétés extensible pour le stockage et la récupération des métadonnées dans les fichiers et les éléments de données auxquels vous accédez. L’Explorateur Windows et le système de recherche Windows, ainsi que d’autres applications, utilisent des gestionnaires de propriétés pour lire et modifier ces métadonnées. Si vous êtes un développeur qui possède un type de fichier spécifique, vous devez inscrire un gestionnaire de propriétés pour permettre au système de propriétés d’accéder aux métadonnées de vos fichiers. Dans certains cas, vous pourrez peut-être utiliser un gestionnaire de propriétés existant capable de lire et de comprendre votre format de fichier et ses propriétés. dans d’autres cas, vous devrez peut-être développer un nouveau gestionnaire de propriétés pour votre type de fichier.

La première étape de l’écriture d’un gestionnaire de propriétés consiste à prendre en compte les propriétés prises en charge par votre type de fichier. Les valeurs de propriété sont stockées dans le flux de fichier, principalement pour permettre la transporter. Lorsque les valeurs de propriété sont stockées dans le fichier lui-même, comme elles sont dans ce système, un utilisateur peut copier un fichier vers un autre ordinateur, un disque mémoire flash USB ou un autre système de fichiers, ou envoyer le fichier sous la forme d’une pièce jointe de courrier électronique, les propriétés voyagent avec le fichier et ne sont jamais désynchronisées ou perdues. Par conséquent, si le format de fichier prend en charge le stockage d’informations supplémentaires, il est préférable de stocker les propriétés dans le fichier lui-même.

L’étape suivante consiste à déterminer les propriétés que le fichier doit fournir. Vous pensez peut-être à l’origine qu’un ensemble limité de propriétés est adéquat. Un fichier audio peut uniquement prendre en charge les propriétés audio et se terminer. Toutefois, ce fichier audio peut être un enregistrement d’une session d’une Cour de justice, archivé par un cabinet d’avocats. Dans ce cas, le cabinet juridique souhaiterait certainement associer d’autres propriétés non audio à ce fichier, comme le numéro de cas. Le fournisseur du format de fichier audio ne peut pas nécessairement déterminer tous les scénarios dans lesquels son format sera utilisé. Ils doivent donc envisager d’activer le stockage global de toute propriété arbitraire prise en charge par le système de propriétés.

## <a name="legacy-technology"></a>Technologie héritée

La technologie de flux secondaire du système de fichiers Microsoft Windows NT (NTFS) a été développée pour prendre en charge la persistance des informations supplémentaires avec le fichier via un autre flux de données au niveau de la couche du système de fichiers. Il peut se demander pourquoi ces flux secondaires ne sont pas utilisés comme méthode principale pour stocker des propriétés, en particulier avec la prise en charge des métadonnées ouvertes. La raison principale est le transport de ces informations supplémentaires. Malheureusement, ces flux alternatifs sont supprimés dans de nombreux scénarios, notamment la prise en charge de la mise en cache côté client (CSC), l’envoi de fichiers en tant que pièces jointes et la copie de fichiers dans un magasin non NTFS.

Les flux secondaires ne fournissent pas une solution robuste dans laquelle les propriétés sont assurées de se déplacer avec le fichier. par conséquent, le système de propriétés Windows Vista ne fournit pas de mécanisme intégré qui exploite les flux de données NTFS secondaires pour le stockage des propriétés. Les éditeurs de logiciels indépendants sont également fortement déconseillés de créer des gestionnaires de propriétés qui utilisent des flux secondaires pour le stockage des propriétés. Bien entendu, il existe des scénarios dans lesquels les flux de données secondaires NTFS sont appropriés, en particulier lorsque les applications peuvent garantir que le fichier avec lequel elles sont gérées est toujours stocké dans un volume NTFS et ne se déplace pas à la suite de l’interaction de l’utilisateur final.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des noms de genres](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Utilisation des listes de propriétés](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisation des gestionnaires de propriétés](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Inscription et distribution des gestionnaires de propriétés](./prophand-reg-dist.md)
</dt> <dt>

[Meilleures pratiques pour le gestionnaire de propriétés et FAQ](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
