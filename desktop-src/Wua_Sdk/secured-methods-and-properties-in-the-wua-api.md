---
description: Lorsque WUA détecte qu’un appelant n’est pas autorisé à accéder à une interface, une méthode ou une propriété, le HRESULT E \_ ACCESSDENIED est retourné.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Sécurisation des interfaces, des méthodes et des propriétés dans l’API WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517516"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a>Sécurisation des interfaces, des méthodes et des propriétés dans l’API WUA

Certaines interfaces, méthodes et propriétés de Windows Update Agent (WUA) sont accessibles uniquement aux appelants qui appartiennent aux groupes de sécurité Windows suivants :

-   Administrateur
-   Utilisateur
-   Utilisateur avancé

Lorsque WUA détecte qu’un appelant n’est pas autorisé à accéder à une interface, une méthode ou une propriété, le **HRESULT** E \_ ACCESSDENIED est retourné.

Les interfaces suivantes sont disponibles pour les groupes de sécurité administrateur, utilisateur et utilisateur avec pouvoir :

-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [**IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) et [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)

> [!Note]  
> Si les conditions suivantes sont remplies, une recherche échoue :
>
> -   Un utilisateur qui n’est pas un administrateur définit la [**propriété UserLocale de l’interface IUpdateSession2 sur des**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) paramètres régionaux qui correspondent à une langue qui n’est pas installée sur l’ordinateur.
> -   La recherche utilise un objet UpdateSearch créé à partir de l’objet UpdateSession.

 

Les interfaces et les méthodes de téléchargement suivantes sont disponibles pour l’administrateur et les groupes d’utilisateurs avec pouvoir :

-   [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [**IUpdate::CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IAutomaticUpdatesSettings2 :: CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent appeler [**IAutomaticUpdatesSettings2 :: checkPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).

     

Les interfaces d’installation, les méthodes et les propriétés suivantes sont disponibles pour les groupes d’administrateurs :

-   [**IAutomaticUpdates ::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates :: Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [**Propriété IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden). Toutefois, seuls les administrateurs et les utilisateurs avec pouvoir peuvent définir les valeurs.

     

-   [**IUpdate :: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > Les administrateurs et les utilisateurs avec pouvoir peuvent appeler la [**méthode AcceptEula de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).

     

-   [**IAutomaticUpdatesSettings :: enregistrer**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [**Propriété NotificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété NotificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel). Toutefois, seuls les administrateurs peuvent définir les valeurs.

     

-   [**Propriété ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday). Toutefois, seuls les administrateurs peuvent définir les valeurs.

     

-   [**Propriété ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Toutefois, seuls les administrateurs peuvent définir les valeurs.

     

-   [**Propriété IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates). Toutefois, seuls les administrateurs peuvent définir les valeurs.

     

 

 



