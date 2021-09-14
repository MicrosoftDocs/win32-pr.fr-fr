---
description: En plus des partitions, qui contiennent une ou plusieurs applications, COM+ comprend également des groupes de partitions qui contiennent une ou plusieurs partitions.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Partitions et Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855393"
---
# <a name="partitions-and-active-directory"></a>Partitions et Active Directory

En plus des partitions, qui contiennent une ou plusieurs applications, COM+ comprend également des *groupes de partitions* qui contiennent une ou plusieurs partitions. Créé dans Active Directory, les groupes de partitions permettent aux utilisateurs d’un domaine d’accéder aux applications COM+ dans l’ensemble du domaine. Lors de la création, chaque utilisateur ou unité d’organisation spécifique est affecté, ou mappé, à un ensemble de partitions.

Un utilisateur ou une unité d’organisation unique peut accéder à plusieurs partitions et à leurs applications, car il existe une corrélation un-à-un entre l’identité d’un utilisateur, l’unité d’organisation et un ensemble de partitions. Sans ensemble de partitions, un utilisateur ou une unité d’organisation a besoin de plusieurs identités d’utilisateur pour accéder aux applications de différentes partitions.

Pour rendre les applications COM+ disponibles pour les utilisateurs du domaine, un administrateur doit effectuer les tâches sur le contrôleur de domaine sur lequel Active Directory réside et sur le serveur sur lequel l’application COM+ est installée.

## <a name="on-the-domain-controller"></a>Sur le contrôleur de domaine

L’administrateur crée d’abord une partition dans Active Directory. La création d’une partition COM+ s’effectue à l’aide de l’outil d’administration utilisateurs et ordinateurs Active Directory ou par programme à l’aide de l’interface de services Active Directory (ADSI).

Une fois la partition créée dans Active Directory, l’administrateur crée un ensemble de partitions. Lors de la création d’un ensemble de partitions, l’administrateur définit les partitions incluses dans cet ensemble. La création d’un jeu de partitions COM+ s’effectue à l’aide de l’outil d’administration utilisateurs et ordinateurs Active Directory ou par programme à l’aide de l’interface de services Active Directory (ADSI).

Enfin, l’administrateur mappe les utilisateurs du domaine ou les unités d’organisation (UO) au jeu de partitions nouvellement créé. Pour ce faire, vous affichez la page de **Propriétés** d’un utilisateur, accédez à l’onglet **groupes de partitions com+** , puis sélectionnez un ensemble de partitions dans la zone de liste.

## <a name="on-the-com-application-server"></a>Sur le serveur d’applications COM+

L’administrateur crée une nouvelle partition, en spécifiant le même nom de partition et le même ID de partition (GUID) que celui de la partition qui a été créée dans Active Directory sur le contrôleur de domaine. Pour ce faire, utilisez le dossier **partitions com+** dans l’outil d’administration Services de composants. Pour simplifier cette tâche, l’outil services de composants permet à l’administrateur de parcourir Active Directory pour sélectionner la partition souhaitée et son GUID.

Lorsque la partition de domaine a été créée sur le serveur d’applications, la partition par défaut d’un utilisateur devient la partition par défaut de l’ensemble de partitions dans le Active Directory. Enfin, l’administrateur peut installer l’application COM+ dans la partition nouvellement créée sur le serveur d’applications.

Pour plus d’informations sur l’administration des partitions pour l’accès des utilisateurs du domaine, consultez l’aide associée à l’outil d’administration utilisateurs et ordinateurs Active Directory.

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Mappage des identités d’utilisateur et des unités d’organisation à des groupes de partitions

Les utilisateurs et les unités d’organisation peuvent être mappés à des groupes de partitions. En mappant les unités d’organisation aux jeux de partitions, un administrateur peut associer plusieurs utilisateurs à un ensemble de partitions à la fois au lieu de devoir mapper plusieurs identités d’utilisateur. Une seule identité d’utilisateur ou unité d’organisation ne peut être mappée qu’à un seul ensemble de partitions. En général, le mappage d’identités utilisateur ou d’unités d’organisation à des jeux de partitions effectue les opérations suivantes :

-   Garantit que les applications sont disponibles pour les utilisateurs appropriés dans le domaine
-   Aide COM+ à déterminer la partition dans laquelle se trouve une application
-   Établit le droit d’accès d’un utilisateur à une application particulière

Pour associer des partitions à des groupes de partitions dans Active Directory et mapper des utilisateurs et des UO à ces jeux de partitions, les administrateurs utilisent les outils d’administration Active Directory utilisateurs et ordinateurs et services de composants. Lorsqu’une partition est créée dans Active Directory, un administrateur doit configurer localement cette partition sur l’ordinateur sur lequel l’application COM+ appropriée doit être installée. Cette configuration locale des partitions créées dans Active Directory s’effectue à l’aide de l’outil d’administration Services de composants.

Si une identité d’utilisateur de domaine n’est pas mappée à un ensemble de partitions, l’utilisateur se voit accorder l’accès par l’unité d’organisation de l’utilisateur, qui est mappée à la partition. Si l’unité d’organisation de l’utilisateur n’est pas mappée à un ensemble de partitions, mais que l’unité d’organisation la plus élevée dans la hiérarchie est mappée à cet ensemble de partitions, l’utilisateur peut accéder à la partition.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Partitions par défaut](default-partitions.md)
</dt> <dt>

[Partitions locales](local-partitions.md)
</dt> <dt>

[Propriétés de partition](partition-properties.md)
</dt> <dt>

[Partition globale](the-global-partition.md)
</dt> </dl>

 

 



