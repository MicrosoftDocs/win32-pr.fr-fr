---
title: Objet de mémoire tampon
description: Objet de mémoire tampon
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media Format SDK, objets de mémoire tampon
- ASF (Advanced Systems Format), objets de mémoire tampon
- ASF (format des systèmes avancés), objets de mémoire tampon
- objets, mémoires tampons
- objets de mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349fcbf5207d28a693950875b4a9b1da1b3ee4bc3bff40361e57c0a004ce6c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931569"
---
# <a name="buffer-object"></a>Objet de mémoire tampon

un objet buffer est utilisé pour contenir des exemples et les fournir entre les objets du kit de développement logiciel (SDK) du Format multimédia Windows et votre application. Lorsque vous écrivez un fichier, vous transmettez vos exemples d’entrée au writer à l’aide d’objets de mémoire tampon. Quand vous lisez un fichier, l’objet lecteur ou l’objet lecteur synchrone fournit des exemples à votre application dans les objets buffer.

Pour écrire des exemples dans un fichier, vous pouvez créer un objet de mémoire tampon à l’aide de la méthode [**IWMWriter :: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) . Pour la lecture des exemples, l’objet lecteur et l’objet lecteur synchrone créent tous deux des objets de mémoire tampon en interne. Si vous le souhaitez, vous pouvez allouer vos propres objets de mémoire tampon pour la lecture de fichier à l’aide de [**IWMReaderAllocatorEx :: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) ou [**IWMReaderAllocatorEx :: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).

Les interfaces suivantes sont prises en charge par chaque objet de mémoire tampon.



| Interface                          | Description                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | Contrôle et fournit l’accès à la mémoire tampon.                          |
| [**INSSBuffer2**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | Non implémenté.                                                     |
| [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | Prend en charge les propriétés de mémoire tampon, qui sont utilisées pour les extensions d’unité de données. |
| [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | Énumère les propriétés de mémoire tampon.                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> </dl>

 

 




