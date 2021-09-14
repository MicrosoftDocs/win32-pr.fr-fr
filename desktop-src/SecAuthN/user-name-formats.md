---
description: Quand une application utilise l’API de gestion des informations d’identification pour demander des informations d’identification, l’utilisateur doit entrer des informations qui peuvent être validées, soit par le système d’exploitation, soit par l’application.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formats de nom d’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096241"
---
# <a name="user-name-formats"></a>Formats de nom d’utilisateur

Quand une application utilise l’API de gestion des informations d’identification pour demander des informations d’identification, l’utilisateur doit entrer des informations qui peuvent être validées, soit par le système d’exploitation, soit par l’application. L’utilisateur peut spécifier les informations d’identification de domaine dans l’un des formats suivants :

-   [Nom d'utilisateur principal](#user-principal-name)
-   [Nom d’ouverture de session de niveau supérieur](#down-level-logon-name)

## <a name="user-principal-name"></a>Nom d’utilisateur principal

Le format UPN ( [*user principal name*](../secgloss/u-gly.md) ) est utilisé pour spécifier un nom de style Internet, tel que <b>UserName@Example.Microsoft.com</b> . Le tableau suivant récapitule les parties d’un UPN.



| Partie                                                        | Exemple                                |
|-------------------------------------------------------------|----------------------------------------|
| Nom du compte d’utilisateur. Également appelé nom d’ouverture de session.<br/> | *UserName*<br/>                  |
| Séparateur. Un littéral de caractère, le signe arobase (@).<br/> | @<br/>                           |
| Suffixe UPN. Également appelé nom de domaine.<br/>       | *Example.Microsoft.com* <br/> |



 

Un UPN peut être défini implicitement ou explicitement. Un UPN implicite est de la forme <b>UserName@DNSDomainName.com</b> . Un UPN implicite est toujours associé au compte de l’utilisateur, même si un UPN explicite n’est pas défini. Un UPN explicite est de la forme <i><b>Name@Suffix</b></i> , où les chaînes de nom et de suffixe sont définies explicitement par l’administrateur.

## <a name="down-level-logon-name"></a>Nom d’ouverture de session Down-Level

Le format du nom d’ouverture de session de niveau supérieur est utilisé pour spécifier un domaine et un compte d’utilisateur dans ce domaine, par exemple <i><b>domaine \\ NomUtilisateur</b></i>. Le tableau suivant récapitule les parties d’un nom d’ouverture de session de niveau supérieur.



| Partie                                                           | Exemple               |
|----------------------------------------------------------------|-----------------------|
| Nom de domaine NetBIOS.<br/>                                | *DOMAIN*<br/>   |
| Séparateur. Littéral de caractère, la barre oblique inverse ( \\ ).<br/> | **\\**<br/>     |
| Nom du compte d’utilisateur. Également appelé nom d’ouverture de session.<br/>    | *UserName*<br/> |



 

 

 
