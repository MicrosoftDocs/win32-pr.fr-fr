---
description: Le type de position d’une table des matières
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Le type de position d’une table des matières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543486"
---
# <a name="the-position-type-of-a-table-of-contents"></a>Le type de position d’une table des matières

Certaines méthodes de l’interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) ont un paramètre nommé *enumTocPosType* qui est de type [**enum TOC \_ pos \_**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type). Ce paramètre spécifie la position dans un fichier multimédia où une table des matières est stockée. L’objectif était que la table des matières pouvait être stockée dans l’en-tête de fichier ou dans le corps du fichier sous la forme d’un objet de niveau supérieur. Cette fonctionnalité n’a pas encore été implémentée.

Actuellement, les tables de matières ne peuvent être stockées qu’en tant qu’objets de niveau supérieur. vous devez donc toujours définir le paramètre *enumTocPosType* sur **TOC \_ pos \_ TOPLEVELOBJECT**. Si vous affectez à *enumTocPosType* la valeur **\_ \_ en-tête de la table des matières TOC**, la méthode retourne **E \_ NOTIMPL**.

Les méthodes suivantes ont un paramètre *enumTocPosType* .

-   [**GetTocCount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**GetTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**RemoveTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**RemoveTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation de l’analyseur de table des matières](toc-parser-programming-guide.md)
</dt> </dl>

 

 



