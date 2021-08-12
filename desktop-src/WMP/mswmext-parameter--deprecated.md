---
title: Paramètre MSWMExt (déconseillé)
description: Paramètre MSWMExt (déconseillé)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Windows Fichiers multimédias, paramètre MSWMExt
- MSWMExt, paramètre
- Paramètre MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ec80530f95d4429769758488e5a2b24b0268c57255248c7685a0d00125aa130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574596"
---
# <a name="mswmext-parameter-deprecated"></a>Paramètre MSWMExt (déconseillé)

Le paramètre *MSWMExt* indique à un programme client le format d’un fichier référencé.

**Syntaxe**


```XML

URL?MSWMExt=.
ext
```



**Exemple de code**


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a>Notes

Les programmes clients utilisent parfois une extension de nom de fichier ou un type MIME pour déterminer s’il faut restituer un fichier multimédia en tant que flux, restituer le fichier après un téléchargement complet ou refuser le rendu du fichier. Si un programme client ne peut pas déterminer comment traiter un fichier multimédia basé sur l’extension de nom de fichier ou le type MIME, il peut déterminer comment traiter le fichier en inspectant le paramètre *MSWMExt* . Par exemple, le client peut traiter le fichier comme s’il avait une extension égale à la valeur du paramètre *MSWMExt* . Pour plus d’informations sur les types MIME et les extensions de nom de fichier, consultez [extensions de nom de fichier](file-name-extensions.md). Pour plus d’informations sur le paramètre *MSWMExt* , voir l’article [236895](https://support.microsoft.com/kb/236895) de la base de connaissances Microsoft.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Versions précédentes de Windows les fichiers multimédias (dépréciés)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




