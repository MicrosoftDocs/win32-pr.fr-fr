---
description: Les fonctions CryptoAPI utilisent des fournisseurs de services de chiffrement (CSP) pour effectuer le chiffrement et le déchiffrement, et pour fournir un stockage et une sécurité de clés.
ms.assetid: 7977e59b-7ce1-4bb4-aae4-d67b7d646493
title: CSP et le processus de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc1813f5f4bff96470c23ff8e777ef15458bddf7773663b4d16d9618e371a15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100929"
---
# <a name="csps-and-the-cryptography-process"></a>CSP et le processus de chiffrement

Les fonctions [*CryptoAPI*](../secgloss/c-gly.md) utilisent des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour effectuer le chiffrement et le déchiffrement, et pour fournir un stockage et une sécurité de clés. Ces fournisseurs de services de chiffrement sont des modules indépendants. Dans l’idéal, les fournisseurs de services de chiffrement sont écrits pour être indépendants d’une application particulière, de sorte que toute application s’exécute avec un grand nombre de fournisseurs de services de chiffrement. En réalité, cependant, certaines applications ont des exigences spécifiques qui requièrent un CSP personnalisé. cela est comparé au modèle [*GDI*](../secgloss/g-gly.md) Windows. Les fournisseurs de services de chiffrement sont analogues aux pilotes de périphériques graphiques.

La qualité de protection des clés dans le système est un paramètre de conception du CSP et non du système dans son ensemble. Cela permet à une application de s’exécuter dans divers contextes de sécurité sans modification.

Les applications Access qui ont accès aux éléments internes de chiffrement sont soigneusement limitées. Cela facilite le développement d’applications portables et sécurisées.

Les trois règles de conception suivantes s’appliquent :

-   Les applications ne peuvent pas accéder directement au support de clé. Étant donné que tous les éléments de clé sont générés au sein du CSP et utilisés par l’application via des handles opaques, il n’y a aucun risque d’une application ou de ses dll associées de divulguer le matériel de génération de clé ou de choisir un support de clé à partir de sources aléatoires médiocres.
-   Les applications ne peuvent pas spécifier les détails des opérations de chiffrement. L’interface CSP permet à une application de choisir un algorithme de chiffrement ou de signature, mais l’implémentation de chaque opération de chiffrement est effectuée par le CSP.
-   Les applications ne gèrent pas les [*informations d’identification*](../secgloss/c-gly.md) de l’utilisateur ou d’autres données d’authentification de l’utilisateur. L’authentification des utilisateurs est effectuée par le fournisseur de services de chiffrement ; par conséquent, les fournisseurs de services de chiffrement futurs avec des fonctionnalités d’authentification avancées, telles que les entrées biométriques, fonctionnent sans qu’il soit nécessaire de modifier le modèle d’authentification de l’application.

Au minimum, un CSP se compose d’une bibliothèque de liens dynamiques (DLL) et d’un [*fichier de signature*](../secgloss/s-gly.md). Le fichier de signature est nécessaire pour garantir que l' [*CryptoAPI*](../secgloss/c-gly.md) reconnaît le CSP. CryptoAPI valide cette signature régulièrement pour s’assurer que toute falsification du CSP est détectée.

Certains fournisseurs de services de chiffrement peuvent implémenter une fraction de leurs fonctionnalités dans un service séparé par une adresse appelé par le biais du service RPC local ou du matériel appelé par le biais d’un pilote de périphérique système. L’isolation des opérations de chiffrement global et d’état de clé global dans un service séparé par une adresse ou dans le matériel empêche les clés et les opérations de falsifier l’espace de données d’une application.

Il est déconseillé pour les applications de tirer parti des attributs spécifiques à un CSP spécifique. Par exemple, le fournisseur de services de chiffrement de base Microsoft (fourni avec CryptoAPI) prend en charge les clés de session 40 bits et les clés publiques 512 bits. Les applications qui manipulent ces clés doivent éviter les hypothèses quant à la quantité de mémoire nécessaire pour stocker ces clés, car l’application risque d’échouer si un CSP différent est utilisé. Les applications bien écrites doivent fonctionner avec un grand nombre de fournisseurs de services de chiffrement.

Pour plus d’informations sur les types de fournisseur de chiffrement et les fournisseurs de services de chiffrement prédéfinis qui peuvent être utilisés avec CryptoAPI, consultez [types de fournisseur de chiffrement](cryptographic-provider-types.md) et [fournisseurs de services de chiffrement Microsoft](microsoft-cryptographic-service-providers.md)

 

 
