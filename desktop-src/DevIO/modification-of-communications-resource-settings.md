---
description: Lorsque la fonction CreateFile ouvre un handle vers une ressource de communication série, le système initialise et configure la ressource en fonction des valeurs configurées lors de la dernière ouverture de la ressource.
ms.assetid: a39881d8-32af-4846-a2d3-508f1945b666
title: Modification des Paramètres de ressources de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8658029470fae9ee2d70ffb1459312c3c4d80ecf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114305"
---
# <a name="modification-of-communications-resource-settings"></a>Modification des Paramètres de ressources de communication

Lorsque la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ouvre un handle vers une ressource de communication série, le système initialise et configure la ressource en fonction des valeurs configurées lors de la dernière ouverture de la ressource. Conserver les paramètres précédents permet à l’utilisateur de conserver les paramètres spécifiés par le biais d’une commande **mode** lorsque l’appareil est rouvert. Les valeurs héritées de l’opération d’ouverture précédente incluent les paramètres de configuration du bloc de contrôle de périphérique (structure [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) ) et les valeurs de délai d’attente utilisées dans les opérations d’e/s. Si l’appareil n’a jamais été ouvert, il est configuré avec les paramètres par défaut du système.

Pour déterminer la configuration initiale d’une ressource de communication série, un processus appelle la fonction [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) , qui remplit une structure de port série [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) avec les paramètres de configuration actuels. Pour modifier cette configuration, un processus spécifie une structure **DCB** dans un appel à la fonction [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) .

Les membres de la structure [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) spécifient les paramètres de configuration tels que la vitesse en bauds, le nombre de bits de données par octet et le nombre de bits d’arrêt par octet. D’autres membres **DCB** spécifient des caractères spéciaux et activent la vérification de parité et le contrôle de Flow. Lorsqu’un processus ne doit modifier que quelques-uns de ces paramètres de configuration, il doit d’abord appeler [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) pour remplir une structure **DCB** avec la configuration actuelle. Le processus peut ensuite ajuster les valeurs importantes dans la structure **DCB** et reconfigurer l’appareil en appelant [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) et en spécifiant la structure **DCB** modifiée. Cette procédure permet de s’assurer que les membres non modifiés de la structure **DCB** contiennent des valeurs appropriées. Par exemple, une erreur courante consiste à configurer un appareil avec une structure **DCB** dans laquelle le membre **XonChar** de la structure est égal au membre **XoffChar** .

La fonction [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba) fournit une autre façon de modifier une structure [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) . **BuildCommDCB** utilise une chaîne ayant la même forme que les arguments de ligne de commande de la commande **mode** pour spécifier la vitesse en bauds, le schéma de parité, le nombre de bits d’arrêt et le nombre de bits de données. Les membres restants de [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) ne sont pas modifiés par cette fonction, sauf que les membres appropriés sont définis pour désactiver XON/XOFF et le contrôle de workflow matériel. **BuildCommDCB** modifie uniquement une structure **DCB** ; elle ne reconfigure pas l’appareil.

Un processus peut reconfigurer une ressource de communication à l’aide de la fonction [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) pour obtenir des informations à partir d’un pilote de périphérique sur les paramètres de configuration qu’il prend en charge. Le processus peut utiliser ces informations pour éviter de spécifier une configuration qui n’est pas prise en charge.

La fonction [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) reconfigure la ressource de communication, mais elle n’affecte pas la sortie interne et les tampons d’entrée du pilote spécifié. Les mémoires tampons ne sont pas vidées et les opérations de lecture et d’écriture en attente ne sont pas terminées prématurément.

Un processus réinitialise une ressource de communication à l’aide de la fonction [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm) , qui effectue les tâches suivantes :

-   Termine les opérations de lecture et d’écriture en attente, même si elles n’ont pas été terminées.
-   Ignore les caractères non lus et libère les mémoires tampons de sortie et d’entrée internes du pilote associé à la ressource spécifiée.
-   Réalloue la sortie interne et les mémoires tampons d’entrée.

Un processus n’est pas obligatoire pour appeler [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm). Si ce n’est pas le cas, le pilote de la ressource Initialise l’appareil avec les paramètres par défaut la première fois que le handle de ressource de communication est utilisé.

 

 
