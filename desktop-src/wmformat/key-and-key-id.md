---
title: ID de clé et de clé
description: ID de clé et de clé
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- gestion des droits numériques (DRM), clés
- DRM (gestion des droits numériques), clés
- gestion des droits numériques (DRM), enfant
- DRM (gestion des droits numériques), enfant
- ID de clé (KID)
- KID (ID de la clé)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106538783"
---
# <a name="key-and-key-id"></a>ID de clé et de clé

Lorsque vous empaquetez un fichier, vous utilisez une clé. Une clé est un élément de données utilisé dans les algorithmes de chiffrement qui protègent le contenu. Il existe deux parties à chaque clé : une valeur initiale de clé de licence et un ID de clé (souvent abrégé en enfants). L’ID de clé est public et est stocké dans l’en-tête de fichier pour identifier la clé requise pour déchiffrer le fichier. La valeur initiale de la clé de licence est une valeur secrète qui doit être partagée par le gestionnaire de package de contenu et l’émetteur de licence.

Un ID de clé identifie le contenu protégé du point de vue de la licence. Bien que vous puissiez utiliser le même ID de clé pour plusieurs fichiers, il est recommandé de toujours utiliser un ID de clé unique pour chaque élément de contenu protégé.

La plupart des méthodes décrites dans cette documentation utilisent des chaînes d’ID de clé pour sélectionner des licences. Ces chaînes contiennent l’ID de clé encodé en base64.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](drmconcepts.md)
</dt> </dl>

 

 




