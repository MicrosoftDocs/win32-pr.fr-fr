---
description: Utilisez des technologies de chiffrement pour le chiffrement à clé publique, les algorithmes de chiffrement, le chiffrement RSA et les certificats numériques.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517472"
---
# <a name="cryptography"></a>Chiffrement

## <a name="purpose"></a>Objectif

Le chiffrement consiste à utiliser des codes pour convertir des données afin que seul un destinataire spécifique puisse les lire à l’aide d’une clé.

Les technologies de chiffrement Microsoft incluent CryptoAPI, les fournisseurs de services de chiffrement (CSP), les outils CryptoAPI, CAPICOM, WinTrust, émettant et gérant les certificats et le développement d’infrastructures de clé publique personnalisables. L’inscription des certificats et des cartes à puce, la gestion des certificats et le développement de modules personnalisés sont également décrits.

## <a name="developer-audience"></a>Développeurs concernés

CryptoAPI est destiné aux développeurs d’applications Windows qui permettent aux utilisateurs de créer et d’échanger des documents et d’autres données dans un environnement sécurisé, en particulier sur des médias non sécurisés tels qu’Internet. Les développeurs doivent être familiarisés avec les langages de programmation C et C++ et dans l’environnement de programmation Windows. Bien que cela ne soit pas obligatoire, il est recommandé de bien comprendre le chiffrement ou les sujets liés à la sécurité.

CAPICOM est un composant de 32 bits uniquement destiné aux développeurs qui créent des applications à l’aide du langage de programmation Visual Basic Scripting Edition (VBScript) ou du langage de programmation C++. CAPICOM peut être utilisé dans les systèmes d’exploitation spécifiés dans Run-Time exigences. Pour un développement futur, nous vous recommandons d’utiliser le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.

## <a name="run-time-requirements"></a>Conditions d’exécution

Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

CAPICOM 2.1.0.2 est pris en charge sur les versions et systèmes d’exploitation suivants :

-   Windows Server 2003
-   Windows XP

CAPICOM est disponible sous la forme d’un fichier redistribuable qui peut être téléchargé à partir de [Platform SDK Redistributable : CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).

Les services de certificats requièrent les versions suivantes de ces systèmes d’exploitation :

-   Windows Server 2008 R2
-   Windows Server 2008
-   Windows Server 2003

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                           | Description                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos du chiffrement](about-cryptography.md)<br/>         | Principaux concepts de chiffrement et une vue de haut niveau des technologies de chiffrement de Microsoft.<br/>                                                                                                                           |
| [Utilisation du chiffrement](using-cryptography.md)<br/>         | Processus de chiffrement, procédures et exemples étendus de programmes C et Visual Basic à l’aide des fonctions CryptoAPI et des objets CAPICOM.<br/>                                                                            |
| [Référence de chiffrement](cryptography-reference.md)<br/> | Description détaillée des fonctions, interfaces, objets, structures et autres éléments de programmation de Microsoft Cryptography. Contient des descriptions de référence de l’API pour l’utilisation de certificats numériques.<br/> |



 

 

 




