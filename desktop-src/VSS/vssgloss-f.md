---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751541"
---
# <a name="f-volume-shadow-copy-service"></a>F (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**composant de groupe de fichiers**
</dt> <dd>

Groupe de fichiers autres que ceux utilisés comme base de données et définis par un enregistreur comme ayant besoin d’être gérés comme une unité lors des opérations de sauvegarde et de restauration. Voir aussi [*composant*](vssgloss-c.md), [*composant base de données*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**jeu de fichiers**
</dt> <dd>

Combinaison d’un chemin d’accès, d’une spécification de fichier et d’un indicateur récursif décrivant un fichier ou un groupe de fichiers. Par exemple, les fichiers sont ajoutés aux composants dans les jeux de fichiers.

Sauf indication contraire, les chemins d’accès d’un jeu de fichiers sont des chemins d’accès Windows standard et peuvent contenir des variables d’environnement (par exemple,% SystemRoot%) mais ne peut pas contenir de caractères génériques. Il n’est pas nécessaire que le chemin d’accès se termine par une barre oblique inverse (« \\ »). Il s’agit des applications qui récupèrent ces informations pour les vérifier.

La spécification de fichier contenue dans un jeu de fichiers indique le nom du ou des fichiers qu’il contient. Cette spécification de fichier ne peut pas contenir de spécifications de répertoire (par exemple, aucune barre oblique inverse), mais peut contenir le ? et les \* caractères génériques.

La balise récursive est une valeur booléenne qui spécifie si le chemin d’accès du jeu de fichiers doit être traité comme un seul répertoire ou s’il indique une hiérarchie de répertoires à traverser de manière récursive. La valeur booléenne est **true** si le chemin d’accès est traité comme une hiérarchie de répertoires à parcourir de manière récursive, ou **false** dans le cas contraire.

Les informations relatives à un jeu de fichiers sont retournées via des instances de l’interface **IVssWMFiledesc** . elles peuvent contenir des chemins d’accès alternatifs, des mappages d’emplacement de remplacement et des paramètres de prise en charge de schéma au niveau du fichier.

Voir aussi [*chemin alternatif*](vssgloss-a.md), [*mappage d’emplacement secondaire*](vssgloss-a.md), [*composant*](vssgloss-c.md), *spécification de fichier*.

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**spécification de fichier**
</dt> <dd>

Utilisé pour faire correspondre des fichiers dans un répertoire et pour définir un jeu de fichiers. Elle ne peut pas contenir de spécifications de répertoire (par exemple, aucune barre oblique inverse), mais elle peut contenir le ? et les \* caractères génériques.

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Service de réplication de fichiers**
</dt> <dd>

Utilisé pour répliquer des fichiers système dans un répertoire de volume système (SysVol) redondant pour prendre en charge la survie du système de fichiers, en particulier pour les systèmes de fichiers distribués.

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**antigel**
</dt> <dd>

Un laps de temps pendant le processus de création de clichés instantanés lorsque tous les enregistreurs ont vidé leurs écritures sur les volumes et ne lancent pas d’écritures supplémentaires.

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Figer l’événement**
</dt> <dd>

Événement VSS indiquant qu’un blocage de cliché instantané est en cours. Voir aussi *figer*, [*cliché instantané*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**applications de niveau frontal**
</dt> <dd>

Indique le point auquel un writer est notifié d’un gel par VSS. Les enregistreurs qui ont été initialisés en tant qu’applications de niveau frontal sont avertis avant l’initialisation des Writers en tant qu’applications de niveau principal ou application système. Voir aussi [*niveau application*](vssgloss-a.md), [*applications de niveau*](vssgloss-b.md)principal, [*applications système*](vssgloss-s.md), [*enregistreur*](vssgloss-w.md).

</dd> </dl>

 

 



