---
title: Conversion de l’espace colorimétrique
description: Conversion de l’espace colorimétrique
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media Format SDK, Color Space conversion
- ASF (Advanced Systems Format), conversion de l’espace colorimétrique
- ASF (format des systèmes avancés), conversion de l’espace colorimétrique
- conversion de l’espace colorimétrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b596b7ae8ed32e64cc3ebe8a23f1bc52dafb5304308104aba083675afe6370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447939"
---
# <a name="color-space-conversion"></a>Conversion de l’espace colorimétrique

Il existe souvent une différence entre la profondeur de couleur du format vidéo compressé dans le profil et le format d’entrée. Dans ce cas, la vidéo source doit être convertie pour se conformer à l’espace colorimétrique de la destination. L’enregistreur gère ce processus et communique avec un convertisseur d’espace colorimétrique interne.

Le lecteur communique également avec le convertisseur d’espace colorimétrique pour rapprocher toute différence entre le format compressé et le format de sortie.

Comme avec toutes les transformations effectuées sur les données, la conversion entre les profondeurs de couleurs peut réduire la qualité de la sortie. Lorsque cela est possible, vous devez utiliser des formats d’entrée et de sortie avec la même profondeur de couleurs que le format compressé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités d’écriture de fichier**](file-writing-features.md)
</dt> <dt>

[**Utilisation des entrées**](working-with-inputs.md)
</dt> <dt>

[**Utilisation des sorties**](working-with-outputs.md)
</dt> </dl>

 

 




