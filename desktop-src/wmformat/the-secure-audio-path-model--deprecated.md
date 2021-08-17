---
title: Le modèle de chemin d’accès audio sécurisé (déconseillé)
description: Le modèle de chemin d’accès audio sécurisé (déconseillé)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- gestion des droits numériques (DRM), Microsoft Secure audio Path (SAP)
- DRM (gestion des droits numériques), Microsoft Secure audio Path (SAP)
- Windows Media Format SDK, Secure audio Path (SAP)
- gestion des droits numériques (DRM), chemin audio sécurisé (SAP)
- DRM (gestion des droits numériques), chemin d’accès audio sécurisé (SAP)
- Microsoft Secure audio Path (SAP), modèle
- Chemin d’accès audio sécurisé (SAP), modèle
- SAP (chemin d’accès audio sécurisé), modèle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a381d29bcbf4b09ae989325cd5b35c332a6f316c1f932868437ac93a7854ab58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084283"
---
# <a name="the-secure-audio-path-model-deprecated"></a>Le modèle de chemin d’accès audio sécurisé (déconseillé)

Cette page documente une fonctionnalité qui sera prise en charge avec une autre solution technique dans les futures versions de Windows.

microsoft secure Audio Path (SAP) est une fonctionnalité de microsoft Windows® et microsoft Windows XP. La nécessité de lire un fichier audio uniquement via un chemin d’accès audio sécurisé est spécifiée dans la licence DRM et appliquée par les composants du client DRM. Aucun chiffrement supplémentaire n’est ajouté pour les fichiers SAP uniquement lorsqu’ils sont protégés initialement. Le chiffrement SAP est ajouté automatiquement par les composants DRM au moment de la lecture, comme le processus d’authentification pour tous les composants logiciels impliqués dans la lecture. le fonctionnement de sap est donc complètement transparent pour les applications. c’est pourquoi il n’existe aucune méthode ou propriété dans le kit de développement logiciel (SDK) de Format de média Windows pour l’activation ou la désactivation de sap. Si vous le souhaitez, lors de la création d’un fichier protégé, le propriétaire du contenu peut ajouter un attribut d’en-tête personnalisé appelé « DRMHeader. SAPRequired » afin d’indiquer à un serveur de licences d’ajouter les exigences SAP à la licence. L’implémentation d’un tel schéma est jusqu’au propriétaire du contenu et au service de licence.

Dans le modèle DRM actuel, si SAP n’est pas appliqué, lorsque la musique numérique protégée est jouée, le contenu chiffré passe au composant client DRM. le client drm vérifie que l’application et le composant drm incorporant le kit de développement logiciel (SDK) Windows Media Format sont valides. S’ils sont valides, le client DRM déchiffre le contenu et l’envoie à l’application, qui l’envoie ensuite aux composants audio de niveau inférieur. À ce stade, la musique déchiffrée est disponible pour les applications en mode utilisateur et les plug-ins et les pilotes en mode noyau qui peuvent intercepter les bits audio déchiffrés.

Lorsque la spécification du chemin d’accès audio sécurisé est appliquée, le contenu n’est pas déchiffré par l’application, mais il est transmis dans un État chiffré à des composants de niveau inférieur, tous ayant été authentifiés par Microsoft comme dignes de confiance. Un composant audio approuvé est un composant qui ne met pas le contenu audio à la disposition d’un composant système, à l’exception d’autres composants de confiance spécifiques. De cette façon, le contenu numérique reste protégé jusqu’au niveau du pilote.

Le diagramme suivant affiche le modèle actuel par rapport au modèle de chemin d’accès audio sécurisé.

![diagramme du modèle de chemin d’accès audio sécurisé](images/sap.png)

 

 




