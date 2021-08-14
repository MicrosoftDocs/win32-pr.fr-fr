---
description: Fonctions permettant de créer un descripteur de sécurité et d’obtenir et de définir les composants d’un descripteur de sécurité.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Création d’un descripteur de sécurité de bas niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6462dcd7672836df5f2c1f6b368723bc3a9488eff290dc22a071ce40279def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781482"
---
# <a name="low-level-security-descriptor-creation"></a>Création d’un descripteur de sécurité de bas niveau

Le contrôle d’accès de bas niveau fournit un ensemble de fonctions permettant de créer un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) et d’obtenir et de définir les composants d’un descripteur de sécurité. Les fonctions de bas niveau pour l’initialisation et la définition des composants d’un descripteur de sécurité fonctionnent uniquement avec des descripteurs de sécurité de format absolu. Les fonctions de bas niveau pour obtenir les composants d’un descripteur de sécurité fonctionnent avec les [descripteurs de sécurité absolus et auto-relatifs](absolute-and-self-relative-security-descriptors.md).

La fonction [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) Initialise une mémoire tampon de [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) . Le descripteur de sécurité initialisé est au format [*absolu*](/windows/desktop/SecGloss/a-gly) et n’a pas de propriétaire, de groupe principal, de [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) ou de liste de contrôle d' [*accès système*](/windows/desktop/SecGloss/s-gly) (SACL). Vous pouvez utiliser les fonctions de bas niveau suivantes pour obtenir ou définir des composants spécifiques d’un descripteur de sécurité spécifié.



| Fonction                                                             | Description                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Récupère des informations de révision et de contrôle à partir d’un descripteur de sécurité.                                                                                                    |
| [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Récupère la liste DACL d’un descripteur de sécurité.                                                                                                                            |
| [**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Récupère l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du groupe principal à partir d’un descripteur de sécurité. |
| [**GetSecurityDescriptorLength**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Retourne la longueur d’un descripteur de sécurité.                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Récupère le SID propriétaire à partir d’un descripteur de sécurité.                                                                                                                       |
| [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Récupère la liste SACL d’un descripteur de sécurité.                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Place une liste DACL dans un descripteur de sécurité, remplaçant toute liste DACL existante.                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Définit le SID du groupe principal d’un descripteur de sécurité.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Définit le SID propriétaire d’un descripteur de sécurité.                                                                                                                              |
| [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Place une liste SACL dans un descripteur de sécurité, remplaçant toute liste SACL existante.                                                                                                    |



 

Pour vérifier le niveau de révision et l' [*intégrité*](/windows/desktop/SecGloss/i-gly) structurelle d’un descripteur de sécurité, appelez la fonction [**IsValidSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor) .

 

 
