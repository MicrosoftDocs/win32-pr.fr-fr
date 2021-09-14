---
description: Insertion d’une image clé forcée
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Insertion d’une image clé forcée (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415839"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Insertion d’une image clé forcée (Microsoft Media Foundation)

Quand vous configurez un objet d’encodeur vidéo, vous pouvez définir un intervalle maximal pour les images clés dans le contenu encodé. Toutefois, le codec place les images clés dans cet intervalle comme indiqué par le contenu. l’intervalle d’image clé n’est pas constant. Pour certaines applications, la distance d’image clé est très importante. Par exemple, une application de modification vidéo a besoin d’images clés à des emplacements logiques à un éditeur, tels que des arrêts de scène et des transitions de capture.

L’insertion d’une image clé forcée est une fonctionnalité qui vous permet de demander qu’une trame d’entrée soit encodée sous la forme d’une image clé. L’encodeur essaiera d’honorer ces requêtes, mais les paramètres de mémoire tampon (vitesse de transmission et fenêtre de mémoire tampon) configurés pour la session d’encodage sont toujours prioritaires.

Les objets d’encodeur vidéo implémentent l’insertion d’une image clé forcée en réponse à une extension d’unité de données jointe à l’exemple d’entrée. Pour plus d’informations sur les extensions d’unité de données, consultez [utilisation des extensions d’unité de données](usingdataunitextensions.md).

Les données d’extension pour l’insertion d’une image clé forcée sont identifiées par la valeur GUID suivante : **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. Les extensions individuelles sont des valeurs **bool** . Définissez la valeur sur **true** pour indiquer une demande d’image clé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des extensions d’unité de données](usingdataunitextensions.md)
</dt> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 



