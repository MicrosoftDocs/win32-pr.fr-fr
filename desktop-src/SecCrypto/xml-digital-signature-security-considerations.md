---
description: Les applications qui signent et vérifient les signatures numériques XML doivent être écrites conformément aux meilleures pratiques suivantes pour éviter les attaques par déni de service, la perte de données et la compromission d’informations privées.
ms.assetid: aa972946-9860-49c1-ae94-3f315684c291
title: Considérations sur la sécurité des signatures numériques XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e54b4c5f3f863e0bc84172a7507bfe8609e2df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534035"
---
# <a name="xml-digital-signature-security-considerations"></a>Considérations sur la sécurité des signatures numériques XML

Les applications qui signent et vérifient les signatures numériques XML doivent être écrites conformément aux meilleures pratiques suivantes pour éviter les attaques par déni de service, la perte de données et la compromission d’informations privées. La liste ci-dessous fournit des conseils généraux. Toutefois, les développeurs sont encouragés à effectuer des analyses de sécurité supplémentaires spécifiques à leurs applications et à passer en revue les meilleures pratiques en matière de signatures numériques publiées par le W3C.

-   [Vérifier l’approbation de la clé de signature](#verify-trust-of-the-signing-key)
-   [Vérifier d’abord la clé de signature et valider SignedInfo, puis valider les références](#first-verify-the-signing-key-and-validate-signedinfo-then-validate-references)
-   [Utiliser l’ensemble minimal d’algorithmes de canonisation et de transformations requis](#use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required)
-   [Vérifier que les URI cibles pointent vers des destinations dans l’étendue attendue](#ensure-target-uris-point-to-destinations-within-the-expected-scope)
-   [Vérifier que les données consommées par l’application sont vérifiées par la signature](#verify-the-data-consumed-by-the-application-is-verified-by-the-signature)
-   [Suivre les meilleures pratiques de chiffrement](#follow-best-cryptographic-practices)

## <a name="verify-trust-of-the-signing-key"></a>Vérifier l’approbation de la clé de signature

Vérifiez que la clé de signature est approuvée en vérifiant le certificat [*X. 509*](../secgloss/x-gly.md) correspondant (et la chaîne de certificat) inclus dans le message signé. En guise d’alternative, l’approbation dans la clé de signature peut être établie en mode hors bande, par exemple un administrateur qui configure un ensemble de clés approuvées ou une application interrogeant un service approuvé sur un canal sécurisé.

## <a name="first-verify-the-signing-key-and-validate-signedinfo-then-validate-references"></a>Vérifier d’abord la clé de signature et valider SignedInfo, puis valider les références

Vérifiez l’approbation dans la clé de signature et l’intégrité de l’élément **SignedInfo** avant de valider les références. De même, les applications doivent valider les éléments de **manifeste** avant de résoudre les références contenues dans les éléments de **manifeste** . Les éléments de **référence** autorisent la spécification des URI cibles, des transformations et des algorithmes de canonisation. Si elles ne sont pas validées, ces champs peuvent potentiellement être utilisés pour créer des attaques par déni de service, perte de données ou autres.

## <a name="use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required"></a>Utiliser l’ensemble minimal d’algorithmes de canonisation et de transformations requis

Les langages XSLT et XPATH ne doivent pas être utilisés dans des éléments non authentifiés, tels que **KeyInfo**. Si une application requiert l’utilisation de XPath, Contraignez le jeu d’expressions XPATH autorisé à uniquement celles qui utilisent l’ancêtre ou les axes Self et ne Calculez pas la valeur de chaîne des éléments. Par défaut, CryptXML prend en charge un ensemble limité d’algorithmes de canonisation (consultez URI pris en charge dans les [algorithmes de chiffrement de signature numérique XML](xml-digital-signature-cryptographic-algorithms.md)). Les développeurs peuvent implémenter des transformations ou des algorithmes de canonisation supplémentaires à utiliser dans leur application. Toutefois, l’utilisation d’algorithmes complexes crée le risque d’attaques par déni de service ou d’interruption des caractéristiques de répudiation d’une signature. Dans les cas où des transformations sont requises par l’application, limitez le nombre de transformations qui peuvent être spécifiées par référence au nombre le plus élevé requis par l’application. Cette pratique atténue les attaques par déni de service basées sur une utilisation excessive des transformations.

## <a name="ensure-target-uris-point-to-destinations-within-the-expected-scope"></a>Vérifier que les URI cibles pointent vers des destinations dans l’étendue attendue

Les applications doivent limiter les URI cibles à la plus petite étendue requise par l’application. Par exemple, les URI peuvent être supposés pointer vers des destinations dans le même document, des fichiers dans un répertoire cible spécifique ou des emplacements réseau dans un domaine DNS spécifique. Les URI définis par une personne malveillante pour pointer à l’extérieur du domaine attendu peuvent entraîner la récupération de contenu malveillant par une application, l’envoi de requêtes HTTP malveillantes (éventuellement contenant des chaînes de requête) ou l’authentification des applications auprès de serveurs malveillants.

## <a name="verify-the-data-consumed-by-the-application-is-verified-by-the-signature"></a>Vérifier que les données consommées par l’application sont vérifiées par la signature

Si l’application valide la clé de signature et les éléments **SignedInfo** et **Reference** , mais que l’application consomme des données importantes qui ne sont pas référencées par la signature, la signature ne fournit aucune protection significative. La signification sémantique d’une signature peut varier en fonction de la position de la signature dans le document. Les applications sont encouragées à vérifier la position de la signature dans un document. En outre, vérifiez l’emplacement des données référencées et des noms d’éléments pour limiter les substitutions et les attaques d’encapsulation.

## <a name="follow-best-cryptographic-practices"></a>Suivre les meilleures pratiques de chiffrement

Les algorithmes de chiffrement sont plus faibles au fil du temps à mesure que de nouvelles attaques sont découvertes et que la puissance de calcul est disponible. Ne codez pas en dur les identificateurs d’algorithme de chiffrement ou les tailles de clé dans vos applications. Pour obtenir une liste plus complète des meilleures pratiques de chiffrement, consultez Michael Howard et Steve Lipner, « SDL minimum Cryptographic standards » dans *le cycle de vie de développement de la sécurité* (Redmond, Washington : Microsoft Press, 2006), 251 – 258.

Des pratiques recommandées supplémentaires sont disponibles sur le site Web du W3C : https://www.w3.org .

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et dans certains pays ou régions.

 

 

 
