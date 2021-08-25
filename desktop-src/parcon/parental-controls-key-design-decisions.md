---
description: Décisions de conception des clés de contrôle parental
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Décisions de conception des clés de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef8f1e1d1b629c9fbb4354fb266376453938a35bde80e7b60f57be8f77da70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939289"
---
# <a name="parental-controls-key-design-decisions"></a>Décisions de conception des clés de contrôle parental

les principales décisions en matière de conception dans le développement des contrôles parentaux Windows Vista sont les suivantes :

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>dépendance essentielle à la fonctionnalité de contrôle de compte d’utilisateur (UAC) Windows Vista

une décision essentielle pour le contrôle Parental Windows Vista consiste à utiliser la nouvelle fonctionnalité de contrôle de compte d’utilisateur (UAC) pour implémenter les identités de compte de droits réduites, particulièrement nécessaires pour les restrictions hors connexion sur les utilisateurs contrôlés. pour plus d’informations sur [le contrôle de compte d’utilisateur, consultez les Windows vista et Windows Server 2008 developer Story : Windows vista Application Development requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)). En résumé, chaque compte disposant de droits d’administrateur a des privilèges suffisants pour l’affichage des données de journal et la définition des stratégies. Les contrôles parentaux ne peuvent être définis que sur les utilisateurs à droits standard (anciennement appelés comptes d’utilisateur dotés de privilèges minimum, ou LUAs), car ils ne peuvent pas modifier les journaux et les paramètres avec les listes de Access Control (ACL) configurés uniquement pour les administrateurs à écrire. En d’autres termes :

-   Une identité parente ou Guardian est implicitement égale à un compte disposant des droits d’un administrateur.
-   Les utilisateurs sous contrôle parent doivent être des utilisateurs standard.

## <a name="nearly-all-settings-are-available-by-apis"></a>presque tous les Paramètres sont disponibles par les api

À l’exception des éléments tels que les définitions de système de contrôle d’accès, les paramètres disponibles pour la manipulation par l’interface utilisateur des contrôles parentaux peuvent également être modifiés par les API exposées. Il est nécessaire que les programmes implémentent l’élévation aux droits d’administration afin de modifier les paramètres, comme indiqué ci-dessus pour le contrôle de compte d’utilisateur.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Windows Le contrôle parental Vista est une technologie exclusivement réservée aux consommateurs.

Windows Les contrôles parentaux Vista ne sont pas destinés à être utilisés avec les comptes de domaine. en tant que technologie de consommation, le contrôle Parental n’est pas déployé sur les références sku commerciales de Windows Vista. Si un ordinateur est joint à un domaine, les liens de l’interface utilisateur de sécurité de famille seront supprimés.

Un mécanisme sera fourni pour exposer les fonctionnalités du cas joint à un domaine, mais seuls les comptes d’utilisateur non-domaine peuvent être configurés avec des contrôles de contrôle parental.

 

 
