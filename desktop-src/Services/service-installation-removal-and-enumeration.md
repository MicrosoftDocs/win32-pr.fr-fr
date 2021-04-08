---
description: Un programme de configuration utilise la fonction CreateService pour installer un nouveau service dans la base de données SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Installation, suppression et énumération des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751060"
---
# <a name="service-installation-removal-and-enumeration"></a>Installation, suppression et énumération des services

Un programme de configuration utilise la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) pour installer un nouveau service dans la base de données SCM. Cette fonction spécifie le nom du service et fournit des informations de configuration qui sont stockées dans la base de données. Pour obtenir une description des informations stockées dans la base de données pour chaque service, consultez [base de données des services installés](database-of-installed-services.md). Pour obtenir un exemple de code, consultez [installation d’un service](installing-a-service.md).

Un programme de configuration utilise la fonction [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) pour supprimer un service installé de la base de données. Pour plus d’informations, consultez [Suppression d’un service](deleting-a-service.md).

Pour obtenir le nom du service, appelez la fonction [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) . Le nom d’affichage du service, utilisé dans l’applet services du panneau de configuration, peut être obtenu en appelant la fonction [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .

Un programme de configuration de service peut utiliser la fonction [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) pour énumérer tous les services et leurs États. Elle peut également utiliser la fonction [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) pour énumérer les services qui dépendent d’un objet de service spécifié.

 

 



