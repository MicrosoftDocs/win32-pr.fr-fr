---
description: Utilisez la journalisation des événements pour enregistrer les erreurs qui se produisent dans la DLL de performance.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Gestion des erreurs dans la DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952012"
---
# <a name="error-handling-in-the-dll"></a>Gestion des erreurs dans la DLL

Utilisez la journalisation des événements pour enregistrer les erreurs qui se produisent dans la DLL de performance. La journalisation des événements d’erreur facilite la résolution des problèmes liés aux applications qui fournissent des données de performances pendant le développement et après l’installation. Vous devez limiter la quantité de journalisation des erreurs qui se produit dans la fonction [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , car la collecte de données peut être fréquente.

Le système enregistre les erreurs suivantes dans le journal des événements en cas de problème avec la fonction [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) . Si l’une des erreurs suivantes se produit, le système n’appelle pas à nouveau la DLL de performance. Au lieu de cela, la DLL est déchargée.

-   **PERFLIB \_ OPEN \_ Proc \_ \_ introuvable**: consigné lorsque le nom de la procédure défini dans le Registre est introuvable dans la dll en tant que fonction exportée. Cela se produit généralement lorsque la DLL ou le service n’est pas installé correctement ou que le nom de la fonction a été renommé sans mettre à jour la procédure d’installation.
-   **PERFLIB \_ \_ \_ Échec** de l’ouverture de la procédure : consigné lorsque la procédure ouverte a retourné un état d’erreur autre que erreur de \_ réussite. Si cela se produit, la DLL doit également avoir entré une entrée du journal des événements décrivant les conditions qui ont provoqué l’échec.
-   **PERFLIB \_ \_ \_ Exception Open proc**: consigné lorsque la procédure Open rencontre une exception non gérée. Cela est généralement dû à une condition d’erreur inattendue rencontrée par la procédure Open.

 

 
