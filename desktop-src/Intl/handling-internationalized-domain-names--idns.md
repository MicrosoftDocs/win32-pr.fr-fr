---
description: Cette rubrique décrit comment vous pouvez utiliser des noms de domaine internationaux (IDNs) dans vos applications.
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: Gestion des noms de domaine internationaux (IDNs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e853f0ea3f62fc3e5ee848431417cc031eaa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203785"
---
# <a name="handling-internationalized-domain-names-idns"></a>Gestion des noms de domaine internationaux (IDNs)

Cette rubrique décrit comment vous pouvez utiliser des noms de domaine internationaux (IDNs) dans vos applications. Les IDNs sont spécifiés par le groupe de travail réseau [RFC 3490 : internationalisation des noms de domaine dans les applications (IDNA)](http://www.faqs.org/rfcs/rfc3490.html). Avant ce brouillon standard, les IDNs étaient limités aux caractères latins sans signes diacritiques. IDNA permet à IDNs d’inclure des caractères latins avec des signes diacritiques, ainsi que des caractères de scripts non-latins, tels que cyrillique, arabe et chinois. La norme établit également des règles pour le mappage des IDNs à des noms de domaine ASCII uniquement. Par conséquent, les problèmes IDNA peuvent être traités côté client, sans qu’il soit nécessaire de modifier le serveur de noms de domaine (DNS).

> [!Caution]  
> La norme RFC 3490 introduit un certain nombre de problèmes de sécurité liés à l’utilisation de IDNs. Pour plus d’informations, consultez la section relative aux considérations relatives à la [sécurité : fonctionnalités internationales](security-considerations--international-features.md).

 

> [!Note]  
> IDNA est actuellement basé sur Unicode 3,2.

 

## <a name="nls-api-functions-for-handling-idns"></a>Fonctions de l’API NLS pour la gestion de IDNs

NLS intègre les fonctions de conversion suivantes, que votre application peut utiliser pour convertir des IDN en représentations différentes. Pour obtenir un exemple de l’utilisation de ces fonctions, consultez [nls : exemple de conversion IDN (Internationalized Domain Name)](nls--internationalized-domain-name--idn--conversion-sample.md).

-   [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii). Convertit les IDN en Punycode.
-   [**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode). Exécute la partie NamePrep de la conversion d’IDN en un nom ASCII. Cette fonction crée une représentation Unicode canonique d’une chaîne.
-   [**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode). Convertit une chaîne Punycode en chaîne UTF-16 normale.

NLS définit également plusieurs fonctions API qui peuvent être utilisées pour atténuer certains des risques de sécurité présentés par la technologie IDN. Sur Windows Vista et versions ultérieures, les fonctions suivantes sont utilisées pour vérifier que les caractères d’un IDN donné sont entièrement dessinés à partir des scripts associés à des paramètres régionaux ou des paramètres régionaux spécifiques. Pour obtenir un exemple de l’utilisation de ces fonctions, consultez l' [exemple d’atténuation NLS (Internationalized Domain Name)](nls--internationalized-domain-name--idn--mitigation-sample.md).

-   [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts). Fournit la liste des scripts utilisés dans une chaîne particulière.
-   [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex). Récupérer les informations relatives aux paramètres régionaux. L’utilisation des fonctions avec *LCTYPE* défini sur [locale \_ SSCRIPTS](locale-sscripts.md) fournit une liste de scripts normalement utilisés pour des paramètres régionaux particuliers.
-   [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts). Compare des listes de scripts. Pour effectuer une vérification par rapport à plusieurs paramètres régionaux, l’application peut effectuer plusieurs appels à [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) et [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

Pour les applications qui s’exécutent sur Windows XP et Windows Server 2003, les fonctions [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md), [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)et [**DownlevelVerifyScripts**](downlevelverifyscripts.md) jouent un rôle similaire aux fonctions mentionnées ci-dessus pour réduire les risques de sécurité. Le téléchargement des [API d’atténuation du nom de domaine international Microsoft (IDN)](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) est disponible sur le [Centre de téléchargement MSDN](https://www.microsoft.com/?ref=go).

## <a name="handle-unicode-strings"></a>Gérer les chaînes Unicode

IDNA prend en charge la transformation de chaînes Unicode en étiquettes de nom d’hôte légitimes, à l’exception des chaînes contenant certains caractères interdits, tels que les caractères de contrôle, les caractères de la zone d’utilisation privée (PUA), etc. Votre application peut utiliser l' \_ indicateur IDN use \_ STD3 \_ ASCII \_ Rules avec plusieurs fonctions de conversion nls pour forcer les fonctions à échouer si elles rencontrent des caractères ASCII autres que des lettres, des chiffres ou des traits d’Union-moins (-), ou si une chaîne commence ou se termine par le caractère de trait d’Union-moins. L’utilisation de ces caractères n’est toujours pas autorisée dans les noms de domaine et reste interdite dans le brouillon standard.

## <a name="handle-unassigned-code-points"></a>Gérer les points de code non assignés

IDNs ne peut pas contenir de points de code non assignés. Par conséquent, les points de code qui ne sont pas associés à un caractère (« assigné ») à partir de l’Unicode 3,2 n’ont pas de mappages IDN définis, bien que l' \_ indicateur IDN autoriser non \_ assigné dans certaines fonctions de conversion les autorise à être mappé à Punycode. Vous trouverez une liste de points de code non attribués dans le [document RFC 3454](http://www.faqs.org/rfcs/rfc3454.html).

> [!Caution]  
> Si votre application encode des points de code non assignés en tant que Punycode, les noms de domaine résultants doivent être illégaux. La sécurité peut être compromise si une version ultérieure de IDNA rend ces noms légaux ou si l’application filtre les caractères non autorisés pour essayer de créer un nom de domaine légal.

 

Les points de code non assignés ne sont pas autorisés dans les chaînes stockées utilisées dans les identificateurs de protocole et les entités nommées, telles que les noms des certificats numériques et les parties du nom de domaine DNS. Toutefois, les points de code sont autorisés dans les chaînes de requête, par exemple, les noms entrés par l’utilisateur pour les autorités de certification numériques et les recherches DNS, qui sont utilisées pour faire correspondre des identificateurs stockés.

> [!Caution]  
> Bien que les chaînes de requête puissent utiliser des points de code non assignés, vous ne devez pas les utiliser dans vos applications. Même une chaîne de requête fournie par l’utilisateur présente le risque d’une attaque d’usurpation d’identité. Dans ce type d’attaque, le site hôte non scrupuleux redirige les utilisateurs à partir du site qu’ils ont l’intention d’accéder à un autre site susceptible de fournir des informations sensibles à un tiers. Par exemple, la copie d’une chaîne à partir d’un courrier électronique entrant peut présenter les mêmes risques qu’un clic sur un lien dans un navigateur.

 

## <a name="convert-domain-names-to-ascii-names"></a>Convertir les noms de domaine en noms ASCII

Votre application peut utiliser la fonction [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) et certaines fonctions d’atténuation pour convertir IDNs en ASCII.

> [!Caution]  
> Étant donné que les chaînes avec des représentations binaires très différentes peuvent être comparées comme identiques, cette fonction peut soulever certains problèmes de sécurité. Pour plus d’informations, consultez la discussion sur les fonctions de comparaison dans considérations sur la [sécurité : fonctionnalités internationales](security-considerations--international-features.md).

 

## <a name="examples"></a>Exemples

[Nls : l’exemple de conversion IDN (Internationalized Domain Name)](nls--internationalized-domain-name--idn--conversion-sample.md) illustre l’utilisation des fonctions de conversion IDN. [Nls : l’exemple d’atténuation des IDN (Internationalized Domain Name)](nls--internationalized-domain-name--idn--mitigation-sample.md) illustre l’utilisation des fonctions d’atténuation des IDN.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
</dt> <dt>

[Considérations relatives à la sécurité : fonctionnalités internationales](security-considerations--international-features.md)
</dt> </dl>

 

 



