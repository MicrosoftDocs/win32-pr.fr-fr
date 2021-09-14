---
description: Les fonctions suivantes sont utilisées ou implémentées par les services.
ms.assetid: 63666848-cbac-4853-8b91-89303f9854c0
title: Fonctions de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431a672e93c94e06a71812471aa3c74d0ac2f96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013554"
---
# <a name="service-functions"></a>Fonctions de service

Les fonctions suivantes sont utilisées ou implémentées par les services.



| Fonction                                                             | Description                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**D**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)                                           | Fonction de rappel définie par l’application utilisée avec la fonction [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) .     |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)                                       | Fonction de rappel définie par l’application utilisée avec la fonction [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) . |
| [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     | Inscrit une fonction pour gérer les demandes de contrôle de service.                                                                              |
| [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) | Inscrit une fonction pour gérer les demandes de contrôle de service étendues.                                                                     |
| [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)                                   | Fonction définie par l’application qui sert de point de départ pour un service.                                                      |
| [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits)                             | Inscrit un type de service avec le gestionnaire de contrôle des services et le service serveur.                                                     |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)                         | Met à jour les informations d’État du gestionnaire de contrôle des services pour le service appelant.                                                     |
| [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)     | Connecte le thread principal d’un processus de service au gestionnaire de contrôle des services.                                                         |



 

Les fonctions suivantes sont utilisées par les programmes qui contrôlent, configurent ou interagissent avec les services.



| Fonction                                                                 | Description                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)                       | Modifie les paramètres de configuration d’un service.                                                                                          |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)                     | Modifie les paramètres de configuration facultatifs d’un service.                                                                                 |
| [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)                         | Ferme le handle spécifié d’un objet de gestionnaire de contrôle des services ou d’un objet de service.                                                        |
| [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)                                 | Envoie un code de contrôle à un service.                                                                                                          |
| [**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)                             | Envoie un code de contrôle à un service.                                                                                                          |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)                                   | Crée un objet de service et l’ajoute à la base de données du gestionnaire de contrôle des services spécifiée.                                                     |
| [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice)                                   | Marque le service spécifié pour suppression de la base de données du gestionnaire de contrôle des services.                                                         |
| [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa)                   | Récupère le nom et l’état de chaque service qui dépend du service spécifié.                                                        |
| [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)                     | Énumère les services de la base de données du gestionnaire de contrôle des services spécifiée en fonction du niveau d’information spécifié.                             |
| [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)                   | Récupère le nom complet du service spécifié.                                                                                        |
| [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea)                           | Récupère le nom de service du service spécifié.                                                                                        |
| [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                 | Signale l’état de démarrage au gestionnaire de contrôle des services.                                                                                     |
| [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea)           | Permet à une application de recevoir une notification lorsque le service spécifié est créé ou supprimé ou lorsque son état change.                 |
| [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)                                   | Établit une connexion au gestionnaire de contrôle des services sur l’ordinateur spécifié et ouvre la base de données du gestionnaire de contrôle des services spécifiée. |
| [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)                                       | Ouvre un service existant.                                                                                                                  |
| [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga)                         | Récupère les paramètres de configuration du service spécifié.                                                                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)                       | Récupère les paramètres de configuration facultatifs du service spécifié.                                                                   |
| [**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation) | Récupère les informations dynamiques relatives au démarrage du service actuel.                                                                         |
| [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)    | Récupère une copie du descripteur de sécurité associé à un objet de service.                                                               |
| [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)                     | Récupère l’état actuel du service spécifié en fonction du niveau d’information spécifié.                                             |
| [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity)        | Définit le descripteur de sécurité d’un objet de service.                                                                                           |
| [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)                                     | Démarre un service.                                                                                                                           |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

Les fonctions suivantes sont obsolètes.<dl>

[**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa)  
[**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)  
[**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)  
[**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)  
[**UnlockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-unlockservicedatabase)  
</dl>

 

 
