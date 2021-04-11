---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: Les valeurs de Registre associées à la \_ \_ \\ \\ clé OLE Microsoft OLE de l’ordinateur local \\ contrôlent les paramètres d’autorisation d’accès et de lancement par défaut ainsi que les fonctionnalités de sécurité au niveau des appels pour les applications com qui n’appellent pas CoInitializeSecurity.
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02406bca5dd69098f8cd49c2fba5f067852fcc5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029772"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE

Les valeurs de Registre associées à la clé **\_ \_ \\ \\ \\ OLE Microsoft OLE de l’ordinateur local** contrôlent les paramètres d’autorisation d’accès et de lancement par défaut ainsi que les fonctionnalités de sécurité au niveau des appels pour les applications com qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Seuls les administrateurs, le créateur de l’objet et le système ont un accès complet à cette partie du Registre. Tous les autres utilisateurs disposent d’un accès en lecture seule.



| Valeur de Registre                                                                         | Description                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md)                 | Définit le niveau de détail des entrées du journal des événements sur les demandes ayant échoué pour le lancement et l’activation des composants.                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | Définit le niveau de détail des entrées du journal des événements sur les appels ayant échoué aux composants.                                                                                                     |
| [**DCOMSCMRemoteCallFlags**](dcomscmremotecallflags.md)                               | Contrôle le comportement des appels du gestionnaire de contrôle des services DCOM local (DCOMSCM) à un DCOMSCM distant.                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | Définit la liste des autorisations d’accès par défaut pour l’ordinateur.                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | Définit la liste de contrôle d’accès de lancement par défaut pour l’ordinateur.                                                                                                                                  |
| [**EnableDCOM**](enabledcom.md)                                                       | Définit la stratégie d’activation globale pour l’ordinateur.                                                                                                                           |
| [**InvalidSecurityDescriptorLoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | Définit le niveau de détail des entrées du journal des événements sur les descripteurs de sécurité non valides pour le lancement et les autorisations d’accès des composants.                                                       |
| [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)                         | Définit le niveau d’authentification par défaut.                                                                                                                                        |
| [**LegacyImpersonationLevel**](legacyimpersonationlevel.md)                           | Définit le niveau d’emprunt d’identité par défaut.                                                                                                                                         |
| [**LegacySecureReferences**](legacysecurereferences.md)                               | Détermine le niveau de sécurité des appels de version de **AddRef** /  .                                                                                                              |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | Définit la stratégie de restriction au niveau de l’ordinateur pour l’accès aux composants.                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | Définit la stratégie de restriction à l’ensemble de l’ordinateur pour le lancement et l’activation de composants.                                                                                                |
| [**Pas de ReDim**](nonredist.md)                                                         | Ajoute des noms à la liste des fichiers qui ne doivent pas être exportés lorsque les applications COM+ sont empaquetées pour être installées sur d’autres ordinateurs. Notez qu’il s’agit d’une sous-clé, et non d’une valeur. |
| [**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)                   | Détermine si les niveaux de confiance de la stratégie de restriction logicielle (SRP) sont utilisés lors des activations de ActivateAsActivator.                                                            |
| [**SRPRunningObjectChecks**](srprunningobjectchecks.md)                               | Détermine si les tentatives de connexion aux objets en cours d’exécution sont filtrées pour les niveaux de confiance de stratégie de restriction logicielle (SRP) compatibles.                                         |



 

 

 




