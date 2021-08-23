---
title: À propos des e/s de fichier multimédia
description: À propos des e/s de fichier multimédia
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows multimédia, e/s de fichier
- multimédia, e/s de fichier
- entrée multimédia, e/s de fichier
- e/s de fichier multimédia, à propos de
- e/s de fichier, à propos de
- entrée et sortie (e/s), à propos de
- E/s (entrée et sortie), à propos de
- e/s de base
- RIFF (Resource Interchange File Format)
- RIFF (Resource Interchange File Format)
- E/S RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584b736ba41fb0ea7dd5f3e6411e1783964db21a9819fbb98364708196dc2943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526639"
---
# <a name="about-multimedia-file-io"></a>À propos des e/s de fichier multimédia

La plupart des applications multimédias nécessitent une entrée et une sortie de fichier (e/s), c’est-à-dire la possibilité de créer, de lire et d’écrire des fichiers sur disque. Les services d’e/s de fichier multimédia fournissent des e/s de fichier mises en mémoire tampon et non mises en mémoire tampon et prennent en charge les fichiers RIFF. Les services sont extensibles avec des procédures d’e/s personnalisées qui peuvent être partagées entre les applications.

La plupart des applications ont uniquement besoin des services d’e/s de base et des services d’e/s de fichier RIFF. Les applications sensibles aux performances d’e/s de fichier, telles que les applications qui diffusent des données à partir d’un CD-ROM en temps réel, peuvent optimiser les performances en utilisant des services pour accéder directement au tampon d’e/s de fichier. Les applications qui accèdent à des systèmes de stockage personnalisés, tels que des Archives de fichiers et des bases de données, peuvent fournir leur propre procédure d’e/s qui lit et écrit des éléments du système de stockage.

 

 




