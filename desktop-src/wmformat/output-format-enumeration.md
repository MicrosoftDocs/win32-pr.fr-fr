---
title: Énumération de format de sortie
description: Énumération de format de sortie
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media Format SDK, énumérations de format de sortie
- ASF (Advanced Systems Format), énumérations de format de sortie
- ASF (format de systèmes avancés), énumérations de format de sortie
- Windows Media Format SDK, interface IWMReaderTypeNegotiation
- ASF (Advanced Systems Format), interface IWMReaderTypeNegotiation
- ASF (format des systèmes avancés), interface IWMReaderTypeNegotiation
- énumérations de format de sortie
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030758"
---
# <a name="output-format-enumeration"></a>Énumération de format de sortie

L’objet lecteur et l’objet lecteur synchrone communiquent avec les codecs pour énumérer les formats de sortie possibles pour les flux compressés. Quand vous lisez un fichier contenant du contenu compressé avec un ou plusieurs codecs Windows Media, vous pouvez examiner les formats de sortie possibles pour choisir celui qui convient le mieux à vos besoins. Pour plus de commodité, chaque codec a un format de sortie par défaut qui est défini sur le format le plus couramment utilisé. Pour plus d’informations sur l’énumération de sortie, consultez [utilisation des sorties](working-with-outputs.md).

Vous pouvez apporter certaines modifications à un format de sortie en fonction du type de média. Pour les flux vidéo, par exemple, vous pouvez modifier la taille de l’image et la profondeur de couleur. Les objets de lecture prennent tous deux en charge une interface pour tester les modifications que vous apportez au format de sortie, appelé [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de lecture de fichier**](file-reading-features.md)
</dt> </dl>

 

 




