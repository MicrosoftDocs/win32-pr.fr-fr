---
description: Les programmeurs et les administrateurs système utilisent des programmes de configuration de service pour modifier ou interroger la base de données des services installés.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programmes de configuration de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112782"
---
# <a name="service-configuration-programs"></a>Programmes de configuration de service

Les programmeurs et les administrateurs système utilisent des programmes de configuration de service pour modifier ou interroger la base de données des services installés. La base de données est également accessible à l’aide des fonctions de registre. Toutefois, vous devez utiliser uniquement les fonctions de configuration SCM, qui garantissent que le service est correctement installé et configuré.

Les fonctions de configuration SCM requièrent soit un handle vers un objet SCManager, soit un handle vers un objet de service. Pour obtenir ces handles, le programme de configuration de service doit :

1.  Utilisez la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) pour obtenir un descripteur de la base de données SCM sur une machine spécifiée.
2.  Utilisez la fonction [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) pour obtenir un handle de l’objet de service.

Pour plus d'informations, voir les rubriques suivantes :

-   [Installation, suppression et énumération des services](service-installation-removal-and-enumeration.md)
-   [Configuration de service](service-configuration.md)
-   [Configuration d’un service à l’aide de SC](configuring-a-service-using-sc.md)

 

 



