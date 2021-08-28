---
title: Modèle de schéma ADSI
description: Un schéma est semblable à un dictionnaire en ce qu’il contient la définition de chaque type d’objet connu d’un service d’annuaire.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI (modèle de schéma ADSI)
- ADSI ADSI, à propos de, schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4893151c81eefa0a17420e18d5d87da232641571
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883872"
---
# <a name="adsi-schema-model"></a>Modèle de schéma ADSI

Un schéma est semblable à un dictionnaire en ce qu’il contient la définition de chaque type d’objet connu d’un service d’annuaire. Les applications clientes ADSI peuvent parcourir un schéma pour découvrir les fonctionnalités de toute implémentation ADSI donnée. En outre, ADSI fournit des interfaces de gestion de schéma qui peuvent être utilisées pour communiquer avec le schéma sous-jacent d’un service d’annuaire.

Certains schémas sont des fournisseurs extensibles et ADSI, ou des fournisseurs tiers peuvent choisir de publier de nouvelles interfaces ou des propriétés supplémentaires pour les interfaces existantes. Les clients ADSI utilisent ces données pour déterminer les fonctionnalités prises en charge pour chaque service d’annuaire.

Il existe trois types d’objets de schéma : les classes, les propriétés et les syntaxes, chacune prenant en charge les interfaces de gestion de schéma [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)et [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

> [!Note]  
> La classe est un terme surchargé. Il existe des classes C++, des classes Java, des classes COM et des classes ADSI. Dans ce document, la classe Word, sauf indication contraire, fait référence à une catégorie ou un type d’objet de schéma.

 

ADSI extrait le schéma de chaque service d’annuaire et le place dans chaque nœud racine de niveau supérieur dans l’objet **namespace** . Pour identifier les classes prises en charge par un service d’annuaire sur un nœud racine donné, vous devez énumérer l’objet de schéma et obtenir la liste des objets de classe, des objets de propriété et des objets de syntaxe. Pour plus d’informations, consultez [utilisation du schéma ADSI](using-the-adsi-schema.md).

## <a name="adsi-ldap-provider-schema-cache"></a>Cache du schéma du fournisseur LDAP ADSI

Le fournisseur LDAP pour ADSI tente de mettre en cache les données de schéma sur l’ordinateur local. Un sous-schéma est identifié par un nom unique stocké dans l’attribut [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) situé à la racine du RootDSE (Directory Service Enterprise). En plus de fournir les données de sous-schéma, les serveurs LDAP v3 doivent exposer un attribut [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) utilisé pour déterminer l’heure de la dernière modification du schéma.

Lorsque l’interface ADSI est liée pour la première fois au serveur LDAP, elle récupère les données de sous-schéma à l’aide de l’attribut [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) . Si ADSI parvient à trouver l’objet de sous-schéma, il stocke un pointeur vers les données du Registre sur l’ordinateur qui se connecte au serveur LDAP. Pour plus d’informations sur l’emplacement exact où ces valeurs sont stockées dans le registre, consultez [ADSI et contrôle de compte d’utilisateur](adsi-and-uac.md).

ADSI tente ensuite de traiter les données de schéma et lit l’attribut [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) . Si l’attribut **modifyTimeStamp** existe et que l’interface ADSI traite correctement le schéma, ADSI écrit le sous-schéma sur le disque et crée les deux valeurs de Registre suivantes sous la clé. Si les données de sous-schéma existent, mais ne peuvent pas être traitées, aucune de ces valeurs de Registre n’est créée :

-   Valeur d' **heure** , qui contient l’attribut [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) . Cette valeur est utilisée pour garantir que les données de schéma sont actuelles et empêche le rechargement constant des données de schéma.
-   Valeur de **fichier** qui contient le chemin d’accès à l’emplacement où ADSI stocke les données de schéma dans le système de fichiers. Par défaut, ADSI met en cache le sous-schéma dans le &lt; &gt; \\ répertoire SystemRoot SchCache avec un nom de fichier correspondant au nom du serveur LDAP.

Si les données de sous-schéma peuvent être traitées, mais qu’aucun attribut [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) n’est exposé, les données de schéma sont mises en cache en mémoire, mais elles ne sont pas écrites sur le disque. Si un serveur LDAP v3 a été contacté par le biais d’ADSI sur l’ordinateur local et qu’un sous-schéma mis en cache n’est pas présent, il est très probable pour l’une des raisons suivantes :

-   Le serveur n’a pas exposé les propriétés correctes.
-   ADSI n’a pas pu traiter le schéma.
-   ADSI n’a pas pu écrire le fichier dans le système de fichiers.

 

 
