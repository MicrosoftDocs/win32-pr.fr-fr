---
title: Modification des attributs de métadonnées
description: Modification des attributs de métadonnées
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media Format SDK, modification des attributs de métadonnées
- ASF (Advanced Systems Format), modification des attributs de métadonnées
- ASF (format de systèmes avancés), modification des attributs de métadonnées
- métadonnées, modifier les attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381556"
---
# <a name="editing-metadata-attributes"></a>Modification des attributs de métadonnées

La modification des attributs de métadonnées est très similaire à la définition de nouveaux attributs. Au lieu d’utiliser [**IWMHeaderInfo3 :: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), utilisez [**IWMHeaderInfo3 :: ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **ModifyAttribute** est identique à **AddAttribute** , sauf que vous ne spécifiez pas de nom d’attribut et que le numéro d’index est un paramètre d’entrée au lieu d’une sortie.

Vous pouvez utiliser le nombre de flux 0xFFFF pour spécifier un attribut à modifier à l’aide de son index global.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




