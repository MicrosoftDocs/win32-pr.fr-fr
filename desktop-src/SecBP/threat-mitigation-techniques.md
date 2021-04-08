---
description: Vous pouvez utiliser un certain nombre de techniques d’atténuation des menaces pour mieux sécuriser les mots de passe.
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: Techniques d’atténuation des menaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ec2b8db3a634ea93ce77d585038909056c7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867801"
---
# <a name="threat-mitigation-techniques"></a>Techniques d’atténuation des menaces

Vous pouvez utiliser un certain nombre de techniques d’atténuation des menaces pour mieux sécuriser les mots de passe. Ces techniques sont implémentées à l’aide d’une ou de plusieurs des quatre technologies principales suivantes.



| Technology                      | Description                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CryptoAPI                       | CryptoAPI fournit un ensemble de fonctions qui vous aident à appliquer des routines de chiffrement aux entités cibles. CryptoAPI peut fournir des hachages, des résumés, un chiffrement et un déchiffrement pour mentionner ses principales fonctionnalités. CryptoAPI possède également d’autres fonctionnalités. Pour en savoir plus sur le chiffrement et l’CryptoAPI, consultez [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).           |
| Listes de contrôle d'accès            | Une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) est une liste de protections de sécurité qui s’applique à un objet. Un objet peut être un fichier, un processus, un événement ou tout autre qui possède un descripteur de sécurité. Pour plus d’informations sur les listes de contrôle d’accès, consultez [listes de Access Control](/windows/desktop/SecAuthZ/access-control-lists) (ACL). |
| API de protection des données             | L’API de protection des données (DPAPI) fournit les quatre fonctions suivantes que vous utilisez pour chiffrer et déchiffrer les données sensibles : [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata), [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata), [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)et [**CryptUnprotectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory).                  |
| Noms d’utilisateur et mots de passe stockés | Fonctionnalité de stockage qui permet de gérer les mots de passe des utilisateurs et d’autres informations d’identification, telles que les clés privées, plus faciles, plus cohérentes et plus sûres. Pour plus d’informations sur cette fonctionnalité, consultez [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).                                                                                                         |



 

Ces technologies ne sont pas disponibles sur tous les systèmes d’exploitation. Par conséquent, l’étendue de la sécurité peut être améliorée en fonction des systèmes d’exploitation impliqués. Voici les technologies qui sont disponibles dans chaque système d’exploitation.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Système d’exploitation</th>
<th>Technology</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Server 2003 et Windows XP</td>
<td><ul>
<li>CryptoAPI</li>
<li>Listes de contrôle d'accès</li>
<li>API de protection des données</li>
<li>Noms d’utilisateur et mots de passe stockés</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 2000</td>
<td><ul>
<li>CryptoAPI</li>
<li>Listes de contrôle d'accès</li>
<li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li>
<li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

Les techniques d’atténuation des menaces suivantes utilisent une ou plusieurs des quatre technologies. Les techniques qui requièrent l’utilisation de technologies qui ne sont pas incluses dans le système d’exploitation ne peuvent pas être utilisées.

## <a name="getting-passwords-from-the-user"></a>Obtention de mots de passe de l’utilisateur

Lorsque vous autorisez l’utilisateur à configurer un mot de passe, forcez l’utilisation de mots de passe forts. Par exemple, exigez que les mots de passe soient d’une longueur minimale de huit caractères ou plus. Les mots de passe doivent également être nécessaires pour inclure des lettres majuscules et minuscules, des chiffres et d’autres caractères du clavier, tels que le signe dollar ($), le point d’exclamation ( !) ou supérieur à (>).

Une fois que vous avez obtenu un mot de passe, utilisez-le rapidement (en utilisant le moins de code possible), puis effacez tous les vestiges du mot de passe. Cela réduit le temps disponible à un intrus pour « piéger » le mot de passe. Le compromis avec cette technique est la fréquence à laquelle le mot de passe doit être récupéré auprès de l’utilisateur. Toutefois, le principe doit être utilisé dans la mesure du possible. Pour plus d’informations sur la façon d’obtenir correctement les mots de passe, consultez [demande d’informations d’identification à l’utilisateur](asking-the-user-for-credentials.md).

Évitez de fournir les options d’interface utilisateur « Mémoriser mon mot de passe ». Souvent, les utilisateurs demandent cette option. Si vous devez le fournir, au minimum, assurez-vous que le mot de passe est enregistré de manière sécurisée. Pour plus d’informations, consultez la section stockage des mots de passe, plus loin dans cette rubrique.

Tentatives de saisie de mot de passe limitées. Après un certain nombre de tentatives sans succès, verrouillez l’utilisateur pendant une certaine durée. Si vous le souhaitez, augmentez le temps de réponse pour chaque tentative sur un maximum. Cette technique est destinée à défaire une attaque de découverte.

## <a name="storing-passwords"></a>Stockage des mots de passe

Ne stockez jamais les mots de passe en texte brut (non chiffré). Le chiffrement des mots de passe augmente considérablement leur sécurité. Pour plus d’informations sur le stockage des mots de passe chiffrés, consultez [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata). Pour plus d’informations sur le chiffrement des mots de passe en mémoire, consultez [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory). Stockez les mots de passe dans le moins de places possible. Plus un mot de passe est stocké, plus il est probable qu’un intrus le trouve. Ne stockez jamais les mots de passe dans une page Web ou dans un fichier Web. Le stockage des mots de passe dans une page Web ou dans un fichier Web leur permet d’être facilement compromis.

Une fois que vous avez chiffré un mot de passe et que vous l’avez stocké, utilisez des ACL sécurisés pour limiter l’accès au fichier. Vous pouvez également stocker des mots de passe et des clés de chiffrement sur les périphériques amovibles. Le stockage des mots de passe et des clés de chiffrement sur un support amovible, tel qu’une carte à puce, permet de créer un système plus sécurisé. Une fois qu’un mot de passe a été récupéré pour une session donnée, la carte peut être supprimée, ce qui élimine la possibilité qu’un intrus puisse y accéder.

 

 
