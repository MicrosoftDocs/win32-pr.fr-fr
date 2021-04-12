---
description: Avec un objet de traitement, des groupes de processus peuvent être gérés en tant qu’unité. Les objets de traitement sont des objets namable, sécurisables et partageables qui contrôlent les attributs des processus qui leur sont associés.
ms.assetid: 59296384-5e78-44dd-8019-f1df6668928b
title: Objets de traitement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d9758faf2b66f047ca60dbba91601b202b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319165"
---
# <a name="job-objects"></a>Objets de traitement

Un *objet de traitement* permet de gérer des groupes de processus en tant qu’unité. Les objets de traitement sont des objets namable, sécurisables et partageables qui contrôlent les attributs des processus qui leur sont associés. Les opérations effectuées sur un objet de traitement affectent tous les processus associés à cet objet. Les exemples incluent des limites d’application, telles que la taille de la plage de travail et la priorité du processus, ou l’arrêt de tous les processus associés à un travail.

-   [Création de travaux](#creating-jobs)
-   [Gestion des processus dans les travaux](#managing-processes-in-jobs)
-   [Limites du travail et notifications](#job-limits-and-notifications)
-   [Comptabilisation des ressources pour les travaux](#resource-accounting-for-jobs)
-   [Gestion des objets de traitement](#managing-job-objects)
-   [Gestion d’une arborescence de processus qui utilise des objets de traitement](#managing-a-process-tree-that-uses-job-objects)

## <a name="creating-jobs"></a>Création de travaux

Pour créer un objet de traitement, utilisez la fonction [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Lorsque le travail est créé, aucun processus n’est associé à ce travail.

Pour associer un processus à un travail, utilisez la fonction [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) . Une fois qu’un processus est associé à un travail, l’Association ne peut pas être interrompue. Un processus peut être associé à plusieurs travaux dans une hiérarchie de travaux imbriqués. Pour plus d’informations, consultez [tâches imbriquées](nested-jobs.md).

**Windows 7, Windows server 2008 R2, Windows XP avec SP3, Windows server 2008, Windows Vista et Windows server 2003 :** Un processus ne peut être associé qu’à un seul travail. Les travaux ne peuvent pas être imbriqués. La capacité à imbriquer des travaux a été ajoutée dans Windows 8 et Windows Server 2012.

Vous pouvez spécifier un descripteur de sécurité pour un objet de traitement lorsque vous appelez la fonction [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Pour plus d’informations, consultez [sécurité et droits d’accès à l’objet de traitement](job-object-security-and-access-rights.md).

## <a name="managing-processes-in-jobs"></a>Gestion des processus dans les travaux

Une fois qu’un processus est associé à un travail, par défaut, tous les processus enfants qu’il crée à l’aide de [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) sont également associés à ce travail. (Les processus enfants créés à l’aide du [**\_ processus Win32. Create**](../cimwin32prov/create-method-in-class-win32-process.md) ne sont pas associés au travail.) Vous pouvez modifier ce comportement par défaut en définissant la \_ \_ dissociation limite de l’objet de tâche de limite étendue \_ \_ OK ou \_ \_ \_ \_ la dissociation silencieuse \_ de limite d’objet de traitement OK pour le travail.

-   Si la limite de la limite de l’objet de tâche de limite étendue est définie \_ \_ \_ \_ sur OK et que le processus parent a été créé avec l’indicateur créer une \_ dissociation \_ à partir d’une \_ tâche, les processus enfants du processus parent ne sont pas associés au travail.
-   Si la \_ \_ dissociation silencieuse de la limite de l’objet de tâche limite étendue est \_ \_ \_ OK, les processus enfants d’un processus parent associé au travail ne sont pas associés à ce travail. Il n’est pas nécessaire de créer des processus parents avec l’indicateur CREATe \_ dissociation \_ from \_ Job.

Si le travail est imbriqué, les paramètres de dissociation des travaux parents dans la hiérarchie déterminent si les processus enfants sont associés à un autre travail dans la hiérarchie. Pour plus d’informations, consultez [tâches imbriquées](nested-jobs.md).

Pour déterminer si un processus s’exécute dans un travail, utilisez la fonction [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob) .

Pour mettre fin à tous les processus actuellement associés à un objet de traitement, utilisez la fonction [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) .

## <a name="job-limits-and-notifications"></a>Limites du travail et notifications

Un travail peut appliquer des limites telles que la taille de la plage de travail, la priorité du processus et la limite de temps de fin de travail sur chaque processus associé au travail. Si un processus associé à un travail tente d’augmenter sa taille de jeu de travail ou sa priorité de processus à partir de la limite établie par le travail, les appels de fonction réussissent mais sont ignorés en mode silencieux. Un travail peut également définir des limites qui déclenchent une notification lorsqu’elles sont dépassées, mais autorisent la poursuite de l’exécution du travail.

Pour définir les limites d’un travail, utilisez la fonction [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) . Pour obtenir la liste des limites possibles qui peuvent être définies pour un travail, consultez les rubriques suivantes :

-   [**\_ \_ informations sur les limites de base de JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**JOBOBJECT \_ \_ restrictions de l’interface utilisateur de base \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**informations de contrôle de la \_ \_ fréquence de l’UC JOBOBJECT \_ \_**](/windows/desktop/api/Winnt/ns-winnt-jobobject_cpu_rate_control_information)
-   [**\_ \_ informations sur la limite étendue JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_ \_ informations sur les limites de notification JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_notification_limit_information)

Les limites de sécurité doivent être définies individuellement pour chaque processus associé à un objet de traitement. Pour plus d’informations, consultez [sécurité des processus et droits d’accès](process-security-and-access-rights.md).

**Windows XP avec SP3 et Windows Server 2003 :** La fonction [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) peut être utilisée pour définir des limites de sécurité pour tous les processus associés à un objet de traitement. À compter de Windows Vista, les limites de sécurité doivent être définies individuellement pour chaque processus associé à un objet de traitement.

Si le travail est imbriqué, les travaux parents dans la hiérarchie influencent la limite appliquée pour le travail. Pour plus d’informations, consultez [tâches imbriquées](nested-jobs.md).

Si le travail est associé à un port de terminaison d’e/s, il peut recevoir des notifications lorsque certaines limites de travail sont dépassées. Le système envoie des messages au port de terminaison lorsqu’une limite est dépassée ou que certains autres événements se produisent. Pour associer un port de terminaison à un travail, utilisez la fonction [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) avec la classe d’informations de l’objet de traitement **JobObjectAssociateCompletionPortInformation** et un pointeur vers une structure de [**\_ \_ \_ port d’achèvement Associate JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port) . Il est préférable de le faire lorsque le travail est inactif, afin de réduire le risque de notifications manquantes pour les processus dont les États changent au cours de l’Association du port de terminaison.

Tous les messages sont envoyés directement à partir du travail comme si le travail avait appelé la fonction [**PostQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-postqueuedcompletionstatus) . Un thread doit surveiller le port de terminaison à l’aide de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) pour récupérer les messages. Notez que, à l’exception des limites définies avec la classe d’informations **JobObjectNotificationLimitInformation** , la remise de messages au port de terminaison n’est pas garantie ; l’échec de l’arrivée d’un message ne signifie pas nécessairement que l’événement ne s’est pas produit. Les notifications pour les limites définies avec **JobObjectNotificationLimitInformation** sont assurées d’arriver sur le port de terminaison. Pour obtenir la liste des messages possibles, consultez [**JOBOBJECT \_ Associate \_ Complete \_ port**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-jobs"></a>Comptabilisation des ressources pour les travaux

L’objet de traitement enregistre les informations de comptabilité de base pour tous les processus associés, y compris ceux qui se sont terminés. Pour récupérer ces informations de comptabilité, utilisez la fonction [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) . Pour obtenir la liste des informations de comptabilité qui sont conservées pour un travail, consultez les rubriques suivantes :

-   [**\_informations de \_ comptabilité de base JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**JOBOBJECT \_ \_ les informations de gestion de base et d' \_ e/s \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)

Si l’objet de traitement est imbriqué, les informations de comptabilité de chaque travail enfant sont agrégées dans son travail parent. Pour plus d’informations, consultez [tâches imbriquées](nested-jobs.md).

## <a name="managing-job-objects"></a>Gestion des objets de traitement

L’état d’un objet de traitement est défini sur signalé lorsque tous ses processus sont terminés, car la limite de durée de fin de travail spécifiée a été dépassée. Utilisez [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) ou [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) pour surveiller l’objet de traitement de cet événement.

Pour obtenir un handle pour un objet de traitement existant, utilisez la fonction [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) et spécifiez le nom donné à l’objet lors de sa création. Seuls les objets de travail nommés peuvent être ouverts.

Pour fermer un handle d’objet de traitement, utilisez la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) . Le travail est détruit lorsque son dernier descripteur a été fermé et que tous les processus associés ont été arrêtés. Toutefois, si le travail a l' \_ \_ indicateur de fin de la limite des objets de tâche sur la fermeture du travail \_ \_ \_ \_ spécifié, la fermeture du dernier descripteur d’objet de travail met fin à tous les processus associés, puis détruit l’objet de traitement lui-même. Si une tâche imbriquée a l' \_ \_ \_ \_ indicateur de fin de la limite des objets de tâche sur la \_ fermeture du travail \_ spécifié, la fermeture du dernier descripteur d’objet de travail met fin à tous les processus associés au travail et à ses tâches enfants dans la hiérarchie.

## <a name="managing-a-process-tree-that-uses-job-objects"></a>Gestion d’une arborescence de processus qui utilise des objets de traitement

À compter de Windows 8 et de Windows Server 2012, une application peut utiliser des [tâches imbriquées](nested-jobs.md) pour gérer une arborescence de processus qui utilise plus d’un objet de traitement. Toutefois, une application qui doit s’exécuter sur Windows 7, Windows Server 2008 R2 ou des versions antérieures de Windows qui ne prennent pas en charge les travaux imbriqués doit gérer l’arborescence de processus d’une autre manière.

Si un outil doit gérer une arborescence de processus qui utilise des objets de traitement et qu’il n’est pas possible d’utiliser des tâches imbriquées, l’outil et les membres de l’arborescence de processus doivent coopérer. Utilisez l’une des options suivantes :

-   Utilisez la limite de la \_ \_ dissociation silencieuse limite de l’objet de traitement \_ \_ \_ OK. Si l’outil utilise cette limite, il ne peut pas surveiller l’intégralité de l’arborescence d’un processus. L’outil peut surveiller uniquement les processus qu’il ajoute au travail. Si ces processus créent des processus enfants, ils ne sont pas associés au travail. Dans cette option, les processus enfants peuvent être associés à d’autres objets de travail.
-   Utilisez la limite de limite d’objet de traitement \_ \_ \_ \_ . Si l’outil utilise cette limite, il peut surveiller l’intégralité de l’arborescence des processus, à l’exception des processus qu’un membre de l’arborescence sépare explicitement de l’arborescence. Un membre de l’arborescence peut créer un processus enfant dans un nouvel objet de traitement en appelant la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) avec l' \_ indicateur Create dissociation \_ from \_ Job, puis en appelant la fonction [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) . Dans le cas contraire, le membre doit gérer les cas dans lesquels **AssignProcessToJobObject** échoue.

    L’indicateur CREATe \_ dissociation \_ from \_ Job n’a aucun effet si l’arborescence n’est pas surveillée par l’outil. Par conséquent, il s’agit de l’option par défaut, mais elle nécessite une connaissance approfondie des processus surveillés.

-   Évitez les dissociations de tout type en ne définissant ni la limite d’objets de tâche \_ \_ OK, ni la limite de \_ \_ \_ \_ \_ \_ dissociation silencieuse \_ de limite d’objet de traitement. Dans cette option, l’outil peut surveiller l’intégralité de l’arborescence des processus. Toutefois, si un processus enfant tente de s’associer lui-même ou un autre processus enfant à un travail en appelant [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject), l’appel échoue. Si le processus a été conçu pour être associé à un travail spécifique, cet échec peut empêcher le processus de fonctionner correctement.

 

 
