---
title: Stockages et flux
description: Un objet de stockage est analogue à un répertoire du système de fichiers.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671769"
---
# <a name="storages-and-streams"></a>Stockages et flux

Un objet de stockage est analogue à un répertoire du système de fichiers. De même qu’un répertoire peut contenir d’autres répertoires et fichiers, un objet de stockage peut contenir d’autres objets de stockage et objets de flux. À l’instar d’un répertoire, un objet de stockage effectue le suivi des emplacements et des tailles des objets de stockage et des objets de flux imbriqués sous celui-ci.

Un objet de flux est analogue à la notion traditionnelle d’un fichier. À l’instar d’un fichier, un flux contient des données stockées sous la forme d’une séquence d’octets consécutive.

Un fichier composé COM se compose d’un objet de stockage racine contenant au moins un objet de flux représentant ses données natives, ainsi qu’un ou plusieurs objets de stockage correspondant à ses objets liés et incorporés. L’objet de stockage racine est mappé à un nom de fichier dans le système de fichiers dans lequel il se trouve. Chacun des objets à l’intérieur du document est également représenté par un objet de stockage contenant un ou plusieurs objets de flux, et peut-être également contenir un ou plusieurs objets de stockage. De cette façon, un document peut se composer d’un nombre illimité d’objets imbriqués. Pour plus d’informations, consultez [fichiers composés](compound-files.md).

 

 




