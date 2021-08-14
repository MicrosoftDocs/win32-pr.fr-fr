---
description: pour déterminer si un descripteur de sécurité est auto-relatif ou absolu, appelez la fonction GetSecurityDescriptorControl et vérifiez la SE \_ \_ indicateur auto relatif \_ du paramètre de contrôle de descripteur de sécurité \_ .
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Descripteurs de sécurité absolus et Self-Relative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a2639d1f17527b92116eabcaca96b637012253bbafc42198e37c9867fc585c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914721"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Descripteurs de sécurité absolus et Self-Relative

Un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) peut être dans un format [*absolu*](/windows/desktop/SecGloss/a-gly) ou [*auto-relatif*](/windows/desktop/SecGloss/s-gly) . Au format absolu, un descripteur de sécurité contient des pointeurs vers ses informations, pas les informations elles-mêmes. Dans un format auto-relatif, un descripteur de sécurité stocke une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) et les informations de sécurité associées dans un bloc de mémoire contigu. pour déterminer si un descripteur de sécurité est auto-relatif ou absolu, appelez la fonction [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) et vérifiez la SE \_ \_ indicateur auto relatif du paramètre de [**\_ \_ contrôle de descripteur de sécurité**](security-descriptor-control.md) . Vous pouvez utiliser les fonctions [**MakeSelfRelativeSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) et [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) pour la conversion entre ces deux formats.

Le format absolu est utile lorsque vous générez un descripteur de sécurité et que vous avez des pointeurs vers tous les composants, par exemple, lorsque les paramètres par défaut du propriétaire, du groupe et de la liste de contrôle d’accès discrétionnaire sont disponibles. Dans ce cas, vous pouvez appeler la fonction [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) pour initialiser une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , puis appeler des fonctions telles que [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) pour ASsigner des pointeurs de liste de contrôle d’accès et sid au descripteur de sécurité.

Dans un format auto-relatif, un descripteur de sécurité commence toujours par une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , mais les autres composants du descripteur de sécurité peuvent suivre la structure dans n’importe quel ordre. Au lieu d’utiliser des adresses mémoire, les composants du descripteur de sécurité sont identifiés par des décalages à partir du début du descripteur. Ce format est utile lorsqu’un descripteur de sécurité doit être stocké sur le disque, transmis au moyen d’un protocole de communication ou copié en mémoire.

À l’exception de [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd), toutes les fonctions qui retournent un descripteur de sécurité utilisent le format auto-relatif. Les descripteurs de sécurité passés comme arguments à une fonction peuvent être de forme auto-relative ou absolue. Pour plus d’informations, reportez-vous à la documentation de la fonction.

 

 
