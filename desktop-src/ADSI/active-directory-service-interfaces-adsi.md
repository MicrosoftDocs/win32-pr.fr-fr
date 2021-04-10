---
title: Interfaces de service Active Directory
description: Présentation des interfaces des services de Active Directory, avec des liens vers différents guides.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Interfaces de service Active Directory (voir ADSI)
- ADSI ADSI, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031855"
---
# <a name="active-directory-service-interfaces"></a>Interfaces de service Active Directory

## <a name="purpose"></a>Objectif

Les interfaces ADSI (Active Directory Service Interfaces) sont un ensemble d’interfaces COM utilisées pour accéder aux fonctionnalités des services d’annuaire à partir de différents fournisseurs de réseau. ADSI est utilisé dans un environnement informatique distribué pour présenter un ensemble unique d’interfaces de service d’annuaire pour la gestion des ressources réseau. Les administrateurs et les développeurs peuvent utiliser les services ADSI pour énumérer et gérer les ressources dans un service d’annuaire, quel que soit l’environnement réseau qui contient la ressource.

ADSI permet des tâches d’administration courantes, telles que l’ajout de nouveaux utilisateurs, la gestion des imprimantes et la localisation des ressources dans un environnement informatique distribué.

> [!Note]  
> La documentation suivante est destinée aux programmeurs informatiques. Si vous êtes un utilisateur final qui tente de déboguer une erreur d’impression ou un problème de réseau à distance, consultez les forums de la [communauté Microsoft](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Le cas échéant

Les administrateurs réseau peuvent utiliser ADSI pour automatiser les tâches courantes, telles que l’ajout d’utilisateurs et de groupes, la gestion des imprimantes et la définition d’autorisations sur les ressources réseau.

Les éditeurs de logiciels indépendants et les développeurs d’utilisateurs finaux peuvent utiliser ADSI pour « activer l’annuaire » de leurs produits et applications. Les services peuvent se publier eux-mêmes dans un répertoire, les clients peuvent utiliser l’annuaire pour rechercher les services, et les deux peuvent utiliser le répertoire pour rechercher et manipuler d’autres objets intéressants. Étant donné que les interfaces de service Active Directory sont indépendantes des services d’annuaire sous-jacents, les produits et les applications compatibles avec l’annuaire peuvent fonctionner correctement dans plusieurs environnements réseau et d’annuaire.

## <a name="developer-audience"></a>Développeurs concernés

Vous pouvez écrire des applications clientes ADSI dans de nombreux langages. Pour la plupart des tâches d’administration, ADSI définit des interfaces et des objets accessibles à partir de langages compatibles Automation tels que Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) et Java à des langages de performances et d’efficacité plus sensibles, tels que C et C++. Une bonne base de la programmation COM est utile pour le programmeur ADSI.

## <a name="run-time-requirements"></a>Conditions d’exécution

Active Directory s’exécute sur les contrôleurs de domaine Windows Server. Toutefois, les applications clientes utilisant ADSI peuvent être écrites et exécutées sur Windows. En outre, les développeurs souhaiteront le kit de développement logiciel (SDK) de la plateforme, également disponible sur le site Web MSDN. Pour examiner le contenu de Active Directory, utilisez le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory. Ce composant logiciel enfichable remplace l’outil ADSVW disponible pour les versions précédentes de Windows.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[À propos d’ADSI](about-adsi.md)
</dt> <dd>

Informations générales sur ADSI.

</dd> <dt>

[Utilisation d’ADSI](using-adsi.md)
</dt> <dd>

Guide de programmation de l’utilisation d’ADSI.

</dd> <dt>

[Didacticiels de démarrage rapide ADSI](adsi-quick-start-tutorials.md)
</dt> <dd>

Utilisation d’ADSI avec Automation pour gérer les répertoires.

</dd> <dt>

[Référence ADSI](adsi-reference.md)
</dt> <dd>

Documentation des interfaces et des méthodes ADSI.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[COM (Component Object Model)](../com/the-component-object-model.md)
</dt> <dt>

[Clients et serveurs COM](../com/com-clients-and-servers.md)
</dt> <dt>

[Active Directory Domain Services](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 