---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d858294c5647e62d1eb949b3fa336d3dcc513a9a374443e0fe9621f1721800
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986539"
---
# <a name="a-volume-shadow-copy-service"></a>A (Service VSS)

A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Événement d’abandon**
</dt> <dd>

Événement VSS émis par le Service VSS indiquant qu’une opération de restauration ou de sauvegarde conforme a été abandonnée. Le gestionnaire d’événements est **CVssWriter :: OnAbort**.

</dd> <dt>

<span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**
</dt> <dd>

Active Directory Service (ADSI) est un service basé sur COM qui fournit un mécanisme de localisation, d’identification et d’accès aux utilisateurs et aux ressources disponibles dans un système d’environnement informatique distribué. en particulier, le service Active Directory est utilisé pour gérer les informations d’annuaire d’entreprise en vue de leur distribution par un serveur de domaine Windows.

</dd> <dt>

<span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**mappage d’emplacement secondaire**
</dt> <dd>

Chemin d’accès, autre que le chemin d’accès d’origine d’un fichier, dans lequel le fichier peut être restauré dans certaines conditions. En règle générale, les mappages d’emplacements de substitution ne sont pas définis pour un seul fichier bien défini, mais pour une paire chemin/spécification de fichier, et peuvent être récursifs.

Un autre mappage d’emplacement est utilisé uniquement au cours d’une opération de restauration et ne doit pas être confondu avec un autre chemin d’accès, qui est utilisé uniquement pendant une opération de sauvegarde. Consultez également *chemin alternatif*.

</dd> <dt>

<span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**autre chemin d’accès**
</dt> <dd>

Pendant les opérations de sauvegarde, une paire chemin/spécification de fichier (gérée par une instance de l’interface **IVssWMFiledesc** ) est considérée comme ayant un chemin alternatif si son descripteur de fichier (tel que retourné par **IVssWMFiledesc :: GetAlternateLocation**) est non null. C’est à partir de ce chemin d’accès, au lieu du chemin d’accès spécifié par défaut, que les fichiers doivent être copiés lorsqu’un volume est sauvegardé.

Un autre chemin d’accès est utilisé uniquement pendant une opération de sauvegarde et ne doit pas être confondu avec un autre mappage d’emplacement. Un mappage d’emplacement de remplacement est utilisé uniquement pendant les opérations de restauration. Voir aussi *mappage d’emplacements alternatifs*.

</dd> <dt>

<span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**niveau de l’application**
</dt> <dd>

Utilisé par VSS pour indiquer le point au cours de la création d’un cliché instantané qu’un enregistreur est averti d’un gel. Voir aussi [*applications de niveau*](vssgloss-b.md)principal, [*figer*](vssgloss-f.md), [*applications frontales*](vssgloss-f.md), clichés [*instantanés*](vssgloss-s.md), [*applications au niveau système*](vssgloss-s.md), [*enregistreur*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**cliché instantané récupéré automatiquement**
</dt> <dd>

Cliché instantané qui a été traité par un enregistreur pour être dans un état totalement cohérent pour les actions de sauvegarde ou d’exploration de données (par exemple, pour restaurer toutes les transactions qui n’ont pas encore été effectuées au point où le cliché instantané a été créé). Cela peut être initié par un enregistreur en spécifiant un indicateur approprié à partir de l’énumération des **\_ \_ indicateurs du composant VSS** dans le membre **dwComponentFlags** de la structure **VSS \_ COMPONENTINFO** ou par un demandeur en ajoutant l’indicateur de **\_ récupération VSS VOLSNAP \_ attr \_ Rollback \_ Recovery** au contexte du cliché instantané. La récupération automatique permet d’utiliser les données de clichés instantanés sur un volume en lecture seule, pour l’exploration de données, des restaurations partielles (par exemple, des éléments sélectionnés dans une base de données) ou d’autres fins.

Voir aussi cliché [*instantané transportable*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**cliché instantané de la mise en sortie automatique**
</dt> <dd>

Cliché instantané qui sera supprimé à la fin d’une opération de sauvegarde. Par programmation, cela signifie que le cliché instantané sera supprimé lors de la libération de l’interface **IVssBackupComponents** . Un cliché instantané de mise en sortie automatique ne peut pas être persistant.

Par défaut, tous les clichés instantanés sont en sortie automatique. Voir aussi cliché [*instantané persistant*](vssgloss-p.md), cliché [*instantané transportable*](vssgloss-t.md).

</dd> </dl>

 

 



