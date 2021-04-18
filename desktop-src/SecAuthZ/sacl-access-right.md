---
description: Le \_ droit accès à la sécurité du système Access \_ contrôle la possibilité d’accéder ou de définir la liste SACL dans un descripteur de sécurité d’objets. Le système accorde ce droit d’accès si le \_ \_ privilège nom de sécurité se est activé dans le jeton d’accès du thread demandeur.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Droit d’accès SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516046"
---
# <a name="sacl-access-right"></a>Droit d’accès SACL

Le \_ droit accès à la sécurité du système Access \_ contrôle la capacité à récupérer ou à définir la liste SACL dans le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet. Le système accorde ce droit d’accès uniquement si le \_ \_ privilège nom de sécurité se est activé dans le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du thread demandeur.

**Pour accéder à la liste SACL d’un objet**

1.  Appelez la fonction [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour activer le \_ privilège de nom de sécurité se \_ .
2.  Demandez le droit accès à la \_ sécurité du système Access \_ lorsque vous ouvrez un handle vers l’objet.
3.  Obtenir ou définir la liste SACL de l’objet à l’aide d’une fonction telle que [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  Appelez [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour désactiver le \_ privilège de nom de sécurité se \_ .

Pour accéder à une liste SACL à l’aide des fonctions [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , activez le \_ privilège nom de sécurité se \_ . La fonction demande en interne le droit d’accès.

Le droit d’accès à la \_ sécurité du système \_ d’accès n’est pas valide dans une liste DACL, car les DACL ne contrôlent pas l’accès à une liste SACL. Toutefois, vous pouvez utiliser le droit accès à la \_ sécurité du système \_ dans une liste SACL pour auditer les tentatives d’utilisation du droit d’accès.

 

 
