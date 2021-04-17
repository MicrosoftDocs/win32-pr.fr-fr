---
description: La visionneuse de frames Moniteur réseau affiche les données analysées dans trois volets.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Affichage des informations analysées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567409"
---
# <a name="viewing-parsed-information"></a>Affichage des informations analysées

La visionneuse de frames Moniteur réseau affiche les données analysées dans trois volets. Le volet supérieur affiche un résumé du frame qui comprend le protocole identifié. Le volet central affiche les propriétés de données mises en forme qui peuvent être organisées hiérarchiquement dans le cadre de l’affichage de l’analyseur. Le volet inférieur affiche les données brutes en surbrillance sélectionnées dans le volet central.

Vous pouvez spécifier le mode d’affichage des informations dans la visionneuse lorsque vous développez votre propre analyseur. L’illustration suivante montre comment les informations peuvent être affichées dans la visionneuse de frames Moniteur réseau.

![visionneuse de trames du moniteur réseau](images/parseui.png)

> [!Note]  
> Les analyseurs n’affichent pas les frames. Les analyseurs reconnaissent les champs dans les informations fournies, puis notifient Moniteur réseau pour afficher le frame. Le filtrage est une opération de niveau supérieur qui permet aux requêtes de filtre d’étendre des analyseurs.

 

Dans votre analyseur, utilisez uniquement les fonctions qui peuvent s’exécuter sur les applications Microsoft Win32. Avant d’attacher des propriétés aux données brutes, un analyseur doit d’abord inscrire toutes les propriétés possibles avec le noyau Moniteur réseau. L’analyseur envoie un message au noyau pour créer une base de données de propriétés, puis remplit la base de données de propriétés avec chaque propriété possible pour son protocole. Chaque propriété de la base de données de propriété contient des informations telles qu’une description textuelle, un type de données et un qualificateur utilisés pour mettre en forme les données brutes, ainsi qu’une routine de mise en forme utilisée pour afficher les données.

 

 



