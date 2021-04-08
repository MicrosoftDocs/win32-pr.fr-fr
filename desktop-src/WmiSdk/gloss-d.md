---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034618"
---
# <a name="d-wmi"></a>D (WMI)

[A](gloss-a.md) B [C](gloss-c.md) D [e](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**Date/heure**
</dt> <dd>

Voir [*DateTime CIM*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**fournisseur découplé**
</dt> <dd>

Fournisseur hébergé dans un processus distinct de WMI. Les fournisseurs découplés sont la méthode recommandée pour instrumenter une application, car le fournisseur peut contrôler sa propre durée de vie au lieu d’être lancé chaque fois qu’un utilisateur accède au fournisseur via WMI.

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**accès direct**
</dt> <dd>

Méthode permettant d’accéder aux propriétés et aux méthodes fournies par WMI dans un script comme s’il s’agissait de propriétés et de méthodes Automation de [**SWbemObject**](swbemobject.md).

Accès indirect : `VolumeName = MyDisk.Properties_("VolumeName")`

Accès direct : `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**DMTF (Distributed Management Task Force)**
</dt> <dd>

Organisation internationale de normalisation qui collabore avec les principaux fournisseurs de technologies, y compris Microsoft, pour mener à bien le développement, l’adoption et l’unification des normes et des initiatives de gestion pour les environnements de bureau, d’entreprise et Internet.

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**
</dt> <dd>

Voir *Distributed Management Task Force (DMTF)*.

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**classe dynamique**
</dt> <dd>

Classe CIM dont la définition est fournie par un [*fournisseur*](gloss-p.md) au moment de l’exécution, selon les besoins. Les classes dynamiques représentent des [*objets managés*](gloss-m.md) spécifiques au fournisseur et ne sont pas stockées dans le [*référentiel CIM*](gloss-c.md). Les classes dynamiques ne prennent en charge que les *instances dynamiques*.

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**instance dynamique**
</dt> <dd>

Instance d’une classe CIM fournie par un [*fournisseur*](gloss-p.md) , le cas échéant. Elle n’est pas stockée dans le [*référentiel CIM*](gloss-c.md). Les instances dynamiques peuvent être fournies pour des classes statiques ou dynamiques. La prise en charge dynamique des instances d’une classe permet à un fournisseur de fournir des valeurs de [*propriété*](gloss-p.md) à la minute.

</dd> </dl>

 

 



