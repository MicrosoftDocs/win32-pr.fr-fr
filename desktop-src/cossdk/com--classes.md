---
description: Voici les classes COM+.
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: Classes COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626c3dfdae542b602cf27a8d8be5cb69dde5910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111686"
---
# <a name="com-classes"></a>Classes COM+

Voici les classes COM+.



| Classe                                                            | Description                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppDomainHelper**](appdomainhelper.md)                       | Lie un objet managé à un domaine d’application, qui est un environnement isolé dans lequel les applications s’exécutent.                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | Récupère des informations sur un assembly lors de l’utilisation du code managé dans le common language runtime .NET Framework.                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | Spécifie et configure les services qui doivent être actifs dans le domaine de service entré lors de l’appel de [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) ou [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).                     |
| [**SecurityCallContext**](securitycallcontext.md)               | Fournit l’accès au contexte de sécurité de l’appel actuel, qui contient des informations sur les appelants d’un objet.                                                                                                                           |
| [**SecurityCallers**](securitycallers.md)                       | Fournit l’accès aux informations sur les appelants individuels dans une collection d’appelants. La collection représente la chaîne d’appels se terminant par l’appel en cours, et chaque appelant de la collection représente l’identité d’un appelant. |
| [**SecurityIdentity**](securityidentity.md)                     | Fournit l’accès à une collection d’informations de sécurité représentant l’identité d’un appelant. À l’aide de cette classe, vous pouvez trouver des informations sur un appelant particulier dans une chaîne d’appelants qui fait partie du contexte de l’appel de sécurité.                 |
| [**SharedProperty**](sharedproperty.md)                         | Définit ou récupère la valeur d’une propriété partagée.                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | Crée les propriétés partagées et y accède dans un groupe de propriétés partagées.                                                                                                                                                                  |
| [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) | Crée des groupes de propriétés partagées et pour obtenir l’accès aux groupes de propriétés partagés existants.                                                                                                                                                 |
| [**TransactionContext**](transactioncontext.md)                 | Crée un objet transactionnel générique qui commence une transaction.                                                                                                                                                                       |
| [**TransactionContextEx**](transactioncontextex.md)             | Crée un objet transactionnel générique qui commence une transaction. En appelant les méthodes de cette classe, vous pouvez composer le travail de plusieurs objets COM dans une transaction unique et valider ou abandonner explicitement la transaction.        |



 

 

 



