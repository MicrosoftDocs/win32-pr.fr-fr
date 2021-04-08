---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751556"
---
# <a name="c-volume-shadow-copy-service"></a>C (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**autorité de certification**
</dt> <dd>

Entité approuvée pour émettre des certificats qui déclarent que le destinataire individuel, l’ordinateur ou l’organisation qui demande le certificat répond aux conditions d’une stratégie établie.

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**cliché instantané accessible par le client**
</dt> <dd>

Cliché instantané créé par le fournisseur système pour prendre en charge clichés instantanés pour dossiers partagés et d’autres mécanismes de restauration, qui permettent aux clients de voir les anciennes versions des fichiers et d’annuler des erreurs sans nécessiter de restauration complète. Un cliché instantané accessible par le client est créé à l’aide de la valeur accessible par le **\_ \_ client \_ CTX VSS** de l’énumération du [**\_ \_ \_ contexte de capture instantanée VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) . En outre, la \_ \_ \_ valeur accessible par le client VSS VOLSNAP attr \_ de l’énumération des [**\_ \_ attributs d' \_ instantané \_ de volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) est définie automatiquement pour les clichés instantanés accessibles par le client. Voir aussi [*clichés instantanés pour dossiers partagés*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**-**
</dt> <dd>

Groupe de fichiers, défini par un enregistreur, qui doit être traité comme une unité lors des opérations de sauvegarde et de restauration. Voir aussi [*composant de base de données*](vssgloss-d.md), [*composant de groupe de fichiers*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dépendance de composant**
</dt> <dd>

Une situation dans laquelle un composant (et le jeu de composants qu’il définit) géré par un enregistreur ne peut pas être sauvegardée ou restaurée indépendamment des composants gérés par d’autres rédacteurs. Une dépendance n’indique pas un ordre de préférence entre le composant avec les dépendances documentées et les composants dont il dépend : une dépendance indique simplement que le composant et les composants dont il dépend doivent toujours être sauvegardés ou restaurés ensemble.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**mode composant**
</dt> <dd>

Mode dans lequel une opération de sauvegarde ou de restauration utilise les informations de composant d’un enregistreur. Voir aussi [*composant sélectionnable*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**ensemble de composants**
</dt> <dd>

Groupe de composants avec au moins un composant sélectionnable (pour la sauvegarde ou la restauration) et un certain nombre de composants non sélectionnables organisés dans une hiérarchie par leurs chemins logiques. La participation implicite à une opération de sauvegarde ou de restauration dépend de l’inclusion explicite du composant sélectionnable de niveau supérieur. Seules les informations sur les composants de ce composant sélectionnable sont incluses dans le document sur les composants de sauvegarde. Un jeu de composants peut inclure des sous-composants sélectionnables et non sélectionnables. Voir aussi [*chemin logique*](vssgloss-l.md), [*composant sélectionnable*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**cliché instantané de copie en écriture**
</dt> <dd>

Cliché instantané créé en enregistrant uniquement les différences par rapport au volume d’origine.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**État de cohérence des incidents**
</dt> <dd>

État des disques équivalant à ce qui serait trouvé à la suite d’une défaillance catastrophique qui arrête brusquement le système. Une restauration à partir d’un tel jeu de clichés instantanés équivaut à un redémarrage après un arrêt brutal. Il s’agit de l’État par défaut des données qui ont été copiées par des clichés instantanés sans la prise en charge des enregistreurs.

</dd> </dl>

 

 



