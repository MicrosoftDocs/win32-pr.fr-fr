---
title: Suivi des modifications
description: Certaines applications doivent assurer la cohérence entre les données spécifiques stockées dans le service d’annuaire Active Directory et d’autres données.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, suivi des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3d8521fbd7b04d2c317246d81e0b9af7bce888bcc8e78b7bc9fcbbdd05b0c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024567"
---
# <a name="tracking-changes"></a>Suivi des modifications

Certaines applications doivent assurer la cohérence entre les données spécifiques stockées dans le service d’annuaire Active Directory et d’autres données. les autres données peuvent être stockées dans le répertoire, dans une table SQL Server, dans un fichier ou dans le registre. Lorsque les données stockées dans le répertoire changent, il peut être nécessaire de modifier les autres données afin de rester cohérentes. Les applications qui ont cette exigence sont les suivantes :

Cette section ne couvre pas les mécanismes utilisés par les applications de surveillance. Il s’agit d’applications qui surveillent les modifications de l’annuaire afin de conserver des données cohérentes entre des magasins distincts, mais en tant qu’outil de gestion du système. Bien que l’analyse des applications puisse utiliser les mêmes mécanismes que ceux qui prennent en charge les applications de suivi des modifications, les mécanismes suivants sont spécifiquement conçus pour la surveillance des applications :

-   Audit de sécurité. En modifiant la partie système de contrôle d’accès système (SACL) du descripteur de sécurité d’un objet, vous pouvez faire en sorte que les accès à l’objet sur un contrôleur de domaine donné génère des enregistrements d’audit dans le journal des événements de sécurité sur ce contrôleur de domaine. Vous pouvez auditer les lectures, les écritures, ou les deux. vous pouvez auditer la totalité de l’objet ou des attributs spécifiques. Pour plus d’informations, consultez [récupération de la liste SACL](retrieving-an-objectampaposs-sacl.md) et [génération d’audit](/windows/desktop/SecAuthZ/audit-generation)d’un objet.
-   Journalisation des événements En modifiant les paramètres du Registre sur un contrôleur de domaine donné, vous pouvez modifier les types d’événements consignés dans le journal des événements du service d’annuaire. Plus précisément, pour consigner toutes les modifications, affectez la valeur 4 à la valeur d' **accès au répertoire 8** sous la clé de Registre suivante.

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    Pour plus d’informations, consultez [journalisation des événements](/windows/desktop/EventLog/event-logging).

-   le suivi d’événement. Windows 2000 a introduit une API de suivi d’événements pour le suivi et la journalisation des événements intéressants dans les logiciels ou le matériel. le système d’exploitation Windows, et Active Directory Domain Services en particulier, prennent en charge l’utilisation du suivi d’événements pour la planification de la capacité et l’analyse détaillée des performances. Pour plus d’informations, consultez [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) et [suivi d’événements dans ADSI](/windows/desktop/ADSI/adsi-and-etw).

Cette section comprend les rubriques suivantes :

-   [Vue d’ensemble des techniques de Change Tracking](overview-of-change-tracking-techniques.md)
-   [Notifications de modifications dans Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md)
-   [Interrogation des modifications à l’aide du contrôle DirSync](polling-for-changes-using-the-dirsync-control.md)
-   [Interrogation des modifications à l’aide de USNChanged](polling-for-changes-using-usnchanged.md)

 

 