---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526266"
---
# <a name="w-volume-shadow-copy-service"></a>W (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z

<dl> <dt>

<span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Protection des fichiers Windows**
</dt> <dd>

Service système qui protège les fichiers de système d’exploitation spéciaux. Si l’un de ces fichiers est supprimé ou remplacé, la protection des fichiers Windows remplace le fichier par le cache d’origine.

</dd> <dt>

<span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**écrit**
</dt> <dd>

Application qui coordonne ses opérations d’e/s avec cliché instantané VSS et les opérations associées aux clichés instantanés (telles que les sauvegardes et restaurations) afin que les données contenues sur le volume cliché instantané soient dans un état cohérent.

Pour prendre en charge cette coordination, un enregistreur doit implémenter une instance d’une classe dérivée de la classe de base abstraite **CVssWriter** pour communiquer avec l’infrastructure VSS. Voir aussi cliché [*instantané*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**classe Writer**
</dt> <dd>

Identificateur global unique (GUID) fourni par un enregistreur pendant l’initialisation pour indiquer qu’il appartient à un type donné d’enregistreurs. Par exemple, plusieurs implémentations d’un writer peuvent partager le même ID de classe de writer.

Les writers de la même classe peuvent être distingués par leurs instances de writer. Il revient à un développeur d’applications de spécifier des classes d’enregistreur. Voir aussi *instance* de l’enregistreur.

</dd> <dt>

<span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**instance d’enregistreur**
</dt> <dd>

Identificateur global unique (GUID) fourni par VSS pour chaque processus d’écriture exécuté sur un système. Une valeur unique pour l’instance du writer est générée à chaque démarrage de l’enregistreur.

</dd> <dt>

<span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Document de métadonnées de l’enregistreur**
</dt> <dd>

Document XML créé par un enregistreur (à l’aide de l’interface **IVssCreateWriterMetadata** ) contenant des informations sur l’État et les composants du writer. Un demandeur peut interroger des documents de métadonnées de l’enregistreur (à l’aide de l’interface **IVssExamineWriterMetadata** ) lors d’une opération de restauration ou de sauvegarde.

Un document de métadonnées de l’enregistreur contient la liste de tous les composants d’un enregistreur, chacun d’entre eux pouvant participer à une sauvegarde. Cela diffère du document sur les composants de sauvegarde du demandeur, qui contient uniquement les composants explicitement inclus pour une opération de sauvegarde ou de restauration.

Une fois construit, le document de métadonnées de l’enregistreur doit être affiché en tant qu’objet en lecture seule. Il peut être enregistré sur le disque. Voir aussi [*document*](vssgloss-b.md)sur les composants de sauvegarde, [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).

</dd> </dl>

 

 



