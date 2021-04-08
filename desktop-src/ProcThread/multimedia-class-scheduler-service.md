---
description: Le service Planificateur de classes multimédias (MMCSS) permet aux applications multimédias de s’assurer que leur traitement qui respecte le temps reçoit un accès prioritaire aux ressources du processeur.
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: Service Planificateur de classes multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80656276af30495c084d0964534a04e11896bcd2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953382"
---
# <a name="multimedia-class-scheduler-service"></a>Service Planificateur de classes multimédias

Le service Planificateur de classes multimédias (MMCSS) permet aux applications multimédias de s’assurer que leur traitement qui respecte le temps reçoit un accès prioritaire aux ressources du processeur. Ce service permet aux applications multimédias d’utiliser la plus grande partie du processeur, sans avoir à refuser les ressources du processeur aux applications de faible priorité.

MMCSS utilise les informations stockées dans le registre pour identifier les tâches prises en charge et déterminer la priorité relative des threads effectuant ces tâches. Chaque thread qui effectue un travail lié à une tâche particulière appelle la fonction [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) ou [**AVSETMMTHREADCHARACTERISTICS**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) pour informer MMCSS qu’il travaille sur cette tâche.

Pour obtenir un exemple de programme qui utilise MMCSS, consultez [flux en mode exclusif](/previous-versions//bb614507(v=vs.85)).

**Windows Server 2003 et Windows XP :** MMCSS n’est pas disponible.

## <a name="registry-settings"></a>Paramètres du Registre

Les paramètres MMCSS sont stockés dans la clé de Registre suivante :

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Multimedia \\ SystemProfile**

Cette clé contient une valeur **reg \_ DWORD** nommée **SystemResponsiveness** qui détermine le pourcentage de ressources du processeur qui doivent être garanties pour les tâches de faible priorité. Par exemple, si cette valeur est de 20, alors 20% des ressources du processeur sont réservées aux tâches de faible priorité. Notez que les valeurs qui ne sont pas divisibles uniformément par 10 sont arrondies au multiple le plus proche de 10. La valeur 0 est également considérée comme 10.

La clé contient également une sous-clé nommée **Tasks** qui contient la liste des tâches. Par défaut, Windows prend en charge les tâches suivantes :

-   **Audio**
-   **Capture**
-   **Distribution**
-   **Jeux**
-   **Lecture**
-   **Audio Pro**
-   **Gestionnaire de fenêtres**

Les OEM peuvent ajouter des tâches supplémentaires selon les besoins.

Chaque clé de tâche contient l’ensemble de valeurs suivant qui représentent les caractéristiques à appliquer aux threads associés à la tâche.

| Valeur                   | Format         | Valeurs possibles                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Affinité**            | **\_valeur DWORD reg** | Masque de masque qui indique l’affinité du processeur. 0x00 et 0xFFFFFFFF indiquent que l’affinité du processeur n’est pas utilisée.                                                                                                                                                                                                                                                 |
| **Arrière-plan uniquement**     | **SZ de REG \_**    | Indique s’il s’agit d’une tâche en arrière-plan (sans interface utilisateur). Les threads d’une tâche en arrière-plan ne changent pas en raison d’une modification du focus de la fenêtre. Cette valeur peut être définie sur true ou false.                                                                                                                                                                            |
| **BackgroundPriority**  | **\_valeur DWORD reg** | Priorité d’arrière-plan. La plage de valeurs est 1-8.                                                                                                                                                                                                                                                                                                                    |
| **Fréquence d’horloge**          | **\_valeur DWORD reg** | Indicateur utilisé par MMCSS pour déterminer la granularité de la planification des ressources du processeur. **Windows Server 2008 et Windows Vista :** Taux d’horloge maximal garanti que le système utilise si un thread rejoint cette tâche, en intervalles de 100 nanosecondes. À compter de Windows 7 et de Windows Server 2008 R2, cette garantie a été supprimée pour réduire la consommation d’énergie du système.<br/> |
| **Priorité GPU**        | **\_valeur DWORD reg** | Priorité du GPU. La plage de valeurs est 0-31. Cette priorité n’est pas encore utilisée.                                                                                                                                                                                                                                                                                           |
| **Priorité**            | **\_valeur DWORD reg** | Priorité de la tâche. La plage de valeurs est comprise entre 1 (faible) et 8 (élevé). Pour les tâches dont la **catégorie de planification** est élevée, cette valeur est toujours traitée comme 2.<br/>                                                                                                                                                                                                           |
| **Catégorie de planification** | **SZ de REG \_**    | Catégorie de planification. Cette valeur peut être définie sur élevé, moyen ou faible.                                                                                                                                                                                                                                                                                                 |
| **Priorité SFIO**       | **SZ de REG \_**    | Priorité d’e/s planifiée. Cette valeur peut être définie sur inactif, faible, normale ou élevée. Cette valeur n'est pas utilisée.                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Pour économiser de l’énergie, les applications ne doivent pas définir la résolution du minuteur à l’échelle du système sur une petite valeur, sauf si cela est absolument nécessaire. Pour plus d’informations, consultez [performances](../win7devguide/performance.md) dans le [Guide des développeurs Windows 7](../win7devguide/windows-7-developer-guide.md).

 

## <a name="thread-priorities"></a>Priorités des threads

Le MMCSS augmente la priorité des threads qui travaillent sur des tâches multimédias de haute priorité.

MMCSS détermine la priorité d’un thread à l’aide des facteurs suivants :

-   Priorité de base de la tâche.
-   Paramètre *Priority* de la fonction [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority) .
-   Indique si l’application est au premier plan.
-   La quantité de temps processeur consommée par les threads dans chaque catégorie.

MMCSS définit la priorité des threads clients en fonction de leur catégorie de planification.

| Category | Priority | Description                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Élevé     | 23-26    | Ces threads s’exécutent à une priorité de thread inférieure à certaines tâches de niveau système. Cette catégorie est conçue pour les tâches audio pro. |
| Moyenne   | 16-22    | Ces threads font partie de l’application qui se trouve au premier plan.                                                                      |
| Faible      | 8-15     | Cette catégorie contient le reste des threads. Ils garantissent un pourcentage minimal de ressources du processeur, si nécessaire.           |
|          | 1-7      | Ces threads ont utilisé leur quota de ressources processeur. Ils peuvent continuer à s’exécuter si aucun thread de faible priorité n’est prêt à s’exécuter.                |



 

 

 
