---
description: Répertorie les exigences imposées par les outils d’administration de système de mot de passe fort.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Mise en œuvre des mots de passe forts et Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b7be524511d52048e06ae83ab110384c3bf5c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009019"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a>Mise en œuvre des mots de passe forts et Passfilt.dll

L’application de mots de passe forts peut être activée à l’aide des outils d’administration système. Si la stratégie d’administration système est activée, les mots de passe doivent respecter la configuration minimale suivante lorsqu’ils sont créés ou modifiés :

-   Les mots de passe ne peuvent pas contenir la valeur samAccountName (nom de compte) de l’utilisateur ou une valeur displayName entière (nom complet). Les deux contrôles ne respectent pas la casse.
-   SamAccountName est vérifié dans son intégralité uniquement pour déterminer s’il fait partie du mot de passe. Si la valeur samAccountName est inférieure à trois caractères, cette vérification est ignorée.
-   DisplayName est analysé pour les délimiteurs : virgules, points, tirets ou traits d’Union, traits de soulignement, espaces, signes dièse et tabulations. Si l’un de ces délimiteurs est trouvé, displayName est fractionné et toutes les sections analysées (jetons) sont confirmées pour ne pas être incluses dans le mot de passe. Les jetons qui contiennent moins de trois caractères sont ignorés et les sous-chaînes des jetons ne sont pas vérifiées. Par exemple, le nom « Erin M. Hagens » est divisé en trois jetons : « Erin », « M » et « Hagens ». Étant donné que le deuxième jeton n’est qu’un caractère de longueur, il est ignoré. Par conséquent, cet utilisateur ne peut pas avoir un mot de passe qui incluait « Erin » ou « Hagens » en tant que sous-chaîne n’importe où dans le mot de passe.
-   Les mots de passe doivent contenir des caractères de trois des cinq catégories suivantes.



| Catégories de caractères                                                                                                                                                      | Exemples                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Lettres majuscules des langues européennes (de A à Z, avec des marques diacritiques, des caractères grecs et cyrilliques)<br/>                                                     | A, B, C, Z<br/>                |
| Lettres minuscules de langues européennes (de a à z, Sharp-s, avec des marques diacritiques, des caractères grecs et cyrilliques)<br/>                                            | a, b, c, z<br/>                |
| Chiffres de la base 10 (0 à 9)<br/>                                                                                                                                   | 0, 1, 2, 9<br/>                |
| Caractères non alphanumériques (caractères spéciaux)<br/>                                                                                                               | $, !,%, ^, () {} \[ \] ;: <> ?<br/> |
| Tout caractère Unicode classé dans la catégorie des caractères alphabétiques, mais qui n’est pas en majuscules ou en minuscules. Cela comprend les caractères Unicode des langues asiatiques.<br/> |                                        |



 

**Pour activer l’application d’un mot de passe fort**

1.  Dans la console Administration de, recherchez **stratégie de sécurité locale**.
2.  Sélectionnez **stratégie de compte**, puis **stratégie de mot de passe**.
3.  Activez le paramètre les **mots de passe doivent respecter des exigences de complexité** .

> [!Note]  
> Un caractère donné ne peut répondre qu’à une seule catégorie. La fonction [GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) est utilisée pour vérifier si chaque caractère dans le mot de passe est en majuscules, en minuscules ou en caractères alphanumériques.

 

 

