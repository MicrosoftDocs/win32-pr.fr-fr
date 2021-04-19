---
description: Les applications qui utilisent des objets CAPICOM doivent être créées à l’aide de CAPICOM.dll. CAPICOM.dll doit également être présente et inscrite au moment de l’exécution pour utiliser les objets CAPICOM.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Préparation à l’utilisation de CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6fc1ad0dbfe3d4f8c4dae3286eb3ffa5e1ae03d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521892"
---
# <a name="getting-ready-to-use-capicom"></a>Préparation à l’utilisation de CAPICOM

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Les applications qui utilisent des objets CAPICOM doivent être créées à l’aide de CAPICOM.dll. CAPICOM.dll doit également être présente et inscrite au moment de l’exécution pour utiliser les objets CAPICOM. CAPICOM.dll doit être ajouté aux références de projets Visual Basic pour utiliser les objets CAPICOM.

CAPICOM est disponible sous la forme d’un fichier redistribuable qui peut être téléchargé à partir de [Platform SDK Redistributable : CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281). Pour plus d’informations sur les versions de CAPICOM, consultez [CAPICOM versions](capicom-versions.md).

**Pour inscrire CAPICOM.dll**

-   À l’invite de commandes, accédez au répertoire dans lequel CAPICOM.dll est stocké, puis entrez la commande suivante :

    **CAPICOM.dllregsvr32**

## <a name="example-code-limitations"></a>Exemples de limitations de code

Pour fournir un code plus concis et plus lisible, les principes d’une bonne pratique de programmation ne sont pas toujours suivis dans ces exemples. En particulier, seules des réponses d’erreur limitées sont affichées. Les applications de travail doivent toujours vérifier les codes d’erreur renvoyés et effectuer les actions appropriées lorsqu’une erreur est rencontrée.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Conteneurs de clés, clés et certificats nécessaires dans CAPICOM

Alors que certaines opérations avec des objets CAPICOM peuvent être effectuées sur n’importe quel ordinateur par un utilisateur, la création de [*signatures numériques*](../secgloss/d-gly.md) et la récupération du contenu en texte en clair d’un message enveloppé à l’aide d’objets CAPICOM sont des opérations basées sur les certificats. L’utilisateur qui crée une signature numérique et l’utilisateur qui récupère le contenu chiffré d’un message enveloppé doit avoir un certificat numérique avec une clé privée associée disponible. Si un certificat avec une clé privée associée n’est pas présent, l’opération de chiffrement échoue. Les utilisateurs des applications CAPICOM doivent s’assurer qu’ils disposent du certificat approprié et de la clé privée disponible lorsque les applications sont en cours d’exécution.

Certains exemples des sections suivantes effectuent des opérations qui nécessitent une [*paire de clés publique/privée*](../secgloss/p-gly.md) disponible pour le chiffrement et le déchiffrement des fichiers, des messages et des signatures. La plupart de ces programmes se compilent et s’exécutent mais échouent au moment de l’exécution sans l’existence de [*conteneurs de clés*](../secgloss/k-gly.md), de clés, de magasins de certificats et de [*certificats*](../secgloss/c-gly.md) appropriés dans ces magasins.

**Pour créer un certificat auto-signé**

1.  Installez les outils de signature. Celles-ci sont installées dans le cadre du kit de développement logiciel (SDK) de Microsoft Windows, du kit de développement logiciel (SDK) de la plateforme ou du kit de développement logiciel (SDK) .NET Framework.
2.  Après avoir téléchargé Makecert.exe, exécutez la commande suivante à partir d’une invite de commandes, en remplaçant le nom d’utilisateur par un nom *d'* utilisateur, le nom de l’organisation par *Nom_organisation* et le nom de société *CompanyName*:

    **Makecert-r-n "CN =**_username_*_, ou =_*_Nom_organisation_*_, o =_*_CompanyName_*_"-SS My_*

3.  Le certificat peut être placé dans le magasin My de l’utilisateur actuel. Importez le certificat créé dans le magasin racine afin qu’il soit approuvé.

 

 
