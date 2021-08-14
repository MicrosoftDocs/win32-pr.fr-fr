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
ms.openlocfilehash: f2390f587d5ce0d18e6e96aaf993115bb523feb340bf2becf60ceb2cff81d952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180829"
---
# <a name="adsi-extension-type-libraries"></a>Bibliothèques de types d’extension ADSI

Les bibliothèques de types pour les extensions ne sont pas fusionnées. Les clients ADSI doivent inclure spécifiquement la bibliothèque de types pour chaque extension. la bibliothèque de types est requise pour Visual Basic pour activer les liaisons antérieures. Les applications clientes écrites en C/C++ peuvent appeler la méthode **QueryInterface** sur les interfaces d’extension définies dans les fichiers d’en-tête d’extension.

 

 




