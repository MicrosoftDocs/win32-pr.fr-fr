---
title: Section Description
description: Section Description
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Lecteur Windows Media Apparences mobiles, section Description
- apparences, section Description
- création d’apparences, section Description
- écriture de code pour les apparences, section Description
- Section Description dans les apparences
- fichiers de définition d’apparence, section Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008483"
---
# <a name="description-section"></a>Section Description

ensuite, vous devez fournir une section qui décrit la taille et l’orientation de l’apparence lors de la création d’une apparence pour Lecteur Windows Media série 9 pour Windows Mobile 2003 et versions ultérieures :


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



La section Description doit commencer par la description du mot entre crochets, puis inclure une ligne qui spécifie les dimensions et la résolution d’affichage de l’apparence.

Les lignes commençant par deux barres obliques ne sont pas traitées et peuvent être utilisées pour les commentaires ou, comme indiqué dans le code précédent, un modèle pour vous aider à vous souvenir de ce qui se trouve dans une section. Vous pouvez également utiliser des modèles pour faciliter l’alignement de tous les éléments en colonnes.

Pour plus d’informations sur la section Description, consultez [Description](description.md) dans la référence de l’apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture du code**](writing-the-code.md)
</dt> </dl>

 

 




