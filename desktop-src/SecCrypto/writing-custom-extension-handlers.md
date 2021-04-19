---
description: Pour créer des extensions personnalisées ou encoder une extension complexe, vous pouvez écrire vos propres gestionnaires d’extension qui exportent des interfaces personnalisées.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Écriture de gestionnaires d’extensions personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522163"
---
# <a name="writing-custom-extension-handlers"></a>Écriture de gestionnaires d’extensions personnalisés

Pour créer des extensions personnalisées ou encoder une extension complexe, vous pouvez écrire vos propres gestionnaires d’extension qui exportent des interfaces personnalisées. Les services de certificats Microsoft sont fournis avec les interfaces suivantes, qui peuvent être utilisées pour encoder différents types de données d’extension : [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)et [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray). Ces interfaces sont contenues dans Certenc.dll. En outre, les informations de type de ces interfaces sont contenues dans Certencl.dll, qui est contenue dans le kit de développement logiciel (SDK) de la plateforme.

Pour plus d’informations sur les gestionnaires d’extension, consultez [gestionnaires d’extension](extension-handlers.md).

 

 



