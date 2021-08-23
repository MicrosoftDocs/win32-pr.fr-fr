---
description: Les trois types d’espaces de noms dans le SPI de Windows Sockets (Winsock) incluent des espaces de noms dynamiques, statiques et persistants.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Types d’espaces de noms dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ec933650825e891a723cbbc041ad4f631c6f54b7b2b4f6a255359b640509ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733189"
---
# <a name="types-of-namespaces-in-the-spi"></a>Types d’espaces de noms dans le SPI

Il existe trois types d’espaces de noms différents dans lesquels un service peut être inscrit :

-   Dynamique
-   statique
-   Persistante

Les espaces de noms dynamiques permettent aux services de s’inscrire avec l’espace de noms à la volée, et pour que les clients découvrent les services disponibles au moment de l’exécution. Les espaces de noms dynamiques s’appuient souvent sur des diffusions pour indiquer la disponibilité continue d’un service réseau. Les exemples d’espaces de noms dynamiques incluent l’espace de noms SAP utilisé dans un environnement NetWare et l’espace de noms NBP utilisé par AppleTalk.

Les espaces de noms statiques requièrent que tous les services soient inscrits à l’avance, c’est-à-dire lorsque l’espace de noms est créé. Le DNS est un exemple d’espace de noms statique. Bien qu’il existe un moyen de résoudre les noms par programmation, il n’existe pas de méthode d’enregistrement des noms par programmation.

Les espaces de noms persistants permettent aux services de s’inscrire à l’espace de noms à la volée. Contrairement aux espaces de noms dynamiques, toutefois, les espaces de noms persistants conservent les informations d’inscription dans un stockage non volatile où il reste jusqu’à ce que le service demande sa suppression. Les espaces de noms persistants sont typified par des services d’annuaire tels que X. 500 et NDS (NetWare Directory Service). Ces environnements permettent l’ajout, la suppression et la modification des propriétés du service. En outre, l’objet de service représentant le service dans le service d’annuaire peut avoir plusieurs attributs associés au service. L’attribut le plus important pour les applications clientes est les informations d’adressage du service.

 

 



