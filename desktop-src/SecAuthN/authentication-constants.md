---
description: Répertorie les constantes utilisées pour les API d’authentification Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Constantes d’authentification (authentification)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538924"
---
# <a name="authentication-constants-authentication"></a>Constantes d’authentification (authentification)

## <a name="credentials-management-constants"></a>Constantes de gestion des informations d’identification

La gestion des informations d’identification utilise les constantes suivantes pour spécifier des tailles de chaîne maximales.



| Constante                                        | Description                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| CREDUI \_ longueur maximale du \_ message \_<br/>         | Nombre maximal de caractères pour le membre **pszMessageText** d’une structure [**CREDUI \_ info**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .<br/> |
| longueur de la \_ légende Max CREDUI \_ \_<br/>         | Nombre maximal de caractères pour le membre **pszCaptionText** d’une structure [**CREDUI \_ info**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .<br/> |
| \_longueur maximale de la \_ \_ cible générique \_ CREDUI<br/> | Nombre maximal de caractères dans une chaîne qui spécifie un nom cible.<br/>                                             |
| \_longueur maximale de la \_ cible de domaine CREDUI \_ \_<br/>  | Nombre maximal de caractères dans une chaîne qui spécifie un nom de domaine.<br/>                                             |
| \_longueur maximale du \_ nom d’utilisateur CREDUI \_<br/>        | Nombre maximal de caractères dans une chaîne qui spécifie un nom de compte d’utilisateur.<br/>                                       |
| \_longueur maximale du \_ mot de passe CREDUI \_<br/>        | Nombre maximal de caractères dans une chaîne qui spécifie un mot de passe.<br/>                                                |



 

## <a name="gina-defined-values"></a>Valeurs définies dans Gina

Les fonctions d’interface [*Gina*](/windows/desktop/SecGloss/g-gly) et les fonctions de prise en charge [*Winlogon*](/windows/desktop/SecGloss/w-gly) utilisent les valeurs définies suivantes.

> [!Note]  
> Les DLL GINA sont ignorées dans Windows Vista.

 



| Valeur                                                              | Description                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**\_option de connexion wlx \_ \_ xxx**](wlx-logon-option-xxx.md)<br/> | Contient des options de connexion prédéfinies. Elle est utilisée par le paramètre *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).<br/> |
| [**\_type wlx \_ SAS \_ xxx**](wlx-sas-type-xxx.md)<br/>         | Définit un type SAS spécifique.<br/>                                                                                              |



 

 

