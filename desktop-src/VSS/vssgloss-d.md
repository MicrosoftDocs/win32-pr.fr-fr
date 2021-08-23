---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3910a2fb09688e26b33b586f4558c05cb804688645486dfec751c9839fcff278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998029"
---
# <a name="d-volume-shadow-copy-service"></a>D (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**composant base de données**
</dt> <dd>

Groupe de fichiers utilisé par une base de données et défini par un enregistreur comme devant être traité comme une unité lors des opérations de sauvegarde et de restauration. Voir aussi [*composant*](vssgloss-c.md), [*composant de groupe de fichiers*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**fournisseur par défaut**
</dt> <dd>

Consultez [*fournisseur système*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**clichés instantanés supprimés**
</dt> <dd>

Les clichés instantanés supprimés ne sont pas accessibles et ne doivent pas être rendus accessibles à l’avenir.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**dépendance**
</dt> <dd>

Consultez [*dépendance des composants*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**objet appareil**
</dt> <dd>

Chaîne indiquant la « racine » d’un volume de clichés instantanés. Les fichiers et les répertoires sur un volume de clichés instantanés peuvent être référencés en ajoutant au début de la chaîne de l’objet périphérique un chemin d’accès correspondant sur le volume d’origine. Comme le membre **m \_ pwszSnapshotDeviceObject** de la structure [**\_ \_ prop instantanés VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , l’objet appareil n’a pas de barre oblique inverse (« \\ »).

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**zone diff**
</dt> <dd>

Emplacement sur le volume où les *données différentielles* sont stockées. Il s’agit également de l’espace de stockage des clichés instantanés.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**fichiers différenciés**
</dt> <dd>

Fichiers impliqués dans une opération de sauvegarde incrémentielle ou différentielle implémentée par la mise à jour de fichiers entiers (par opposition à la modification de sections de ces fichiers à l’aide de la prise en charge partielle des fichiers). Par exemple, si vous souhaitez implémenter une sauvegarde différentielle, un fichier entier (au lieu de la section modifiée uniquement) est copié sur un support de sauvegarde, ce fichier est un fichier différent. Voir aussi [*opérations de sauvegarde incrémentielle*](vssgloss-i.md), *opérations de sauvegarde différentielle*, [*prise en charge partielle des fichiers*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**opérations de sauvegarde différentielle**
</dt> <dd>

Une opération de sauvegarde ou de restauration effectuée uniquement sur les fichiers créés ou modifiés depuis la dernière sauvegarde complète a été enregistrée. Voir aussi [*opérations de sauvegarde incrémentielle*](vssgloss-i.md), [*prise en charge partielle*](vssgloss-p.md)des fichiers, *fichiers différenciés*.

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**données différentielles**
</dt> <dd>

Données qui peuvent être appliquées à un volume d’origine pour générer un volume de clichés instantanés. C’est également ce que l’on appelle des données de copie sur écriture, mais cette documentation utilise les données différentielles du terme.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**ciblage dirigé**
</dt> <dd>

Mode de restauration par lequel un writer indique que lors de la restauration d’un fichier, il (le fichier source) doit être remappé. Le fichier peut être restauré vers un nouvel emplacement de restauration et/ou des plages de ses données restaurées sur un décalage différent avec l’emplacement de restauration.

</dd> </dl>

 

 



