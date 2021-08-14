---
description: Un descripteur de sécurité fonctionnel valide contient des informations de sécurité au format binaire.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Chaînes de descripteur de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbefeb87a7fca30f0c33d6f180315df5e5d576dc018e69dc680391050a840d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413789"
---
# <a name="security-descriptor-strings"></a>Chaînes de descripteur de sécurité

Un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) fonctionnel valide contient des informations de sécurité au format binaire. l’API Windows fournit des fonctions permettant de convertir des descripteurs de sécurité binaires vers et à partir de chaînes de texte. Les descripteurs de sécurité au format chaîne ne sont pas fonctionnels, mais ils peuvent être utiles pour stocker ou transporter des informations de descripteur de sécurité.

Pour convertir un descripteur de sécurité en un format de chaîne, appelez la fonction [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) . Pour convertir un descripteur de sécurité au format chaîne en un descripteur de sécurité fonctionnel valide, appelez la fonction [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .

Pour plus d’informations, consultez [langage de définition du descripteur de sécurité](security-descriptor-definition-language.md).

 

 
