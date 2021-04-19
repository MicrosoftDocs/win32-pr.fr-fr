---
description: Vous pouvez modéliser un fournisseur de classes comme un fournisseur push ou pull, qui spécifie comment un fournisseur s’attend à interagir avec WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Détermination de l’état d’envoi ou d’extraction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543688"
---
# <a name="determining-push-or-pull-status"></a>Détermination de l’état d’envoi ou d’extraction

Vous pouvez modéliser un fournisseur de classes comme un fournisseur push ou pull, qui spécifie comment un fournisseur s’attend à interagir avec WMI. Les fournisseurs d’extraction reçoivent une requête de WMI et répondent à la demande en générant les données dynamiquement ou en les récupérant à partir d’un cache local. Les fournisseurs d’extraction doivent également implémenter un grand nombre d’interfaces.

Un fournisseur d’extraction génère des définitions de classe de manière dynamique. En règle générale, les données gérées par un fournisseur d’extraction changent fréquemment, ce qui oblige le fournisseur à générer la classe dynamiquement ou à récupérer la classe à partir d’un cache local chaque fois qu’une application émet une requête. Un fournisseur d’extraction doit implémenter ses propres mécanismes de récupération de données, de cache et de notification d’événement. Étant donné que la plupart des fournisseurs sont des fournisseurs d’extraction, la documentation de ce fichier suppose que vous générez un fournisseur d’extraction, sauf indication contraire.

En revanche, WMI utilise les données de l’espace de stockage WMI pour gérer toutes les demandes d’application pour les fournisseurs de notifications push. Les fournisseurs de notifications push utilisent également moins de méthodes d’interface et sont donc plus faciles à implémenter. Un fournisseur d’émission utilise le référentiel WMI comme zone de stockage pour les informations sur l’objet géré et met à jour ces informations uniquement pendant l’initialisation. Par exemple, le fournisseur de classes WDM inclus dans la section WMI du kit de développement logiciel (SDK) Microsoft Windows est modélisé comme un fournisseur de notifications push.

En utilisant le référentiel WMI comme zone de stockage, un fournisseur de notifications push bénéficie des avantages suivants par rapport à un fournisseur d’extraction :

-   Le fournisseur n’a pas besoin d’implémenter un cache local pour stocker les données.
-   Le fournisseur n’a pas besoin de prendre en charge la récupération des données. au lieu de cela, le fournisseur peut s’appuyer sur WMI pour assurer la prise en charge de la récupération.
-   Lorsqu’une application demande des données fournies par le fournisseur, WMI effectue cette demande.
-   Le fournisseur peut également s’appuyer sur WMI pour prendre en charge la notification d’événements.

Toutefois, étant donné qu’un fournisseur push est mis à jour uniquement pendant l’initialisation, toute modification apportée à une classe peut ne pas être reflétée dans l’espace de stockage WMI pendant un certain temps. Par conséquent, le modèle de fournisseur Push fonctionne mieux avec les classes qui changent peu ou sont totalement statiques.

 

 



