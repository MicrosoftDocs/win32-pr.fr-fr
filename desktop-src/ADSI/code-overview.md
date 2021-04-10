---
title: Vue d’ensemble du code
description: La figure suivante est une représentation conceptuelle des blocs de code nécessaires pour implémenter le composant fournisseur d’exemples ADSI.
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- Vue d’ensemble du code AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99a4974ac97488fc051ea80dbde7a8a83fa329e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031860"
---
# <a name="code-overview"></a>Vue d’ensemble du code

La figure suivante est une représentation conceptuelle des blocs de code nécessaires pour implémenter le composant fournisseur d’exemples ADSI. Chaque section est décrite dans la figure suivante. Les programmeurs COM expérimentés peuvent trouver qu’il s’agit d’une vue d’ensemble appropriée du composant de l’exemple de fournisseur. Pour plus d’informations, consultez [Détails du code](code-details.md).

![exemple d’implémentation de fournisseur](images/dssmco.png)

Les éléments numérotés suivants correspondent à des éléments de bloc dans la figure.

1.  Chargement de la DLL (LibMain. cpp, Guid. cpp). Point d’entrée de la DLL. Définitions d’objets statiques de fabrique de classes pour les deux objets de fournisseur : GUID. cpp contient les définitions CLSID pour les implémentations des différents objets de composant de fournisseur d’exemple.
2.  Code de création et de fabrique de classe de l’objet fournisseur (Cprovcf. cpp, Cprov. cpp, stdfact. cpp). L’objet fournisseur est l’objet qui prend en charge [**IParseDisplayName**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) pendant les opérations de liaison de moniker, comme indiqué dans recherche et liaison dans le composant de fournisseur d’exemple.
3.  Liaison à un objet (Getobj. cpp). Ce code appelle l’analyseur pour vérifier que l’ADsPath donné est syntaxiquement correct, puis effectue tout mappage nécessaire à partir de l’ADsPath vers le chemin d’accès du service d’annuaire natif pour l’élément en cours de création en tant qu’objet Active Directory. Il recherche la définition de schéma pour ce type d’objet et remplit les propriétés obligatoires. Après la création de l’objet Active Directory, un pointeur d’interface vers [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) est récupéré pour l’appelant.
4.  Analyseur pour l’espace de noms du fournisseur (Parse. cpp). Il s’agit du code appelé par l’élément 3. L’analyseur vérifie que la chaîne ADsPath transmise est correcte syntaxiquement pour son propre espace de noms.
5.  Fabrique de classe, création et énumération pour l’objet espace de noms (Cnamcf. cpp, Cnamesp. cpp, Cenumns. cpp). L’objet Namespace est un objet conteneur qui peut être énuméré pour rechercher tous les objets de nœud racine pour cet espace de noms.
6.  La fabrique de classe et le code de création pour un objet Active Directory générique, et la fabrique de classe, le code de création et d’énumération pour un objet conteneur ADs générique (Cgenobj. cpp, Cenumobj. cpp, Common. cpp, Core. cpp). Ce code est exécuté lorsqu’un objet Active Directory est créé.
7.  Filtrage et énumération des VARIANTs (Cenumvar. cpp, Object. cpp). Quand une collection d’éléments VARIANT d’un même type est gérée dans ADSI, ce code est utilisé.
8.  Globals (Globals. cpp). Les mots clés d’espace de noms, les structures de mappage de syntaxe des formats de données natifs au type VARIANT Automation ADs sont tous définis ici.
9.  Marshaling/démarshaling de données (Pack. cpp, Property. cpp, Smpoper. cpp). La conversion des formats de données natifs vers l’ensemble pris en charge de types VARIANT Automation se produit lorsque les propriétés d’un objet sont chargées dans le cache de propriétés. Une autre gestion spéciale des données doit être effectuée lorsque des structures avec des pointeurs sont copiées, supprimées ou déplacées en mémoire.
10. Cache de propriétés (cProps. cpp). La mise en cache des propriétés est une fonctionnalité de l’environnement ADSI. Les méthodes [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo), [**IADs :: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)et [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) agissent sur le cache de propriétés.
11. Gestion de la mémoire (Memory. cpp). L’utilisation d’un ensemble de fonctions mémoire pour allouer et libérer de la mémoire permet à l’exemple de composant fournisseur d’effectuer le suivi de l’utilisation de la mémoire et d’arrêter les fuites de mémoire.
12. Objets de schéma et gestion (Cschobj. cpp, Cprpobj. cpp, Cclsobj. cpp, Cenumsch. cpp). Cela comprend des routines pour créer, gérer et énumérer les objets de schéma. Cela comprend les objets de classe de schéma, les objets de propriété et les objets de syntaxe, en plus de pouvoir énumérer l’objet conteneur de classe de schéma.
13. Appels spécifiques au système d’exploitation (RegDSAPI. cpp). Cela comprend tous les appels qui font référence au système d’exploitation natif. Parmi d’autres fonctions, elles incluent des fonctions d’ouverture, de fermeture, de lecture et de modification d’objets, ainsi que ceux qui accèdent au schéma et aux données de propriété. L’exemple de composant fournisseur s’est produit pour simuler une hiérarchie de répertoires à l’aide du Registre. Seuls les noms de fonctions doivent être très intéressants pour un writer de fournisseur.
14. Implémentation [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (Cdispmgr. cpp). Ce code accède aux données de la bibliothèque de types pour permettre aux méthodes d’interface d’être appelées de manière compatible Automation.

 

 