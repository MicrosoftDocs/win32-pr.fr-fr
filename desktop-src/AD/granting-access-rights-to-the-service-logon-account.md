---
title: Octroi de droits d’accès au compte d’ouverture de session du service
description: L’un des principaux points à prendre en compte lors de l’installation d’une instance de service est de s’assurer que le service installé peut accéder aux ressources nécessaires.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Octroi de droits d’accès à l’AD du compte d’ouverture de session du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d13d3e06432b3501961f65a3e27ca00a46f18197bef23d78e6f7ca0deec59b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189078"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Octroi de droits d’accès au compte d’ouverture de session du service

L’un des principaux points à prendre en compte lors de l’installation d’une instance de service est de s’assurer que le service installé peut accéder aux ressources nécessaires. Pour ce faire, définissez les ACE dans les descripteurs de sécurité des objets auxquels le service doit accéder. Un ACE peut accorder ou refuser des droits d’accès à un principal de sécurité spécifié, tel que le compte d’utilisateur du service, ou le compte d’ordinateur pour un service LocalSystem, ou un groupe auquel appartient le compte du service. Pour plus d’informations sur les ACE, les descripteurs de sécurité et le contrôle d’accès, consultez [contrôle de l’accès aux objets dans Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) et [Access Control](/windows/desktop/SecAuthZ/access-control).

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir une entrée du contrôle d’accès qui permet au service de modifier son point de connexion de service, consultez [activation du compte de service pour accéder aux propriétés SCP](enabling-service-account-to-access-scp-properties.md).

Dans certains cas, vous devez ajouter votre compte d’utilisateur de service en tant que membre d’un ou de plusieurs groupes de sécurité. Par exemple, si vous créez un groupe administrateurs pour votre service, vous pouvez faire en sorte que le service soit membre du groupe. Vous pouvez ensuite accorder des droits d’accès au groupe plutôt que de les accorder explicitement au compte de service. Pour plus d’informations sur les groupes de sécurité, consultez [gestion des groupes](managing-groups.md).

 

 