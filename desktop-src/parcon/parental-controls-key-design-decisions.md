---
description: Décisions de conception des clés de contrôle parental
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Décisions de conception des clés de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042744"
---
# <a name="parental-controls-key-design-decisions"></a>Décisions de conception des clés de contrôle parental

Les principales décisions en matière de conception dans le développement des contrôles parentaux Windows Vista sont les suivantes :

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Dépendance essentielle sur la fonctionnalité de contrôle de compte d’utilisateur (UAC) de Windows Vista

Une décision essentielle pour le contrôle parental de Windows Vista consiste à s’appuyer sur la nouvelle fonctionnalité de contrôle de compte d’utilisateur (UAC) pour implémenter les identités de compte de droits réduites, particulièrement nécessaires pour les restrictions hors connexion sur les utilisateurs contrôlés. Pour plus d’informations sur [le contrôle de compte d’utilisateur, consultez Windows Vista et Windows Server 2008 Developer Story : Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)). En résumé, chaque compte disposant de droits d’administrateur a des privilèges suffisants pour l’affichage des données de journal et la définition des stratégies. Les contrôles parentaux ne peuvent être définis que sur les utilisateurs à droits standard (anciennement appelés comptes d’utilisateur dotés de privilèges minimum, ou LUAs), car ils ne peuvent pas modifier les journaux et les paramètres avec les listes de Access Control (ACL) configurés uniquement pour les administrateurs à écrire. En d’autres termes :

-   Une identité parente ou Guardian est implicitement égale à un compte disposant des droits d’un administrateur.
-   Les utilisateurs sous contrôle parent doivent être des utilisateurs standard.

## <a name="nearly-all-settings-are-available-by-apis"></a>Presque tous les paramètres sont disponibles par les API

À l’exception des éléments tels que les définitions de système de contrôle d’accès, les paramètres disponibles pour la manipulation par l’interface utilisateur des contrôles parentaux peuvent également être modifiés par les API exposées. Il est nécessaire que les programmes implémentent l’élévation aux droits d’administration afin de modifier les paramètres, comme indiqué ci-dessus pour le contrôle de compte d’utilisateur.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Le contrôle parental de Windows Vista est une technologie exclusivement réservée aux consommateurs.

Les contrôles parentaux Windows Vista ne sont pas destinés à être utilisés avec les comptes de domaine. En tant que technologie de consommation, le contrôle parental n’est pas déployé sur les références SKU commerciales de Windows Vista. Si un ordinateur est joint à un domaine, les liens de l’interface utilisateur de sécurité de famille seront supprimés.

Un mécanisme sera fourni pour exposer les fonctionnalités du cas joint à un domaine, mais seuls les comptes d’utilisateur non-domaine peuvent être configurés avec des contrôles de contrôle parental.

 

 
