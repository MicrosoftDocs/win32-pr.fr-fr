---
title: Clé de file_extension
description: Associe une extension de nom de fichier à un ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363460"
---
# <a name="file_extension-key"></a>Clé de> de l’extension de fichier <\_

Associe une extension de nom de fichier à un ProgID.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>Remarques

les informations contenues dans la clé d’extension de nom de fichier sont utilisées par l’explorateur de Windows et les monikers de fichiers. [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) utilise la clé d’extension de nom de fichier pour fournir le CLSID associé.

La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**FileType**](filetype-key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




