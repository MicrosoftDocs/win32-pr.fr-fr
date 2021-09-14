---
title: Fichier d’en-tête
description: Le fichier d’en-tête contient les définitions de tous les types de données et opérations déclarés dans le fichier IDL, ainsi que tous les types de données et opérations déclarés dans les fichiers inclus avec la directive \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL et RPC MIDL, interfaces, fichier d’en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093141"
---
# <a name="the-header-file"></a>Fichier d’en-tête

Le fichier d’en-tête contient les définitions de tous les types de données et opérations déclarés dans le fichier IDL, ainsi que tous les types de données et opérations déclarés dans les fichiers inclus avec la \# directive include. Les types de données des fichiers importés avec la directive import ne sont pas répliqués dans le fichier d’en-tête. au lieu de cela, le fichier d’en-tête généré contient une ligne include dans le fichier H généré à partir du fichier importé. Le fichier d’en-tête doit être inclus par tous les modules d’application qui appellent les opérations définies, implémentent les opérations définies ou manipulent les types définis.

Le compilateur MIDL bascule [**/header**](-header.md) et [**/out**](-out.md) sur le fichier d’en-tête.

 

 




