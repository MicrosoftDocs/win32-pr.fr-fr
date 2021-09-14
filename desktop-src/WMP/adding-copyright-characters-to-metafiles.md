---
title: Ajout de caractères de copyright aux sous-fichiers
description: Les caractères pour les symboles de copyright et de marque déposée (\ 169 ; ou \ 174 ;) peuvent ne pas s’afficher correctement si le métafichier n’est pas encodé à l’aide du schéma d’encodage UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- ajout de caractères de Copyright aux fichiers Lecteur Windows Media
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324301"
---
# <a name="adding-copyright-characters-to-metafiles"></a>Ajout de caractères de copyright aux sous-fichiers

Les caractères des symboles de copyright et de marque déposée (© ou®) peuvent ne pas s’afficher correctement si le métafichier n’est pas encodé à l’aide du schéma d’encodage UTF-8. Dans ce cas, pour afficher correctement l’un de ces symboles pour tous les utilisateurs, vous pouvez utiliser les équivalents ASCII (c) et (r) à l’intérieur de l’élément de **Copyright** , comme indiqué dans le code suivant.


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



Si le métafichier est encodé à l’aide de UTF-8, les symboles de copyright et de marque s’affichent correctement.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




