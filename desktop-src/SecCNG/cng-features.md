---
description: CNG offre les fonctionnalités suivantes.
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: Fonctionnalités CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df40606a255adc90bd36540571979c1c34579611
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237744"
---
# <a name="cng-features"></a>Fonctionnalités CNG

CNG offre les fonctionnalités suivantes.

-   [Agilité de chiffrement](#cryptographic-agility)
-   [Certification et conformité](#certification-and-compliance)
-   [Prise en charge de Suite B](#suite-b-support)
-   [Prise en charge héritée](#legacy-support)
-   [Prise en charge du mode noyau](#kernel-mode-support)
-   [Audit](#auditing)
-   [Générateurs de nombres aléatoires remplaçables](#replaceable-random-number-generators)
-   [Cohérence de thread](#thread-safety)
-   [Mode de fonctionnement](#mode-of-operation)

## <a name="cryptographic-agility"></a>Agilité de chiffrement

L’une des propositions de valeur de clé du CNG est l’agilité de chiffrement, parfois appelée le décodeur de chiffrement. Toutefois, la conversion de l’implémentation de protocoles tels que le [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL) ou TLS ( [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) ), CMS (S/MIME), IPSec, Kerberos, etc. en CNG, a été nécessaire pour rendre cette capacité utile. Au niveau CNG, il était nécessaire de fournir une substitution et une détectabilité pour tous les types d’algorithmes (fonctions symétriques, asymétriques, de hachage), la génération de nombres aléatoires et d’autres fonctions utilitaires. Les modifications au niveau du protocole sont plus importantes, car dans de nombreux cas, les API de protocole devaient ajouter la sélection d’algorithmes et d’autres options de flexibilité qui n’existaient pas auparavant.

CNG est tout d’abord disponible dans Windows Vista et est positionné pour remplacer les utilisations existantes de [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) dans la pile logicielle Microsoft. Les développeurs tiers trouveront un grand nombre de nouvelles fonctionnalités dans CNG, notamment :

-   Un nouveau système de configuration de chiffrement, prenant en charge une meilleure agilité de chiffrement.
-   Abstraction plus fine pour le stockage des clés (et séparation du stockage des opérations de l’algorithme).
-   Isolation des processus pour les opérations avec des clés à long terme.
-   Générateurs de nombres aléatoires remplaçables.
-   Suspension des restrictions de signature d’exportation.
-   Sécurité des threads dans toute la pile.
-   API de chiffrement en mode noyau.

En outre, CNG prend en charge tous les algorithmes Suite B requis, y compris le [*chiffrement à courbe elliptique*](/windows/desktop/SecGloss/e-gly) (ECC). Les applications CryptoAPI existantes continueront de fonctionner lorsque CNG sera disponible.

## <a name="certification-and-compliance"></a>Certification et conformité

CNG est validé sur les normes FIPS 140-2 et fait partie de la cible de l’évaluation pour le Windows certification critères communs. CNG a été conçu pour être utilisable en tant que composant dans un système validé FIPS niveau 2.

CNG est conforme aux exigences de critères communs en stockant et en utilisant des clés à long terme dans un processus sécurisé.

## <a name="suite-b-support"></a>Prise en charge de Suite B

La prise en charge des algorithmes Suite B est une fonctionnalité importante de CNG. En février 2005, la NSA (National Security Agency) du États-Unis a annoncé un ensemble coordonné de chiffrement symétrique, d’accord de secret asymétrique (également connu sous le nom d’échange de clés), de signature numérique et de fonctions de hachage pour l’utilisation future du gouvernement des États-Unis, appelée *suite B*. La NSA a annoncé que des implémentations de Suite B certifiées peuvent et seront utilisées pour la protection des informations désignées par des informations confidentielles, secrètes et privées, qui, dans le passé, étaient décrites comme sensibles, mais non classées. Pour cette raison, la prise en charge Suite B est très importante pour les fournisseurs de logiciels d’application et les intégrateurs de systèmes, ainsi que pour Microsoft.

Tous les algorithmes Suite B sont publiquement connus. Ils ont été développés en dehors de l’étendue du secret gouvernemental historiquement associé au développement de l’algorithme de chiffrement. Dans ce laps de temps, certains pays et régions européens ont également proposé les mêmes exigences de Suite B pour la protection de leurs informations.

le chiffrement Suite B recommande l’utilisation de l’algorithme ECDH (elliptic curve Diffie-Hellman) dans de nombreux protocoles existants tels que le protocole IKE (Internet Key Exchange) (IKE, principalement utilisé dans IPsec), le protocole TLS ( [*transport layer security*](/windows/desktop/SecGloss/t-gly) ) et le protocole mime (S/mime).

CNG prend en charge Suite B qui s’étend à tous les algorithmes requis : AES (toutes les tailles de clé), la famille SHA-2 (SHA-256, SHA-384 et SHA-512) des algorithmes de hachage, ECDH et ECDSA (Elliptic Curve DSA) sur les courbes prime NIST-standard P-256, P-384 et P-521. les courbes binaires, les courbes Koblitz, les courbes prime personnalisées et la courbe elliptique Menezes-Qu-Vanstone (ECMQV) ne sont pas prises en charge par les fournisseurs d’algorithmes Microsoft inclus avec Windows Vista.

## <a name="legacy-support"></a>Prise en charge héritée

CNG prend en charge l’ensemble actuel d’algorithmes dans [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1,0. Chaque algorithme actuellement pris en charge dans *CryptoAPI* 1,0 sera toujours pris en charge dans CNG.

## <a name="kernel-mode-support"></a>Prise en charge du mode noyau

CNG prend en charge le chiffrement en mode noyau. Les mêmes API sont utilisées en mode noyau et utilisateur pour prendre entièrement en charge les fonctionnalités de chiffrement. SSL/TLS et IPsec fonctionnent en mode noyau en plus des processus de démarrage qui utiliseront CNG. Toutes les fonctions CNG ne peuvent pas être appelées à partir du mode noyau. La rubrique de référence pour les fonctions qui ne peuvent pas être appelées à partir du mode noyau indique explicitement que la fonction ne peut pas être appelée à partir du mode noyau. Dans le cas contraire, toutes les fonctions CNG peuvent être appelées à partir du mode noyau si l’appelant est en cours d’exécution au **\_ niveau passif** [*IRQL*](/windows/desktop/SecGloss/i-gly). En outre, certaines fonctions CNG en mode noyau peuvent être appelées **au \_ niveau** de l’IRQL de niveau de dispatch, en fonction des capacités du fournisseur.

L’interface du fournisseur de support de Microsoft Kernel Security (Ksecdd.sys) est un module de chiffrement à usage général, basé sur logiciel et résidant au niveau du mode noyau de Windows. Ksecdd.sys s’exécute en tant que pilote d’exportation en mode noyau et fournit des services de chiffrement via les interfaces documentées aux composants du noyau. Le seul algorithme de fournisseur Microsoft intégré qui n’est pas pris en charge par Ksecdd.sys est DSA.

**Windows Server 2008 et Windows Vista :** CNG ne prend pas en charge les algorithmes et les fournisseurs enfichables en mode noyau. Les seuls algorithmes de chiffrement pris en charge disponibles en mode noyau sont les implémentations fournies par Microsoft par le biais des API CNG en mode noyau.

## <a name="auditing"></a>Audit

Pour se conformer à certaines des exigences de critères communs en plus de fournir une sécurité complète, de nombreuses actions qui se produisent dans la couche CNG sont auditées dans le fournisseur de stockage de clés (KSP) de Microsoft. Le KSP Microsoft respecte les instructions suivantes pour créer des enregistrements d’audit dans le journal de sécurité :

-   Les échecs de génération de clé et de paire de clés, y compris les échecs d’auto-test, doivent être audités.
-   L’importation et l’exportation de clé doivent être auditées.
-   Les échecs de destruction de clé doivent être audités.
-   Les clés persistantes doivent être auditées lorsqu’elles sont écrites et lues à partir de fichiers.
-   Les échecs de vérification de cohérence par paire doivent être audités.
-   Les erreurs de validation de clé secrète, le cas échéant, doivent être auditées, par exemple, les vérifications de parité sur les clés 3DES.
-   Les défaillances du chiffrement, du déchiffrement, du hachage, de la signature, de la vérification, de l’échange de clés et de la génération de nombres aléatoires doivent être auditées.
-   Les tests automatiques de chiffrement doivent être audités.

En général, si une clé n’a pas de nom, il s’agit d’une clé éphémère. Une clé éphémère n’est pas persistante et le KSP Microsoft ne génère pas d’enregistrements d’audit pour les clés éphémères. Le KSP Microsoft génère des enregistrements d’audit en mode utilisateur dans le processus LSA uniquement. Aucun enregistrement d’audit n’est généré par CNG en mode noyau. Les administrateurs doivent configurer la stratégie d’audit pour obtenir tous les journaux d’audit KSP à partir du journal de sécurité. Un administrateur doit exécuter la ligne de commande suivante pour configurer des audits supplémentaires générés par KSP :

**Auditpol/Set/Subcategory : « Other System Events »/Success : Enable/Failure : Enable**

## <a name="replaceable-random-number-generators"></a>Générateurs de nombres aléatoires remplaçables

Une autre amélioration apportée par le CNG est la possibilité de remplacer le générateur de nombres aléatoires par défaut (RNG). Dans CryptoAPI, il est possible de fournir un autre RNG dans le cadre d’un fournisseur de services de chiffrement (CSP), mais il n’est pas possible de rediriger les fournisseurs de services de chiffrement de base Microsoft pour utiliser un autre RNG. CNG permet de spécifier explicitement un RNG particulier à utiliser dans des appels particuliers.

## <a name="thread-safety"></a>Cohérence de thread

Toutes les fonctions qui modifient simultanément la même zone de mémoire (sections critiques) quand elles sont appelées à partir de threads distincts ne sont pas thread-safe.

## <a name="mode-of-operation"></a>Mode de fonctionnement

CNG prend en charge cinq modes d’opérations qui peuvent être utilisés avec les chiffrements par blocs symétriques via les API de chiffrement. Ces modes et leur prise en charge sont répertoriés dans le tableau suivant. Le mode d’opération peut être modifié en définissant la propriété [**\_ \_ mode de chaînage BCRYPT**](cng-property-identifiers.md) pour le fournisseur d’algorithme à l’aide de la fonction [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .



| Mode de fonctionnement           | Valeur du mode de \_ chaînage BCRYPT \_ | Algorithmes              | Standard  |
|-----------------------------|------------------------------|-------------------------|-----------|
| BCE (livre de livre électronique)   | **\_ \_ BCE en mode de chaîne BCRYPT \_** | Chiffrements par blocs symétriques | SP800-38A |
| CBC (chaînage de blocs de chiffrement) | **\_mode chaîne \_ BCRYPT \_ CBC** | Chiffrements par blocs symétriques | SP800-38A |
| CFB (commentaires de chiffrement)       | **\_mode de chaîne BCRYPT \_ \_ CFB** | Chiffrements par blocs symétriques | SP800-38A |
| CCM (compteur avec CBC)      | **\_ \_ CCM en mode \_ chaîné** | AES                     | SP800-38C |
| GCM (mode Galois/Counter)   | **\_mode de chaîne BCRYPT \_ \_ GCM** | AES                     | SP800-38D |



 

> [!Note]  
> seuls les modes d’opération ECB, CBC et CFB sont définis dans Windows Vista. GCM et CCM requièrent Windows Vista avec Service Pack 1 (SP1) ou Windows Server 2008.

 

 

 
