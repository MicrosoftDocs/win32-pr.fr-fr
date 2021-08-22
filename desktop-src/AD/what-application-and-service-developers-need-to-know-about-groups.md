---
title: Ce que les développeurs d’applications et de services doivent savoir sur les groupes
description: Lors du développement d’une application ou d’un service, vous pouvez utiliser des groupes pour déléguer l’administration ou contrôler l’accès à l’application ou au service en totalité ou en partie.
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- Ce que les développeurs d’applications et de services doivent savoir sur les groupes
- groupes Active Directory, informations pour les développeurs d’applications et de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b59a8a1ce369d9b5fa1093297f219bf6a206178a950b9d0762fde3069846551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024390"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>Ce que les développeurs d’applications et de services doivent savoir sur les groupes

Lors du développement d’une application ou d’un service, vous pouvez utiliser des groupes pour déléguer l’administration ou contrôler l’accès à l’application ou au service en totalité ou en partie. Par exemple, une application peut contrôler qui peut effectuer diverses opérations d’administration. Pour ce faire, créez des ACE qui accordent des droits d’accès spécifiés aux groupes appropriés. Il est recommandé de disposer d’un ACE qui accorde l’accès à un groupe plutôt que d’avoir plusieurs ACE qui accordent l’accès à des utilisateurs individuels ou à des ordinateurs.

Il est recommandé que les applications utilisent les recommandations suivantes lors de l’utilisation de groupes :

-   Ne créez pas de dépendances sur des groupes codés en dur, ce qui peut créer des complications si le groupe est supprimé ou déplacé.
-   Évitez d’utiliser des groupes intégrés, sauf si la fonction du groupe fournit les besoins spécifiques de l’application. Par exemple, il n’est pas nécessaire qu’un utilisateur soit membre du groupe administrateurs uniquement pour accorder à l’utilisateur l’autorisation de créer un compte d’ordinateur. Cela permet à l’utilisateur d’avoir des autorisations et des privilèges dont ils n’ont peut-être pas besoin, ce qui peut entraîner une faille de sécurité. Au lieu de cela, vous devez créer un nouveau groupe de sécurité qui dispose des autorisations spécifiques requises et ajouter l’utilisateur à ce nouveau groupe.
-   Lorsque vous créez de nouveaux groupes, gardez à l’esprit les recommandations suivantes :
    -   Protégez le groupe en définissant des ACE qui contrôlent qui peut ajouter ou supprimer des membres.
    -   Utilisez des groupes globaux s’ils sont utilisés pour le contrôle d’accès sur des objets dans Active Directory Domain Services.
    -   Utilisez des groupes universels uniquement si nécessaire (les données de membre sont requises globalement à l’aide d’un catalogue global ; le groupe peut contenir n’importe quel utilisateur/groupe). Si vous utilisez des groupes universels, placez les groupes globaux dans le groupe universel et ajoutez/supprimez des utilisateurs dans le groupe global. Évitez toute modification excessive des groupes universels pour améliorer l’efficacité de la réplication.
-   N’utilisez pas l’appartenance à un groupe pour le contrôle d’accès. Au lieu de cela, utilisez une entrée ACE et contrôlez l’accès en demandant au système d’effectuer une vérification d’accès.

pour contrôler l’accès aux opérations qui ne tiennent pas dans les droits d’accès prédéfinis pour les objets dans domaine Active Directory services, utilisez la fonctionnalité contrôler les droits d’accès du contrôle d’accès dans Windows 2000. Pour plus d’informations, [**consultez \_ \_ énumération des droits ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum).

**Pour utiliser un droit d’accès de contrôle pour contrôler le droit d’effectuer une opération**

1.  Créez un droit d’accès de contrôle qui définit le type d’accès à l’application ou au service. Pour plus d’informations, consultez [contrôler les droits d’accès](control-access-rights.md).
2.  Créez un objet dans Active Directory Domain Services qui représente l’application, le service ou la ressource.
3.  Ajoutez des ACE d’objet à la liste DACL dans le descripteur de sécurité de l’objet pour accorder ou refuser aux utilisateurs ou aux groupes le droit d’accès au contrôle sur cet objet. Pour plus d’informations, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).
4.  Lorsqu’un utilisateur tente d’exécuter l’opération protégée, votre application ou service utilise la fonction [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) pour déterminer si le droit d’accès au contrôle est accordé à l’utilisateur. Pour plus d’informations, consultez [vérification du droit d’accès à un contrôle dans la liste](checking-a-control-access-right-in-an-objectampaposs-acl.md)de contrôle d’accès d’un objet.
5.  En fonction du résultat de la vérification d’accès sur l’objet, votre application ou service peut accorder ou refuser à l’utilisateur l’accès à l’application ou au service.

Une application de service peut également créer un groupe dont les membres seraient les différentes instances de service. Par exemple, un service avec des instances installées sur plusieurs ordinateurs dans une entreprise peut avoir un fichier journal commun sur lequel toutes les instances de service sont écrites. Le programme d’installation du service crée le fichier journal et utilise une liste DACL pour accorder l’accès uniquement aux membres d’un groupe. Les membres du groupe sont les comptes d’utilisateur sous lesquels les différentes instances de service s’exécutent, ou si les services s’exécutent sous le compte LocalSystem, les membres sont les comptes d’ordinateur des serveurs hôtes.

 

 