---
description: Moniteur réseau utilise trois types d’objets BLOB (Binary Large Objects) pour sélectionner et connecter des cartes d’interface réseau (NIC), capturer des données et manipuler des données NPP.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Types d’objets BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210582"
---
# <a name="blob-types"></a>Types d’objets BLOB

Moniteur réseau utilise trois types d’objets BLOB (Binary Large Objects) pour sélectionner et connecter des cartes d’interface réseau (NIC), capturer des données et manipuler des données NPP.

## <a name="npp-blob"></a>OBJET BLOB NPP

Les applications utilisent des objets BLOB NPP pour se connecter à une carte réseau spécifique via un NPP. (L’application établit la connexion avec un appel à **CreateNPPInterface** et les données d’emplacement dans l’objet BLOB NPP.) Une application peut également stocker ses données de configuration dans l’objet BLOB NPP pour configurer le NPP. En outre, une application qui enregistre son objet BLOB NPP n’est pas obligée de parcourir le Finder pour réutiliser cet objet BLOB.

## <a name="filter-blob"></a>Filtrer l’objet BLOB

Un objet BLOB de filtres contient des critères définis par l’application que vous pouvez utiliser pour sélectionner un NPP et une carte réseau. Par exemple, une application peut demander une carte réseau spécifique, uniquement des cartes Ethernet ou des cartes qui prennent en charge une fréquence de capture de frame spécifique.

## <a name="special-blob"></a>Objet BLOB spécial

Lorsqu’un NPP requiert des données supplémentaires avant de pouvoir retourner un objet BLOB NPP à une application, le NPP utilise un objet BLOB spécial. Le plus souvent, l’application n’a pas besoin ou n’utilise pas d’objets BLOB spéciaux afin qu’ils ne soient pas renvoyés à une application, sauf si un indicateur spécifique est défini dans un appel de fonction. Par exemple, un NPP distant utilise un objet BLOB spécial, car un nom de chemin d’accès est requis pour établir une connexion. Une application qui reçoit un objet BLOB spécial NPP distant peut ajouter la chaîne et effectuer un rappel dans le Finder pour obtenir une table BLOB NPP. Pour plus d’informations, consultez [entrées d’objets BLOB spéciaux](special-blob-entries.md).

 

 



