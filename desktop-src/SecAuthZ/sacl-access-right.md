---
description: Le \_ droit accès à la sécurité du système Access \_ contrôle la possibilité d’accéder ou de définir la liste SACL dans un descripteur de sécurité d’objets. le système accorde ce droit d’accès si le \_ \_ privilège SE nom de sécurité est activé dans le jeton d’accès du thread demandeur.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Droit d’accès SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88256664db25c6e906f3b4ca0459217a29d0cc7c0e2dd544c1cf198bc24fff5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780514"
---
# <a name="sacl-access-right"></a>Droit d’accès SACL

Le \_ droit accès à la sécurité du système Access \_ contrôle la capacité à récupérer ou à définir la liste SACL dans le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet. le système accorde ce droit d’accès uniquement si le \_ \_ privilège SE nom de sécurité est activé dans le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du thread demandeur.

**Pour accéder à la liste SACL d’un objet**

1.  appelez la fonction [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour activer le \_ privilège SE \_ nom de sécurité.
2.  Demandez le droit accès à la \_ sécurité du système Access \_ lorsque vous ouvrez un handle vers l’objet.
3.  Obtenir ou définir la liste SACL de l’objet à l’aide d’une fonction telle que [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  appelez [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour désactiver le \_ privilège de nom de sécurité SE \_ .

pour accéder à une liste SACL à l’aide des fonctions [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , activez le \_ privilège SE nom de sécurité \_ . La fonction demande en interne le droit d’accès.

Le droit d’accès à la \_ sécurité du système \_ d’accès n’est pas valide dans une liste DACL, car les DACL ne contrôlent pas l’accès à une liste SACL. Toutefois, vous pouvez utiliser le droit accès à la \_ sécurité du système \_ dans une liste SACL pour auditer les tentatives d’utilisation du droit d’accès.

 

 
