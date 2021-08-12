---
title: À propos de DDEML
description: Cette rubrique traite de l’échange dynamique de données.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Windows Interface utilisateur, échange dynamique de données (DDE)
- échange dynamique de données (DDE), à propos de
- DDE (échange dynamique de données), à propos de
- échange de données, échange dynamique de données (DDE)
- Windows Interface utilisateur, échange dynamique de données Management Library (DDEML)
- bibliothèque de gestion des échange dynamique de données (DDEML), à propos de
- DDEML (bibliothèque de gestion échange dynamique de données), à propos de
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755d4efea534918ac3fd3da46364e3cb528e4199498ea7533c1635af6780cc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545560"
---
# <a name="about-the-ddeml"></a>À propos de DDEML

échange dynamique de données (DDE) diffère du mécanisme de transfert de données du presse-papiers. L’une des différences est que le presse-papiers est presque toujours utilisé comme réponse ponctuelle à une action spécifique de l’utilisateur, par exemple en cliquant sur **coller** à partir d’un menu. Bien que l’échange DDE puisse également être initié par un utilisateur, il continue généralement sans l’intervention de l’utilisateur.

la bibliothèque de gestion des échange dynamique de données (DDEML) fournit une interface qui simplifie la tâche d’ajout de la fonctionnalité DDE à une application. Au lieu d’envoyer, de publier et de traiter des messages DDE directement, une application utilise les fonctions fournies par le DDEML pour gérer les conversations DDE. Une conversation DDE est l’interaction entre les applications client et serveur. Le DDEML fournit également un moyen de gérer les chaînes et les données partagées entre les applications DDE. Au lieu d’utiliser des atomes et des pointeurs vers des objets mémoire partagés, les applications DDE créent et échangent des handles de chaîne, qui identifient les chaînes et les handles de données qui identifient les objets DDE. DDEML fournit une fonction ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) qui permet à une application serveur d’inscrire les noms de service qu’elle prend en charge. Les noms de service sont ensuite diffusés à d’autres applications dans le système, qui utilisent les noms pour se connecter au serveur. Le DDEML garantit également la compatibilité entre les applications DDE en exigeant qu’elles implémentent le protocole DDE de manière cohérente.

Les applications existantes utilisant le protocole DDE basé sur des messages sont entièrement compatibles avec celles qui utilisent DDEML. autrement dit, une application utilisant un DDE basé sur des messages peut établir des conversations et exécuter des transactions avec des applications à l’aide de DDEML. Au lieu d’utiliser des messages DDE dans votre nouvelle application, tirez parti du DDEML et des nombreuses améliorations qu’il offre.

Pour utiliser DDEML, vous devez inclure DDEML. Fichier d’en-tête H dans vos fichiers sources, lien avec USER32. Fichier LIB, et assurez-vous que le fichier DDEML.DLL réside dans le chemin d’accès du système.

Chaque fois qu’une fonction DDEML échoue, une application peut appeler la fonction [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) pour déterminer la cause de l’échec. **DdeGetLastError** retourne une valeur d’erreur qui spécifie la cause de l’erreur la plus récente.

 

 




