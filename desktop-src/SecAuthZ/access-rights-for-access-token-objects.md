---
description: Une application ne peut pas modifier la liste de contrôle d’accès d’un objet, sauf si l’application a les droits nécessaires.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Droits d’accès pour les objets Access-Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb6a62a8c1518dca30f2abbc4481fa5e11cf081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319037"
---
# <a name="access-rights-for-access-token-objects"></a>Droits d’accès pour les objets Access-Token

Une application ne peut pas modifier la liste de contrôle d’accès d’un objet, sauf si l’application a les droits nécessaires. Ces droits sont contrôlés par un descripteur de sécurité dans le jeton d’accès de l’objet. Pour plus d’informations sur la sécurité, consultez [Access Control modèle](access-control-model.md).

Pour obtenir ou définir le [descripteur de sécurité](security-descriptors.md) d’un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly), appelez les fonctions [**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) et [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) .

Quand vous appelez la fonction [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) ou [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) pour obtenir un handle à un jeton d’accès, le système vérifie les [droits d’accès](access-rights-and-access-masks.md) demandés par rapport à la liste DACL dans le descripteur de sécurité du jeton.

Les droits d’accès valides pour les objets de jeton d’accès sont les suivants :

-   Droits d’accès standard de suppression, de \_ contrôle de lecture, d’écriture \_ DAC et de propriétaire d’écriture \_ . [](standard-access-rights.md) Les jetons d’accès ne prennent pas en charge le droit d’accès synchronisation standard.
-   [Droit de \_ \_ sécurité du système d’accès](sacl-access-right.md) permettant d’extraire ou de définir la liste SACL dans le descripteur de sécurité de l’objet.
-   Les droits d’accès spécifiques pour les jetons d’accès, qui sont répertoriés dans le tableau suivant.

    | Valeur                     | Signification                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | réglage du jeton \_ \_ par défaut    | Requis pour modifier le propriétaire par défaut, le groupe principal ou la liste DACL d’un jeton d’accès.                                                                                                                                                                                                  |
    | \_groupes d’ajustement de jeton \_     | Requis pour ajuster les attributs des groupes dans un jeton d’accès.                                                                                                                                                                                                               |
    | \_privilèges d’ajustement de jeton \_ | Requis pour activer ou désactiver les privilèges dans un jeton d’accès.                                                                                                                                                                                                                  |
    | ID de session d' \_ ajustement de jeton \_  | Requis pour ajuster l’ID de session d’un jeton d’accès. Le \_ privilège de \_ nom TCB se est requis.                                                                                                                                                                                    |
    | affectation de jeton \_ \_ principal    | Requis pour attacher un [*jeton principal*](/windows/desktop/SecGloss/p-gly) à un [*processus*](/windows/desktop/SecGloss/p-gly). Le \_ \_ privilège de nom de ASSIGNPRIMARYTOKEN se est également requis pour accomplir cette tâche. |
    | JETON \_ dupliqué          | Requis pour dupliquer un jeton d’accès.                                                                                                                                                                                                                                            |
    | exécution du jeton \_            | Combine \_ les autorisations standard \_ Execute et Token \_ Impersonate.                                                                                                                                                                                                                        |
    | emprunter l’identité du jeton \_        | Requis pour attacher un jeton d’accès d’emprunt d’identité à un processus.                                                                                                                                                                                                                    |
    | requête de jeton \_              | Requis pour interroger un jeton d’accès.                                                                                                                                                                                                                                                |
    | SOURCE de la requête de jeton \_ \_      | Requis pour interroger la source d’un jeton d’accès.                                                                                                                                                                                                                                  |
    | lecture du jeton \_               | Combine la \_ \_ lecture des droits standard et la requête de jeton \_ .                                                                                                                                                                                                                                 |
    | écriture de jeton \_              | Combine \_ \_ les privilèges d’écriture de droits standard, d’ajustement de jeton, d’ajustement de \_ \_ jeton \_ et d' \_ ajustement de jeton \_ \_ par défaut.                                                                                                                                                                   |
    | JETON \_ tout \_ accès        | Combine tous les droits d’accès possibles pour un jeton.                                                                                                                                                                                                                                  |

    

     

 

 
