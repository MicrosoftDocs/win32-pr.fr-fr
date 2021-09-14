---
description: Windows 7 et Windows Server 2008 R2 incluent les éléments de programmation nouveaux et mis à jour suivants pour les services.
ms.assetid: 4be7e244-ad4c-440d-b04e-23afb4c7ddf2
title: nouveautés des Services pour Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bd2e8bfa5426447e24485ed026f27e90fdcaa1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311266"
---
# <a name="whats-new-in-services-for-windows-7"></a>nouveautés des Services pour Windows 7

Windows 7 et Windows Server 2008 R2 incluent les éléments de programmation nouveaux et mis à jour suivants pour les services.

## <a name="new-capabilities"></a>Nouvelles fonctionnalités

Un service peut s’inscrire pour être démarré ou arrêté lorsqu’un événement déclencheur se produit. Cela élimine la nécessité de démarrer les services au démarrage du système, ou pour que les services interinterrogent ou attendent activement un événement. un service peut démarrer quand il est nécessaire, au lieu de démarrer automatiquement, qu’il y ait ou non un travail à effectuer. Pour plus d’informations, consultez [événements déclencheurs de service](service-trigger-events.md).

## <a name="updated-functions"></a>Fonctions mises à jour



| Fonction                                                        | Description                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)<br/>   | Modifie les paramètres de configuration d’un service. Cette fonction prend en charge les comptes de service administrés et les comptes virtuels. Pour plus d’informations, consultez le [Guide pas à pas des comptes de service](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/>                                      |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)<br/> | Modifie les paramètres de configuration facultatifs d’un service. Cette fonction prend en charge de nouveaux niveaux d’informations de configuration pour les groupes de processeurs et les événements de déclencheur de service.<br/>                                                                                                        |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)<br/>               | Crée un objet de service et l’ajoute à la base de données du gestionnaire de contrôle des services spécifiée. Cette fonction prend en charge les comptes de service administrés et les comptes virtuels. Pour plus d’informations, consultez le [Guide pas à pas des comptes de service](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/> |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                       | Fonction de rappel définie par l’application utilisée avec la fonction [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) . Cette fonction de rappel prend en charge de nouveaux codes de contrôle étendu pour les changements d’heure système et les événements de déclencheur de service.<br/>                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)<br/>   | Récupère les paramètres de configuration facultatifs d’un service. Cette fonction prend en charge de nouveaux niveaux d’informations de configuration pour les groupes de processeurs et les événements de déclencheur de service.<br/>                                                                                                      |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)<br/>         | Met à jour les informations d’État du gestionnaire de contrôle des services pour le service appelant. Cette fonction prend en charge de nouveaux codes de contrôle étendu pour les changements d’heure système et les événements de déclencheur de service.<br/>                                                                                         |



 

## <a name="new-structures"></a>Nouvelles structures



| Structure                                                                                       | Description                                                            |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**\_informations sur le TIMECHANGE de service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info)<br/>                         | Contient les paramètres de modification de l’heure système. <br/>                      |
| [**\_déclencheur de service**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)<br/>                                          | Représente un événement de déclencheur de service.<br/>                         |
| [**\_informations sur le déclencheur de service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)<br/>                               | Contient les informations d’événement de déclencheur pour un service.<br/>           |
| [**\_élément de \_ \_ données spécifique à un DÉCLENCHEur de service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | Contient des données spécifiques au déclencheur pour un événement de déclencheur de service.<br/> |



 

 

