---
description: Un jeton restreint est un jeton d’accès principal ou d’emprunt d’identité qui a été modifié par la fonction CreateRestrictedToken.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Jetons restreints
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee8e6c89915e3edd0a9206f84a0d3d5697a3cb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193819"
---
# <a name="restricted-tokens"></a>Jetons restreints

Un jeton restreint est un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) [*principal*](/windows/desktop/SecGloss/p-gly) ou d’emprunt d’identité qui a été modifié par la fonction [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . Un [*processus*](/windows/desktop/SecGloss/p-gly) ou l’emprunt de l’identité d’un thread qui s’exécute dans le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) d’un jeton restreint est limité dans sa capacité à accéder aux objets sécurisables ou à effectuer des opérations privilégiées. La fonction **CreateRestrictedToken** peut restreindre un jeton des manières suivantes :

-   Supprimez les [privilèges](privileges.md) du jeton.
-   Appliquez l’attribut de refus uniquement aux sid dans le jeton afin qu’ils ne puissent pas être utilisés pour accéder aux objets sécurisés. Pour plus d’informations sur l’attribut de refus uniquement, consultez [attributs SID dans un jeton d’accès](sid-attributes-in-an-access-token.md).
-   Spécifiez une liste de SID de restriction, qui peut limiter l’accès aux objets sécurisables.

Le système utilise la liste des SID restreints lorsqu’il vérifie l’accès du jeton à un objet sécurisable. Quand un processus ou un thread restreint tente d’accéder à un objet sécurisable, le système effectue deux vérifications d’accès : une utilisant les SID activés du jeton et une autre à l’aide de la liste des SID de restriction. L’accès est accordé uniquement si les deux contrôles d’accès autorisent les droits d’accès demandés. Pour plus d’informations sur les contrôles d’accès, consultez [Comment les DACL contrôlent l’accès à un objet](how-dacls-control-access-to-an-object.md).

Vous pouvez utiliser un [*jeton principal*](/windows/desktop/SecGloss/p-gly) restreint dans un appel à la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . en règle générale, le processus qui appelle **CreateProcessAsUser** doit avoir le \_ privilège SE ASSIGNPRIMARYTOKEN \_ NAME, qui est généralement détenu uniquement par le code système ou par les services s’exécutant dans le compte LocalSystem. Toutefois, si l’appel de **CreateProcessAsUser** spécifie une version limitée du jeton principal de l’appelant, ce privilège n’est pas requis. Cela permet aux applications ordinaires de créer des processus restreints.

Vous pouvez également utiliser un jeton principal ou d' [*emprunt d’identité*](/windows/desktop/SecGloss/i-gly) restreint dans la fonction [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .

Pour déterminer si un jeton a une liste de sid restreints, appelez la fonction [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) .

> [!Note]  
> Les applications qui utilisent des jetons restreints doivent exécuter l’application restreinte sur des ordinateurs de bureau autres que le bureau par défaut. Cela est nécessaire pour empêcher une attaque par une application restreinte, à l’aide de **SendMessage** ou **PostMessage**, à des applications non restreintes sur le bureau par défaut. Si nécessaire, basculez entre les ordinateurs de bureau à des fins d’application.

 

 

 
