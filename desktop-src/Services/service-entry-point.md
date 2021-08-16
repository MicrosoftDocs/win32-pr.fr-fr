---
description: Les services sont généralement écrits sous forme d’applications console.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Point d’entrée de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8f44322048351161bb8f3b8afdd619129d18b5effb5dc850d8909afbb3673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888971"
---
# <a name="service-entry-point"></a>Point d’entrée de service

Les services sont généralement écrits sous forme d’applications console. Le point d’entrée d’une application console est sa fonction **principale** . La fonction **main** reçoit des arguments de la valeur **ImagePath** de la clé de Registre pour le service. Pour plus d’informations, consultez la section Notes de la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .

Lorsque le SCM démarre un programme de service, il attend qu’il appelle la fonction [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) . Suivez les instructions ci-dessous.

-   Un service de type SERVICE \_ Win32 \_ propre \_ doit appeler [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) immédiatement, à partir de son thread principal. Vous pouvez effectuer n’importe quelle initialisation après le démarrage du service, comme décrit dans [fonction service ServiceMain](service-servicemain-function.md).
-   Si le type de service est \_ service \_ de partage Win32 de service \_ et qu’il y a une initialisation commune pour tous les services dans le programme, vous pouvez effectuer l’initialisation dans le thread principal avant d’appeler [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), à condition qu’il prenne moins de 30 secondes. Dans le cas contraire, vous devez créer un autre thread pour effectuer l’initialisation commune, tandis que le thread principal appelle **StartServiceCtrlDispatcher**. Vous devez toujours effectuer toute initialisation spécifique au service après le démarrage du service.

La fonction [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) prend une structure d' [**\_ \_ entrée de table de service**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) pour chaque service contenu dans le processus. Chaque structure spécifie le nom du service et le point d’entrée du service. Pour obtenir un exemple, consultez [écriture de la fonction principale d’un programme de service](writing-a-service-program-s-main-function.md).

Si [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) s’effectue correctement, le thread appelant n’est pas retourné tant que tous les services en cours d’exécution du processus n’ont pas entré l’état d’arrêt du service \_ . Le SCM envoie des demandes de contrôle à ce thread via un canal nommé. Le thread joue le rôle de répartiteur de contrôle, en effectuant les tâches suivantes :

-   Créez un nouveau thread pour appeler le point d’entrée approprié lorsqu’un nouveau service est démarré.
-   Appelez la [fonction de gestionnaire](service-control-handler-function.md) appropriée pour gérer les demandes de contrôle de service.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de la fonction principale d’un programme de service](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



