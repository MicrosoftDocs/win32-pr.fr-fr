---
title: Résolution de noms pour les fournisseurs de services et de DLL
description: Les paragraphes suivants décrivent comment les \_32.dll Ws2 et les fournisseurs d’espaces de noms implémentent les services de résolution de noms pris en charge par l’API Winsock.
ms.assetid: 25fcb1c2-2d28-41a0-9124-05608f22420f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f0ecd7e40d27d6dd9faa541bbca8f7543e6538702599de78a64104f10b1c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097709"
---
# <a name="name-resolution-for-dll-and-service-providers"></a>Résolution de noms pour les fournisseurs de services et de DLL

Les paragraphes suivants décrivent comment les \_32.dll Ws2 et les fournisseurs d’espaces de noms implémentent les services de résolution de noms pris en charge par l’API Winsock.

## <a name="ws2_32dll-functionality-for-name-resolution"></a>La \_ fonctionnalité Ws232.dll pour la résolution de noms

Le \_32.dll Ws2 gère le chargement de l’inscription et de la demande des dll du fournisseur d’espace de noms individuel. il est également responsable du routage des opérations d’espace de noms à partir d’une application Windows sockets 2 vers l’ensemble approprié de fournisseurs d’espaces de noms. Ce mappage est régi par la valeur des paramètres de l’identificateur d’espace de noms et du fournisseur de services qui se trouvent dans les fonctions d’API individuelles. En règle générale, lorsqu’un fournisseur d’espaces de noms spécifique est référencé, l’opération est routée uniquement vers un fournisseur identifié. Si l’identificateur du fournisseur d’espace de noms est null mais qu’un espace de noms particulier est référencé, l’opération est routée vers tous les fournisseurs d’espaces de noms qui prennent en charge l’espace de noms identifié. Si l’identificateur du fournisseur d’espace de noms a la valeur null et que l’identificateur d’espace de noms est donné comme NS \_ All, l’opération est routée vers tous les fournisseurs d’espaces de noms actifs.

Dans le cadre du démarrage d’une requête sur un ou plusieurs fournisseurs de services, le \_32.dll Ws2 alloue un objet pour effectuer le suivi de l’État en cours de la requête. Un handle opaque représentant cet objet est retourné à l’application qui a démarré la requête. L’application fournit ce descripteur en tant que paramètre chaque fois qu’il appelle une fonction d’interface d’application de façon répétée pour récupérer l’unité de données suivante résultant de la requête.

En réponse à ces appels de procédure d’interface d’application, le \_32.dll Ws2 utilise les informations qu’il stocke dans l’objet pour effectuer les appels correspondants aux fournisseurs d’espaces de noms impliqués dans la requête. L' \_32.dll Ws2 met à jour les informations de son objet à mesure que chaque appel d’interface d’application successif se produit afin que les appels correspondants aux fournisseurs d’espaces de noms progressent correctement par le biais de tous les fournisseurs d’espaces de noms impliqués dans la requête.

## <a name="namespace-provider-functionality"></a>Fonctionnalité du fournisseur d’espace de noms

chaque fournisseur d’espaces de noms est chargé de mapper l’ensemble des fonctions figurant dans le SPI Windows sockets 2 de résolution de noms aux transactions appropriées avec l’espace de noms pris en charge. Dans certains cas, il s’agit essentiellement de mapper le SPI à l’interface native qui existe pour l’espace de noms. Dans d’autres, le fournisseur d’espaces de noms doit exécuter des transactions avec le fournisseur d’espaces de noms sur le réseau. certains fournisseurs d’espaces de noms effectuent cela en effectuant des appels à l’API Windows sockets, d’autres utilisent des interfaces privées pour les piles de transport associées.

 

 



