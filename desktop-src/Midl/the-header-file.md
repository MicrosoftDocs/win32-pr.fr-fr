---
title: Fichier d’en-tête
description: Le fichier d’en-tête contient les définitions de tous les types de données et opérations déclarés dans le fichier IDL, ainsi que tous les types de données et opérations déclarés dans les fichiers inclus avec la directive \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL et RPC MIDL, interfaces, fichier d’en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd107bbf741f3259ac474d03a3ec1eba5c4ab8217df3ff6afa5ef45e7b4945a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582129"
---
# <a name="the-header-file"></a>Fichier d’en-tête

Le fichier d’en-tête contient les définitions de tous les types de données et opérations déclarés dans le fichier IDL, ainsi que tous les types de données et opérations déclarés dans les fichiers inclus avec la \# directive include. Les types de données des fichiers importés avec la directive import ne sont pas répliqués dans le fichier d’en-tête. au lieu de cela, le fichier d’en-tête généré contient une ligne include dans le fichier H généré à partir du fichier importé. Le fichier d’en-tête doit être inclus par tous les modules d’application qui appellent les opérations définies, implémentent les opérations définies ou manipulent les types définis.

Le compilateur MIDL bascule [**/header**](-header.md) et [**/out**](-out.md) sur le fichier d’en-tête.

 

 




