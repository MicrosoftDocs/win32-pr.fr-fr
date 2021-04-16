---
title: Bibliothèques de types d’extension ADSI
description: Les bibliothèques de types pour les extensions ne sont pas fusionnées.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- Bibliothèques de types d’extension ADSI ADSI
- ADSI d’extensions, bibliothèques de types d’extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507042"
---
# <a name="adsi-extension-type-libraries"></a>Bibliothèques de types d’extension ADSI

Les bibliothèques de types pour les extensions ne sont pas fusionnées. Les clients ADSI doivent inclure spécifiquement la bibliothèque de types pour chaque extension. La bibliothèque de types est requise pour Visual Basic pour activer les liaisons antérieures. Les applications clientes écrites en C/C++ peuvent appeler la méthode **QueryInterface** sur les interfaces d’extension définies dans les fichiers d’en-tête d’extension.

 

 




